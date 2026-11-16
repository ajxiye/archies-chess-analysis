# Third-party software

Archie's Chess Analysis uses the projects listed below. Each project keeps its
own licence. The MIT licence in this repository applies only to the original
Archie's Chess Analysis code.

## Stockfish.js 19.0.1

- Use: chess engine and browser worker
- Licence: GNU General Public License, version 3 (GPL-3.0)
- Package: https://www.npmjs.com/package/stockfish
- Source: https://github.com/nmrugg/stockfish.js
- Upstream engine: https://github.com/official-stockfish/Stockfish

The app loads the single-threaded Lite WebAssembly build from the Stockfish.js
19.0.1 package. That build is distributed under GPL-3.0. The engine is a
separate program and keeps its own licence.

## chess.js 1.4.0

- Use: PGN parsing, legal moves, and game rules
- Licence: BSD 2-Clause
- Source and licence: https://github.com/jhlywa/chess.js

## chessboard.js 1.0.0

- Use: interactive chessboard
- Licence: MIT
- Source and licence: https://github.com/oakmac/chessboardjs

## Cburnett chess piece artwork (SVG)

- Use: vector chess piece images displayed on the board
- Artist: Colin M. L. Burnett
- Source: https://github.com/lichess-org/lila/tree/master/public/piece/cburnett
- Licence: GNU General Public License, version 2 or later (GPL-2.0+)
- Upstream attribution: https://github.com/lichess-org/lila/blob/master/COPYING.md

The app loads the SVG pieces from the Lichess source repository. The artwork
retains its own licence and is separate from the MIT-licensed application code.

## jQuery 3.7.1

- Use: required by chessboard.js
- Licence: MIT
- Source and licence: https://jquery.com/license/

These libraries are loaded from their public CDNs when the page opens. An
internet connection is required to load them and the Stockfish engine.
