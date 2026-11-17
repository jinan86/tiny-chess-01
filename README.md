# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/jinan86/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/jinan86/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in a single `main.py` of 3,760 bytes: 0x88 board, negamax
with alpha-beta, quiescence search, transposition table, killer moves,
MVV-LVA ordering, null-move pruning and iterative deepening on a fixed
60,000-node budget per move. Its evaluation mirrors the house eval
(material 100/320/330/500/900, formula piece-square terms, bishop pair,
tapered king). It plays the gauntlet through the env at
`MAKEFUN_ENV_URL` (`POST /game`, `POST /move`), deterministically: no
clock, no randomness. `main.py` is an LZMA payload packed with the kit's
`makefun compress`; the readable source is `engine_src.py`, kept beside
the sessions and not committed.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

## Grade it locally

```sh
node cli/makefun.mjs grade-local --kit <kit> --bot <this repo> --driver docker
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=jinan86&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
