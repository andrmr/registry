## Registry with base images
### Rust dev
[![rust-dev](https://github.com/andrmr/registry/actions/workflows/rust-dev.yml/badge.svg?event=push)](https://github.com/andrmr/registry/actions/workflows/rust-dev.yml)  

```Dockerfile
FROM ghcr.io/andrmr/registry/rust-dev:latest as rust-dev
```
Rust base image for blazingly fast dev compilation. Based on slim-bookworm.  
[➡️See more](./rust/README.md)
