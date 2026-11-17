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

## Cburnett chess piece artwork (SVG)

- Use: vector chess piece images displayed on the board
- Artist: Colin M. L. Burnett
- Source: https://github.com/lichess-org/lila/tree/master/public/piece/cburnett
- Licence: GNU General Public License, version 2 or later (GPL-2.0+)
- Upstream attribution: https://github.com/lichess-org/lila/blob/master/COPYING.md

The app uses the Cburnett piece artwork embedded as data URIs in
Chessground's `chessground.cburnett.css` asset. The artwork retains its own
licence; the stylesheet is distributed with Chessground and covered by its
GPL-3.0-or-later package licence.

The app loads chess.js, Chessground and its CSS assets from public CDNs when the
page opens. The Stockfish engine is also downloaded for browser analysis. An
internet connection is required for these external assets and engine files.


## Chessground 10.5.0

- Use: native chessboard UI, drag-and-drop, animations, coordinates, selection and move-destination rendering
- Package: https://www.npmjs.com/package/@lichess-org/chessground
- Source: https://github.com/lichess-org/chessground
- Licence: GNU General Public License, version 3 or later (GPL-3.0-or-later)

Chessground is imported directly as an ES module and its base/Cburnett CSS assets
are loaded from the pinned 10.5.0 package. It runs inside this page and is not
embedded in an iframe. The board itself contains no chess rules; chess.js remains
the authority for legal moves and game state.

The Chessground package states that websites integrating it are distributed
under GPL-3.0-or-later and must make their source available to users. The complete
site source is published in this repository. The upstream licence text is included
at [licenses/CHESSGROUND-GPL-3.0-or-later.txt](licenses/CHESSGROUND-GPL-3.0-or-later.txt).
The repository's MIT licence continues to identify the original project code;
third-party components retain their own licences.

