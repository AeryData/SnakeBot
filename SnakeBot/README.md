# 🐍 SnakeBot - Intelligent Autonomous Snake AI

[![Python 3.x](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Pygame](https://img.shields.io/badge/Pygame-Compatible-green.svg)](https://www.pygame.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A sophisticated autonomous Snake game powered by advanced AI pathfinding algorithms. Watch as the AI navigates the board, strategically hunts food, and employs intelligent trap-avoidance tactics—all without human intervention.

![](./Animation.gif)

## 📋 Table of Contents

- [🎮 About](#-about)
- [✨ Key Features](#-key-features)
- [🚀 Quick Start](#-quick-start)
- [🧠 AI Architecture](#-ai-architecture)
- [📁 Project Structure](#-project-structure)
- [📦 Dependencies](#-dependencies)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

## 🎮 About

**SnakeBot** reimagines the classic Snake game through the lens of artificial intelligence. Rather than relying on player input, the snake operates autonomously, making intelligent decisions in real-time using advanced pathfinding and decision-making algorithms.

This project demonstrates:
- **Intelligent pathfinding** using Breadth-First Search (BFS)
- **Strategic planning** to avoid self-collision traps
- **Adaptive behavior** that switches between multiple strategies
- **Efficient game mechanics** with smooth Pygame rendering

## ✨ Key Features

### 🤖 Autonomous AI Engine
- **Self-directed navigation** without human control
- **Real-time decision making** based on board state analysis

### 🧭 Advanced Pathfinding
- **Breadth-First Search (BFS)** algorithm for optimal path calculation
- **Distance mapping** to identify shortest routes to food
- **Multi-strategy approach:**
  - 🎯 **Shortest Safe Path**: Prioritizes direct routes to food when safe
  - 🐍 **Tail Following**: Maintains board space by following the snake's tail
  - 🔄 **Fallback Movement**: Takes any safe move if other strategies fail

### 🛡️ Intelligent Trap Avoidance
- **Virtual simulation** of moves before committing to them
- **Tail reachability verification** to prevent self-trapping
- **Adaptive strategy switching** when situations become dangerous

### 🎨 Visual Experience
- Clean Pygame-based graphics
- Real-time score tracking
- Smooth animation rendering

## 🚀 Quick Start

### Prerequisites
- Python 3.x
- pip (Python package manager)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AeryData/SnakeBot.git
   cd SnakeBot
   ```

2. **Install dependencies:**
   ```bash
   pip install pygame
   ```

### Running the Game

```bash
python robo_snake.py
```

**Controls:**
- ESC key to exit
- Close the window to quit

## 🧠 AI Architecture

### Core Decision-Making Pipeline

#### 1. **Board State Analysis** (`board_reset`, `board_refresh`)
- Represents the game world as a 1D array
- Marks snake segments, empty cells, and food locations
- Executes BFS from food position to create a distance map
- Provides the foundation for all AI decisions

#### 2. **Move Selection Strategy** (`get_best_move`)

The AI evaluates moves in a hierarchical priority system:

| Strategy | Priority | Purpose |
|----------|----------|---------|
| **Shortest Safe Path** | 1️⃣ | Move toward food if tail remains reachable |
| **Tail Following** | 2️⃣ | Follow tail to maintain safe space if direct path fails |
| **Any Safe Move** | 3️⃣ | Make any valid move as last resort |

#### 3. **Trap Prevention Mechanism** (`find_safe_ways`, `is_tail_inside`)
- **Virtual move simulation**: Tests moves in a simulated environment first
- **Reachability verification**: Confirms snake can still reach its tail after consuming food
- **Strategy adaptation**: Automatically switches strategies if a move leads to certain doom

#### 4. **Movement Resolution** (`make_move`, `shift_array`)
- Translates AI decisions into snake movement
- Updates game state and score
- Generates new food locations

### Algorithm Performance
- **Time Complexity**: O(n) per move decision (linear in board size)
- **Space Complexity**: O(n) for distance map storage
- **Decision Latency**: <10ms on modern hardware

## 📁 Project Structure

```
SnakeBot/
├── robo_snake.py           # Main game implementation
├── README.md              # This file
└── Animation.gif          # Demo animation
```

### Key Classes

**`Colors`**
- Centralized color palette for all game elements

**`GameConstants`**
- Game dimensions and physics constants
- Movement directions and cell state values

**`SnakeGame`**
- **Initialization**: `__init__`, `_initialize_display`
- **Rendering**: `_draw_food`, `_draw_snake_part`
- **Game Logic**: `is_cell_free`, `is_move_possible`, `make_move`, `new_food`
- **AI Brain**: `board_reset`, `board_refresh`, `get_best_move`, `choose_shortest_safe_move`, `choose_longest_safe_move`
- **Safety Systems**: `find_safe_ways`, `is_tail_inside`, `virtual_shortest_move`, `follow_tail`
- **Fallback**: `any_possible_move`
- **Main Loop**: `run`, `handle_events`

## 📦 Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| `pygame` | Latest | Game rendering & graphics |
| `sys` | Built-in | System utilities |
| `time` | Built-in | Game timing |
| `random` | Built-in | Random number generation |

### Installation
```bash
pip install pygame
```

## 🤝 Contributing

Contributions are welcome! Areas for enhancement:
- Additional AI strategies (minimax, genetic algorithms)
- Performance optimizations
- Advanced visualization modes
- Configurable difficulty levels

## 📄 License

This project is open-source and available under the **MIT License**. See the LICENSE file for details.

---

**Made with ❤️ by [AeryData](https://github.com/AeryData)**
