# Cleaning Robot Simulation with A*, RRT, and Actor–Critic Reinforcement Learning

**Author:** Mahmoud M. Shoieb  
**Collaborators:** University Project Team  
*(All collaborators are credited in the Acknowledgements section)*

---

## Project Overview

This project implements a **cleaning robot simulation** capable of navigating a 2D grid-based environment while avoiding obstacles and optimizing its cleaning path.

Two major approaches were explored:

1. **Classical Path Planning Algorithms:**
   - **A\*** (A-star Search): Finds optimal paths based on heuristic distance.
   - **RRT** (Rapidly-Exploring Random Tree): Explores feasible paths in complex environments.

2. **Reinforcement Learning:**
   - **Actor–Critic Agent:** The robot learns to navigate and clean the environment efficiently through trial and error using a policy-based reinforcement learning algorithm.

The goal was to compare the **deterministic efficiency** of classical algorithms with the **adaptability** of reinforcement learning methods in the same environment.

---

## Table of Contents
- [Overview](#project-overview)
- [Tech Stack](#tech-stack)
- [Repository Structure](#repository-structure)
- [Setup / Installation](#setup--installation)
- [How to Run](#how-to-run)
- [Methodology](#methodology)
- [Results Summary](#results-summary)
- [My Contributions](#my-contributions)
- [Acknowledgements](#acknowledgements)
- [License](#license)
- [Contact](#contact)

---

## Tech Stack

**Language:** Python 3.8+  
**Libraries Used:**
- `pygame` – environment simulation and visualization  
- `numpy` – matrix and environment representation  
- `heapq` – priority queue for A\*  
- `random` – RRT random sampling  
- `matplotlib` / `seaborn` – results visualization  
- `tensorflow` / `keras` (if used for Actor–Critic agent)

---

## Repository Structure

```
Cleaning-Robot-Path-Planning/
├─ notebooks/
│  ├─ Cleaning_robot_(A_star+RRT).ipynb
│  └─ Cleaning_robot_(Actor-Critic).ipynb
├─ docs/
│  ├─ Cleaning_Robot_Report_(A_star+RRT).pdf
│  └─ Cleaning_Robot_Report_(Actor-Critic).pdf
├─ images/
│  └─ *.png, *.jpg
├─ .gitignore
├─ requirements.txt
└─ README.md
```

---

## Setup / Installation

**1. Clone the repository**
```bash
git clone https://github.com/Mahmoudshoiebb/Cleaning-Robot-A_star-RRT-Actor-Critic-.git
cd Cleaning-Robot-Path-Planning
```

**2. Create a virtual environment**
```bash
python -m venv venv
venv\Scripts\activate  # Windows
# or
source venv/bin/activate  # macOS/Linux
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

If `requirements.txt` is missing, you can manually install:
```bash
pip install pygame numpy matplotlib seaborn tensorflow
```

---

## How to Run

### Run A* and RRT Simulation
Open:
```
notebooks/Cleaning_robot_(A_star+RRT).ipynb
```

### Run Actor–Critic Reinforcement Learning
Open:
```
notebooks/Cleaning_robot_(Actor-Critic).ipynb
```

Run all cells in Jupyter Notebook or Colab.  
Make sure your environment supports display (for Pygame windows).

---

## Methodology

### A* Path Planning
- Uses a grid representation of the environment.  
- Implements heuristic-based search for shortest path to clean unvisited cells.  

### RRT Path Planning
- Randomly explores the environment to find feasible collision-free paths.  
- Useful in complex obstacle layouts.  

### Actor–Critic Reinforcement Learning
- The agent learns to move and clean efficiently by receiving rewards for covering new tiles.  
- Combines **policy-based** (actor) and **value-based** (critic) learning.  
- Gradually optimizes navigation strategy through training episodes.

---

## Results Summary
- **A\***: Deterministic, optimal paths but limited adaptability.  
- **RRT**: Handles complex maps but less optimal.  
- **Actor–Critic:** Adapts dynamically and learns efficient cleaning policies over time.  

The combination of all three approaches provided insight into **trade-offs between classical and learned navigation strategies**.

---

## My Contributions
This was a **group project** completed as part of a university Artificial Intelligence course.  

My specific contributions included:
- Implementing **A\*** and **RRT** algorithms.  
- Developing environment visualization using **Pygame**.  
- Designing comparison experiments between classical and RL approaches.  
- Writing sections of the report related to algorithm design and evaluation.

---

## Acknowledgements
This project was conducted in collaboration with my teammates.  
Special thanks to the course instructor and colleagues for their insights and teamwork.  

All team members are acknowledged for their shared contributions in project ideation and documentation.

---

## License
This repository is available under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Contact
**Mahmoud M. Shoieb**  
GitHub: (https://github.com/Mahmoudshoiebb)  
Email: (mahmoudshoieb12@gmail.com)
