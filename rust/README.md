## Rust dev
[![rust-dev](https://github.com/andrmr/registry/actions/workflows/rust-dev.yml/badge.svg?event=push)](https://github.com/andrmr/registry/actions/workflows/rust-dev.yml)  

```Dockerfile
FROM ghcr.io/andrmr/registry/rust-dev:latest as rust-dev
```
Rust base image for blazingly fast dev compilation. Based on slim-bookworm.  
Includes:
- [mold linker](https://github.com/rui314/mold)
- [cranelift backend](https://github.com/rust-lang/rustc_codegen_cranelift)
- nightly toolchain  

To enable these features, add these lines to `.cargo/config.toml`:
```toml
# .cargo/config.toml

[unstable]
codegen-backend = true

[profile.dev]
codegen-backend = "cranelift"
rustflags = ["-Z", "threads=16"]

[target.x86_64-unknown-linux-gnu]
linker = "mold"
rustflags = ["-C", "link-arg=-fuse-ld=mold"]
```
