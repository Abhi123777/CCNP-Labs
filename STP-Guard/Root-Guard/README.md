# Root Guard Lab (CCNP)

## Objective
To protect the root bridge from unauthorized switches using Root Guard.

## Topology
- SWITCH-1: Root Bridge
- SWITCH-2: Root Guard applied
- SWITCH-3: Rogue switch (attempted to become root)

## Configuration
- Applied Root Guard on designated port (SW2)

## Verification
- Observed port blocking when superior BPDU was received
- Verified root-inconsistent state using:
- show spanning-tree inconsistentports

- Confirmed original root bridge remained unchanged

## Key Learning
Root Guard prevents unwanted root bridge election and maintains Layer 2 stability.
