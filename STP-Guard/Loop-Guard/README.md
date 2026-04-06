# Loop Guard Lab – CCNP Enterprise

## Objective
To understand how Loop Guard protects the network from Layer 2 loops when BPDUs stop arriving on a non-designated/blocked path.

## Topology Used
- SW1 = Root Bridge
- SW2 = Intermediate Switch
- SW3 = Neighbor switch used to simulate BPDU loss

## Configuration Performed
- Enabled Rapid PVST
- Configured root bridge priority on SW1
- Applied Loop Guard on SW2 interface Gi0/1
- Enabled BPDU Filter on SW3 to stop BPDU transmission

## Verification
- Verified SW1 remained the root bridge
- Observed SW2 interface Gi0/1 entering `loop-inconsistent` state
- Confirmed protection using:
- show spanning-tree
- show spanning-tree inconsistentports

## Key Observation
- When BPDUs stopped arriving from SW3, Loop Guard prevented the port from incorrectly transitioning   to forwarding state.

## What I Learned
- Loop Guard protects STP from unexpected BPDU loss
- It helps prevent Layer 2 switching loops
- It places affected ports into loop-inconsistent state instead of allowing unsafe forwarding

## Screenshots Included
- Topology view and root bridge verification
- Loop Guard configuration on SW-2
- loop-inconsistent state proof & BPDU Filter trigger configuration on SW3



