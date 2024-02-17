## Pre-requisites

You'll need to install:

- [Rust](https://www.rust-lang.org/tools/install)
- [Docker](https://docs.docker.com/get-docker/)

There are also some OS-specific requirements.

### Windows

```bash
cargo install -f cargo-binutils
rustup component add llvm-tools-preview
```

### Linux

```bash
# Ubuntu
sudo apt-get install lld clang
# Arch
sudo pacman -S lld clang
```

### MacOS

```bash
brew install michaeleisel/zld/zld
```

## How to build

Launch a (migrated) Postgres database via Docker:

```bash
./scripts/init_db.sh
```

Launch `cargo`:

```bash
cargo build
```

## How to test

Launch a (migrated) Postgres database via Docker:

```bash
./scripts/init_db.sh
```

Launch `cargo`:

```bash
cargo test
```