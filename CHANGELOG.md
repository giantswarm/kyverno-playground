# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.0.1] - 2026-09-03

- added: Artifact Hub metadata (`artifacthub.io/license`, `artifacthub.io/links`) in the chart template ([roadmap#3940](https://github.com/giantswarm/roadmap/issues/3940)).

- changed: Regenerated `.circleci` config with `devctl gen circleci` — adopt the dynamic-config setup workflow (`config.yml` + `workflows.yml`) and bump the architect orb to v9.5.2.
- changed: `app.giantswarm.io` label group was changed to `application.giantswarm.io`

[Unreleased]: https://github.com/giantswarm/kyverno-playground/compare/v0.0.1...HEAD
[0.0.1]: https://github.com/giantswarm/kyverno-playground/releases/tag/v0.0.1
