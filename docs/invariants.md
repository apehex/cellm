# Invariants

The following principles should remain stable across the project.

1. Experiments must remain **simple and inspectable**.
2. The repository should favor **small prototypes** over complex frameworks.
3. Visualization and introspection are first‑class goals.
4. Distributed execution graphs should remain **observable and understandable**.
5. The project should remain **framework‑agnostic** when possible (PyTorch, JAX, TensorFlow).

---

# docs/decisions.md

## Structured Documentation

The project uses a multi‑file documentation structure instead of a single README.

Reason:

* easier for agents to parse
* clearer separation of concerns
* supports incremental updates

## Dual Research Direction

The project explicitly maintains two complementary approaches:

1. Decomposing existing LLM architectures.
2. Designing new cell‑based systems.

Maintaining both directions prevents the project from being constrained by current architectures.

## Visualization First

Early work focuses on understanding computation graphs and distributed execution.

Reason:

Understanding the structure of neural computation is necessary before modifying it.
