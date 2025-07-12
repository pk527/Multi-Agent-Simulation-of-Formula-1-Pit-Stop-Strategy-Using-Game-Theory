# 🌟 Multi-Agent Simulation of Pit Stop Strategy Using Game Theory

Welcome to the official repository of **Multi-Agent Simulation of Pit Stop Strategy Using Game Theory**, where **F1 racing meets intelligent decision-making**. This project models pit stop strategies of Formula 1 teams like Ferrari and McLaren using **Bayesian game theory** and **agent-based simulation**, delivering an **interactive HTML dashboard** packed with visual insights and analytical tools.

> 💡 *"In F1, milliseconds matter. Pit stop decisions can win or lose races. This project simulates those decisions under uncertainty using game theory."*

---

## 🏁 Race Context: 2024 Spanish Grand Prix

This simulation is grounded in real-world data from the **2024 Spanish Grand Prix**, making the analysis both relevant and realistic. Using data pulled from the **FastF1 API**, the model integrates:

* Actual lap times
* Sector performance metrics
* Tire compound usage
* Pit stop events

📡 **FastF1** (a Python package for accessing F1 telemetry and timing data) allowed us to replicate timing and strategy dynamics for the 2024 Circuit de Barcelona-Catalunya race, providing a factual backbone to all strategic simulations.

---

## 🚀 Project Overview

This repository simulates the high-stakes world of Formula 1 racing — but from a **strategic lens**. Each team acts as an autonomous agent making calculated pit stop decisions in a multi-agent environment. Unlike traditional simulations, this project focuses on **how strategies interact**, not just performance in isolation.

You’ll explore:

* Strategic behavior of **Ferrari and McLaren** using **Bayesian reasoning**.
* Outcomes shaped by tire wear, timing, rival moves, and traffic.
* Real-time visualization and comparison of **36+ strategy combinations**.
* Strategy impact modeled on **Spanish GP race conditions**.

The output is a **dynamic HTML dashboard** that turns theory into action, helping users simulate, explore, and make sense of racing’s most important decision: *When do you pit?*

---

## 🔄 Key Questions Answered

This simulation isn't just technical — it's *curious*. Here are some of the questions it lets you explore:

* 🏎️ **What strategy should Ferrari use if McLaren pits on Lap 12?**
* 🍓 **Which 10 pit combinations are globally most effective in all scenarios?**
* ❌ **What happens when both teams pit under the safety car?**
* 🌟 **Is undercutting always better than extending the stint?**
* ⚖️ **Which combinations are fair, risky, or dominant?**

You can explore these answers **live** using dropdowns, simulation buttons, and embedded visualizations in the dashboard.

---

## 📊 Dashboard Breakdown (Detailed)

The dashboard is a feature-rich HTML interface designed to guide users through strategy analysis, simulations, and performance metrics with ease. Below are the main sections with in-depth functionality:

### 🔢 1. Bayesian Strategy Matrix

* **Purpose**: Evaluate Ferrari vs. McLaren strategy pairings.
* **Visuals**: A dynamic payoff table that updates as strategies are selected.
* **Interaction**: Drop-downs allow users to choose any of the predefined strategies for each team.
* **Output**: Shows the payoff (in seconds) for Ferrari, color-coded as:

  * 🟩 Green: Advantageous
  * 🟨 Neutral
  * 🟥 Risky/Loss
* **Utility**: Allows comparison of the impact of strategic timing.

### 🌿 2. Sankey Advantage Flow Plot

* **Purpose**: Visualizes payoff flow between strategic choices.
* **Visuals**: Sankey diagram with nodes for strategies and links for their payoff flows.
* **Interaction**: Auto-generated from simulation outcomes.
* **Output**:

  * Direction of advantage (from losing to winning choice).
  * Thickness of flow indicates payoff strength.
  * Color highlights benefiting agent (Ferrari/McLaren).

### ⏱ 3. Lap Time Analyzer

* **Purpose**: Track time loss/gain across laps and stints.
* **Visuals**: Line chart comparing Ferrari and McLaren lap-by-lap.
* **Interaction**: Dynamically updates after simulating.
* **Output**:

  * Slope change = tire degradation.
  * Drop = pit entry cost.
  * Jump = new-tire pace improvement.
