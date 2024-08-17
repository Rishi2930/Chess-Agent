# Chess AI Engine

Welcome to the Chess AI Engine repository! This project is a Python-based chess engine designed to evaluate chess positions and select optimal moves using various strategies. It's built with the `chess` library and includes several advanced techniques to improve performance and accuracy.

## Features

- Piece-Square Tables: Uses evaluation charts for different pieces (pawns, knights, bishops, rooks, queens, and kings) to assess the strength of board positions.
- Material Evaluation: Calculates the balance of material between the white and black pieces.
- Transposition Table: Stores evaluated board positions to avoid redundant calculations and enhance performance.
- Alpha-Beta Pruning: Implements a minimax search algorithm with alpha-beta pruning to efficiently find the best moves.
- Quiescence Search: Improves move evaluation during captures to mitigate the horizon effect and produce more accurate assessments.

## How It Works

1. Board Evaluation: The engine evaluates the current board state by considering material balance and piece positions.
2. Move Selection: It explores legal moves and uses alpha-beta pruning to minimize the number of nodes explored in the game tree.
3. Caching: Evaluated positions are stored in a transposition table for quick retrieval, reducing computation time for repeated board states.

## Usage

To use this Chess AI engine, you can create an instance of the `group1` class, passing the desired color as an argument. The `makemove` method will return the best move in UCI format.

Example:
```python
import chess
from chess_ai import group1

board = chess.Board()
ai = group1("white")

# Get the best move from the AI
best_move = ai.makemove(board)
print(f"Best move: {best_move}")
```

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request with improvements, bug fixes, or new features.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
