# Build procedure
## Windows
```cmd

```

## Linux
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
. "$HOME/.cargo/env"
apt install --update -y protobuf-compiler gcc pkg-config libssl-dev
git clone --branch No_libcrux https://github.com/JamesParrott/openmls
cd openmls/
cargo build -p openmls
cargo build --workspace --exclude openmls-fuzz
```