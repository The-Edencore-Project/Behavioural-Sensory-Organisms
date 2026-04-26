# 🔁 Runtime — Behaviour OS Loop Engine

This document defines the runtime loop used by Behavioural Sensory Organisms. The loop transforms sensory pressure into coherent behaviour through a deterministic four‑phase cycle.

---

## 🌿 Overview

The runtime loop is the core of the Behaviour OS. It processes perception, executes reflex protocols, resolves dominance, and determines the organism’s global posture.

The loop is intentionally minimal. It avoids cognition, planning, interpretation, and world modelling. Its purpose is to maintain behavioural stability under all conditions.

---

# 🧩 The Four Phases of the Loop

The Behaviour OS loop runs continuously. Each cycle processes the environment and updates the organism’s internal state.

---

## 1. 🌡 Perception Phase  
*Convert raw sensor readings into pressure*

The runtime collects sensor values and passes them through filtering, smoothing, noise floors, and hysteresis. This produces stable pressure gradients.

Perception defines the organism’s sensitivity and determines how strongly it reacts to environmental change.

---

## 2. ⚡ Reflex Phase  
*Execute protocol state machines*

Each protocol receives updated pressure values and transitions through Idle, Watching, Triggered, or Recovering states. Protocols do not interpret or reason.

The reflex phase generates the organism’s behavioural texture.

---

## 3. 🧩 Dominance Phase  
*Resolve conflicts and select the active tier*

The runtime evaluates all protocol states and determines which tier dominates. Higher tiers suppress lower tiers to maintain coherence.

Dominance ensures the organism behaves as a unified entity rather than a collection of competing reflexes.

---

## 4. 🌙 Posture Phase  
*Collapse behaviour into a global mode*

The runtime maps the dominant tier to one of three global modes: Calm, Active, or Protective. This posture defines the organism’s outward expression.

Posture provides behavioural clarity and prevents chaotic output.

---

# 🌊 Loop Timing

The runtime loop operates at a fixed interval. Timing must remain stable to ensure predictable behaviour. Each cycle processes all four phases before the next begins.

The loop must avoid drift, jitter, and blocking operations. Deterministic timing is essential for behavioural stability.

---

# 🧬 Internal State

The runtime maintains a small internal state:

- current pressure values  
- protocol states  
- dominant tier  
- global posture  
- residual tension  

This state is updated every cycle and never grows beyond the minimal required footprint.

---

# 🛡 Safety Guarantees

The runtime enforces strict safety rules:

- safety protocols always dominate  
- posture transitions follow deterministic paths  
- no protocol can bypass dominance  
- no behaviour can occur outside the loop  

These guarantees prevent unpredictable behaviour.

---

# 🏛 Implementation Notes

The runtime is designed for small devices and low‑power environments. It avoids heavy computation and maintains strict timing guarantees.

All implementations must preserve the four‑phase loop and the dominance hierarchy.

---

# ⭐ Summary

The runtime loop is the behavioural engine of a BSO. It processes sensory pressure, executes reflexes, resolves dominance, and expresses a single global posture.

This deterministic cycle creates stable, coherent behaviour without cognition.