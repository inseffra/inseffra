<div align="center">

# Inseffra

**Advanced Minecraft Automation Tool**

[![Version](https://img.shields.io/badge/version-2.2.0-7B68EE.svg)](https://github.com/inseffra/inseffra-minecraft-clicker/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-0078D6.svg)](https://github.com/inseffra/inseffra-minecraft-clicker/releases)
[![Downloads](https://img.shields.io/github/downloads/inseffra/inseffra-minecraft-clicker/total?color=7B68EE)](https://github.com/inseffra/inseffra-minecraft-clicker/releases)
[![License](https://img.shields.io/badge/license-Proprietary-red.svg)](LICENSE)

<img src="assets/previeww.png" alt="Inseffra Preview" width="700"/>

[**Download**](https://github.com/inseffra/inseffra-minecraft-clicker/releases/latest) • [Features](#features) • [Security](#security-analysis) • [Documentation](#documentation)

</div>

---

## Overview

Inseffra is a high-performance desktop automation tool designed for Minecraft PvP. Built with modern C++ and optimized for minimal resource usage, it provides advanced macro capabilities while maintaining undetectability.

**Key Highlights:**
- Native C++ implementation for optimal performance
- Stream-proof rendering (invisible to screen capture software)
- Multi-language support (English, Turkish)
---

## Features

### Clicker Systems

**Left Clicker**
- Configurable CPS (1-40) with randomization
- Block-hit automation
- Mouse shake simulation
- Multiple click patterns (Basic, Butterfly, Jitter)
- Break blocks mode
- Hold mode support

**Right Clicker**
- Fast bridging optimization
- Eating mode support
- Auto slot switching
- Customizable CPS and randomization

### Movement Features

**Auto Sprint** - Automatic sprint activation when moving forward  
**Sprint Reset** - W-Tap or S-Tap for enhanced knockback  
**Strafing** - Automated A/D movement on attack

### Utility

**AutoText** - Hotkey-triggered message sending  
**Anti-AFK** - Automated movement to prevent kick  
**Click Sounds** - Realistic mouse audio (7 different mice)  
**Custom Hotkeys** - Full keybind customization  
**Analytics Dashboard** - Real-time usage statistics

### Privacy & Safety

**Stream Proof** - Invisible to Discord, OBS, Teams, Zoom, and other capture software  
**Focus Detection** - Only active when Minecraft window is focused  
**Menu Pause** - Automatic pause in inventory/chat/ESC menu  
**Minimize to Tray** - Background operation support

---

## Compatibility

**Tested Environments:**
- Craftrise, Sonoyuncu (Full compatibility)
- Hypixel (Use with caution)
- Vanilla, Lunar Client, Badlion Client (Full compatibility)

**System Requirements:**
- Windows 10/11 (64-bit)
- 10MB disk space
- No additional dependencies required

---

## Installation

1. Download `Inseffra.exe` from [Releases](https://github.com/inseffra/inseffra-minecraft-clicker/releases/latest)
2. Run the executable (no installation needed)
3. Configure settings and hotkeys

**Note:** Windows Defender may flag the application due to autoclicker behavior patterns. This is a false positive. Click "More info" → "Run anyway" or add an exclusion.

---

## Security Analysis

Inseffra uses standard Windows APIs for input simulation and is frequently flagged by heuristic antivirus engines. All detections are false positives.

### Independent Sandbox Analysis

| Platform | Result | Report |
|----------|--------|--------|
| Tria.ge | 6/10 - Likely Benign | [View Report](https://tria.ge/260102-zsgvhssmfs/behavioral1) |
| Hybrid Analysis | Full Behavioral Analysis | [View Report](https://hybrid-analysis.com/sample/3908b6950ddd8845c46c4c9c56696ce65773943819c602cd203ab209c713a471) |

### Detection Explanations

| Detection | Reason |
|-----------|--------|
| Keyboard/Mouse simulation | Uses `SendInput` and `mouse_event` Windows APIs - core autoclicker functionality |
| Hotkey detection | Uses `GetAsyncKeyState` to detect configured hotkeys - does not log keystrokes |
| Clipboard access | AutoText feature uses clipboard for faster message sending |
| Screen capture API | Stream Proof uses `SetWindowDisplayAffinity` to hide from capture software |
| Network connection | Update checker connects to `raw.githubusercontent.com` and anonymous analytics to `supabase.co` |
| Sleep calls | CPS timing requires precise delays between clicks |
| Unsigned binary | Code signing certificates cost $200-400/year - absence does not indicate malware |

### Actual Behavior

**Network:** GitHub (updates), Supabase (anonymous analytics)  
**File System:** `%LOCALAPPDATA%\Inseffra\options.json` only  
**Privacy:** No personal data collection  
**Processes:** Single-process application, no injection  
**Registry:** No modifications  
**Startup:** Does not auto-start with Windows

---

## Documentation

### Click Sounds

Available audio profiles:
- Logitech G303, G502, G Pro
- Bloody, Razer, Glorious, Zowie

### Hotkey Configuration

All features support custom keybinds including:
- Standard keys (A-Z, 0-9, F1-F12)
- Mouse buttons (Mouse4, Mouse5)
- Modifiers (Shift, Ctrl, Alt)

---

## Screenshots

<div align="center">
<img src="assets/screenshot-movement.png" width="45%" alt="Movement Features"/>
<img src="assets/screenshot-setingsss.png" width="45%" alt="Settings Interface"/>
</div>

---

## Changelog

**v2.2.0** - Current Release
- Movement Features: Auto Sprint, Sprint Reset (W-Tap/S-Tap), Strafing
- Auto Slot Switch for right-click automation

**v2.1.1**
- Tray icon hiding
- Focus detection fixes

**v2.1.0**
- AutoText messaging system
- Embedded click sounds
- Anti-tamper protection

**v2.0.0**
- Complete C++ rewrite
- Stream Proof implementation
- Modern ImGui interface
- Multi-language support

---

## License

Proprietary software. All rights reserved.  
Unauthorized distribution, modification, or reverse engineering is prohibited.

---

<div align="center">

**Made by effra**

</div>
