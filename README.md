# 🎮 Sudoku Game

A Python-based Sudoku game with a beautiful graphical user interface built using Pygame. This implementation features a playable Sudoku puzzle with visual solving capabilities, hints, and real-time feedback.

## 🚀 Features

- 🎨 Interactive Sudoku board with GUI
- 🎲 Random puzzle generation
- 👀 Visual puzzle solving animation
- 💡 Hint system
- ✅ Real-time error checking
- ⏱️ Timer to track solving duration
- ❌ Wrong move counter

## 📋 Requirements

- Python 3.8 or above
- Pygame 2.0.1 or above

## 🔧 Installation

1. Make sure you have Python installed on your system
2. Install the required package:
```bash
pip install pygame
```

## 🎯 How to Run

Run the game by executing the SudokuGUI.py file:
```bash
python SudokuGUI.py
```

## 🎮 How to Play

- 🖱️ Click on a cell to select it
- 🔢 Type a number (1-9) to fill the selected cell
- 🗑️ Press DELETE to clear a cell
- ⏯️ Press SPACE to visualize the solving algorithm
- 💡 Press H for a hint
- ✅ Press ENTER to check if your solution is correct

## 🎛️ Game Controls

| Key | Action |
|-----|--------|
| Left Mouse Click | Select a cell |
| Number Keys (1-9) | Enter a number in the selected cell |
| Delete | Clear the selected cell |
| Space | Visualize the solving algorithm |
| H | Get a hint |
| Return | Check solution |

## 📁 Project Structure

### `SudokuGUI.py`
Contains the game's GUI implementation and main game loop.

#### Classes and Functions:

1. **Board Class**
   - `__init__(self, window)`: Initializes the Sudoku board and creates a solved version
   - `draw_board(self)`: Draws the Sudoku board on the Pygame window
   - `deselect(self, tile)`: Deselects all tiles except the given tile
   - `redraw(self, keys, wrong, time)`: Redraws the board with current state
   - `visualSolve(self, wrong, time)`: Solves the board visually with animation
   - `hint(self, keys)`: Provides a hint by filling in a random empty tile

2. **Tile Class**
   - `__init__(self, value, window, x1, y1)`: Initializes a tile with position and value
   - `draw(self, color, thickness)`: Draws the tile with specified color and border
   - `display(self, value, position, color)`: Displays the tile's value
   - `clicked(self, mousePos)`: Checks if the tile was clicked

### `sudokutools.py`
Contains the core Sudoku logic including board generation, validation, and solving algorithms.

#### Functions:

1. **Board Generation and Display**
   - `print_board(board)`: Prints the Sudoku board in a readable format
   - `generate_board()`: Creates a random, solvable Sudoku board
   - `fill_cells(board, row, col)`: Helper function to fill remaining cells

2. **Solving Logic**
   - `find_empty(board)`: Finds the next empty cell in the board
   - `valid(board, pos, num)`: Checks if a number is valid in a given position
   - `solve(board)`: Solves the Sudoku board using backtracking

## 🔍 Technical Details

### Algorithms Used

1. **Backtracking Algorithm**
   - Used for both puzzle solving and generation
   - Recursively tries possible numbers until a solution is found
   - Efficiently handles invalid moves by backtracking

2. **Random Puzzle Generation**
   - Starts with a solved board
   - Removes numbers while ensuring a unique solution
   - Maintains Sudoku rules throughout the process

3. **Real-time Validation**
   - Checks row, column, and 3x3 box constraints
   - Provides immediate feedback on valid/invalid moves

## 🎨 Visual Features

- Color-coded feedback for correct/incorrect moves
- Animated solving visualization
- Clean, modern interface
- Responsive grid layout
- Timer and error counter display

## 🤝 Contributors

- 202401053 - Anghan Nena
- 202401103 - Ruhan Kureshi
- 202401105 - Jay Lavingiya
- 202401111 - Manali Malani

## 📝 License

This project is open source and available under the MIT License.

---

Made with ❤️ using Python and Pygame
