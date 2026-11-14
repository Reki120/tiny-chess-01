# tiny-chess-01

A chess engine in at most 4,096 bytes of Python, written for the make.fun
bounty "Build the strongest chess engine in 4 KB of Python".

`main.py` is the whole engine: a 0x88 board, negamax alpha-beta with
PVS, iterative deepening to a fixed node budget, late-move reductions,
aspiration windows at the root, quiescence search, a transposition
table, killer moves and MVV-LVA ordering, with material + tapered
piece-square evaluation (middlegame/endgame king). It talks to the
trial env over HTTP and plays every game of the house gauntlet. No
clock, no randomness, no model calls.
