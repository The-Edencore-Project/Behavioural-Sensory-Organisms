# ⚙️ behaviour-os — Runtime Engine Structure

This folder contains the full implementation of the Behaviour OS. It includes the runtime loop, perception pipeline, reflex engine, dominance resolver, and posture system.

`

`markdown
behaviour-os/
│
├── init.py
│
├── runtime/
│   ├── init.py
│   ├── loop.py                # The four‑phase runtime loop
│   ├── timing.py              # Loop interval, drift control, stability
│   └── state.py               # Internal state: pressure, tier, posture
│
├── perception/
│   ├── init.py
│   ├── sensors.py             # Sensor interfaces + raw readings
│   ├── filtering.py           # Smoothing, noise floors, hysteresis
│   └── pressure.py            # Gradient + residual pressure model
│
├── reflex/
│   ├── init.py
│   ├── protocol_base.py       # Idle/Watching/Triggered/Recovering state machine
│   ├── protocol_loader.py     # Loads all 26 protocols
│   └── protocols/             # Individual protocol implementations
│       ├── init.py
│       ├── safety_*.py
│       ├── anomaly_*.py
│       ├── rhythm_*.py
│       └── tone_*.py
│
├── dominance/
│   ├── init.py
│   ├── hierarchy.py           # Tier definitions + suppression rules
│   └── resolver.py            # Determines dominant tier each loop
│
├── posture/
│   ├── init.py
│   ├── resolver.py            # Maps tier → Calm/Active/Protective
│   └── expression.py          # Logs, signals, behavioural presence
│
└── utils/
    ├── init.py
    ├── logging.py             # Behaviour‑safe logging
    └── config.py              # Sensitivity + thresholds
`

---

🌿 Why this structure is correct

# 1. It mirrors the four natural layers
- perception  
- reflex  
- dominance  
- posture  

Each layer has its own folder, its own responsibilities, and no cognitive contamination.

# 2. The runtime is isolated
The loop is its own subsystem.  
Nothing else can bypass it.

# 3. Protocols are modular
Each protocol is a file.  
Each file is a tiny state machine.  
No cross‑talk.  
No interpretation.

# 4. Dominance is centralised
All suppression logic lives in one place.  
This prevents behavioural chaos.

# 5. Posture is clean and final
Only one resolver.  
Only one expression layer.  
Only three modes.

---
