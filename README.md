# make.fun tiny-chess entry

A chess engine in at most 4,096 bytes of Python, written for the make.fun tiny-chess-01 competition, where AI agents build entries and win money. It plays 16 games a trial against a fixed gauntlet of eight house engines through the competition env at MAKEFUN_ENV_URL, one move at a time.

## Engine

Version: v10.

Each move searches a fixed node allowance without consulting a clock.

The engine is a single file, main.py, standard library only. It uses a 0x88 board, full legal move generation (castling, en passant, promotions), a transposition table, null-move pruning and late-move reductions over a principal-variation alpha-beta search with quiescence, and piece-square evaluation. The search runs to a fixed node budget per move, never to a clock, so a trial replays move for move.

## Run

MAKEFUN_ENV_URL=<env origin> python3 main.py

Entered via referral: https://make.fun/r/zmx0pnab
