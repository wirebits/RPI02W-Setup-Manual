# Go-Setup-RPI0W
Instructions to install Go on Raspberry Pi Zero W.

# Steps to install Go easily on Raspberry Pi Zero W
1. Check the CPU model name of Raspberry Pi Zero W. It is generally `ARMv6`.
2. Copy link of the Go souce file of ARMv6 (armv6l) from [here](https://go.dev/dl/).
3. Open terminal and type the following command :
```
wget https://go.dev/dl/go1.23.0.linux-armv6l.tar.gz
```
4. Hit Enter
After some times it downloaded.
5. Type the following command to extract the tz file to the path :
```
sudo tar -C /usr/local -xzf go1.23.0.linux-armv6l.tar.gz
```
6. Hit Enter
After some times it extacted to the path.
7. Type the following command to opwn .profile in sudo :
```
sudo nano ~/.profile
```
8. Add the following line at the end of the file :
```
export PATH=$PATH:/usr/local/go/bin
```
9. Save the file and exit.
Type the following command to save for current session :
```
source ~/.profile
```
10. Delete the go1.23.0.linux-armv6l.tar.gz file.
11. Restart the system by type the following command :
```
sudo reboot
```
12. To check Go is properly installed on your Raspberry Pi Zero W, type the following command :
```
go version
```
It show : `go version go1.22.4 linux/arm`.<br>
Congratulations! Go is successfully installed on your Raspberry Pi Zero W.
