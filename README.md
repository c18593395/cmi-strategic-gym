# VCMI Strategic Gym

Reinforcement-learning training stack for **adventure-map (strategic) AI** in
[VCMI](https://github.com/vcmi/vcmi) — the open engine for Heroes of Might and Magic III.

The official VCMI ecosystem ships ML-based *combat* AIs (MMAI), but there is no
ML-driven *adventure/strategic* AI. This project fills that gap: a gym
environment over the VCMI server, PPO training pipelines, and model releases
that can be dropped into a VCMI build to play full maps (heroes, towns,
mines, battles).

> Status: active development. Engine-side pieces live in a companion
> `vcmi-native` fork; see the training docs for the build contract.

## Layout

```
connectors/   C++ pybind11 connectors (v13/v14/v15) bridging the VCMI engine and Python
envs/         Python environments (v13: strategic + battle, v14, v15)
tools/        arena / benchmarking utilities
```

## Quick start

Training environment and engine build prerequisites are documented in the
companion training repo (`hero3_fresh`). To build the connector:

```bash
cd connectors
cmake -B build -G Ninja
cmake --build build
```

## License

MIT (this repository). VCMI engine code is GPL-2.0+.
