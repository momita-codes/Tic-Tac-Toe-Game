# Tic‑Tac‑Toe Game

A minimal, browser-based Tic‑Tac‑Toe implementation built with plain HTML, CSS, and JavaScript.

This small project provides a playable 3×3 board for local two‑player play, win/draw detection, and simple controls to reset or start a new game. It is intended as a learning example of DOM manipulation and basic game logic.

## Features

- Local two‑player gameplay (players alternate placing O and X)
- Win and draw detection using a predefined set of winning patterns
- Visual result message and board disable on game end
- New Game and Reset controls
- No build step or external libraries required — just open index.html

## Files

- `index.html` — game UI (9 buttons for the board, message container, control buttons)
- `style.css` — styles for layout and presentation
- `app.js` — game logic (turn management, win checks, enabling/disabling board)

## How to run

1. Clone or download the repository:

```bash
git clone https://github.com/momita-codes/Tic-Tac-Toe-Game.git
cd Tic-Tac-Toe-Game
```

2. Open `index.html` in your browser (double-click or File → Open). No server, build tools, or dependencies required.

Optional: Serve with a static HTTP server for a local URL (recommended if you want to test remote assets):

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Implementation notes

- The board is represented by nine `.box` buttons in `index.html`. The script in `app.js` listens for clicks on these buttons and alternates the `turnO` state to place `O` and `X` marks.
- Winning combinations are defined in `app.js` in the `winPattern` array (arrays of three indices corresponding to the `.box` ordering). `checkWinner()` iterates those patterns and calls `showWinner()` when a match is found.
- After a win, the board is disabled and a message container (`.msg-container`) is shown. The `New Game` and `Reset` buttons call `resetGame()` to clear and re-enable the board.

## Potential improvements

- Add a single‑player AI (basic heuristic or Minimax) so a user can play against the computer.
- Highlight the winning line visually when a player wins.
- Add keyboard accessibility (arrow navigation) and ARIA attributes for screen readers.
- Add score tracking across rounds and persist scores in localStorage.

## Contributing

Contributions are welcome. To propose changes:

1. Fork the repository
2. Create a branch: `git checkout -b feature/your-feature`
3. Make your changes and commit them
4. Push to your fork and open a Pull Request

