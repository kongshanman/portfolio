# AetherCode Labs

The static studio website for AetherCode Labs: an independent software studio focused on AST analysis, automated unit-test generation, and command-line tooling.

[Visit the website](https://kongshanman.github.io/portfolio/) · [Studio profile](https://github.com/kongshanman) · [Browser-only deployment guide (Chinese)](BROWSER-DEPLOYMENT.zh-CN.md)

## Repositories and materials

| Repository | Purpose | English material |
| --- | --- | --- |
| [kongshanman](https://github.com/kongshanman/kongshanman) | GitHub profile for AetherCode Labs | [Profile README](materials/profile-README.md) |
| [ast-refactor-core](https://github.com/kongshanman/ast-refactor-core) | AST analysis and code smell detection specification | [Project README](materials/ast-refactor-core-README.md) |
| [cli-testgen](https://github.com/kongshanman/cli-testgen) | Unit-test and mock generation CLI specification | [Project README](materials/cli-testgen-README.md) |
| [portfolio](https://github.com/kongshanman/portfolio) | Single-page studio website | [index.html](index.html) |

## Site contents

- `index.html`: responsive single-page website with project specifications.
- `materials/`: downloadable studio and project READMEs.
- `LICENSE`: MIT License.
- `.nojekyll`: serves the static files without Jekyll processing.
- `BROWSER-DEPLOYMENT.zh-CN.md`: click-by-click repository creation, README editing, and GitHub Pages publication instructions.

The projects described on this site are at the design stage. No executable tool releases or passing CI results are claimed.

The page includes Tailwind's browser CDN as requested. Tailwind documents this CDN as a development and demonstration option, not a production build. The complete layout is also defined in ordinary CSS, so content and layout do not depend on the CDN loading. A later production cleanup can remove the optional CDN dependency.

## GitHub Pages

Publish the `main` branch and `/ (root)` directory through repository Settings → Pages → Deploy from a branch.

## License

MIT. See [LICENSE](LICENSE).
