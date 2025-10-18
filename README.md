# FIXING

<div align="center">

```
███████╗██╗██╗  ██╗██╗███╗   ██╗ ██████╗ 
██╔════╝██║╚██╗██╔╝██║████╗  ██║██╔════╝ 
█████╗  ██║ ╚███╔╝ ██║██╔██╗ ██║██║  ███╗
██╔══╝  ██║ ██╔██╗ ██║██║╚██╗██║██║   ██║
██║     ██║██╔╝ ██╗██║██║ ╚████║╚██████╔╝
╚═╝     ╚═╝╚═╝  ╚═╝╚═╝╚═╝  ╚═══╝ ╚═════╝ 
```

**Advanced System Diagnostic & Repair Tool for Linux**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Bash](https://img.shields.io/badge/Bash-5.0+-green.svg)](https://www.gnu.org/software/bash/)
[![Platform](https://img.shields.io/badge/Platform-Linux-orange.svg)](https://www.linux.org/)

Ultra-powerful system scanner that detects and repairs corrupted files, broken symlinks, and permission issues with a professional terminal interface.

[Installation](#installation) • [Usage](#usage) • [Features](#features) • [Examples](#examples)

</div>

---

## 🚀 Features

- **🔍 Ultra-Deep Scanning** - Scans entire home directory with maximum depth, no limitations
- **🔗 Broken Symlink Detection** - Finds all symbolic links pointing to non-existent targets
- **📄 Zero-Byte File Detection** - Identifies empty configuration files (.json, .conf, .xml, .yml, .ini)
- **🔐 Permission Issue Detection** - Locates files and folders with access problems
- **⚡ Auto-Repair System** - Automatically fixes detected issues with one command
- **🎨 Professional UI** - Beautiful color-coded terminal interface
- **💪 Bulletproof Validation** - Strict command validation for security

---

## 📦 Installation

### Quick Install (Recommended)

```bash
curl -O https://raw.githubusercontent.com/Mariwan001/fixing/main/fixing
sudo mv fixing /usr/local/bin/
sudo chmod +x /usr/local/bin/fixing
```

### Manual Install

1. Download the `fixing` script
2. Make it executable: `chmod +x fixing`
3. Move to system path: `sudo mv fixing /usr/local/bin/`
4. Run: `fixing`

---

## 🎯 Usage

### Run Diagnostic Scan

```bash
fixing
```

This will scan your entire home directory and display all detected issues with:
- **Blue bold** - Corrupted files
- **Red bold** - Corrupted folders
- **Yellow bold** - Reason for corruption
- **Green bold** - Suggested solution

### Auto-Repair Issues

```bash
fixing fix [filename] path=[full/path/to/file]
```

**Example:**
```bash
fixing fix broken-link path=/home/user/Desktop/broken-link
```

---

## 📊 What It Detects

| Issue Type | Detection Method | Auto-Fix |
|------------|------------------|----------|
| **Broken Symlinks** | Multiple validation methods | ✅ Removes broken link |
| **Zero-byte Configs** | File size + extension check | ✅ Regenerates with template |
| **Permission Errors** | Read/execute access tests | ✅ Applies correct permissions |
| **Inaccessible Directories** | Directory execution checks | ✅ Fixes directory permissions |

---

## 💡 Examples

### Example 1: Scan System
```bash
$ fixing

███████╗██╗██╗  ██╗██╗███╗   ██╗ ██████╗ 
██╔════╝██║╚██╗██╔╝██║████╗  ██║██╔════╝ 
█████╗  ██║ ╚███╔╝ ██║██╔██╗ ██║██║  ███╗
██╔══╝  ██║ ██╔██╗ ██║██║╚██╗██║██║   ██║
██║     ██║██╔╝ ██╗██║██║ ╚████║╚██████╔╝
╚═╝     ╚═╝╚═╝  ╚═╝╚═╝╚═╝  ╚═══╝ ╚═════╝ 

Initializing ULTRA-DEEP diagnostic scan...
Target: /home/user
Mode: MAXIMUM DEPTH - NO LIMITS

[✓] Scan complete!

╔══════════════════════════════════════════════════════════════════════════╗
║                         DIAGNOSTIC RESULTS                               ║
╚══════════════════════════════════════════════════════════════════════════╝

→ Found 3 issue(s)

Corrupted Files:
──────────────────────────────────────────────────────────────────────────

FILE: broken-link
└─ Path: /home/user/Desktop/broken-link
   ⚠ Reason: Broken symbolic link - target does not exist
   ✓ Solution: Remove: rm '/home/user/Desktop/broken-link'
```

### Example 2: Fix Corrupted File
```bash
$ fixing fix broken-link path=/home/user/Desktop/broken-link

╔══════════════════════════════════════════════════════════════════════════╗
║                         REPAIR PROCESS                                   ║
╚══════════════════════════════════════════════════════════════════════════╝

Target: broken-link
Path: /home/user/Desktop/broken-link

▶ Removing broken symlink... ✓

✓ REPAIR COMPLETED SUCCESSFULLY
```

### Example 3: Invalid Command Protection
```bash
$ fixing help

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  ✗ ERROR: Invalid command 'help'
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Valid Commands:
  → fixing                              (Run diagnostic scan)
  → fixing fix [name] path=[path]       (Auto-repair item)

Examples:
  $ fixing
  $ fixing fix broken-link path=/home/user/Desktop/broken-link
```

---

## 🛠️ Technical Details

- **Language:** Bash 5.0+
- **Platform:** Linux (Ubuntu, Debian, Fedora, Arch, etc.)
- **Dependencies:** None (uses only built-in Unix utilities)
- **Scan Scope:** User home directory (`$HOME`)
- **Scan Method:** Deep recursive search with multiple validation techniques
- **Output:** Color-coded ANSI terminal output

---

## 🎨 UI Color Scheme

- **🔵 Blue Bold** - Corrupted files
- **🔴 Red Bold** - Corrupted folders
- **🟡 Yellow Bold** - Corruption reasons
- **🟢 Green Bold** - Solutions
- **🔷 Cyan** - Headers and accents
- **🟣 Purple** - Subtitles and tips
- **⚪ Gray** - Secondary information

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

---

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👨‍💻 Creator

**Mariwan Iraj**

- GitHub: [@Mariwan001](https://github.com/Mariwan001)

---

## ⭐ Support

If you find this tool useful, please consider giving it a star ⭐

---

<div align="center">

**Made with ❤️ for the Linux community**

</div>
