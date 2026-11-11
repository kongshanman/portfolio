# cli-testgen

A proposed CLI for unit-test scaffolds and explicit mocks, designed by **AetherCode Labs**.

[![License: MIT](https://img.shields.io/badge/License-MIT-475569.svg)](https://github.com/kongshanman/cli-testgen/blob/main/LICENSE)
![Status: Design stage](https://img.shields.io/badge/Status-design_stage-9a3412.svg)

[Studio website](https://kongshanman.github.io/portfolio/) · [Studio profile](https://github.com/kongshanman) · [Related project: ast-refactor-core](https://github.com/kongshanman/ast-refactor-core)

> Design specification. No executable CLI or package release is available. These options describe a proposed interface.

## Installation Status

No installable package is available yet. On GitHub, select **Code** then **Download ZIP** to obtain the design materials. Runtime support and installation instructions will accompany an executable release.

## Features — Planned

- Discover exported JavaScript and TypeScript functions through static inspection.
- Generate editable Vitest or Jest test scaffolds.
- Generate explicit mock stubs for imports when requested.
- Mark unknown expected results as TODO items.
- Preview output without writing files.
- Refuse to overwrite files unless explicitly requested.

## Proposed Usage

```text
cli-testgen ./src/math.ts --framework vitest --out-dir ./tests --dry-run
```

This command documents proposed syntax; it cannot run until an implementation is released.

## Proposed Parameters

| Parameter | Values | Default | Purpose |
| --- | --- | --- | --- |
| `<input>` | File or directory | Required | Source to inspect |
| `--framework` | vitest, jest | vitest | Test template format |
| `--out-dir` | Directory path | ./tests | Output directory |
| `--mock` | none, imports | none | Mock generation mode |
| `--dry-run` | Flag | false | Preview without writing |
| `--overwrite` | Flag | false | Permit replacing target files |
| `--help` | Flag | false | Display usage |
| `--version` | Flag | false | Display release version |

## Generated-Test Policy

Generated scaffolds require human review. Expected values must come from requirements or verified examples. Mocks must expose dependency assumptions. Passing-test and coverage claims require real execution.

## Contributing

1. Open an issue with the use case, minimal source example, and expected test structure.
2. Check for existing proposals before adding an option.
3. Select **Fork** on GitHub and create the fork in your account. Open the relevant file in your fork, select its pencil-shaped **Edit** button, make the change, and select **Commit changes**.
4. Include input and expected-output fixtures with future generator changes.
5. Include a file collision case for changes affecting writes.
6. In your fork, select **Contribute**, then **Open pull request**. Confirm the base repository is `kongshanman/cli-testgen`, describe the change and checks actually performed, and select **Create pull request**.

Documentation and design contributions are the current contribution path. Development commands will be added with the implementation.

## License

MIT License. See [LICENSE](https://github.com/kongshanman/cli-testgen/blob/main/LICENSE).
