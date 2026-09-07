# 🐍 Snake-Game-Bot-Reinforcement-Learning

A modular Deep Reinforcement Learning project where an AI agent learns to master the classic Snake game using advanced Deep Q-Network (DQN) techniques.

---

## 🚀 Overview

This project implements a self-learning Snake bot trained with modern RL strategies:
* 🧠 **Deep Q-Network (DQN)** architecture powered by PyTorch
* 📊 **Live training analytics** with Seaborn and Matplotlib
* 📁 **Dynamic data logging** to CSV for automated performance tracking
* 🎮 **Real-time game rendering & monitoring dashboard** using Pygame
* 💾 **Model persistence** to save and load trained neural network weights

The agent starts with random behavior and progressively learns optimal survival and food collection strategies through real-time feedback.

---

## 📁 Project Structure

```text
Snake_game/
│
├── againt.py             # Main training loop & agent execution logic
├── game_ai.py            # Pygame environment, rules, and UI dashboard
├── model.py              # PyTorch Neural Network architecture & QTrainer
├── helper.py             # Real-time performance plotter (Seaborn/Matplotlib)
├── training_data_dqn.csv # Auto-generated dataset tracking score progression
└── model/
    └── model.pth         # Saved neural network weights of the trained agent
```

---

## 🧠 Model Architecture

The neural network utilizes a fully connected feedforward architecture to approximate Q-values based on an 11-feature state representation.

* **Input Layer (11 nodes):** Encapsulates immediate danger (straight, right, left), movement directions, and relative food coordinates.
* **Hidden Layer (256 nodes):** Applies non-linear transformations via ReLU activation to capture spatial patterns.
* **Output Layer (3 nodes):** Evaluates Q-values for three possible actions: `[Straight, Right, Left]`.

---

## 📊 Training Visualizations

The live training dashboard tracks key metrics to ensure stable learning progress:
* **Score & Moving Average:** Visualizes performance growth over episodes.
* **Exploration Rate (ε):** Tracks the shift from random exploration to policy exploitation.

---

## ⚙️ Installation

Make sure you have Python 3.10+ installed on your system.

```bash
pip install torch pygame matplotlib seaborn numpy pandas
```

---

## ▶️ Running the Project

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Snake-Game-Bot-Reinforcement-Learning.git](https://github.com/YOUR_USERNAME/Snake-Game-Bot-Reinforcement-Learning.git)
   cd Snake-Game-Bot-Reinforcement-Learning
   ```

2. **Run the training script:**
   ```bash
   python againt.py
   ```
   * A Pygame window will open displaying the live game environment and monitoring dashboard.
   * Training performance charts will update in real-time.

---

## 🎮 How It Works

1. **Observe State:** The agent reads the 11-value feature vector from the game grid.
2. **Choose Action:** Uses an ε-greedy policy to choose between exploration (random moves) and exploitation (neural network predictions).
3. **Execute & Reward:** The environment processes the action and outputs rewards (+10 for food, -10 for collision).
4. **Optimize:** Calculates Mean Squared Error (MSE) loss and updates network weights via backpropagation (Adam optimizer).

---

## 📈 Training Behavior

| Phase | Agent Behavior |
| :--- | :--- |
| **Early** | Pure random movement and frequent collisions |
| **Mid** | Learns to actively track and navigate toward food |
| **Late** | Executes efficient self-preservation and high-score survival loops |

---

## ⚙️ Key Hyperparameters

| Parameter | Value |
| :--- | :--- |
| Learning Rate (lr) | 0.001 |
| Discount Factor (γ) | 0.9 |
| Epsilon Start (ε_start) | 1.0 |
| Epsilon Minimum (ε_min) | 0.01 |
| Epsilon Decay (ε_decay) | 0.99 |

---

## 🔥 Features Breakdown

✔ **Stable Deep Learning Pipeline:** Uses PyTorch with automated loss optimization and gradient steps.  
✔ **Smart UI Dashboard:** Real-time on-screen monitoring of game count, scores, and epsilon decay.  
✔ **Automated Data Export:** Logs session metrics into `training_data_dqn.csv` for report generation.  
✔ **Model Serialization:** Automatically saves top-performing agent weights to `./model/model.pth`.  

---

## 🎯 Project Purpose

This project demonstrates:
* Practical implementation of Deep Reinforcement Learning.
* End-to-end integration of game engines (Pygame) with deep learning frameworks (PyTorch).
* Building clean, modular, and extensible AI systems.

Ideal for academic minor projects, machine learning portfolios, and reinforcement learning experimentation.

---

## 📜 License

Free to use, modify, and learn from under the MIT License.

---

## ✨ Author

**Yogesh Verma**
