## Registry with base images
### rust-crossbuild
[![rust-crossbuild](https://github.com/andrmr/registry/actions/workflows/rust-crossbuild.yml/badge.svg?event=push)](https://github.com/andrmr/registry/actions/workflows/rust-crossbuild.yml)  

```Dockerfile
FROM ghcr.io/andrmr/registry/rust-crossbuild:latest as crossbuild
```
Rust base for multi-arch images. Enabled targets:
- `x86_64-unknown-linux-gnu`
- `aarch64-unknown-linux-gnu`
