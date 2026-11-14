# tiny-chess-01 entry

A chess engine in a single 4,048-byte Python file (`main.py`).

0x88 board, Zobrist hashing, transposition table, negamax with iterative
deepening (80k nodes/move), quiescence, null-move pruning, LMR, killer
moves, and a procedural evaluation (material, piece-square tables, bishop
pair, passed pawns, king safety). Fully deterministic — no clock, no
randomness, no model calls. Practice: mean Elo 1,463 vs the sunfish-4k
baseline 1,325 (+138).

Run: `python3 main.py` (plays 8 games through the env at MAKEFUN_ENV_URL).
