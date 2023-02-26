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
cargo install espup
```

Instalar el toolchain para Apple Silicon

https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads

```
export PATH="/Applications/ArmGNUToolchain/12.2.rel1/arm-none-eabi/bin:$PATH"
```

Crear directorio de trabajo

```
ls
cd Documents
mkdir rust-workshop
cd rust-workshop
ls
cargo generate --git https://github.com/rust-embedded/cortex-m-quickstart --name esp32  
ls
cd esp32
ls
ls src/
vim .cargo/config.toml 
```

Editar el build 

```
[build]
# Pick ONE of these default compilation targets
# target = "thumbv6m-none-eabi"        # Cortex-M0 and Cortex-M0+
# target = "thumbv7m-none-eabi"        # Cortex-M3
target = "thumbv7em-none-eabi"       # Cortex-M4 and Cortex-M7 (no FPU)
# target = "thumbv7em-none-eabihf"     # Cortex-M4F and Cortex-M7F (with FPU)
# target = "thumbv8m.base-none-eabi"   # Cortex-M23
# target = "thumbv8m.main-none-eabi"   # Cortex-M33 (no FPU)
# target = "thumbv8m.main-none-eabihf" # Cortex-M33 (with FPU)
```

```
rustup default esp
```

Para programar instalar  OpenOCD

```
brew install open-ocd
```
Si no se tiene homebrew:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
