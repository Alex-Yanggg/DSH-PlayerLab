# Contributing to DSH-PlayerLab

Thank you for helping make the research useful and reproducible.

## Before starting an experiment

- State the hypothesis, success signal, risks, owner, and teardown condition in the experiment documentation.
- Confirm whether the work belongs in the lab, DSH-Player2, or a standalone DSH plugin before building shared infrastructure.

## Pull requests

- Keep each experiment runnable from a clean checkout and document its environment, inputs, provider settings, and evaluation command.
- Do not commit credentials, personal play data, proprietary game content, or generated build output.
- Include focused automated checks when feasible; otherwise provide exact manual reproduction and verification steps.
- Keep DeepSeek Harness changes in a separate upstream proposal. Lab work may use public DSH releases but must not patch the core as a shortcut.
- Follow the [operating model](docs/operating-model.md) for research intake, evidence, Git hygiene, promotion, and owner gates.
