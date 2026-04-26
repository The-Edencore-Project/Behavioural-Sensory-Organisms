behaviour-os/
│
├── runtime/        (3 files)
│     loop.py
│     timing.py
│     state.py
│
├── perception/     (3 files)
│     sensors.py
│     filtering.py
│     pressure.py
│
├── reflex/         (28 files)
│     protocol_base.py
│     protocol_loader.py
│     protocols/
│         safety_*.py      (x6)
│         anomaly_*.py     (x6)
│         rhythm_*.py      (x7)
│         tone_*.py        (x7)
│
├── dominance/      (2 files)
│     hierarchy.py
│     resolver.py
│
├── posture/        (2 files)
│     resolver.py
│     expression.py
│
├── utils/          (2 files)
│     config.py
│     logging.py
│
└── identity/       (2 files)
      constitution.py
      boundaries.py