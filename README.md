# 🎮 Connect Four AI

> **An Artificial Intelligence-based implementation of the classic Connect Four board game, developed as a Semester 6 group project.**

[![Project](https://img.shields.io/badge/Project-Academic%20%7C%20AI-blue)](#)
[![Course](https://img.shields.io/badge/Course-Artificial%20Intelligence-purple)](#)
[![Game](https://img.shields.io/badge/Game-Connect%20Four-orange)](#)
[![Status](https://img.shields.io/badge/Status-Completed-success)](#)

---

## 📌 Overview

**Connect Four AI** is an Artificial Intelligence-based implementation of the classic Connect Four strategy game.

The project was developed as a **Semester 6 Artificial Intelligence group project**, with the goal of applying fundamental AI concepts to a practical, interactive game environment.

The system recreates the traditional Connect Four gameplay while incorporating an AI component capable of making decisions based on the current state of the game board.

The project demonstrates how concepts from **Artificial Intelligence, game-state representation, decision making, search strategies, and algorithmic problem solving** can be applied to a real-world interactive application.

---

## 🎯 Project Objectives

The main objectives of this project were to:

* Implement the classic Connect Four game.
* Represent and manage the game board programmatically.
* Implement valid player moves and turn management.
* Detect winning and draw conditions.
* Develop an AI-based opponent.
* Enable the AI to analyze the current game state.
* Apply Artificial Intelligence concepts to game decision-making.
* Create an interactive and understandable gameplay experience.
* Demonstrate the practical application of AI algorithms.

---

## 🧩 What is Connect Four?

Connect Four is a two-player strategy game played on a vertical grid.

Players take turns dropping their pieces into columns. Because of gravity, each piece occupies the lowest available position in the selected column.

The objective is to be the first player to create a continuous line of **four pieces**.

A winning combination can be:

* Horizontal
* Vertical
* Diagonal

The game can also end in a draw when the board is completely filled without either player creating a winning combination.

---

## 🤖 Artificial Intelligence Component

The main purpose of this project is to demonstrate how Artificial Intelligence can be used to make decisions in a game environment.

At every AI turn, the system can be understood conceptually as:

```text
Current Board State
        │
        ▼
Generate Possible Moves
        │
        ▼
Evaluate Game States
        │
        ▼
Select Best Move
        │
        ▼
Update Board
        │
        ▼
Continue Game
```

The AI therefore does not simply choose a random column. It evaluates the available game states according to the implemented decision-making strategy.

> **Implementation note:** The exact AI algorithm, evaluation function, and search strategy should be documented here according to the code contained in `Connect Four.zip`.

---

## 🎮 Game Features

### Core Gameplay

* Interactive Connect Four board
* Turn-based gameplay
* Valid move detection
* Automatic piece placement
* Board-state management
* Win detection
* Draw detection
* Game-over handling

### AI Gameplay

* AI-controlled opponent
* Automated move selection
* Board-state evaluation
* Strategic decision making

### User Experience

* Clear game board
* Player turn indication
* Game result notification
* Restart / new-game functionality *(if implemented)*

---

## 🧠 Game Logic

The game maintains the current state of the board and updates it after every valid move.

A simplified game cycle is:

```text
Start Game
    │
    ▼
Initialize Board
    │
    ▼
Player Makes Move
    │
    ▼
Validate Move
    │
    ├── Invalid → Request Another Move
    │
    └── Valid
          │
          ▼
      Update Board
          │
          ▼
      Check Winner
          │
       ┌──┴──┐
       │     │
      Yes    No
       │     │
       ▼     ▼
    Game Over
             │
             ▼
        AI Makes Move
             │
             ▼
        Update Board
             │
             ▼
        Check Winner
             │
             ▼
        Continue Game
```

---

## 🏆 Winning Condition

After each move, the system checks whether the newly placed piece contributes to a sequence of four matching pieces.

The system checks the possible winning directions:

### Horizontal

```text
● ● ● ●
```

### Vertical

```text
●
●
●
●
```

### Diagonal

```text
●
  ●
    ●
      ●
```

If four connected pieces are detected, the corresponding player wins.

---

## 🗺️ Board Representation

The Connect Four board is represented as a structured grid.

Conceptually:

```text
┌───┬───┬───┬───┬───┬───┬───┐
│   │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │   │
└───┴───┴───┴───┴───┴───┴───┘
```

Each cell represents an available or occupied position.

---

## 🔄 Game State Management

The application maintains information such as:

* Current board configuration
* Current player
* Available moves
* Occupied positions
* AI state
* Winner state
* Game-over state

Every move causes the state of the game to be updated before the next decision is made.

---

## 🏗️ System Architecture

The application can be conceptually divided into the following components:

```text
                    ┌─────────────────┐
                    │   Game Interface│
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   Game Manager  │
                    └────────┬────────┘
                             │
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
       ┌────────────┐ ┌────────────┐ ┌────────────┐
       │ Board      │ │ Game Logic │ │ AI Engine  │
       │ Management │ │            │ │            │
       └────────────┘ └────────────┘ └──────┬─────┘
                                             │
                                             ▼
                                      Move Selection
```

> The final architecture diagram should be updated after inspecting the actual source code.

---

## 🛠️ Technology Stack

| Category                | Technology                |
| ----------------------- | ------------------------- |
| Programming Language    | **[Verify from project]** |
| AI / Algorithm          | **[Verify from project]** |
| User Interface          | **[Verify from project]** |
| Framework / Library     | **[Verify from project]** |
| Development Environment | **[Verify from project]** |

The technology stack should reflect the actual implementation rather than assumptions.

---

## 📂 Project Structure

The repository currently contains the project implementation in:

```text
Connect Four.zip
```

After extraction, the project structure should be documented here.

For example:

```text
Connect-Four/
│
├── source/
│   ├── ...
│
├── assets/
│   ├── ...
│
├── README.md
└── ...
```

> This section should be replaced with the exact structure of the submitted project.

---

## 🚀 Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/eshaeman003/connect-four-game-project.git
```

### 2. Navigate to the project

```bash
cd connect-four-game-project
```

### 3. Extract the project

Extract:

```text
Connect Four.zip
```

### 4. Install required dependencies

```bash
[Add actual installation command]
```

### 5. Run the application

```bash
[Add actual run command]
```

> The installation and execution commands should be updated according to the actual project technology.

---

## 🎮 How to Play

### Step 1 — Start the Game

Launch the application.

### Step 2 — Make a Move

Select an available column / position according to the implemented interface.

### Step 3 — AI Response

After the player's move, the AI analyzes the current game state and selects its move.

### Step 4 — Continue Playing

Players and the AI continue taking turns.

### Step 5 — Win or Draw

The game ends when:

* A player connects four pieces, or
* The board becomes full.

---

## 🧪 Testing

The project should be tested against different game scenarios, including:

| Test Case       | Expected Result              |
| --------------- | ---------------------------- |
| Valid move      | Piece is placed successfully |
| Invalid move    | Move is rejected             |
| Horizontal four | Player wins                  |
| Vertical four   | Player wins                  |
| Diagonal four   | Player wins                  |
| Full board      | Draw detected                |
| AI turn         | AI generates a valid move    |
| Game restart    | Board resets correctly       |

Additional test cases can be added based on the implemented functionality.

---

## 🧠 AI Concepts Demonstrated

This project provides practical exposure to several Artificial Intelligence concepts:

* Game-playing AI
* State-space representation
* Decision making
* Search-based reasoning
* Game-state evaluation
* Adversarial environments
* Heuristic evaluation *(if implemented)*
* Optimization of AI decisions *(if implemented)*

The exact algorithms used by the project should be listed here after reviewing the implementation.

---

## 📊 Example Game Flow

```text
Player
  │
  │ selects column
  ▼
Validate Move
  │
  ▼
Update Board
  │
  ▼
Check Winning State
  │
  ├──── Winner ────► End Game
  │
  ▼
AI Analysis
  │
  ▼
AI Move
  │
  ▼
Update Board
  │
  ▼
Check Winning State
  │
  ├──── Winner ────► End Game
  │
  ▼
Next Turn
```

---

## 🔮 Future Improvements

Potential improvements include:

* Multiple AI difficulty levels
* Improved AI decision making
* More advanced search strategies
* Performance optimization
* Player statistics
* Score tracking
* Sound effects
* Animations
* Improved visual design
* Game history
* Undo functionality
* Human vs Human mode
* AI vs AI mode
* Online multiplayer
* Responsive interface
* Deployment as a web application

---

## 🎓 Academic Context

This project was developed as a **group project for the Semester 6 Artificial Intelligence course**.

The project provided practical experience in translating theoretical Artificial Intelligence concepts into an interactive application.

### Learning Outcomes

Through this project, we explored:

* Artificial Intelligence fundamentals
* Game-playing systems
* Algorithmic problem solving
* State representation
* Decision-making
* Programming logic
* Debugging and testing
* Collaborative software development

---

## 👥 Project Type

**Type:** Academic Group Project of 3
**Semester:** 6
**Course:** Artificial Intelligence
**Domain:** Artificial Intelligence / Game Development
**Repository:** `connect-four-game-project`

---

## ⚠️ Project Status

This project represents an academic implementation developed for learning and demonstration purposes.

The repository may contain a packaged project archive rather than a fully separated source-code structure.

---

## 👩‍💻 Author

**Esha Eman and two members of group**

Software Engineering Student
Capital University of Science and Technology (CUST)
professor: Dre Ameer Nadeem

GitHub: **[@eshaeman003](https://github.com/eshaeman003)**

---

## 📄 License

No specific open-source license is currently documented for this repository.

If you intend to make the source code available for reuse, an appropriate license can be added to the repository.

---

## ⭐ Acknowledgements

Developed as part of the **Semester 6 Artificial Intelligence coursework** under the supervision of Cust Senior Professor Dr Ameer Nadeem.

---

<p align="center">
  <strong>Connect Four AI</strong><br>
  <em>Where game strategy meets Artificial Intelligence.</em>
</p>
