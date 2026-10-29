# zsh設定ファイルの履歴監視と復元

`shellconfiglock` is a macOS-first security CLI. This repository is one of 31 small tools in the [security-tools workspace](https://github.com/HiroyukiGPU/security-tools).

## Install

```sh
cargo install --git https://github.com/HiroyukiGPU/shellconfig-lock.git
```

## Commands

```sh
shellconfiglock --help
shellconfiglock scan . --json
shellconfiglock init .
shellconfiglock verify
shellconfiglock watch .
shellconfiglock quarantine suspicious-file --dry-run
```

The shared engine supports scanning, polling watch, SHA-256 baselines, verification, reversible quarantine, restore, trusted values and JSON output. Detection is static and heuristic. This tool does not claim kernel-level isolation, complete network filtering, or prevention of every execution path. Review findings before taking action. State is stored under the OS local data directory in `HiroyukiGPU/shellconfig-lock`.

## Build

```sh
cargo build --release
cargo test
```
