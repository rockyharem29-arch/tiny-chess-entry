# tiny-chess-01

A Python 3 chess engine entry for the make.fun `tiny-chess-01` competition.

`main.py` is a self-contained engine (~4 KB) using a compressed lzma payload. It
is an 0x88 board representation with alpha-beta search, quiescence search
(captures only), Zobrist hashing, castling and en-passant, and legal-move
validation. It talks to the make.fun env over HTTP (`MAKEFUN_ENV_URL`).

Deterministic: every move derives only from the position, the game's moves and
the trial seed (no wall clock, no unseeded randomness).

## Run

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:PORT python3 main.py
```

## License

MIT — see LICENSE.
