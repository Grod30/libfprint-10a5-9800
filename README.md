# Bash script to enable fingerprint scanner on ThinkPad E14 Gen5 and Thinkpad E16 Gen1 running Fedora
Patched libfprint for FPC fingerprint scanner with ID 10a5:9800

# Note:
Be aware that this package shouldn't be updated because won't load the patch

Rebuilt from xuwd1's AUR package: https://aur.archlinux.org/packages/libfprint-fpcmoh-git
Forked from: https://github.com/furcom/libfprint-patched

## How to install:
1. Clone repository:
```
git clone https://github.com/furcom/libfprint-patched.git
```
2. Make script executable and run it:
```
chmod +x ./install.sh && ./install.sh
```
3. Reboot system and execute following:
```
fprintd-enroll your_username
```
4. Open the dnf.conf file:
```
sudo nano /etc/dnf/dnf.conf
```
5. Add this line to the dnf.conf file to exclude libfprint package from updating:
```
exclude=libfprint
```
