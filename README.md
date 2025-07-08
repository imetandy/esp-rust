# Testing ESP dev in Rust for tiny IoT sensors. 

## Setup
I assume this is going to be annoying, so lets record all settings: 
```
## Tooling
Rustup toolchain version: rustup 1.28.2 (e4f3ad6f8 2025-04-28)
Rust version: rustc 1.87.0-nightly (1dc879ca2 2025-05-27) (1.87.0.0)


## Rust crates
espflash
esp-generate
esp-println

esp-generate --chip=esp32s3 esp-test

## Brew
brew tap probe-rs/probe-rs
brew install probe-rs
brew install xz

Everytime I open new terminal run: 
. $HOME/export-esp.sh 

## Install espup
curl -L https://github.com/esp-rs/espup/releases/latest/download/espup-aarch64-apple-darwin -o espup
chmod a+x espup

./espup install
```


To flash device: 
`cargo run --release -- --port /dev/cu.usbmodem21201`

To monitor device: 
`espflash monitor --port /dev/tty.usbmodem21201`