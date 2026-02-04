# PEAS Based Soccer Agent 

A Python-based simulation of an autonomous intelligent agent modeled as a soccer player. This project demonstrates the application of the **PEAS framework** (Performance, Environment, Actuators, Sensors) and **Model-Based Reflex Agent** architecture within the domain of Artificial Intelligence.

---

## 🚀 Overview
This repository contains a rule-based AI agent that perceives a dynamic, stochastic soccer environment and makes rational decisions to maximize its performance utility. The agent tracks state changes through an internal world model and executes actions such as shooting, passing, and dribbling based on environmental thresholds.

## 🧠 Key AI Concepts
* **PEAS Framework:** Structured definition of the agent's task environment.
* **Model-Based Reflex Agent:** Maintains an internal state (World Model) to handle the dynamic nature of the field.
* **Rationality:** Decision-making logic optimized to increase a defined performance measure.
* **Stochastic Environment:** A soccer field simulation where ball velocity and player positions change dynamically.

---

## 🏗️ System Architecture
The project is built with a modular Object-Oriented Programming (OOP) approach:

| Module | Responsibility |
| :--- | :--- |
| **SoccerEnvironment** | The simulation engine handling state space and dynamics. |
| **PerceptionModule** | Processes raw sensory data into usable information. |
| **WorldModel** | Maintains the agent's internal representation of the game (history/state). |
| **DecisionMakingModule** | The inference engine using rule-based logic to select actions. |
| **ActionExecutionModule** | The actuator interface that translates decisions into movement. |



---

## 📊 PEAS Analysis
To design this intelligent agent, we define the task environment using the PEAS framework:

* **Performance:** Goals scored, successful passes, distance covered, and minimizing ball loss.
* **Environment:** Soccer field, teammates, opponents, and the ball (Stochastic & Dynamic).
* **Sensors:** Vision (proximity sensors), ball position coordinates, and player stamina levels.
* **Actuators:** Motor functions (Move, Kick, Pivot, Accelerate).

---
### Decision Algorithm (Pseudocode)
```text
WHILE Match_Is_Active:
    1. SENSE environment (Get distances to Ball and Goal)
    2. UPDATE Internal State (Check Stamina)
    
    3. DECIDE Action based on Priority:
       IF Stamina < 20% -> PRIORITY: SURVIVAL
          └── Action: REST
          
       ELSE IF Distance_To_Ball > 5 units -> PRIORITY: ACQUISITION
          └── Action: RUN_TO_BALL
          
       ELSE (Agent has Ball) -> PRIORITY: ATTACK
          IF Distance_To_Goal < 25 units:
             └── Action: SHOOT
          ELSE:
             └── Action: DRIBBLE
             
    4. ACT (Update Physics and Score).

---

## 🛠️ Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/umersmx/PEAS-based-Soccer-Player-Agent.git](https://github.com/umersmx/PEAS-based-Soccer-Player-Agent.git)
