# mouser-engine-skia

Mouser's Skia renderer (engine "skia") as an engine library on the C ABI (mouser-engine-abi v2).

Part of [Mouser](https://github.com/WeirdBrains/mouser), the terminal emulator. It is one of Mouser's official rendering engines, built on the same public API anyone can use ([mouser-engine-abi](https://github.com/WeirdBrains/mouser-engine-abi)).

## Install

Mouser ships with it. To install or update it yourself:

```sh
mouser engine install skia
mouser engine install gh:WeirdBrains/mouser-engine-skia
mouser engine use skia
```

Or in Mouser: `esc :ei skia`.

## Build

```sh
cargo build --release
# then: mouser engine install target/release   (with engine.toml beside the library)
```

## Documentation

- [docs/](docs/README.md)
- Mouser: [plugins](https://github.com/WeirdBrains/mouser/blob/main/docs/plugins.md), [engines](https://github.com/WeirdBrains/mouser/blob/main/docs/engines.md), [installing and updating](https://github.com/WeirdBrains/mouser/blob/main/docs/downloads.md)

## Releases and signatures

Published on [crates.io](https://crates.io/crates/mouser-engine-skia). GitHub releases are signed with the WeirdBrains minisign key ([minisign.pub](minisign.pub), `61BA1720747F9146`), the key Mouser pins for official plugins and engines:

```sh
minisign -Vm FILE -P RWRGkX90IBe6YaOypKF9r1wz4OqpCp3Ggb1Ag2omAzxTRaqoHzsNQSdP
```

## License

BSD-3-Clause, see [LICENSE](LICENSE).
