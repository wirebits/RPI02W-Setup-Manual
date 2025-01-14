# Rust-Setup-RPI02W
Setup Rust in Raspberry Pi Zero 2 W

# Steps to install Rust easily on Raspberry Pi Zero 2 W
1. Type the following command :
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
2. Hit Enter
3. Type 1.
4. Hit Enter.
5. Wait for some time, it is downloaded and show that `Rust is installed now. Great!`.
6. Type the following command to save for current session :
```
source $HOME/.cargo/env
```
7. Restart the system by type the following command :
```
sudo reboot
```
8. To check Rust is properly installed on your Raspberry Pi Zero 2 W, type the following command :
```
rustc -V
```
It show : `rustc 1.84.0 (9fc6b4312 2025-01-07)`.<br>
Congratulations! Rust is successfully installed on your Raspberry Pi Zero 2 W.