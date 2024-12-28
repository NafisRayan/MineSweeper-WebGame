# MineSweeper Game

## Description
A simple Minesweeper game built using HTML and Tailwind CSS. The game features a 10x10 grid with 15 mines. The objective is to reveal all cells that do not contain mines without triggering any of them.

## Features
- Click on a cell to reveal its contents.
- Right-click (or use context menu) on a cell to flag it as a potential mine.
- The game alerts you if you hit a mine or win by revealing all non-mine cells.

## How to Run
1. Clone or download the repository.
2. Open the `index.html` file in a web browser.

## Controls
- **Left Click**: Reveal a cell.
- **Right Click**: Flag a cell as a potential mine.

## Game Logic

### Initialization
- **Grid Size**: 10x10
- **Mine Count**: 15

#### createBoard()
- Initializes the game board with a 10x10 grid filled with zeros.
- Randomly places 15 mines on the grid.
- Calculates the number of adjacent mines for each cell.

### Game Functions

#### revealCell(row, col)
- Reveals the cell at the specified row and column.
- If the cell contains a mine, the game ends, and all mines are revealed.
- If the cell is empty, it recursively reveals adjacent cells.
- Checks if the player has won by revealing all non-mine cells.

#### flagCell(row, col)
- Toggles a flag on the cell at the specified row and column.
- Prevents revealing flagged cells.

#### revealAllMines()
- Reveals all mines on the grid when the game is over.

#### checkWin()
- Checks if the player has won by revealing all non-mine cells.
- Alerts the player if they have won.

#### renderBoard()
- Renders the game board in the HTML document.
- Sets up event listeners for cell interactions.

