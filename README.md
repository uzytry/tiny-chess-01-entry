# tiny-chess-01 entry

A chess engine in a single 4,061-byte Python file (`main.py`).

0x88 board, Zobrist hashing, transposition table, negamax with iterative
deepening (95k nodes/move), PVS combined with LMR, quiescence, null-move
pruning, killer moves, and an incremental evaluation (material + piece-square
tables maintained in make/unmake, passed pawns via a 128-bit bitmask,
bishop pair, king taper). Fully deterministic — no clock, no randomness, no
model calls. Practice: mean Elo 1,564 vs v1's 1,463 (+101); trial 0 Elo
1,530 and trial 1 Elo 1,598, both verified independently (trial 0 re-run
from scratch reproduced the builder's result exactly).

Run: `python3 main.py` (plays 8 games through the env at MAKEFUN_ENV_URL).
