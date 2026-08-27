# DSH-PlayerLab

DSH-PlayerLab is a public research lab for testing DSH-powered game-companion ideas. It turns questions into small, repeatable experiments and promotes only proven, reusable work into a product or standalone plugin.

## Relationship to DeepSeek Harness

The lab treats [DeepSeek Harness](https://github.com/dsh2026/test-Alex-Yanggg) as an upstream plugin platform. Experiments use public DSH contracts; they do not fork, patch, vendor, or depend on Harness source internals.

## What belongs here

- Reproducible experiments about companion behavior, permissions, game integration, and evaluation.
- Thin prototypes that answer a stated question and can be removed cleanly.
- Evidence needed to decide whether work should move to DSH-Player2, become a separate plugin, or be deleted.

## What does not belong here

- A replacement agent harness or a copy of DeepSeek Harness.
- Unbounded prototypes with no hypothesis or exit condition.
- Gameplay bots, cheating tools, or concealed autonomous player actions.

## Contributing

Read [AGENTS.md](AGENTS.md) and [CONTRIBUTING.md](CONTRIBUTING.md) before starting an experiment.

The current [continuous-integration policy](docs/ci.md) protects the repository documentation while experiments are being defined.

The current experiment contracts live in [docs/experiments/README.md](docs/experiments/README.md). They are decision records, not an approval to build all three paths.

## License

A license has not yet been selected. Do not assume permission to reuse the repository contents until one is published.
