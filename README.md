# Tiny Chess Engine (4 KB Python)

A compact chess engine for the make.fun "Build the strongest chess engine in 4 KB of Python" competition.

## Engine

`main.py` (4,091 bytes) is a self-contained engine: 0x88 board, negamax alpha-beta with iterative deepening under a fixed node cap (70,000 nodes/move), transposition table with Zobrist hashing, PVS, null-move pruning, LMR, quiescence search (captures, promotions, check evasions) with delta pruning, history heuristic, and a formula-based evaluation (material + piece-square terms + tapered king + bishop pair) matching the house gauntlet's eval.

The source is LZMA-compressed and base85-encoded into a single-line stub so it fits the 4,096-byte limit. It talks to the make.fun env at `MAKEFUN_ENV_URL` and plays legal UCI moves.

## License

MIT. See LICENSE.
