# Archie's Chess Analysis

A browser-based chess game review tool with a native Chessground board, chess.js
rules and PGN handling, and Stockfish analysis. Games are processed in the
browser and are not sent to a server.

## Use it

1. Open the website or serve this folder as a static website.
2. Choose **Play**, **Analyse**, or **Puzzles** from the navigation.
3. In Analyse, import a PGN or open the example game.
4. Select a piece or drag it to a highlighted legal destination. Use the move
   list or the navigation buttons to review a game.
5. Select **Start analysis** to request Stockfish feedback.

## Chessboard integration

The current site is plain HTML, CSS and JavaScript with no build step. It imports
pinned ES-module releases directly from jsDelivr in `index.html`:

- `@lichess-org/chessground@10.5.0` for the board UI and animation
- `chess.js@1.4.0` for move legality, turn state, check, promotion, PGN and FEN

The page also loads Chessground's `chessground.base.css` and
`chessground.cburnett.css`. The latter embeds the Cburnett piece artwork, while
custom CSS supplies this site's board colours, move dots, highlights and
coordinates. No iframe or Lichess-branded interface is used.

For a local npm/bundler setup instead, install the same pinned versions:

```sh
npm install @lichess-org/chessground@10.5.0 chess.js@1.4.0
```

Then import `Chessground` from `@lichess-org/chessground`, `Chess` from
`chess.js`, and the package styles from
`@lichess-org/chessground/assets/chessground.base.css` and
`@lichess-org/chessground/assets/chessground.cburnett.css`.

## Hosting

The project can be hosted on GitHub Pages. Keep `index.html`, `LICENSE`,
`THIRD_PARTY_NOTICES.md`, and the `licenses` directory in the repository root.
No backend is required. The board libraries, fonts and Stockfish engine are
loaded from public CDNs, so an internet connection is required.

## Analysis notes

Move accuracy is an estimate based on the change in engine score between
positions. Brilliant/Great labels are heuristics based on the engine's top two
candidate lines and a material-sacrifice check. Playing-strength estimates are
experimental and are not official ratings.

## Licences

The original project code is available under the MIT licence. Chessground is
GPL-3.0-or-later; Stockfish.js is GPL-3.0; chess.js is BSD-2-Clause; and the
Cburnett artwork is GPL-2.0-or-later. These components retain their own terms.
See [LICENSE](LICENSE), [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md), and
the included [Chessground licence](licenses/CHESSGROUND-GPL-3.0-or-later.txt).
