# tiny-chess-01 entry

A chess engine in 4 KB of Python: 0x88 board, alpha-beta/PVS search with
iterative deepening under a fixed node budget, transposition table, killer
moves, LMR, null-move pruning, quiescence (captures, promotions, check
evasions), material + formula piece-square eval with tapered king tables
and the bishop pair. Deterministic: fixed node budget, no clock, no
unseeded randomness — the same position always gets the same move.

## Files

- `main.py` — the entry (3,828 bytes), produced by the kit's own
  `makefun compress` from `source.py` (see below).
- `source.py` — the readable engine source (kept uncommitted; the
  submitted snapshot holds only `main.py`, `LICENSE` and this README).
- `LICENSE` — MIT.

## Build

From the kit directory, after any change to `source.py`, run as its own
command:

    node cli/makefun.mjs compress source.py --out main.py

## Grade locally

    node cli/makefun.mjs grade-local --kit <kit> --bot . --driver docker

Or run the practice trial against the kit env directly (see
`../tiny-chess-dev/run_trial.sh` in the author's workspace).

## Size

- `main.py`: 3,828 bytes (limit 4,096)
- Snapshot (`main.py` + `LICENSE` + `README.md`): under 8,192 bytes,
  no file over 4,096.
