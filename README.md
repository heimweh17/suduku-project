
# Sudoku-Project

---

## Sudoku — Python + Pygame

A playable Sudoku game implemented in Python using Pygame. It features on-the-fly puzzle generation at multiple difficulties, keyboard and mouse controls, reset/restart options, and simple pencil-marks. The generator is adapted (with attribution) from a GeeksforGeeks algorithm and wrapped in a class used by the game.

---

## Features

-   **Start screen** with difficulty selection: Easy, Medium, Hard.
-   **Random puzzle generation** per difficulty (by number of removed cells).
-   **Mouse selection** and **keyboard navigation** across a 9×9 grid.
-   **Pencil-marks** (small gray numbers) before committing a value.
-   **Reset** current puzzle, **restart** to difficulty menu, or **exit**.
-   **Win/Lose screens** and board-check on demand.

---

## Tech Stack

-   Python 3.9+
-   Pygame
-   Pure-Python Sudoku generator (adapted from GeeksforGeeks; see Attribution).

---

## Project Structure

├── main.py             # Game loop, rendering, input handling, menus

└── sudoku_generator.py # SudokuGenerator class and generate_sudoku() helper

---

## How to Play

-   **Start Menu**: Click a difficulty to generate a new puzzle.
    -   **Easy**: removes 30 cells
    -   **Medium**: removes 40 cells
    -   **Hard**: removes 50 cells

-   **Select a Cell**: Click within the 9×9 board (top 720×720 area).

-   **Move Selection**: Arrow keys `←` `→` `↑` `↓`

-   **Enter Numbers (1–9)**:
    -   If the cell is empty (not a given), pressing `1–9` adds a pencil-mark (light gray).
    -   Press **Enter/Return** to commit the pencil-mark to the board for the selected cell.

-   **Erase**: **Backspace** clears your entry in a non-given cell.

-   **Check Board**: Press **Enter/Return** while a non-editable (given) cell is selected to check the entire board against the solution.
    -   If correct: Win screen
    -   If incorrect: Lose screen

-   **Buttons (bottom toolbar)**:
    -   **RESET**: Restore the puzzle to the state it had right after generation.
    -   **RESTART**: Go back to the start menu (pick difficulty again).
    -   **EXIT**: Quit the game.

---

## Notes on Behavior

-   **Pencil-marks** are shown in smaller gray text. When you press **Enter/Return** on a selected editable cell with a pencil-mark, that value is committed to the main board.
-   The board check is performed when pressing **Enter/Return** on a given (non-editable) cell; the game compares the current board to the solved board.
