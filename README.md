# Ace 6 (PLQ110) Android device tree

## Status

- [X] Display
- [X] MTP/OTG Storage
- [X] ADB/Fastbootd
- [X] Vibrator
- [X] Display Settings
- [X] Flashing 
- [X] Backup & Restore 
- [X] Factory Reset
- [X] Touch
- [X] Decryption

# Building

### Clone & sync source
```
mkdir -p ~/OrangeFox_14
cd ~/OrangeFox_14
git clone https://gitlab.com/OrangeFox/sync.git
cd sync
./orangefox_sync.sh --branch 14.1 --path ~/fox_14.1
```
### Clone device tree
```
cd ~/fox_14.1/device
mkdir -p oneplus
cd oneplus
git clone https://github.com/NullCode1337/ofox_device_oneplus_ktm ktm
```
### BUILD
```
cd ~/fox_14.1
source build/envsetup.sh
lunch twrp_ktm-ap2a-eng
mka adbd recoveryimage
```
