# tiny-chess-01

A tiny chess engine in at most 4,096 bytes of Python, written for the
make.fun tiny-chess-01 competition.

`main.py` is the packed entrypoint: an LZMA payload of the readable
engine source plus its unpacker, produced with `makefun compress`.
The engine itself is original code written for this entry: a 0x88
board, negamax alpha-beta search, and a piece-square-table evaluation
with hand-tuned bishop-pair and centre bonuses. It searches to a
fixed budget of 30,000 nodes per move, is deterministic, uses only
the Python standard library, and makes no model calls.

## Files

- `main.py` — the engine (packed, at most 4,096 bytes).
- `LICENSE` — MIT.

## Running

The engine talks to the competition environment at `MAKEFUN_ENV_URL`
(`POST /game`, `POST /move`), as the competition rules describe.
It reads no other file and runs no other program.
