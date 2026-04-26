# ❓ How Edenshell Stores Memory — Q&A Mode
*Mode 1 — Clean, direct, grounded*  

---

## ❓ **Q: Does Edenshell store data to remember patterns?**
**A:** Yes — but only in the simplest possible form. It stores **baselines**, not **logs**. A baseline is a single evolving value that represents what “normal” looks like.

---

## ❓ **Q: What’s the difference between a baseline and a log?**
**A:** A **log** stores events, timestamps, sequences, and meaning. A **baseline** stores only the *current average state*. It’s a number, not a diary.

---

## ❓ **Q: Why doesn’t Edenshell store event history?**
**A:** Because APM is designed to avoid:
- identity tracking
- behavioural logging
- privacy issues
- AI‑style interpretation

It remembers patterns through **drift**, not storage.

---

## ❓ **Q: So what exactly does Edenshell store?**
**A:** Only values like:
- average noise level
- average vibration level
- average airflow pattern
- average movement density

These are simple floating‑point numbers updated over time.

---

## ❓ **Q: How does Edenshell update these baselines?**
**A:** Through a rolling average, such as:

new_baseline = (old_baseline * 0.99) + (current_reading * 0.01)

This slow update *is* the memory.

---

## ❓ **Q: Does Edenshell store past events?**
**A:** No. It stores **only the present**, very slowly. It never keeps:
- logs
- recordings
- sequences
- identities
- timestamps

APM is memory without history.

---

## ❓ **Q: How does Edenshell detect change without logs?**
**A:** By comparing:
- the **current reading**
- the **baseline reading**

If the difference exceeds a threshold, Edenshell reacts.

---

## ❓ **Q: Why is this safe and buildable in the real world?**
**A:** Because it mirrors how real systems work:
- thermostats
- smoke alarms
- seismographs
- adaptive lighting
- noise‑cancelling headphones

All of these use baselines, not logs.

---

## ❓ **Q: Does this make Edenshell intelligent?**
**A:** No. It makes Edenshell **sensitive**, not smart. It reacts to deviations, not meanings.

---

## ❓ **Q: What’s the simplest way to describe this?**
**A:** Edenshell doesn’t remember the past. It remembers the *present*, slowly.

It stores:
- baselines
- thresholds
- drift

It does **not** store:
- events
- stories
- identities
- intent

---

## ⭐ **Summary**
- Edenshell stores **baselines**, not logs.
- Baselines update slowly — that’s the memory.
- No events, no history, no AI.
- APM is memory as *state*, not storage.
- Edenshell compares the present to its baseline to detect change.

It doesn’t think — it **notices**.