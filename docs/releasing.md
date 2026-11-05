# Releasing mouser-engine-skia

1. Bump `version` in Cargo.toml and engine.toml, update CHANGELOG.md.
2. Commit, tag `vX.Y.Z`, push the tag.
3. `.github/workflows/release.yml` builds for x86_64 Linux, macOS (arm64 and x86_64) and x86_64 Windows, adds `FILE.sha256` and `FILE.minisig` (minisign, from the `MINISIGN_SECRET_KEY` and `MINISIGN_PASSWORD` secrets) and publishes the GitHub release.
4. `cargo publish` (crates.io).
5. Point Mouser's `crates/mouser-core/src/plugins.lock` at the new assets.

Assets are named `mouser-engine-skia-VERSION-TARGET.tar.gz`, the layout `mouser engine install gh:WeirdBrains/mouser-engine-skia` expects.
