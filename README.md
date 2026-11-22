# Rackside

<img src="docs/img/icon.svg" width="72" alt="">

_Formerly Console Connect. Version 5.0 renamed the app; existing installs update automatically and keep their settings._

Serial, USB-C, SSH, Telnet and SFTP console for network gear, with config backups, a TFTP and syslog server, and network tools. For Windows 10/11, macOS 12 or later, and Linux (64-bit).

## Download

| Your computer | Download |
| --- | --- |
| **Windows** 10 or 11 | [Rackside-Setup-Windows.exe](https://github.com/braydendolph/console-connect-releases/releases/latest/download/Rackside-Setup-Windows.exe) |
| **Mac with Apple silicon** (M1, M2, M3, M4…) | [Rackside-Mac-AppleSilicon.zip](https://github.com/braydendolph/console-connect-releases/releases/latest/download/Rackside-Mac-AppleSilicon.zip) |
| **Mac with an Intel processor** | [Rackside-Mac-Intel.zip](https://github.com/braydendolph/console-connect-releases/releases/latest/download/Rackside-Mac-Intel.zip) |
| **Linux**: Ubuntu, Debian, Mint | [Rackside-Linux-amd64.deb](https://github.com/braydendolph/console-connect-releases/releases/latest/download/Rackside-Linux-amd64.deb) |
| **Linux**: other distributions | [Rackside-Linux-x86_64.AppImage](https://github.com/braydendolph/console-connect-releases/releases/latest/download/Rackside-Linux-x86_64.AppImage) |

These links always give you the newest version. Not sure which Mac you have? Open the Apple menu › **About This Mac**: "Chip: Apple M…" means Apple silicon, "Processor: Intel" means Intel.

You only install once. After that, Rackside updates itself automatically.

## Install on Windows

1. Run **Rackside-Setup-Windows.exe**.
2. If Windows shows **"Windows protected your PC"**, click **More info**, then **Run anyway**. Windows asks once because the app isn't from the Microsoft Store.
3. Click **Install**, then **Finish**. No administrator rights are needed.

## Install on Mac

1. Open the downloaded zip (Safari usually opens it for you) and drag **Rackside** into your **Applications** folder.
2. Double-click it. macOS says it **can't check it for malicious software**. Click **OK**. This is expected the first time.
3. Open the Apple menu › **System Settings** › **Privacy & Security**, scroll to the bottom, and click **Open Anyway** next to "Rackside" was blocked. Enter your Mac password and click **Open Anyway** again.

That's it: it opens normally from then on, and updates don't ask again.

On macOS 14 or earlier you can instead Control-click the app in Applications, choose **Open**, then **Open**.

<details>
<summary>No "Open Anyway" button?</summary>

The button only shows for about an hour after step 2, so double-click the app again first. If it still isn't there, open **Terminal** (Command + Space, type Terminal), paste this line and press Return, then open the app normally:

```
xattr -dr com.apple.quarantine "/Applications/Rackside.app"
```
</details>

## Install on Linux

1. **Ubuntu, Debian, Mint:** run `sudo apt install ./Rackside-Linux-amd64.deb` (or open the file in your software installer).
   **Other distributions:** run `chmod +x Rackside-Linux-x86_64.AppImage`, then open it.
2. To use USB console cables, add yourself to the serial group once: `sudo usermod -aG dialout $USER`, then sign out and back in.

## What's new

See the [latest release](https://github.com/braydendolph/console-connect-releases/releases/latest) for what changed in each version.

## Checking a download

Each release lists a SHA-256 fingerprint next to every file. To compare, run `certutil -hashfile Rackside-Setup-Windows.exe SHA256` on Windows or `shasum -a 256 Rackside-Mac-AppleSilicon.zip` on a Mac.
