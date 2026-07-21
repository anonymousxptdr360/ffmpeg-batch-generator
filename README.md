# ⚡ FFmpeg Batch Command Generator

A simple, zero-dependency HTML utility that generates custom, single-line FFmpeg commands to batch compress and convert video folders across Windows, macOS, and Linux.

---

## 📖 About

**Born from a quick fix.** I built this lightweight tool to stop manually editing terminal scripts for batch video compression. Open it in your browser, tweak your FFmpeg settings (paths, codecs, CRF, presets), and copy a ready-to-run command. No installation, no extra software.

---

## ✨ Features

- 💻 **Cross-Platform:** Supports Windows (CMD & PowerShell) and macOS/Linux (Bash/Zsh).
- ⚙️ **Fully Customizable:** Choose video codec (H.264 / H.265), CRF value, preset, audio codec, bitrate, output folder, and more.
- 📋 **One-Click Copy:** Instantly copy the generated command to your clipboard.
- 🔒 **100% Local & Private:** Everything runs directly in your browser. No files, paths, or data are uploaded.
- 🚀 **Zero Dependencies:** A single HTML file with no installation, frameworks, or build tools required.

---

## ⚙️ Prerequisites

The generated commands require **FFmpeg** to be installed and accessible from your terminal.

### Windows

Open **Command Prompt** or **PowerShell** and install FFmpeg using Winget:

```cmd
winget install Gyan.FFmpeg
```

If FFmpeg is already installed, update it with:

```cmd
winget upgrade Gyan.FFmpeg
```

> **Note:** If `winget` is not recognized, install **App Installer** from the Microsoft Store:
>
> https://apps.microsoft.com/detail/9nblggh4nns1?hl=fr-FR&gl=FR

### macOS

Using Homebrew:

```bash
brew install ffmpeg
```

### Linux

Ubuntu / Debian:

```bash
sudo apt update
sudo apt install ffmpeg
```

Fedora:

```bash
sudo dnf install ffmpeg
```

Arch Linux:

```bash
sudo pacman -S ffmpeg
```

---

## 🚀 How to Use

1. Clone or download this repository.

```bash
git clone https://github.com/anonymousxptdr360/ffmpeg-batch-generator.git
```

Or download it as a ZIP from GitHub.

2. Open `index.html` in your favorite web browser.

3. Enter the path to your video folder.

Example:

**Windows**

```text
C:\Users\YourName\Desktop\Videos
```

**macOS / Linux**

```text
/home/username/Videos
```

4. Select your preferred encoding settings.

5. Click **Copy Command**.

6. Paste the generated command into your terminal and run it.

---

## 📂 Generated Commands

The tool generates optimized batch commands that can:

- Compress entire folders
- Convert video codecs
- Preserve or re-encode audio
- Keep the original folder untouched
- Create converted files in a new output directory

No scripting knowledge required.

---

## 🔒 Privacy

This tool works entirely offline.

- No analytics
- No tracking
- No network requests
- No server
- No data collection

Everything happens locally in your browser.

---

## 📄 License

This project is licensed under the **MIT License**.

See the LICENSE file for details.

---

## ⭐ Repository

GitHub:

https://github.com/anonymousxptdr360/ffmpeg-batch-generator
