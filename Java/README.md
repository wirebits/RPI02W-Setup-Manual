# Java-Setup-RPI02W
Setup Java in Raspberry Pi Zero 2 W

# Steps to install Java easily on Raspberry Pi Zero 2 W
1. Run the following command to get all supported JDK on Raspberry Pi Zero 2 W:<br>
```
apt search openjdk
```
2. Select openjdk version of your choice.
3. Run the following command to download selected openjdk:<br>
```
sudo apt install openjdk-17-jdk -y
```
4. Hit Enter.
After some times it downloaded.
5. Run the following command to show the jre path :
```
cd /usr/lib/jvm/java-17-openjdk-armhf/bin
```
6. Hit Enter
7. Run the following command to get full path of jre :
```
pwd
```
7. Copy the path.
8. Run the following command to set the path of jre and apply :
```
sudo echo 'export PATH=$PATH:/usr/lib/jvm/java-17-openjdk-armhf/bin' >> ~/.bashrc && source ~/.bashrc
```
9. Hit Enter.
10. Run the following command to restart the system :
```
sudo reboot
```
11. Run the following command to check java jdk is properly installed or not on the system :
```
java -version
```
It show : <br>
`openjdk version "17.0.13" 2024-10-15
OpenJDK Runtime Environment (build 17.0.13+11-Raspbian-1deb11u1rpt1)
OpenJDK Client VM (build 17.0.13+11-Raspbian-1deb11u1rpt1, mixed mode, emulated-client)`.<br>
12. Run the following command to check java jre is properly installed or not on the system :
```
javac -version
```
It show : `javac 17.0.13`.<br>
Congratulations! Java is successfully installed on your Raspberry Pi Zero 2 W.

# Note
- `armhf` → 32-bit OS
- `arm64` → 64-bit OS
