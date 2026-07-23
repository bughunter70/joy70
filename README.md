# Kali Linux Latest Version 2026.7 (Termux)

## Requirements
- Android 8+
- Termux (Latest)
- Minimum 8 GB Free Storage
- Stable Internet Connection

## Update Termux

```bash
pkg update && pkg upgrade -y
```

## Install Required Packages

```bash
pkg install wget proot tar -y
```

(Optional)

```bash
pkg install git curl nano -y
```

## Download Installer

```bash
wget https://raw.githubusercontent.com/bughunter70/joy70/main/kali.sh
```

## Give Permission

```bash
chmod +x kali.sh
```

## Install Kali

```bash
./kali.sh
```

## Start Kali

```bash
nh
```
## Kali Root Login

```bash
sudo su
```
## Password For Kali

```bash
kali
```

## Mandatory Step
```bash
## ⚠️ Mandatory Step: Fix DNS (Required for Update/Upgrade)

In the Kali PRoot environment, **fixing the DNS configuration is compulsory** for `apt update` and `apt upgrade` to function properly. Without this step, package updates will fail.

Run the following commands inside your Kali Linux terminal:

```bash
# Remove old resolv.conf symlink
sudo rm -f /etc/resolv.conf

# Add custom DNS resolvers (Cloudflare & Google)
echo "nameserver 1.1.1.1" | sudo tee /etc/resolv.conf
echo "nameserver 8.8.8.8" | sudo tee -a /etc/resolv.conf

# Lock file to prevent overwriting during updates
sudo chattr +i /etc/resolv.conf
```

## Kali Update And Upgrade Command

```bash
apt update && sudo apt full-upgrade -y
```

# Finish setting up any unconfigured packages
sudo dpkg --configure -a

# Attempt another fix-broken install in case anything was missed
sudo apt --fix-broken install

# Clean up those unused dependencies APT mentioned in your output
sudo apt autoremove



## Kali All tools Installation Command

```bash
apt install kali-linux-default -y
```
