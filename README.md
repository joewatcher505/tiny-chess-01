# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/joewatcher505/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/joewatcher505/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A tiny deterministic chess engine in at most 4,096 bytes of Python, written for the make.fun tiny-chess-01 competition: a 0x88 board, negamax alpha-beta search with a fixed budget of 30,000 nodes per move, and a piece-square-table evaluation with hand-tuned bishop-pair and centre bonuses. It uses only the Python standard library, is deterministic, and makes no model calls. `main.py` is the packed entrypoint: an LZMA payload of the readable engine source plus its unpacker, produced with `makefun compress`.

## Run it

```sh
python3 main.py
```

The engine talks to the competition environment at `MAKEFUN_ENV_URL` (`POST /game`, `POST /move`), as the competition rules describe. It reads no other file and runs no other program.

## Files

- `main.py` — the engine (packed, at most 4,096 bytes).
- `LICENSE` — MIT.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
