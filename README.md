<div align="center">

# 🎮 Inseffra

### Advanced Minecraft Macro Tool for PvP

[![Version](https://img.shields.io/badge/version-2.1.0-purple.svg)](https://github.com/inseffra/inseffra-minecraft-clicker/releases)
[![Windows](https://img.shields.io/badge/platform-Windows%2010%2F11-blue.svg)](https://github.com/inseffra/inseffra-minecraft-clicker/releases)
[![Downloads](https://img.shields.io/github/downloads/inseffra/inseffra-minecraft-clicker/total?color=purple)](https://github.com/inseffra/inseffra-minecraft-clicker/releases)
[![License](https://img.shields.io/badge/license-Proprietary-red.svg)](LICENSE)

<img src="assets/preview.png" alt="Inseffra Preview" width="650"/>

**[⬇️ Download](https://github.com/inseffra/inseffra-minecraft-clicker/releases/latest) • [📖 Features](#-features) • [🔒 Security](#-security-analysis)**


*A lightweight, undetectable macro tool designed for Minecraft PvP.*

</div>

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 🖱️ Left Clicker
- Adjustable CPS (1-40)
- Smart Randomization
- Blockhit Support
- Mouse Shake
- Multiple Click Patterns
- Break Blocks Mode

</td>
<td width="50%">

### 🖱️ Right Clicker
- Fast Bridging
- Allow Eating Mode
- Customizable CPS
- Hold Mode Support

</td>
</tr>
<tr>
<td>

### 🛡️ Safety Features
- 👻 Stream Proof
- Pause in Menu
- Only in Focus Mode

</td>
<td>

### ⚙️ Advanced
- 🔊 Click Sounds (7 mice)
- 🌍 Multi-Language (EN/TR)
- ⌨️ Custom Hotkeys
- Anti-AFK System

</td>
</tr>
</table>

---

## 👻 Stream Proof

Stay safe during screen shares! Inseffra is **completely invisible** to:

| Application | Hidden? |
|-------------|---------|
| Discord Screen Share | ✅ Yes |
| OBS Studio | ✅ Yes |
| Windows Game Bar | ✅ Yes |
| Zoom / Teams | ✅ Yes |
| AnyDesk / TeamViewer | ✅ Yes |

---

## 🎯 Tested Servers

| Server | Status |
|--------|--------|
| Craftrise | ✅ Works |
| Sonoyuncu | ✅ Works |
| Hypixel | ⚠️ Use carefully |
| Lunar Client | ✅ Works |
| Badlion Client | ✅ Works |
| Vanilla | ✅ Works |

---

## 🚀 Installation

1. Download the latest version from [**Releases**](https://github.com/inseffra/inseffra-minecraft-clicker/releases/latest)
2. Run `Inseffra.exe` (single file, no installation needed)
3. Configure and enjoy!

> ⚠️ **Windows Defender:** May show false positive. Click "More info" → "Run anyway" or add an exception.

---

## 🔒 Security Analysis

**Inseffra is 100% clean.** Some antivirus software flags autoclickers because they simulate mouse input - this is a false positive.

### Sandbox Analysis Reports

| Platform | Score | Link |
|----------|-------|------|
| Tria.ge | **3/10** (Likely Benign) | [View Report](https://tria.ge/260102-zsgvhssmfs/behavioral1) |
| Hybrid Analysis | Full behavior analysis | [View Report](https://hybrid-analysis.com/sample/3908b6950ddd8845c46c4c9c56696ce65773943819c602cd203ab209c713a471) |

### Why some AV flag this? (Detailed Explanation)

| Detection | Real Reason |
|-----------|-------------|
| "Keyboard/Mouse simulation" | **Core autoclicker feature.** Uses `SendInput` and `mouse_event` Windows APIs to simulate clicks. This is literally what an autoclicker does. |
| "Keylogger/Keyboard strokes" | **Hotkey detection.** Uses `GetAsyncKeyState` to detect when you press your configured hotkeys (e.g., Mouse4 to toggle clicker). Does NOT record or save any keystrokes. |
| "Clipboard access" | **AutoText feature.** When you press your AutoText hotkey, the program copies your message to clipboard and pastes it in-game using Ctrl+V. This is faster and more reliable than simulating individual keypresses. |
| "Screenshot API" | **Stream Proof feature.** Uses `SetWindowDisplayAffinity` to make the window invisible to screen capture. Needs to query display information to work properly. Does NOT take screenshots. |
| "Network connection" | **Update checker** connects to `raw.githubusercontent.com` to check for new versions. **Anonymous analytics** sends session count to Supabase (no personal data). |
| "Unknown user-agent" | **Custom user-agent.** Update checker uses `Inseffra Updater` as user-agent string instead of a browser name. |
| "Anti-debug/VM detection" | **Tamper protection.** Prevents analysis tools from modifying program behavior. Standard protection used by many legitimate applications. |
| "Terminate process" | **Self-destruct feature.** Allows user to quickly close the program with a hotkey. Only terminates its own process. |
| "Sleeps many times" | **CPS timing.** Program uses `Sleep()` to create delays between clicks. 15 CPS = ~66ms sleep between each click. |
| "Queries IE/cache settings" | **WinINet API side effect.** Using Windows internet APIs for update checking triggers this detection. Does NOT access your browser data. |
| "Unsigned PE" | **No code signing certificate.** Certificates cost $200-400/year. This doesn't mean the program is malicious. |

### What Inseffra actually does:

✅ **Network:** Connects only to `raw.githubusercontent.com` (updates) and `supabase.co` (anonymous session analytics)  
✅ **Files:** Writes only to `%LOCALAPPDATA%\Inseffra\` (settings file: `options.json`)  
✅ **Privacy:** No personal data collected - only anonymous session count  
✅ **Processes:** No hidden processes, no injection into other programs  
✅ **Registry:** No registry modifications  
✅ **Startup:** Does not add itself to Windows startup

---

## 📸 Screenshots

<div align="center">
<img src="assets/screenshot-clickerr.png" width="400" alt="Clicker Tab"/>
<img src="assets/screenshot-settingss.png" width="400" alt="Settings Tab"/>
</div>

---

## 🔊 Click Sounds

Realistic mouse click sounds to mask macro usage in recordings:

- Logitech G303
- Logitech G502  
- Logitech G Pro
- Bloody
- Razer
- Glorious
- Zowie

---

## ⌨️ Hotkeys

All features can be bound to custom hotkeys including:
- Keyboard keys (A-Z, F1-F12, etc.)
- Mouse buttons (Mouse4, Mouse5)
- Special keys (Shift, Ctrl, Alt)

---

## 🛡️ Safety Features

| Feature | Description |
|---------|-------------|
| Stream Proof | Hidden from screen capture software |
| Pause in Menu | Auto-pause in inventory/chat |
| Only in Focus | Only works when Minecraft is active |
| Randomization | Natural click patterns |
| Mouse Shake | Human-like cursor movement |

---

## 📝 Changelog

### v2.1.0 - Latest
- ✨ AutoText feature (send messages with hotkey)
- 🔊 Click sounds now embedded in exe
- 🛡️ Anti-tamper protection
- 🐛 Bug fixes and performance improvements

### v2.0.0 - Major Update
- 🎉 Complete C++ rewrite
- 👻 Stream Proof feature
- 🔊 Click sounds (7 mice)
- 🌍 English & Turkish
- ⚡ Better performance
- 🎨 Modern ImGui UI

---

## 💖 Support

Love Inseffra? Consider supporting development!

<a href="https://buymeacoffee.com/inseffra">
  <img src="https://img.shields.io/badge/Buy%20Me%20A%20Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black"/>
</a>

---

## 📜 License

This software is proprietary. All rights reserved.  
Unauthorized distribution, modification, or reverse engineering is prohibited.

---

<div align="center">

**Made with 💜 by effra**

[![GitHub](https://img.shields.io/badge/GitHub-inseffra-purple?style=flat&logo=github)](https://github.com/inseffra)

</div>
