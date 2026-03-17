# Context Of The Project

**cellm** explores whether neural networks can be organized as systems of semi-autonomous computational "cells".

The project investigates how modern large language models (LLMs) can be decomposed into interacting components that:

* maintain local state
* exchange messages with neighboring components
* adapt through local rules

The long-term objective is to study learning systems where adaptation can emerge from interactions between distributed components rather than from a single centralized optimization procedure.

## Core Observation

Large neural networks are already executed as distributed systems.

Training and inference of LLMs rely on strategies such as:

* Data Parallelism
* Tensor Parallelism
* Pipeline Parallelism
* Fully Sharded Data Parallel
* Context / Sequence Parallelism

These strategies transform a neural network into a **distributed execution graph** composed of computation shards communicating through explicit synchronization and data exchange.

This structure resembles a system of interacting units rather than a monolithic function.

## Two Exploration Paths

### Top‑Down

Start from existing pretrained models and progressively decompose them into smaller computation shards.

Goals:

* extract computation graphs
* visualize distributed execution
* identify natural boundaries for "cells"

### Bottom‑Up

Design minimal computational cells and observe what kinds of computation emerge from their interactions.

Goals:

* implement message‑passing cells
* explore local plasticity rules
* investigate emergent routing or attention
