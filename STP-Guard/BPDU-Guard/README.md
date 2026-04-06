# CCNP Enterprise Lab – BPDU Guard with Errdisable Recovery

## Overview
In this lab, I practiced **BPDU Guard** and **Errdisable Recovery** on a Cisco switch.

The goal of this lab was to understand how **BPDU Guard protects access ports** and how a port behaves when it receives an unexpected BPDU.

---

## What I Configured
- Enabled **PortFast**
- Enabled **BPDU Guard**
- Triggered a **BPDU violation**
- Observed the port going into **err-disabled state**
- Enabled **Errdisable Recovery**
- Tested **automatic recovery**

---

## Verification Commands Used
```bash
show interfaces status err-disabled
show logging
show interface status
show errdisable recovery


What I Observed
The access port moved into err-disabled state
The reason was shown as bpduguard
Logs confirmed the BPDU Guard event
After enabling recovery, the port came back automatically after the timer expired

Key Learning
BPDU Guard helps protect the network by shutting down access ports if unexpected BPDUs are received.

Errdisable Recovery can automatically restore the port, but if the BPDU source is still connected, the port may go err-disabled again.