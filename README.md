# Othello AI Bot

This project is an implementation of an Othello (Reversi) game-playing AI using the **Minimax algorithm** with **Alpha-Beta Pruning** and a **Transposition Table** to improve efficiency. The AI can play against itself or be used in a human vs. AI or human vs. human game.

## Table of Contents
- [Features](#features)
- [Usage](#usage)
- [Game Rules](#game-rules)
- [Minimax and Alpha-Beta Pruning](#minimax-and-alpha-beta-pruning)
- [Transposition Table](#transposition-table)
- [File Structure](#file-structure)

## Features
- **Play Modes**:
  - **Human vs. Human**: Play against another human on the same device.
  - **Human vs. AI**: Play against the AI that uses the Minimax algorithm with Alpha-Beta Pruning.
  - **AI vs. AI**: Watch two AI players play against each other.

- **AI**:
  - **Minimax Algorithm**: AI calculates the best possible move by exploring potential future moves.
  - **Alpha-Beta Pruning**: Reduces the number of nodes evaluated in the minimax tree.
  - **Transposition Table**: Caches board states to avoid redundant calculations and optimize performance.


## Usage
Once the game is started, you can choose between different modes:

1. **Human vs. Human**: Play by inputting the coordinates of your move.
2. **Human vs. AI**: You will be prompted to play your move, then the AI will make its move.
3. **AI vs. AI**: You can observe how two AI agents play against each other.

### How to Play
- The game board consists of an 8x8 grid.
- Players take turns placing their colored piece (black or white) on the board.
- The goal is to capture your opponent's pieces by sandwiching them between your pieces in any direction (horizontal, vertical, or diagonal).
- The game ends when neither player can make a valid move. The player with the most pieces on the board at the end wins.

## Game Rules
- Each player must place a piece on the board in a position where it will sandwich at least one of the opponent’s pieces.
- The game alternates between players, and if a player has no valid move, they must pass their turn.
- The game ends when both players have no valid moves remaining or when the board is completely filled.

## Minimax and Alpha-Beta Pruning
The AI uses the **Minimax algorithm** to explore possible moves up to a defined depth. It evaluates each move using a scoring function, considering the current state of the board, mobility, piece count, and control of corners and edges.

**Alpha-Beta Pruning** is used to improve the efficiency of the Minimax algorithm by pruning unnecessary branches in the game tree that don't affect the final decision, reducing the number of possible states to evaluate.

## Transposition Table
A **Transposition Table** is used to cache previously encountered board states and their evaluation scores. This prevents the AI from re-evaluating the same board positions multiple times, speeding up the decision-making process.

## File Structure
The project consists of the following files:
- **othello.py**: The main file that contains the Othello game logic and game modes.
- **ai.py**: Contains the Minimax algorithm with Alpha-Beta Pruning and the evaluation function for board states.
- **transposition_table.py**: Implements the transposition table to cache previously evaluated board states.
- **print_board.py**: Helper function to print the current board state.
