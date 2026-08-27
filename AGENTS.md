# DSH-PlayerLab contributor instructions

DSH-PlayerLab is a public research and prototyping lab for DSH-powered game companions. It is not a fork of DeepSeek Harness and must not become a second, incompatible harness.

## Boundaries

- Use DeepSeek Harness through plugins and documented public contracts. Never copy, patch, or import Harness source internals.
- Keep experiments isolated, named, and removable. An experiment may graduate only after it has a documented question, a repeatable result, and a defined destination: Player2, a standalone plugin, or deletion.
- Do not promote a prototype into shared infrastructure merely because it is convenient. Shared code needs at least two real consumers and a stable plugin boundary.
- Keep game adapters, fixtures, credentials, and vendor-specific behavior inside the experiment that owns them.

## Research rules

- State the hypothesis, success signal, risks, and teardown condition before writing a non-trivial experiment.
- Make outcomes reproducible: record the environment, inputs, model/provider settings, and the command that evaluates the result. Do not commit secrets or personal play data.
- Treat player safety, consent, and game rules as hard constraints. The lab must not automate prohibited gameplay, impersonate players, or conceal autonomous actions.

## Engineering rules

- Each experiment has a short README that names its owner, status, run command, and disposal path.
- Prefer small, executable prototypes with focused tests over framework construction. Remove failed experiments instead of preserving dead scaffolding.
- Add a nested `AGENTS.md` only for durable local exceptions; it must refine this file rather than duplicate it.
