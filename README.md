# RPI02W-Setup-Manual
A simple manual for setup of Raspberry Pi Zero 2 W and languages.

# Micro SD Card
- Use atleast 16 GB and it is FAT32 formatted.

# Setup Raspberry Pi Zero 2 W without Monitor
1. Download `Raspberry Pi Imager Tool` according to Operating System from [here](https://www.raspberrypi.com/software/).
2. Simply install it.
3. Open the Raspberry Pi Imager Tool.
4. Select the `Raspberry Pi Zero 2 W` in `Choose Device`.
5. Select the `Raspberry Pi OS (Legacy, 64-Bit) Lite - Debian Bullseye` from `Raspberry Pi OS (other)` in `Choose OS`.
6. Plug the Micro SD Card in the computer.
7. Select that Micro SD Card in `Choose Storage`.
8. Click on `Next`.
9. Click on `Edit Settings`.
10. Set `Hostname`, `Username`, `Password`, `Wifi SSID and Password`, `Wifi Country`, `Local Settings` under `General` Tab.
11. Enable `SSH` with `Use Password Authentication` option under `Services` Tab.
12. Click on `Save` button.
13. Click on `Yes` button.
14. Again, click on `Yes` button.
- Wait for some time, it writes and verify the OS on the Micro SD Card.
15. Unplug the Micro SD Card and then plug again.
16. Open the Micro SD Card.
17. Open the `cmdline.txt` file and put the following just befor the `rootwait` word :
```
modules-load=dwc2,g_ether
```
18. Save it and close the file.
19. Open the `config.txt` file and put the following at the end of the file :
```
dtoverlay=dwc2
```
20. Save it and close the file.
21. Download `ssh` file and put in the SD Card.
22. It want to add more networks so that your Raspberry Pi Zero 2 W can connect to many networks as in the range then, add `wpa_supplicant.conf` after editing in the SD Card.
23. Eject the Micro SD Card from the computer.
24. Put the Micro SD Card in Raspberry Pi Zero 2 W.
25. Power it by connecting to the `PWR IN` pin.
26. Wait for sometime, it connect to that wifi which is set during writing of OS.
27. Download PuTTY from [here](https://www.putty.org/).
28. Simply install it.
29. Put the IP address and open it.
30. Click on `Accept`.
31. Enter Username and hit enter.
32. Enter Password and hit enter.
- After that, it opens the terminal in this format : `Username`@`Hostname`.

# Setup Networks on Raspberry Pi Zero 2 W without Monitor
- There is a file named `wpa_supplicant.conf`.
- You can many networks as you can.
- Edit the following before put the file in SD Card :
  1. Country Code
  2. YOUR_SSID
  3. YOUR_PASSWORD
- You can set priority of the networks.

# Setup Languages on Raspberry Pi Zero 2 W
1. Go - [here](https://github.com/wirebits/RPI02W-Setup-Manual/tree/main/Go).
2. Java - [here](https://github.com/wirebits/RPI02W-Setup-Manual/tree/main/Java).
3. Rust - [here](https://github.com/wirebits/RPI02W-Setup-Manual/tree/main/Rust).