* **Insights**: Undercut vs Overcut visual performance comparison.

### 🔹 4. Real-Time Race Simulation

* **Purpose**: Visualizes lap progression in real-time.
* **Visuals**: Animated timeline showing each agent’s pit event.
* **Interaction**:

  * Buttons: Start / Pause / Reset.
  * Parameters: Simulation speed slider.
* **Output**: Shows lap count, pit events, and driver state.
* **Use Case**: Demonstrates how real pit timings evolve into strategic gain or loss.

### 👍 5. Strategy Shortcut Panel

* **Buttons**:

  * 🚀 `Top 10 Global Best Strategies`
  * 🎯 `Ferrari Best vs Each McLaren`
  * ❌ `Worst Case Scenarios`
* **Functionality**:

  * Auto-calculates and displays ranked results.
  * Presents full strategy descriptions with payoff values.
  * Saves time by summarizing optimal paths.

---

## 🔢 Technical Architecture

| Module                  | Purpose                                        |
| ----------------------- | ---------------------------------------------- |
| `agents.py`             | Implements rational agents using game theory   |
| `simulator.py`          | Manages race logic, lap counts, time evolution |
| `payoff_matrix.py`      | Calculates outcomes for strategy pairs         |
| `dashboard.html`        | Renders all analytics visually in browser      |
| `fastf1_data_loader.py` | Pulls lap/pit/tire data from 2024 Spanish GP   |

> Fully written in **Python**, with **HTML + JavaScript** visuals. Uses **FastF1 API** for real telemetry-based modeling.

---

## 🔬 Results Overview

The simulation evaluates **every strategy combination** between two agents (Ferrari and McLaren). Outputs include:

```text
Ferrari: Undercut      | McLaren: Pit_Lap_12     | Payoff: +2.9 seconds
Ferrari: DoubleStack   | McLaren: SC_Pit         | Payoff: +1.8 seconds
Ferrari: Extend_Stint  | McLaren: Undercut       | Payoff: -1.5 seconds
```

### ⭐ Best Strategy (Example)

* Ferrari: **Undercut Lap 11**
* McLaren: **Pit Lap 13**
* Ferrari gains: **+3.1s**

### ❌ Worst Case (Example)

* Ferrari: **Extend Stint Late**
* McLaren: **SC Pit**
* Ferrari loses: **-2.8s**

These results are available **instantly** inside the dashboard.

---

## 📈 Visual Components

Each visual has a purpose:

* 🌐 **Sankey Diagram**

  * Visualizes strategy flow of payoff.
  * Color and direction indicate performance.

* 📊 **Strategy Payoff Matrix Table**

  * Table highlighting numeric payoffs.
  * Dropdown driven, dynamically updated.

* 🔍 **Lap Time Chart**

  * Line chart comparing driver pace.
  * Key to analyzing degradation/impact of pits.

* ⏳ **Simulation Controls**

  * Interactive buttons to simulate real races.
  * Useful for teaching and demoing live scenarios.

---

## 🎯 Strategy Concepts Applied

This isn't just a simulator — it's a classroom on wheels. Concepts used:

* **Bayesian Game Theory**: Predicts opponent behavior using probabilities.
* **Nash Equilibrium**: Identifies optimal mutual strategies.
* **Expected Payoff**: Uses utility theory to decide best moves.
* **Regret Minimization**: Avoids high-risk low-reward paths.
* **Matrix Games**: Visualizes decisions in payoff tables.

`

---

## 🌐 Use Cases

This project is ideal for:

* 🏎️ Motorsport data analysts
* 🎓 Game theory learners and instructors
* 📊 Strategy modeling students
* 📚 AI & multi-agent systems research

---



## 💡 Roadmap: What’s Next?

* 🔄 Add **Monte Carlo simulation** to simulate 1000s of races
* 🌧️ Add **weather-based strategy modeling**
* 🛠️ Extend to **multi-agent (4+ teams)** games
* 📄 Export simulation results to CSV or JSON for research

---

