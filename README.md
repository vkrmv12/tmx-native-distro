# Termux Native Desktop Installation with
# 🧑‍💻 VS Code (Code-OSS) on Termux (Native, No proot-distro)

# 🌨️ Install Termux & Termux-X11 ( if not already )
---
## Download Termux through this official link below 👇 
[Download Termux App](https://github.com/termux/termux-app/releases/download/v0.118.3/termux-app_v0.118.3+github-debug_universal.apk)
## Termux-X11 👇
[Download TERMUX-X11](https://github.com/termux/termux-x11/releases/download/nightly/app-universal-debug.apk)

## 🎥 Video Tutorial (Many cmds used was manually entered in video, So make sure you must use cmds given here. It's a example video tutorial).

#### Video link :- [Watch on Telegram](https://t.me/networkv12/178)

## ✨ Features
- Native Termux environment
- No Linux distro / proot
- Termux:X11 + XFCE desktop
- Code-OSS (Open Source VS Code)
- Clean helper scripts
- GitHub copy-enabled commands

---

## 📋 Table of Contents
- Requirements
- Warning
- Step-by-step Installation
- Install Code-OSS
- One-shot Install
- Troubleshooting

---

## ✅ Requirements
- Android device
- Termux (F-Droid / GitHub version recommended)
- Termux:X11
- Stable internet connection
- Sufficient storage

---

## ⚠️ Warning
⚠️ If you are not familiar with Termux, use step-by-step commands.
⚠️ If you have unlimited & stable internet, you may try the one-shot command.
⚠️ XFCE + Code-OSS are heavy packages.

---

## 🧩 Step-by-step Installation

### First Run (Mandatory)

```bash
termux-setup-storage
```

---

### Step -∆- 1 : Update system
```bash
pkg update && pkg upgrade
```

If update fails:
```bash
apt --fix-broken install
```

---

### Step -∆- 2 : Install repos, X11 & XFCE
```bash
apt install -y x11-repo termux-x11-nightly tur-repo proot-distro wget git pulseaudio
```

Then install desktop:
```bash
apt --fix-broken install -y && apt install -y xfce4 xfce4-goodies
```

---

### Step -∆- 3 : Install tmx launcher
```bash
cd "$HOME" && wget https://raw.githubusercontent.com/vkrmv12/tmx-native-distro/refs/heads/main/tmx
```

```bash
mv tmx $PREFIX/bin/
```

```bash
chmod +x $PREFIX/bin/tmx
```

---

### Step -∆- 4 : Start X11 session
```bash
tmx
```

Open Termux:X11
Open terminal inside X11

---

## 🧠 Install Code-OSS

### Install vscode launcher
```bash
cd "$HOME" && wget https://raw.githubusercontent.com/vkrmv12/tmx-native-distro/refs/heads/main/vscode
```

```bash
mv vscode $PREFIX/bin/
```

```bash
chmod +x $PREFIX/bin/vscode
```

---

### Install Code-OSS package
```bash
apt update && apt install -y code-oss
```

---

### Run VS Code
```bash
vscode
```

Happy Coding!

---

## 🚀 One-shot Install (Advanced)

⚠️ Use only if you understand what it does.

```bash
termux-setup-storage && \
pkg update -y && pkg upgrade -y && \
apt install -y x11-repo termux-x11-nightly tur-repo proot-distro wget git pulseaudio && \
apt --fix-broken install -y && \
apt install -y xfce4 xfce4-goodies && \
cd "$HOME" && \
wget -q https://raw.githubusercontent.com/vkrmv12/tmx-native-distro/refs/heads/main/tmx && \
wget -q https://raw.githubusercontent.com/vkrmv12/tmx-native-distro/refs/heads/main/vscode && \
mv tmx vscode $PREFIX/bin/ && \
chmod +x $PREFIX/bin/tmx $PREFIX/bin/vscode && \
echo "Installation finished. Run: tmx"
```

---

## 🛠 Troubleshooting

Fix broken packages:
```bash
apt --fix-broken install -y
dpkg --configure -a
```

Command not found:
```bash
ls -l $PREFIX/bin/tmx $PREFIX/bin/vscode
```

```bash
chmod +x $PREFIX/bin/tmx $PREFIX/bin/vscode
```

XFCE not starting / black screen:
```bash
tmx
```

Restart Termux and Termux:X11 if needed.

---

⭐ Star the repo if it helped
Maintained by vkrmv12
