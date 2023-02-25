# rust-esp
Katas de Embedded Rust 

1 - 25/2/2023 https://aindustriosa.org/Kata-de-Embedded_Rust-por-Eloy-Coto/

* Instalar Rust

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
Setup:
```
rustup update
rustup component add llvm-tools-preview
rustup target add thumbv7em-none-eabihf
cargo install cargo-binutils cargo-embed cargo-flash cargo-expand
cargo install cargo-generate

* Instalar Rust ESP 32

https://kerkour.com/rust-on-esp32
