# ast-refactor-core

A lightweight AST parsing and code smell detection toolkit designed by **AetherCode Labs**.

[![License: MIT](https://img.shields.io/badge/License-MIT-475569.svg)](https://github.com/kongshanman/ast-refactor-core/blob/main/LICENSE)
![Status: Design stage](https://img.shields.io/badge/Status-design_stage-9a3412.svg)

[Studio website](https://kongshanman.github.io/portfolio/) · [Studio profile](https://github.com/kongshanman) · [Related project: cli-testgen](https://github.com/kongshanman/cli-testgen)

> Design specification. No working analyzer or published package is available in this starter project. The following behavior is proposed.

## Features — Planned

- Parse JavaScript and TypeScript with source locations.
- Traverse syntax nodes through an explicit rule interface.
- Detect configurable structural smells, starting with nesting depth and function length.
- Emit diagnostics with rule identifiers, severity, location, and explanation.
- Export structured JSON without modifying source files.

## Installation

No installable package is available yet. Package names and supported runtime versions will be documented with the first executable release. Downloading this repository provides design materials, not an installed analyzer.

To obtain the current materials without a terminal, open this repository on GitHub, select **Code**, then **Download ZIP**. Extract the archive and read `README.md` and `LICENSE`. This does not install or execute an analysis tool.

## Usage — Pseudocode

```text
source = read_text("src/example.ts")
tree = parse_source(source, language="typescript", locations=true)
diagnostics = analyze(tree, rules={"max-nesting-depth": {"limit": 4}})
for diagnostic in diagnostics:
    print(diagnostic.rule, diagnostic.location, diagnostic.message)
```

This is an illustrative data flow, not an executable API or recorded result.

## Boundaries

Code smells are review signals, not proof of defects. Automatic rewriting, runtime execution, and whole-program semantic analysis are outside the initial scope. Parser coverage and supported syntax remain to be specified.

## Contributing

Propose a rule with a minimal input, expected diagnostic, and a similar example that should not trigger it. Keep changes focused and document trade-offs.

## License

MIT License. See [LICENSE](https://github.com/kongshanman/ast-refactor-core/blob/main/LICENSE).
