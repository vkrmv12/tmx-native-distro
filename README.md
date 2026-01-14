# tmx-native-distro

# 🧑‍💻 VS Code (Code-OSS) on Termux — Native (No proot-distro)

Run **Code-OSS (VS Code OSS build)** on **Termux natively** using **Termux:X11 + XFCE**,  
**without proot-distro** 🚀

---

## ✨ Features
- ✅ Native Termux (no Linux distro)
- ✅ Termux:X11 + XFCE Desktop
- ✅ Code-OSS (VS Code Open Source build)
- ✅ Lightweight helper scripts (`tmx`, `vscode`)
- ✅ Fully copy-friendly commands 📋

---

## 📋 Table of Contents
- [Requirements](#-requirements)
- [⚠️ Warning](#️-warning)
- [Step-by-step Installation](#-step-by-step-installation)
- [Install Code-OSS](#-install-code-oss)
- [🚀 One-shot Install](#-one-shot-install)
- [Troubleshooting](#-troubleshooting)

---

## ✅ Requirements
- Android device
- Termux (F-Droid / GitHub version recommended)
- Termux:X11
- Stable internet connection

---

## ⚠️ Warning
If you are **not familiar with Termux**, use **step-by-step commands**.

If you have **unlimited / stable internet**, you may try the **one-shot command** at the end.

---

## 🧩 Step-by-step Installation

### 🔹 First Run (Mandatory)
```bash
termux-setup-storage
🔹 Step -∆- 1 : Update packages
Copy code
Bash
pkg update && pkg upgrade
If it fails:
Copy code
Bash
apt --fix-broken install
🔹 Step -∆- 2 : Install X11, repos & XFCE
Copy code
Bash
apt install -y x11-repo termux-x11-nightly tur-repo proot-distro wget git pulseaudio
Then:
Copy code
Bash
apt --fix-broken install -y && apt install -y xfce4 xfce4-goodies
🔹 Step -∆- 3 : Install tmx helper
Copy code
Bash
cd "$HOME" && wget https://raw.githubusercontent.com/vkrmv12/tmx-native-distro/refs/heads/main/tmx
Copy code
Bash
mv tmx $PREFIX/bin/
Copy code
Bash
chmod +x $PREFIX/bin/tmx
🔹 Step -∆- 4 : Start X11 session
Copy code
Bash
tmx
➡️ Now open Termux:X11 app
➡️ Open terminal inside X11
🧠 Install Code-OSS
🔹 Install vscode helper
Copy code
Bash
cd "$HOME" && wget https://raw.githubusercontent.com/vkrmv12/tmx-native-distro/refs/heads/main/vscode
Copy code
Bash
mv vscode $PREFIX/bin/
Copy code
Bash
chmod +x $PREFIX/bin/vscode
🔹 Install Code-OSS package
Copy code
Bash
apt update && apt install -y code-oss
🔹 Run VS Code
Copy code
Bash
vscode
🎉 Happy Coding!
🚀 One-shot Install (Advanced Users)
⚠️ Use only if you know what you're doing
Copy code
Bash
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
echo "✅ Done! Run: tmx → then install code-oss → run vscode"
🛠 Troubleshooting
Fix broken packages
Copy code
Bash
apt --fix-broken install -y
dpkg --configure -a
tmx or vscode not found
Copy code
Bash
ls -l $PREFIX/bin/tmx $PREFIX/bin/vscode
Copy code
Bash
chmod +x $PREFIX/bin/tmx $PREFIX/bin/vscode
Black screen / XFCE not starting
Copy code
Bash
tmx
Restart Termux & Termux:X11 if needed.
⭐ If this helped you, star the repo
🛠 Maintained by vkrmv12
Copy code

---

### ✅ What I fixed for copy-option
- ✔️ Every command is in a **pure fenced code block**
- ✔️ No emojis inside command blocks
- ✔️ GitHub will auto-show **📋 Copy button**
- ✔️ One-shot command also copyable

If you want next:
- 🔥 **Badges + screenshots section**
- 🔥 **Auto installer script**
- 🔥 **README with animations (GIFs)**

Just say the word 😎
