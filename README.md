# tmx-native-distro

# 🧑‍💻 VS Code (Code-OSS) on Termux — Native (No proot-distro)

[![Platform](https://img.shields.io/badge/Platform-Termux-2ea44f)](#)
[![UI](https://img.shields.io/badge/UI-termux--x11--nightly-blue)](#)
[![Desktop](https://img.shields.io/badge/Desktop-XFCE-orange)](#)
[![Editor](https://img.shields.io/badge/Editor-Code--OSS-purple)](#)

Run **Code-OSS (VS Code OSS build)** on **Termux natively** using **Termux:X11 + XFCE**, **without** `proot-distro`.

---

## ✨ What you get
- ✅ Native Termux setup (no Linux distro in proot)
- ✅ Termux:X11 UI + XFCE Desktop
- ✅ Install and run `code-oss`
- ✅ Simple launcher scripts (`tmx`, `vscode`)

---

## 📌 Table of Contents
- [Requirements](#-requirements)
- [⚠️ Warning](#️-warning)
- [Step-by-step Install](#-step-by-step-install)
- [Install Code-OSS inside X11](#-install-code-oss-inside-x11)
- [🚀 One-shot Install Command](#-one-shot-install-command)
- [Troubleshooting](#-troubleshooting)
- [Uninstall](#-uninstall)
- [Credits](#-credits)

---

## ✅ Requirements
- Android device with **Termux** installed  
- **Termux:X11** (recommended)
- Stable internet connection
- Enough storage (XFCE + Code-OSS can be big)

> Tip: Keep Termux updated from a trusted source (F-Droid / GitHub releases).

---

## ⚠️ Warning
This setup installs X11 + XFCE + packages that may be heavy and may fail on slow or unstable networks.

✅ If you’re not familiar with Termux setups, **use the step-by-step commands**.

🚀 If you have **unlimited / stable internet**, you can try the **one-shot command** at the end.

---

## 📋 Step-by-step Install

> 🔥 **First time only:** grant storage permission  
> Tap to copy:

```bash
termux-setup-storage
