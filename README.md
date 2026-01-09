# Inseffra2 - High Performance Desktop Automation Tool

## Overview
Inseffra2 is a complete C++20 port of the original Python-based Inseffra tool. It provides significant performance improvements with lower CPU usage and sub-millisecond timing precision.

## Features
- **Native C++20 Performance**: Compiled to native machine code for maximum efficiency
- **ImGui + DirectX 11 GUI**: Smooth, responsive user interface
- **Low Latency Input**: Uses Windows `SendInput` API for precise input simulation
- **JSON Configuration**: Easy-to-edit settings file
- **All Original Modules**: LeftClicker, RightClicker, SprintReset, Strafing, AntiAFK

## Building

### Prerequisites
- **CMake 3.20+**
- **Visual Studio 2019/2022** with C++ workload
- **Windows 10/11 SDK**

### Build Steps

1. **Configure the project:**
   ```powershell
   cd inseffra2
   mkdir build
   cd build
   cmake .. -G "Visual Studio 17 2022" -A x64
   ```

2. **Build the project:**
   ```powershell
   cmake --build . --config Release
   ```

3. **Run the executable:**
   ```powershell
   .\Release\Inseffra2.exe
   ```

## Project Structure

```
inseffra2/
├── CMakeLists.txt          # Build configuration
├── README.md               # This file
├── include/
│   ├── config.h            # Application constants
│   ├── clicker.h           # Clicker module header
│   ├── overlay.h           # GUI overlay header
│   ├── settings.h          # Settings manager header
│   ├── input.h             # Input handler header
│   └── stb_image.h         # Image loading (stub)
├── src/
│   ├── main.cpp            # Entry point
│   ├── clicker.cpp         # Click automation logic
│   ├── overlay.cpp         # ImGui GUI implementation
│   ├── settings.cpp        # JSON config system
│   └── input.cpp           # Window/input monitoring
└── assets/
    └── options.json        # Default configuration
```

## Modules

### LeftClicker
- CPS (Clicks Per Second): 1-40
- Randomization: 0-10
- Shake Effect: 0-10 pixels
- Blockhit Chance: 0-100%
- Click Patterns: Basic, Butterfly, Jitter
- Options: Hold Leftclick, Break Blocks

### RightClicker
- CPS: 1-40
- Randomization: 0-10
- Shake Effect: 0-10 pixels
- Options: Hold Rightclick, Allow Eating

### SprintReset
- Delay: 0.01-1.0 seconds
- Randomization: 0.00-0.20 seconds
- Hold Time: 0.00-0.50 seconds
- Modes: W-Tap, S-Tap, Crouch

### Strafing
- Delay: 0.01-1.0 seconds
- Randomization: 0.00-0.20 seconds
- Hold Time: 0.00-0.50 seconds
- Option: Random Direction

### AntiAFK
- Timer: 1-120 seconds
- Randomization: 1-20 seconds

## Technical Details

### Input Simulation
Uses the standard Windows `SendInput` API which is:
- ✅ Safe and legal
- ✅ Works with all applications
- ✅ No memory injection
- ✅ No driver installation required

### Timing Precision
Uses `std::chrono` high-resolution clock for precise timing:
- Microsecond-level accuracy
- Thread-based non-blocking design
- Minimal CPU overhead

### Window Detection
Automatically detects Minecraft and variants:
- java.exe / javaw.exe
- Lunar Client
- Badlion Client
- LabyMod
- Feather Client
- PvPLounge
- Salwyrr

## License
This software is for educational and accessibility testing purposes only.

## Credits
- Original Python version: effra
- C++ Port: Based on the original Inseffra architecture
- GUI: Dear ImGui by ocornut
- JSON: nlohmann/json library
