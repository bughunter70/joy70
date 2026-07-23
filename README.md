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
nethunter
```

or

```bash
nh
```
##Kali Root Login

```bash
sudo su
```
##Password For Kali

```bash
kali
```

```bash
# 1. Purani symlink file ko remove karein
sudo rm -f /etc/resolv.conf

# 2. Apni pasand ka custom DNS add karein (Cloudflare & Google)
echo "nameserver 1.1.1.1" | sudo tee /etc/resolv.conf
echo "nameserver 8.8.8.8" | sudo tee -a /etc/resolv.conf

# 3. File ko immutable (lock) kar dein taaki apt update ya systemd ise change na kar sake
sudo chattr +i /etc/resolv.conf
```


##Kali Update And Upgrade Command

```bash
apt update && sudo apt full-upgrade -y
```
##Kali All tools Installation Command

```bash
apt install kali-linux-default -y
```
