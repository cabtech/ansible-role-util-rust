# ansible-role-util-rust
Installs Rust using RustUp

## Default variables
| Name | Type | Value | Comment |
| ---- | ---- | ----- | ------- |
| rust_flag | UnixPath | `.cargo/env` | relative to homedir |
| rust_installer | UnixPath | `/usr/local/bin/install-rustup.sh` |
| rust_other_pkgs | list(string) | [] | extra pkgs to install; e.g. if using KDB |
| rust_users | list(UnixUser) | [] ||

## Notes
Rather than pull the RustUp script all the time and the risk that entails, we download and review it and add it to the role for reuse.
```
https://www.rust-lang.org/tools/install

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs > files/install-rustup.sh
```
