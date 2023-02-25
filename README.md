# rust-esp
Katas de Embedded Rust 

1 - 25/2/2023 https://aindustriosa.org/Kata-de-Embedded_Rust-por-Eloy-Coto/

**Instalar Rust**

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
Setup:
```
rustup update
rustup component add llvm-tools-preview
rustup target add thumbv7em-none-eabihf
cargo install cargo-binutils cargo-embed cargo-flash cargo-expand
cargo install cargo-generate
```

**Instalar para STM**


arm-toolchain
```
wget https://armkeil.blob.core.windows.net/developer/Files/downloads/gnu-rm/10.3-2021.10/gcc-arm-none-eabi-10.3-2021.10-x86_64-linux.tar.bz2
```
Initialize:
```
https://docs.rust-embedded.org/book/start/qemu.html
```
```
cargo generate --git https://github.com/rust-embedded/cortex-m-quickstart --name stm
```


**Instalar Rust ESP 32**

https://kerkour.com/rust-on-esp32

Instalar herramientas para ESP32

```
cargo install -f ldproxy espflash espmonitor
```

Y luego ejecutar

```
rustup default esp
```
