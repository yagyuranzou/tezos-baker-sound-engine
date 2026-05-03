# TEZOS BAKER SOUND ENGINE v4

**delegation → probability → selection → sound → replay**

---

## overview

Tezos Baker Sound Engine v4 is a self-contained browser simulation.

It models a simplified baker system where stake distribution influences probabilistic selection, and each selection is rendered as sound.

All activity is generated locally.
There is no external data input.

---

## what this actually is

* not a blockchain client
* not connected to Tezos network
* not live data

It is a **closed system** that mimics:

* delegation
* stake weighting
* validator selection

and turns the result into a continuous audio stream.

---

## core mechanics

### stake → probability

Each baker has:

* self stake (adjustable)
* delegated stake (from fixed delegators)

Total stake defines selection weight.

---

### selection (consensus simulation)

Every tick:

* total weights are calculated
* one baker is selected via weighted randomness
* previous winner is penalized (reduced weight)

This prevents static dominance and creates variation.

---

### sound

Each selected baker triggers:

* a square wave oscillator
* fixed frequency per baker
* short pulse (per event)

Each selection = one sonic event.

---

### timeline memory

Every event is recorded:

* baker id
* frequency
* total stake

This creates a linear history.

---

### replay system

The system can:

* replay past events sequentially
* scrub via timeline slider
* re-trigger sound from stored history

Replay is not regeneration.
It is **re-execution of memory**.

---

## interface

### controls

* START — begin simulation
* STOP — halt simulation
* REPLAY — play recorded sequence
* STOP REPLAY — stop replay

---

### sliders

Each baker's self stake can be adjusted in real time.

This directly reshapes probability distribution.

---

### timeline

* accumulates events over time
* allows navigation through past states
* decouples playback from generation

---

## structure

This system reduces a complex process into five layers:

delegation
→ stake
→ probability
→ selection
→ sound

with an added layer:

→ memory (timeline)

---

## v4 focus

v4 is defined by:

* persistent event history
* timeline control
* replay as a core feature

The system is no longer only live.

It can be revisited.

---

## note

Every run produces a different sequence.

Not because of data,
but because of probability.

---

creatived by Yagyu Ranzou
2026


## launch

https://yagyuranzou.github.io/tezos-baker-sound-engine/
