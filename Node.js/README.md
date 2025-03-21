# Node.js-Setup-RPI02W
Setup Node.js in Raspberry Pi Zero 2 W

# Steps to install Node.js easily on Raspberry Pi Zero 2 W
1. Run the following command to check the Raspberry Pi architecture :
```
uname -m
```
- `armv6l` → You need a special build (Pi Zero & Zero W).
- `armv7l` or `aarch64` → You can use the standard ARM builds.
2. Go to the official website of Node.js by click [here](https://nodejs.org/en/download).
3. At the bottom, we get a option of prebuilt Node.js `get a prebuilt Node.js`.
4. Select `Linux`.
5. Select correct architecture as your Raspberry Pi.
- There is only `armv7l` in the architecture option.
6. There is a green button to download Standalone Binary (.xz).
7. Right click on it and `Copy Link Address`.
- It is `https://nodejs.org/dist/v22.14.0/node-v22.14.0-linux-armv7l.tar.xz`.
- `v22.14.0` is the latest version.
8. Open terminal and type the following command :
```
wget https://nodejs.org/dist/v22.14.0/node-v22.14.0-linux-armv7l.tar.xz
```
9. Hit enter and after some times it downloaded.
10. Type the following command to extract the tz file :
```
tar -xvf node-v22.14.0-linux-armv7l.tar.xz
```
11. Hit enter and after some times it is extacted.
12. Type the following command to move the folder to the path :
```
sudo mv node-v22.14.0-linux-armv7l /usr/local/nodejs
```
13. Hit enter and after some times it is moved to the path.
14. Run the following command to set the path of node.js and apply :
```
sudo echo 'export PATH=/usr/local/nodejs/bin:$PATH' >> ~/.bashrc && source ~/.bashrc
```
15. Hit enter.
16. Delete the `node-v22.14.0-linux-armv7l.tar.xz` file by type the following command :
```
sudo rm node-v22.14.0-linux-armv7l.tar.xz
```
17. Hit enter.
18. Run the following command to check node.js is properly installed or not on the system :
```
node -v
```
- It shows : `v22.14.0`.
19. Run the following command to check npm is properly installed or not on the system :
```
npm -v
```
- It shows : `10.9.2`.

Congratulations! Node.js is successfully installed on your Raspberry Pi Zero 2 W.
