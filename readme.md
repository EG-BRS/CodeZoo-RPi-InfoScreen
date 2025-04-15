# CodeZoo Info Screen

> Clone this project for quick setup of an infoscreen based on Raspberry Pi

## Requirements
1. Raspberry Pi OS (w. Desktop environment)
2. Username is codezoo (ID: 1000) - if not `files/codezoo-chromium-autostart.service` needs to be updated accordingly
3. Available internet

## Steps

First change you directory to the root of this project!

### 1. Update and install Chromium
```bash
sudo apt update
```
```bash
sudo apt install chromium-browser
```

### 2. Add the start script

#### 2.1 Edit the `files/start-chromium.sh`
Replace the **https://example.com** with the URL that you want.

#### 2.2 Copy the file
```bash
cp ./files/start-chromium.sh ~/start-chromium.sh
```

### 3. Add the service
```bash
sudo cp ./files/codezoo-chromium-autostart.service /etc/systemd/system/codezoo-chromium-autostart.service
```
```bash
sudo systemctl enable codezoo-chromium-autostart.service
```

### 4. Good to go!
```bash
sudo reboot
```
