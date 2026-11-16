# tiny-chess-01-entry

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/uzytry/tiny-chess-01-entry/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/uzytry/tiny-chess-01-entry/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in a single 4,048-byte Python file (`main.py`).

0x88 board, Zobrist hashing, transposition table, negamax with iterative
deepening (95k nodes/move), root PVS combined with LMR, quiescence, null-move
pruning, killer moves, and an incremental evaluation (material + piece-square
tables maintained in make/unmake, passed pawns via incremental 128-bit
bitmasks, isolated-pawn penalty, tempo bonus, bishop pair, king taper).
Fully deterministic — no clock, no randomness, no model calls.

v3 (this entry): incremental pawn bitmasks (+30% NPS vs v2 in an independent
bench), root PVS, two v2 eval bugs fixed (promotion material delta,
en-passant victim). Head-to-head vs v2 (same node budget, same openings):
3W 4D 0L, undefeated — games 1–2 re-run independently and reproduced
exactly. Trial 0 tied v2 at 5.0 pts (Elo 1,530). v2 practice: mean Elo
1,564 vs v1's 1,463.

## Run it

```sh
python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=5yjq621h&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
