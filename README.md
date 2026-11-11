# AetherCode Labs

The static studio website for AetherCode Labs: an independent software studio focused on AST analysis, automated unit-test generation, and command-line tooling.

## Site contents

- `index.html`: responsive single-page website with project specifications.
- `materials/`: downloadable studio and project READMEs.
- `LICENSE`: MIT License.
- `.nojekyll`: serves the static files without Jekyll processing.

The projects described on this site are at the design stage. No executable tool releases or passing CI results are claimed.

The page includes Tailwind's browser CDN as requested. Tailwind documents this CDN as a development and demonstration option, not a production build. The complete layout is also defined in ordinary CSS, so content and layout do not depend on the CDN loading. A later production cleanup can remove the optional CDN dependency.

## GitHub Pages

Publish the `main` branch and `/ (root)` directory through repository Settings → Pages → Deploy from a branch.

## License

MIT. See [LICENSE](LICENSE).
