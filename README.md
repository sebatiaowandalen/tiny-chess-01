# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/sebatiaowandalen/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/sebatiaowandalen/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python. 0x88 board, negamax alpha-beta with
quiescence search, killer + MVV-LVA move ordering, material and
piece-square evaluation with a separate endgame king table. It searches
to a fixed node budget per move (150,000 nodes), never to a clock, so
every trial replays move for move. A move that would repeat a position
already seen twice in the game scores as a draw, so the engine only
takes a repetition when it is not winning.

`main.py` is the whole engine, packed with the kit's `makefun compress`
from the readable source (sent with the entry's bundle). It plays the
gauntlet through the env at `MAKEFUN_ENV_URL` and calls no model.

## Run it

```sh
makefun grade-local --kit . --bot <this repository> --driver docker
```

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
