FROM rust:slim-bookworm

RUN apt-get update && apt-get install -y \
    mold clang-15 g++-x86-64-linux-gnu \
    && rm -rf /var/lib/apt/lists/*

RUN rustup toolchain install nightly && rustup update
RUN rustup component add rustc-codegen-cranelift-preview --toolchain nightly

LABEL org.opencontainers.image.description="Rust base image for blazingly fast dev compilation. Based on slim-bookworm."
LABEL org.opencontainers.image.source=https://github.com/andrmr/registry
