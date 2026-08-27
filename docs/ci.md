# Continuous integration and delivery

The repository runs [CI](../.github/workflows/ci.yml) for every pull request, push to `main`, and manual workflow dispatch.

## What CI checks today

The lab has no executable experiment yet. The workflow rejects whitespace errors and runs [`scripts/verify-docs.mjs`](../scripts/verify-docs.mjs), which requires one H1 per Markdown document and validates repository-relative Markdown links.

## Merge rule

Protect `main` in GitHub: require the CI check to pass and require review before merge. Pull requests must provide the experiment hypothesis, success signal, teardown condition, and verification evidence required by [CONTRIBUTING.md](../CONTRIBUTING.md).

## Delivery rule

Lab experiments do not publish product releases. When an experiment produces a buildable plugin or tool, its promotion pull request must add build, test, and package validation. Releases must run only from protected tags and publish a traceable artifact; credentials belong in GitHub Environments or an identity provider, never in the repository.
