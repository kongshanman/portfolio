# cli-testgen

A proposed CLI for unit-test scaffolds and explicit mocks, designed by **AetherCode Labs**.

> Design specification. No executable CLI or package release is available. These options describe a proposed interface.

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
3. Fork the repository and keep each change focused.
4. Include input and expected-output fixtures with future generator changes.
5. Include a file collision case for changes affecting writes.
6. Open a pull request describing the change and checks actually performed.

Documentation and design contributions are the current contribution path. Development commands will be added with the implementation.

## License

MIT License. See [LICENSE](../LICENSE).
