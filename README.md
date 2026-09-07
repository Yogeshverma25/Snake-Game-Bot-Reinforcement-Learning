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

DATA : 
Game: 1 | Score: 0 | Best: 0 | Epsilon: 0.99\n
Game: 2 | Score: 0 | Best: 0 | Epsilon: 0.98
Game: 3 | Score: 1 | Best: 1 | Epsilon: 0.97
Game: 4 | Score: 0 | Best: 1 | Epsilon: 0.96
Game: 5 | Score: 0 | Best: 1 | Epsilon: 0.95
Game: 6 | Score: 0 | Best: 1 | Epsilon: 0.94
Game: 7 | Score: 1 | Best: 1 | Epsilon: 0.93
Game: 8 | Score: 0 | Best: 1 | Epsilon: 0.92
Game: 9 | Score: 0 | Best: 1 | Epsilon: 0.91
Game: 10 | Score: 1 | Best: 1 | Epsilon: 0.90
Game: 11 | Score: 0 | Best: 1 | Epsilon: 0.90
Game: 12 | Score: 0 | Best: 1 | Epsilon: 0.89
Game: 13 | Score: 0 | Best: 1 | Epsilon: 0.88
Game: 14 | Score: 0 | Best: 1 | Epsilon: 0.87
Game: 15 | Score: 0 | Best: 1 | Epsilon: 0.86
Game: 16 | Score: 1 | Best: 1 | Epsilon: 0.85
Game: 17 | Score: 0 | Best: 1 | Epsilon: 0.84
Game: 18 | Score: 1 | Best: 1 | Epsilon: 0.83
Game: 19 | Score: 0 | Best: 1 | Epsilon: 0.83
Game: 20 | Score: 0 | Best: 1 | Epsilon: 0.82
Game: 21 | Score: 0 | Best: 1 | Epsilon: 0.81
Game: 22 | Score: 0 | Best: 1 | Epsilon: 0.80
Game: 23 | Score: 0 | Best: 1 | Epsilon: 0.79
Game: 24 | Score: 0 | Best: 1 | Epsilon: 0.79
Game: 25 | Score: 0 | Best: 1 | Epsilon: 0.78
Game: 26 | Score: 0 | Best: 1 | Epsilon: 0.77
Game: 27 | Score: 1 | Best: 1 | Epsilon: 0.76
Game: 28 | Score: 0 | Best: 1 | Epsilon: 0.75
Game: 29 | Score: 0 | Best: 1 | Epsilon: 0.75
Game: 30 | Score: 0 | Best: 1 | Epsilon: 0.74
Game: 31 | Score: 1 | Best: 1 | Epsilon: 0.73
Game: 32 | Score: 1 | Best: 1 | Epsilon: 0.72
Game: 33 | Score: 0 | Best: 1 | Epsilon: 0.72
Game: 34 | Score: 0 | Best: 1 | Epsilon: 0.71
Game: 35 | Score: 0 | Best: 1 | Epsilon: 0.70
Game: 36 | Score: 0 | Best: 1 | Epsilon: 0.70
Game: 37 | Score: 0 | Best: 1 | Epsilon: 0.69
Game: 38 | Score: 0 | Best: 1 | Epsilon: 0.68
Game: 39 | Score: 0 | Best: 1 | Epsilon: 0.68
Game: 40 | Score: 0 | Best: 1 | Epsilon: 0.67
Game: 41 | Score: 0 | Best: 1 | Epsilon: 0.66
Game: 42 | Score: 0 | Best: 1 | Epsilon: 0.66
Game: 43 | Score: 0 | Best: 1 | Epsilon: 0.65
Game: 44 | Score: 0 | Best: 1 | Epsilon: 0.64
Game: 45 | Score: 0 | Best: 1 | Epsilon: 0.64
Game: 46 | Score: 1 | Best: 1 | Epsilon: 0.63
Game: 47 | Score: 0 | Best: 1 | Epsilon: 0.62
Game: 48 | Score: 0 | Best: 1 | Epsilon: 0.62
Game: 49 | Score: 0 | Best: 1 | Epsilon: 0.61
Game: 50 | Score: 0 | Best: 1 | Epsilon: 0.61
Game: 51 | Score: 0 | Best: 1 | Epsilon: 0.60
Game: 52 | Score: 1 | Best: 1 | Epsilon: 0.59
Game: 53 | Score: 0 | Best: 1 | Epsilon: 0.59
Game: 54 | Score: 0 | Best: 1 | Epsilon: 0.58
Game: 55 | Score: 0 | Best: 1 | Epsilon: 0.58
Game: 56 | Score: 1 | Best: 1 | Epsilon: 0.57
Game: 57 | Score: 0 | Best: 1 | Epsilon: 0.56
Game: 58 | Score: 1 | Best: 1 | Epsilon: 0.56
Game: 59 | Score: 0 | Best: 1 | Epsilon: 0.55
Game: 60 | Score: 1 | Best: 1 | Epsilon: 0.55
Game: 61 | Score: 0 | Best: 1 | Epsilon: 0.54
Game: 62 | Score: 1 | Best: 1 | Epsilon: 0.54
Game: 63 | Score: 0 | Best: 1 | Epsilon: 0.53
Game: 64 | Score: 1 | Best: 1 | Epsilon: 0.53
Game: 65 | Score: 0 | Best: 1 | Epsilon: 0.52
Game: 66 | Score: 1 | Best: 1 | Epsilon: 0.52
Game: 67 | Score: 0 | Best: 1 | Epsilon: 0.51
Game: 68 | Score: 0 | Best: 1 | Epsilon: 0.50
Game: 69 | Score: 1 | Best: 1 | Epsilon: 0.50
Game: 70 | Score: 0 | Best: 1 | Epsilon: 0.49
Game: 71 | Score: 0 | Best: 1 | Epsilon: 0.49
Game: 72 | Score: 0 | Best: 1 | Epsilon: 0.48
Game: 73 | Score: 1 | Best: 1 | Epsilon: 0.48
Game: 74 | Score: 1 | Best: 1 | Epsilon: 0.48
Game: 75 | Score: 0 | Best: 1 | Epsilon: 0.47
Game: 76 | Score: 1 | Best: 1 | Epsilon: 0.47
Game: 77 | Score: 1 | Best: 1 | Epsilon: 0.46
Game: 78 | Score: 0 | Best: 1 | Epsilon: 0.46
Game: 79 | Score: 1 | Best: 1 | Epsilon: 0.45
Game: 80 | Score: 1 | Best: 1 | Epsilon: 0.45
Game: 81 | Score: 0 | Best: 1 | Epsilon: 0.44
Game: 82 | Score: 0 | Best: 1 | Epsilon: 0.44
Game: 83 | Score: 0 | Best: 1 | Epsilon: 0.43
Game: 84 | Score: 1 | Best: 1 | Epsilon: 0.43
Game: 85 | Score: 0 | Best: 1 | Epsilon: 0.43
Game: 86 | Score: 0 | Best: 1 | Epsilon: 0.42
Game: 87 | Score: 0 | Best: 1 | Epsilon: 0.42
Game: 88 | Score: 0 | Best: 1 | Epsilon: 0.41
Game: 89 | Score: 1 | Best: 1 | Epsilon: 0.41
Game: 90 | Score: 0 | Best: 1 | Epsilon: 0.40
Game: 91 | Score: 0 | Best: 1 | Epsilon: 0.40
Game: 92 | Score: 0 | Best: 1 | Epsilon: 0.40
Game: 93 | Score: 1 | Best: 1 | Epsilon: 0.39
Game: 94 | Score: 0 | Best: 1 | Epsilon: 0.39
Game: 95 | Score: 1 | Best: 1 | Epsilon: 0.38
Game: 96 | Score: 1 | Best: 1 | Epsilon: 0.38
Game: 97 | Score: 0 | Best: 1 | Epsilon: 0.38
Game: 98 | Score: 1 | Best: 1 | Epsilon: 0.37
Game: 99 | Score: 0 | Best: 1 | Epsilon: 0.37
Game: 100 | Score: 0 | Best: 1 | Epsilon: 0.37
Game: 101 | Score: 1 | Best: 1 | Epsilon: 0.36
Game: 102 | Score: 1 | Best: 1 | Epsilon: 0.36
Game: 103 | Score: 1 | Best: 1 | Epsilon: 0.36
Game: 104 | Score: 0 | Best: 1 | Epsilon: 0.35
Game: 105 | Score: 0 | Best: 1 | Epsilon: 0.35
Game: 106 | Score: 0 | Best: 1 | Epsilon: 0.34
Game: 107 | Score: 0 | Best: 1 | Epsilon: 0.34
Game: 108 | Score: 1 | Best: 1 | Epsilon: 0.34
Game: 109 | Score: 1 | Best: 1 | Epsilon: 0.33
Game: 110 | Score: 1 | Best: 1 | Epsilon: 0.33
Game: 111 | Score: 0 | Best: 1 | Epsilon: 0.33
Game: 112 | Score: 1 | Best: 1 | Epsilon: 0.32
Game: 113 | Score: 0 | Best: 1 | Epsilon: 0.32
Game: 114 | Score: 0 | Best: 1 | Epsilon: 0.32
Game: 115 | Score: 1 | Best: 1 | Epsilon: 0.31
Game: 116 | Score: 1 | Best: 1 | Epsilon: 0.31
Game: 117 | Score: 1 | Best: 1 | Epsilon: 0.31
Game: 118 | Score: 1 | Best: 1 | Epsilon: 0.31
Game: 119 | Score: 2 | Best: 2 | Epsilon: 0.30
Game: 120 | Score: 1 | Best: 2 | Epsilon: 0.30
Game: 121 | Score: 1 | Best: 2 | Epsilon: 0.30
Game: 122 | Score: 0 | Best: 2 | Epsilon: 0.29
Game: 123 | Score: 0 | Best: 2 | Epsilon: 0.29
Game: 124 | Score: 1 | Best: 2 | Epsilon: 0.29
Game: 125 | Score: 1 | Best: 2 | Epsilon: 0.28
Game: 126 | Score: 1 | Best: 2 | Epsilon: 0.28
Game: 127 | Score: 1 | Best: 2 | Epsilon: 0.28
Game: 128 | Score: 0 | Best: 2 | Epsilon: 0.28
Game: 129 | Score: 3 | Best: 3 | Epsilon: 0.27
Game: 130 | Score: 2 | Best: 3 | Epsilon: 0.27
Game: 131 | Score: 1 | Best: 3 | Epsilon: 0.27
Game: 132 | Score: 2 | Best: 3 | Epsilon: 0.27
Game: 133 | Score: 0 | Best: 3 | Epsilon: 0.26
Game: 134 | Score: 1 | Best: 3 | Epsilon: 0.26
Game: 135 | Score: 1 | Best: 3 | Epsilon: 0.26
Game: 136 | Score: 1 | Best: 3 | Epsilon: 0.25
Game: 137 | Score: 0 | Best: 3 | Epsilon: 0.25
Game: 138 | Score: 2 | Best: 3 | Epsilon: 0.25
Game: 139 | Score: 0 | Best: 3 | Epsilon: 0.25
Game: 140 | Score: 0 | Best: 3 | Epsilon: 0.24
Game: 141 | Score: 1 | Best: 3 | Epsilon: 0.24
Game: 142 | Score: 3 | Best: 3 | Epsilon: 0.24
Game: 143 | Score: 0 | Best: 3 | Epsilon: 0.24
Game: 144 | Score: 1 | Best: 3 | Epsilon: 0.24
Game: 145 | Score: 1 | Best: 3 | Epsilon: 0.23
Game: 146 | Score: 3 | Best: 3 | Epsilon: 0.23
Game: 147 | Score: 1 | Best: 3 | Epsilon: 0.23
Game: 148 | Score: 1 | Best: 3 | Epsilon: 0.23
Game: 149 | Score: 0 | Best: 3 | Epsilon: 0.22
Game: 150 | Score: 2 | Best: 3 | Epsilon: 0.22
Game: 151 | Score: 2 | Best: 3 | Epsilon: 0.22
Game: 152 | Score: 1 | Best: 3 | Epsilon: 0.22
Game: 153 | Score: 1 | Best: 3 | Epsilon: 0.21
Game: 154 | Score: 1 | Best: 3 | Epsilon: 0.21
Game: 155 | Score: 0 | Best: 3 | Epsilon: 0.21
Game: 156 | Score: 1 | Best: 3 | Epsilon: 0.21
Game: 157 | Score: 2 | Best: 3 | Epsilon: 0.21
Game: 158 | Score: 2 | Best: 3 | Epsilon: 0.20
Game: 159 | Score: 1 | Best: 3 | Epsilon: 0.20
Game: 160 | Score: 1 | Best: 3 | Epsilon: 0.20
Game: 161 | Score: 2 | Best: 3 | Epsilon: 0.20
Game: 162 | Score: 1 | Best: 3 | Epsilon: 0.20
Game: 163 | Score: 3 | Best: 3 | Epsilon: 0.19
Game: 164 | Score: 1 | Best: 3 | Epsilon: 0.19
Game: 165 | Score: 0 | Best: 3 | Epsilon: 0.19
Game: 166 | Score: 1 | Best: 3 | Epsilon: 0.19
Game: 167 | Score: 0 | Best: 3 | Epsilon: 0.19
Game: 168 | Score: 2 | Best: 3 | Epsilon: 0.18
Game: 169 | Score: 1 | Best: 3 | Epsilon: 0.18
Game: 170 | Score: 3 | Best: 3 | Epsilon: 0.18
Game: 171 | Score: 1 | Best: 3 | Epsilon: 0.18
Game: 172 | Score: 3 | Best: 3 | Epsilon: 0.18
Game: 173 | Score: 1 | Best: 3 | Epsilon: 0.18
Game: 174 | Score: 1 | Best: 3 | Epsilon: 0.17
Game: 175 | Score: 1 | Best: 3 | Epsilon: 0.17
Game: 176 | Score: 0 | Best: 3 | Epsilon: 0.17
Game: 177 | Score: 1 | Best: 3 | Epsilon: 0.17
Game: 178 | Score: 2 | Best: 3 | Epsilon: 0.17
Game: 179 | Score: 1 | Best: 3 | Epsilon: 0.17
Game: 180 | Score: 4 | Best: 4 | Epsilon: 0.16
Game: 181 | Score: 4 | Best: 4 | Epsilon: 0.16
Game: 182 | Score: 3 | Best: 4 | Epsilon: 0.16
Game: 183 | Score: 1 | Best: 4 | Epsilon: 0.16
Game: 184 | Score: 1 | Best: 4 | Epsilon: 0.16
Game: 185 | Score: 2 | Best: 4 | Epsilon: 0.16
Game: 186 | Score: 0 | Best: 4 | Epsilon: 0.15
Game: 187 | Score: 2 | Best: 4 | Epsilon: 0.15
Game: 188 | Score: 1 | Best: 4 | Epsilon: 0.15
Game: 189 | Score: 10 | Best: 10 | Epsilon: 0.15
Game: 190 | Score: 6 | Best: 10 | Epsilon: 0.15
Game: 191 | Score: 4 | Best: 10 | Epsilon: 0.15
Game: 192 | Score: 2 | Best: 10 | Epsilon: 0.15
Game: 193 | Score: 2 | Best: 10 | Epsilon: 0.14
Game: 194 | Score: 3 | Best: 10 | Epsilon: 0.14
Game: 195 | Score: 1 | Best: 10 | Epsilon: 0.14
Game: 196 | Score: 4 | Best: 10 | Epsilon: 0.14
Game: 197 | Score: 3 | Best: 10 | Epsilon: 0.14
Game: 198 | Score: 0 | Best: 10 | Epsilon: 0.14
Game: 199 | Score: 4 | Best: 10 | Epsilon: 0.14
Game: 200 | Score: 8 | Best: 10 | Epsilon: 0.13
Game: 201 | Score: 0 | Best: 10 | Epsilon: 0.13
Game: 202 | Score: 1 | Best: 10 | Epsilon: 0.13
Game: 203 | Score: 2 | Best: 10 | Epsilon: 0.13
Game: 204 | Score: 1 | Best: 10 | Epsilon: 0.13
Game: 205 | Score: 9 | Best: 10 | Epsilon: 0.13
Game: 206 | Score: 4 | Best: 10 | Epsilon: 0.13
Game: 207 | Score: 3 | Best: 10 | Epsilon: 0.12
Game: 208 | Score: 1 | Best: 10 | Epsilon: 0.12
Game: 209 | Score: 5 | Best: 10 | Epsilon: 0.12
Game: 210 | Score: 3 | Best: 10 | Epsilon: 0.12
Game: 211 | Score: 6 | Best: 10 | Epsilon: 0.12
Game: 212 | Score: 5 | Best: 10 | Epsilon: 0.12
Game: 213 | Score: 1 | Best: 10 | Epsilon: 0.12
Game: 214 | Score: 7 | Best: 10 | Epsilon: 0.12
Game: 215 | Score: 2 | Best: 10 | Epsilon: 0.12
Game: 216 | Score: 4 | Best: 10 | Epsilon: 0.11
Game: 217 | Score: 13 | Best: 13 | Epsilon: 0.11
Game: 218 | Score: 6 | Best: 13 | Epsilon: 0.11
Game: 219 | Score: 10 | Best: 13 | Epsilon: 0.11
Game: 220 | Score: 1 | Best: 13 | Epsilon: 0.11
Game: 221 | Score: 8 | Best: 13 | Epsilon: 0.11
Game: 222 | Score: 3 | Best: 13 | Epsilon: 0.11
Game: 223 | Score: 2 | Best: 13 | Epsilon: 0.11
Game: 224 | Score: 9 | Best: 13 | Epsilon: 0.11
Game: 225 | Score: 1 | Best: 13 | Epsilon: 0.10
Game: 226 | Score: 0 | Best: 13 | Epsilon: 0.10
Game: 227 | Score: 5 | Best: 13 | Epsilon: 0.10
Game: 228 | Score: 7 | Best: 13 | Epsilon: 0.10
Game: 229 | Score: 2 | Best: 13 | Epsilon: 0.10
Game: 230 | Score: 3 | Best: 13 | Epsilon: 0.10
Game: 231 | Score: 3 | Best: 13 | Epsilon: 0.10
Game: 232 | Score: 6 | Best: 13 | Epsilon: 0.10
Game: 233 | Score: 16 | Best: 16 | Epsilon: 0.10
Game: 234 | Score: 20 | Best: 20 | Epsilon: 0.10
Game: 235 | Score: 1 | Best: 20 | Epsilon: 0.09
Game: 236 | Score: 9 | Best: 20 | Epsilon: 0.09
Game: 237 | Score: 8 | Best: 20 | Epsilon: 0.09
Game: 238 | Score: 3 | Best: 20 | Epsilon: 0.09
Game: 239 | Score: 15 | Best: 20 | Epsilon: 0.09
Game: 240 | Score: 19 | Best: 20 | Epsilon: 0.09
Game: 241 | Score: 5 | Best: 20 | Epsilon: 0.09
Game: 242 | Score: 10 | Best: 20 | Epsilon: 0.09
Game: 243 | Score: 11 | Best: 20 | Epsilon: 0.09
Game: 244 | Score: 1 | Best: 20 | Epsilon: 0.09
Game: 245 | Score: 8 | Best: 20 | Epsilon: 0.09
Game: 246 | Score: 10 | Best: 20 | Epsilon: 0.08
Game: 247 | Score: 3 | Best: 20 | Epsilon: 0.08
Game: 248 | Score: 12 | Best: 20 | Epsilon: 0.08
Game: 249 | Score: 7 | Best: 20 | Epsilon: 0.08
Game: 250 | Score: 17 | Best: 20 | Epsilon: 0.08
Game: 251 | Score: 10 | Best: 20 | Epsilon: 0.08
Game: 252 | Score: 7 | Best: 20 | Epsilon: 0.08
Game: 253 | Score: 5 | Best: 20 | Epsilon: 0.08
Game: 254 | Score: 7 | Best: 20 | Epsilon: 0.08
Game: 255 | Score: 13 | Best: 20 | Epsilon: 0.08
Game: 256 | Score: 12 | Best: 20 | Epsilon: 0.08
Game: 257 | Score: 23 | Best: 23 | Epsilon: 0.08
Game: 258 | Score: 5 | Best: 23 | Epsilon: 0.07
Game: 259 | Score: 13 | Best: 23 | Epsilon: 0.07
Game: 260 | Score: 14 | Best: 23 | Epsilon: 0.07
Game: 261 | Score: 14 | Best: 23 | Epsilon: 0.07
Game: 262 | Score: 0 | Best: 23 | Epsilon: 0.07
Game: 263 | Score: 16 | Best: 23 | Epsilon: 0.07
Game: 264 | Score: 0 | Best: 23 | Epsilon: 0.07
Game: 265 | Score: 8 | Best: 23 | Epsilon: 0.07
Game: 266 | Score: 11 | Best: 23 | Epsilon: 0.07
Game: 267 | Score: 4 | Best: 23 | Epsilon: 0.07
Game: 268 | Score: 7 | Best: 23 | Epsilon: 0.07
Game: 269 | Score: 7 | Best: 23 | Epsilon: 0.07
Game: 270 | Score: 11 | Best: 23 | Epsilon: 0.07
Game: 271 | Score: 4 | Best: 23 | Epsilon: 0.07
Game: 272 | Score: 8 | Best: 23 | Epsilon: 0.06
Game: 273 | Score: 12 | Best: 23 | Epsilon: 0.06
Game: 274 | Score: 0 | Best: 23 | Epsilon: 0.06
Game: 275 | Score: 9 | Best: 23 | Epsilon: 0.06
Game: 276 | Score: 4 | Best: 23 | Epsilon: 0.06
Game: 277 | Score: 6 | Best: 23 | Epsilon: 0.06
Game: 278 | Score: 10 | Best: 23 | Epsilon: 0.06
Game: 279 | Score: 1 | Best: 23 | Epsilon: 0.06
Game: 280 | Score: 2 | Best: 23 | Epsilon: 0.06
Game: 281 | Score: 13 | Best: 23 | Epsilon: 0.06
Game: 282 | Score: 27 | Best: 27 | Epsilon: 0.06
Game: 283 | Score: 5 | Best: 27 | Epsilon: 0.06
Game: 284 | Score: 6 | Best: 27 | Epsilon: 0.06
Game: 285 | Score: 17 | Best: 27 | Epsilon: 0.06
Game: 286 | Score: 11 | Best: 27 | Epsilon: 0.06
Game: 287 | Score: 10 | Best: 27 | Epsilon: 0.06
Game: 288 | Score: 7 | Best: 27 | Epsilon: 0.06
Game: 289 | Score: 15 | Best: 27 | Epsilon: 0.05
Game: 290 | Score: 12 | Best: 27 | Epsilon: 0.05
Game: 291 | Score: 11 | Best: 27 | Epsilon: 0.05
Game: 292 | Score: 7 | Best: 27 | Epsilon: 0.05
Game: 293 | Score: 11 | Best: 27 | Epsilon: 0.05
Game: 294 | Score: 5 | Best: 27 | Epsilon: 0.05
Game: 295 | Score: 21 | Best: 27 | Epsilon: 0.05
Game: 296 | Score: 3 | Best: 27 | Epsilon: 0.05
Game: 297 | Score: 9 | Best: 27 | Epsilon: 0.05
Game: 298 | Score: 13 | Best: 27 | Epsilon: 0.05
Game: 299 | Score: 9 | Best: 27 | Epsilon: 0.05
Game: 300 | Score: 7 | Best: 27 | Epsilon: 0.05
Game: 301 | Score: 12 | Best: 27 | Epsilon: 0.05
Game: 302 | Score: 11 | Best: 27 | Epsilon: 0.05
Game: 303 | Score: 9 | Best: 27 | Epsilon: 0.05
Game: 304 | Score: 19 | Best: 27 | Epsilon: 0.05
Game: 305 | Score: 1 | Best: 27 | Epsilon: 0.05
Game: 306 | Score: 2 | Best: 27 | Epsilon: 0.05
Game: 307 | Score: 14 | Best: 27 | Epsilon: 0.05
Game: 308 | Score: 5 | Best: 27 | Epsilon: 0.05
Game: 309 | Score: 12 | Best: 27 | Epsilon: 0.04
Game: 310 | Score: 7 | Best: 27 | Epsilon: 0.04
Game: 311 | Score: 9 | Best: 27 | Epsilon: 0.04
Game: 312 | Score: 13 | Best: 27 | Epsilon: 0.04
Game: 313 | Score: 15 | Best: 27 | Epsilon: 0.04
Game: 314 | Score: 12 | Best: 27 | Epsilon: 0.04
Game: 315 | Score: 14 | Best: 27 | Epsilon: 0.04
Game: 316 | Score: 24 | Best: 27 | Epsilon: 0.04
Game: 317 | Score: 15 | Best: 27 | Epsilon: 0.04
Game: 318 | Score: 18 | Best: 27 | Epsilon: 0.04
Game: 319 | Score: 17 | Best: 27 | Epsilon: 0.04
Game: 320 | Score: 6 | Best: 27 | Epsilon: 0.04
Game: 321 | Score: 2 | Best: 27 | Epsilon: 0.04
Game: 322 | Score: 19 | Best: 27 | Epsilon: 0.04
Game: 323 | Score: 12 | Best: 27 | Epsilon: 0.04
Game: 324 | Score: 11 | Best: 27 | Epsilon: 0.04
Game: 325 | Score: 30 | Best: 30 | Epsilon: 0.04
Game: 326 | Score: 21 | Best: 30 | Epsilon: 0.04
Game: 327 | Score: 41 | Best: 41 | Epsilon: 0.04
Game: 328 | Score: 33 | Best: 41 | Epsilon: 0.04
Game: 329 | Score: 3 | Best: 41 | Epsilon: 0.04
Game: 330 | Score: 15 | Best: 41 | Epsilon: 0.04
Game: 331 | Score: 6 | Best: 41 | Epsilon: 0.04
Game: 332 | Score: 6 | Best: 41 | Epsilon: 0.04
Game: 333 | Score: 3 | Best: 41 | Epsilon: 0.04
Game: 334 | Score: 16 | Best: 41 | Epsilon: 0.03

BEFORE :
<img width="1251" height="705" alt="Screenshot 2026-09-07 213332" src="https://github.com/user-attachments/assets/db9cc868-3ce3-4aea-bfcc-1fa2154f8bfa" />
<img width="646" height="513" alt="Screenshot 2026-09-07 213351" src="https://github.com/user-attachments/assets/1417e636-82dd-45ef-8e02-9ce1f8536a36" />

AFTER :
<img width="637" height="513" alt="Screenshot 2026-09-07 232843" src="https://github.com/user-attachments/assets/b37e41b6-e5fc-4cea-8a2c-2a4af73db2d2" />

<img width="1242" height="711" alt="Screenshot 2026-09-07 232931" src="https://github.com/user-attachments/assets/50a169a8-e4a2-4f9c-852b-2f2e30ca92cf" />



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
