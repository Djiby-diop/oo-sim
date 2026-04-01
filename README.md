# oo-sim — Operating Organism Simulation Layer

> **Couche 3 — Simulation Layer** | [oo-system architecture](https://github.com/Djiby-diop/oo-system)

Part of the [Operating Organism](https://github.com/Djiby-diop/oo-system) ecosystem.

Bac à sable pour tester les comportements OO sans hardware réel.
Objectif Phase 2 : premier monde simulé (agents + politique D+).


The goal is to have a small, controllable "world" where the OO logic can be exercised without
needing real hardware, UEFI or a full operating system.

Typical scenarios for oo-sim:

- Simulate tasks, resources and deadlines that an OO instance has to manage.
- Run many steps quickly to test OO scheduling, agendas and policies.
- Explore how different modes (SAFE / DEGRADED / NORMAL) affect behaviour.
- Feed synthetic events into the same kinds of journals and states used by the real system.

### Status

At the moment this is just a skeleton with a single C entry point under `src/`.
It does not define a full simulation model yet.

All code in this directory should:

- Stay small and composable.
- Use plain C and the standard library.
- Stay ASCII only.
- Avoid heavy frameworks or complex build systems.

### Building

There is no complex build system yet.

From this directory, on a machine with a C compiler, you can start with:

```bash
cc -Wall -Wextra -O2 -std=c11 -o oo-sim.exe src/oo_sim_main.c
```

On Windows you can adapt this to your compiler of choice.

