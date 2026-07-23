# kali-linux

# Kali Linux NetHunter (Termux)

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
wget -O install-nethunter-termux https://offs.ec/2MceZWr
```

## Give Permission

```bash
chmod +x install-nethunter-termux
```

## Install Kali NetHunter

```bash
./install-nethunter-termux
```

## Start Kali

```bash
nethunter
```

or

```bash
nh
```
