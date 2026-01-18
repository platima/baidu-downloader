<img align="right" src="https://visitor-badge.laobi.icu/badge?page_id=platima.baidu-downloader" height="20" />

# Chinese Cloud Storage Direct Download Helper (Unlicensed)

[![License](https://img.shields.io/badge/license-AGPLv3.0-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Mac%20%7C%20Linux-blue.svg)]()
[![Tampermonkey](https://img.shields.io/badge/TamperMonkey-v4.13+-brightgreen.svg)]()

A free and genuinely open source userscript for downloading files from Chinese cloud storage services. No licence codes, no paywalls, no nonsense.

**Supported Services:**
- ✅ Baidu Netdisk (百度网盘)
- ✅ Aliyun Drive (阿里云盘)
- ✅ Tianyi Cloud (天翼云盘)
- ✅ Xunlei Cloud (迅雷云盘)
- ✅ Quark Drive (夸克网盘)
- ✅ China Mobile Cloud (移动云盘)

## What This Is

This is an unlicensed fork of the [original baiduyun userscript](https://github.com/syhyz1990/baiduyun). The original repository claimed to be "free and open source" but required a licence code to actually use it - which defeats the entire point of being open source.

This fork:
- **Removes all licence validation** - just install and use
- **Translates everything to English** for international users
- **Updates regularly** via Tampermonkey's built-in update mechanism
- **Maintains the AGPL-3.0 licence** as required

All credit for the original code goes to [YouXiaoHou](https://github.com/syhyz1990). This fork simply removes the artificial restrictions.

## Installation

1. Install [Tampermonkey](https://www.tampermonkey.net/) (or Violentmonkey/Greasemonkey)
2. Click here to install: **[baidu-downloader.user.js](https://github.com/platima/baidu-downloader/raw/main/baidu-downloader.user.js)**
3. Navigate to any supported cloud storage site
4. Click the "Download Helper" button that appears

That's it. No licence codes, no registration, no bullshit.

## Features

- **Multiple Download Methods:**
  - Direct API download (triggers IDM if installed)
  - Aria2 RPC integration
  - cURL commands for terminal use
  - BitComet protocol links
  
- **RPC Downloader Support:**
  - Motrix
  - Aria2
  - aria2c
  - Any JSON-RPC compatible downloader

- **Platform Support:**
  - Windows (CMD, PowerShell)
  - macOS (Terminal)
  - Linux (Bash, Shell)

- **Customisation:**
  - Theme colours
  - Download paths
  - RPC configuration
  - Terminal type selection

## Download Methods Explained

### API Download
Downloads directly through your browser. Will attempt to trigger IDM if you have it installed, otherwise falls back to browser's native download.

**Best for:** Single files, quick downloads, IDM users

### Aria2 Download
Generates aria2c command-line instructions you can paste into your terminal or Aria2 GUI.

**Best for:** Power users, batch downloads, resumable downloads

### RPC Download
Sends download links directly to your configured RPC downloader (Motrix, Aria2, etc.).

**Best for:** Automated downloading, running downloaders on different machines

### cURL Download
Generates cURL commands for downloading via command line.

**Best for:** Servers, automation scripts, Linux users

### BC Download
Creates BitComet protocol links.

**Best for:** BitComet users who want magnet-link style downloading

## Configuration

Click the "Settings" menu item in the download helper dropdown to configure:

- **RPC Settings:** Host, port, path, authentication token
- **Download Path:** Where files should be saved
- **Terminal Type:** Match your operating system's terminal
- **Theme Colour:** Customise the interface appearance

## Known Limitations

- Folders cannot be downloaded directly - select files inside them
- Some cloud services have rate limits
- Large batches may need to be split into multiple downloads
- Requires you to be logged into the cloud storage service

## Troubleshooting

### "BDUSS cookie not found"
You need to log in to Baidu Netdisk first. The script reads your authentication cookie from the browser.

### "Failed to get download links"
The page may have expired. Try refreshing and selecting files again.

### "RPC send failed"
Check your RPC settings in the configuration menu. Make sure your RPC downloader (Motrix/Aria2) is running and accessible.

### IDM not triggering
Go to IDM → Options → File Types and ensure the file extension is listed. Some cloud services use non-standard extensions.

## For Developers

This is a userscript (Greasemonkey-style), not a browser extension. It runs via Tampermonkey/Violentmonkey/Greasemonkey.

**Key files:**
- `baidu-downloader.user.js` - Main userscript
- Updates pulled automatically from GitHub via Tampermonkey

**To modify:**
1. Edit `baidu-downloader.user.js`
2. Increment version number in metadata
3. Tampermonkey will auto-update for users who installed via GitHub

## Why This Fork Exists

The original project claimed to be "free and open source" under AGPL-3.0, but required users to obtain licence codes before the script would actually function. This defeats the entire purpose of open source software.

This fork honours the original AGPL-3.0 licence by:
- Keeping the code open and auditable
- Removing artificial usage restrictions
- Maintaining attribution to the original author
- Allowing anyone to use, modify, and distribute freely

If you support genuinely free and open source software, please star this repository and share it with others who might benefit.

## Licence

AGPL-3.0 - see [LICENSE](LICENSE)

Original code by YouXiaoHou. Unlicensed fork maintained by [Platima](https://github.com/platima).

## Contributing

Pull requests welcome! Please maintain the existing code style and ensure all text is in English (Australian preferred 😉).

**Particularly appreciated:**
- Bug fixes
- Support for additional cloud storage services
- UI/UX improvements
- Documentation improvements

## Disclaimer

This tool is for personal use only. Respect copyright laws and terms of service of the cloud storage providers. The maintainers of this project are not responsible for how you use it.

---

**Note:** If you want the original, licence-encumbered version, it's at [syhyz1990/baiduyun](https://github.com/syhyz1990/baiduyun). But why would you?
