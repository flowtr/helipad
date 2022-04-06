# Helipad 

[![CI](https://github.com/flowtr/helipad/actions/workflows/lint.yml/badge.svg)](https://github.com/flowtr/helipad/actions/workflows/lint.yml)

> A cross-platform, lightweight and fast CI/CD Server/Client written in Rust (WIP).

**WIP Note:** This is a very early **proof of concept** CI/CD Server/Client project yet so any ideas or contributions are welcome.

## Overview

Unlike the "well-known" variety of software of this kind. The aim of this one in particular is to provide a lean and controlled CI/CD Server/Client regarding features which leverages [Rust power and safety](https://cacm.acm.org/magazines/2021/4/251364-safe-systems-programming-in-rust/fulltext). It means a fast CI/CD Server/Client with lower resource needs and cross-platform.

The project also serves as an excuse to explore new oportunities to improve the software itself and prove Rust safety on this kind of space. Of course learning and fun do not have to be lacking.

If you are interested please don't hesitate to get involved.

## Example

To see how pipelines are executed, just nagivate to [the `devel` Github Actions workflow](https://github.com/joseluisq/helipad/actions), then pick up whatever Linux, Macos, FreeBSD or Windows job and finally expand the `Run execution tests` step.

Pipeline files can be found under [.pipelines/](./.pipelines) directory.

## TODO

**Note:** This is a non-exhaustive list of features.

- [x] Host Commands Executor (HCE) for pipelines that are executed directly on a Host machine. 
- [x] Pipelines, steps and scripts support via an individual pipeline file. E.g [`pipeline.linux.toml`](.pipelines/pipeline.linux.toml)
- [x] Pipelines, steps and scripts support via multiple pipeline files. E.g [`.pipelines/`](.pipelines/)
- [x] Environment variables support for steps
- [x] Automatic OS/Arch pipeline detection
- [ ] Encrypted secrets
- [ ] Git clone over HTTPS
- [ ] Git clone over SSH
- [ ] Cross-platform HTTP Server
- [ ] Parallel Steps
- [ ] Parallel Pipelines
- [ ] Server REST API
- [ ] Podman Commands Executor (DCE) for pipelines that are executed using Podman containers.
- [ ] Cross-platform HTTP Client Service
- [ ] ???

## Usage

```sh
# After build Helipad try
$ helipad -c ./.pipelines

# or just run it directly via Cargo
$ cargo run -- -c ./.pipelines
```

