# GraphFusion website

Publishes [graphfusion.github.io](https://graphfusion.github.io/) from the
[documentation source](https://github.com/GraphFusion/GraphFusion/tree/main/website).
Edit and review documentation in `GraphFusion/GraphFusion`.

The Pages workflow checks `main` daily at 09:00 Asia/Shanghai (01:00 UTC) and rebuilds when the
source commit changes, including Rust engine changes. GitHub may delay scheduled runs. Use **Actions →
Publish documentation → Run workflow** for immediate publication or to publish a
specific source branch or commit. Source must use the root (`/`) base path.

The workflow builds the browser engine with Rust 1.98.0, wasm-bindgen 0.2.128,
and checksum-verified Binaryen 133 before building the site. Browser tests must
pass before publication. The first build takes several minutes; Cargo and
bindings are cached for later runs. `/source-revision.txt` records the published
GraphFusion source commit.

Pages uses GitHub Actions. No deploy keys or cross-repository secrets are needed.
