# Archie's Chess Analysis

A browser-based chess game review tool. Paste a PGN to view the game, check
moves, and run Stockfish analysis. Games are processed in the browser and are
not sent to a server.

## Use it

1. Open the website or serve this folder as a static website.
2. Paste a PGN into the box and select **Load game**.
3. Select **Start analysis** to analyse the game.
4. Select a move to view that position on the board.

You can also play moves from the starting position by dragging pieces on the
board. Use the buttons below the board to move through the game.

## Hosting

The project can be hosted on GitHub Pages. Keep `index.html`, `LICENSE`, and
`THIRD_PARTY_NOTICES.md` in the repository root. No backend is required.

The page loads chess.js, chessboard.js, jQuery, and Stockfish from public CDNs,
so an internet connection is needed. Stockfish runs in a Web Worker and uses
its single-threaded WebAssembly build, which does not need special server
headers.

## Analysis notes

Move accuracy is an estimate based on the change in the engine score between
positions. The rating shown for each player is a rough estimate from one game,
not an official rating and not a substitute for a recognised rating system.

## Licences

The original project code is available under the MIT licence. Third-party
software keeps its own licence. See [LICENSE](LICENSE) and
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
