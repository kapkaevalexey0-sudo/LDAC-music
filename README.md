#High Quality Music Driver (HQMD)
Professional audio driver installer for high-resolution music playback over Bluetooth using LDAC technology.

#📋 Overview
HQMD is a Windows application that installs and manages the LDAC audio driver, enabling high-quality wireless audio transmission (up to 990 kbps / 96 kHz / 24-bit) on compatible Bluetooth devices.

#✨ Features
One-click driver installation via PnPUtil

Automatic driver file copying to Windows DriverStore

Administrator privilege detection with auto-restart option

Real-time installation log with status updates

Driver verification after installation

Modern dark-themed interface with progress tracking

Multilingual support (Russian/English)

Uninstall support - removes driver cleanly

#🎵 Technical Specifications
Parameter	Value
Sample Rate	96 kHz
Bitrate	990 kbps
Bit Depth	24-bit
Codec	LDAC (Sony)
Quality	Hi-Res Audio
Available Modes
🚀 990 kbps — 96 kHz / 24-bit (Hi-Res mode)

⚡ 660 kbps — 96 kHz / 24-bit (Balanced mode)

📱 330 kbps — 48 kHz / 16-bit (Stable connection mode)

#🚀 Installation
Prerequisites
Windows 10/11 (64-bit)

Bluetooth adapter with LDAC support

Administrator rights

Python 3.7+ (for development)

Quick Start
Download the latest installer from releases page

Run HQMD_Setup_7.0.2.1.exe as administrator

Follow the installation wizard

Launch HQMD and click "Install Driver"

#🔧 Building from Source
1. Clone repository
git clone https://github.com/yourusername/hqmd.git
cd hqmd
2. Install dependencies
pip install -r requirements.txt
3. Build executable
python build.py
Or use the provided batch files:

bash'''
build_exe.bat     # Builds only the EXE
build_full.bat    # Builds EXE + Installer
Requirements.txt
PyQt6>=6.4.0
pyinstaller>=5.13.0
#📦 Installation Package Structure
HQMD Setup/
├── HQMD_Installer.exe          # Main application
├── Driver/
│   └── ldac/
│       ├── AltA2DP.inf         # LDAC driver
│       └── ... (other driver files)
└── version.txt                  # Version information
#🎮 Usage
Launch HQMD (as administrator)

Select INF file (default: Driver/ldac/AltA2DP.inf)

Click "Install Driver"

Monitor progress in the log window

Restart computer when prompted

Command-line options
HQMD_Installer.exe              # Normal mode
HQMD_Installer.exe --silent      # Silent installation
HQMD_Installer.exe --uninstall   # Remove driver
📊 Application Interface
┌─────────────────────────────────────┐
│  🎧 High Quality Music Driver       │
├─────────────────────────────────────┤
│  ┌─────────────┬─────────────┐     │
│  │ 96 kHz      │ 990 kbps    │     │
│  │ Frequency   │ Bitrate     │     │
│  ├─────────────┼─────────────┤     │
│  │ 24-bit      │ Hi-Res      │     │
│  │ Depth       │ Quality     │     │
│  └─────────────┴─────────────┘     │
│                                     │
│  📁 Driver file:                    │
│  [Driver/ldac/AltA2DP.inf] [Browse] │
│                                     │
│  [🚀 INSTALL DRIVER]                 │
│                                     │
│  [════════════] 75%                  │
│                                     │
│  📋 Installation Log                 │
│  ✓ Driver found                      │
│  ✓ Files copied                      │
│  ✓ Installation complete             │
│                                     │
│  [Clear] [About] [Exit]             │
└─────────────────────────────────────┘
#🔄 Driver Installation Process
Privilege check - Ensures administrator rights

File verification - Validates INF file existence

DriverStore copy - Copies files to Windows DriverStore

PnPUtil execution - Installs driver via pnputil /add-driver

Verification - Confirms driver presence in system

Fallback methods - DevCon or rundll32 if needed

#🧹 Uninstallation
#Via Windows
Open Settings → Apps → Installed apps

Find "High Quality Music Driver"

Click Uninstall

#Via Command Line
bash
pnputil /delete-driver "C:\Program Files\High Quality Music Driver\Driver\ldac\AltA2DP.inf"
#❗ Troubleshooting
Issue	Solution
"Access denied"	Run as administrator
"INF not found"	Check file path or use Browse button
"Installation failed"	Disable antivirus temporarily
"Device not working"	Restart computer after installation
"No LDAC option"	Verify Bluetooth adapter supports LDAC
📝 Version History
Version 7.0.2.1 (Latest)
Added modern dark theme interface

Improved driver verification

Added multiple installation methods

Enhanced error handling

Version 7.0.1.0
Initial release

Basic PnPUtil installation

Simple GUI interface

#🤝 Contributing
Fork the repository

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit changes (git commit -m 'Add AmazingFeature')

Push to branch (git push origin feature/AmazingFeature)

Open a Pull Request

#📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

#👥 Authors
Aviatrec Digital Company - Initial work

#🙏 Acknowledgments
Sony for LDAC technology

Qt for PyQt framework

Inno Setup for installer creation

Open source community

Note: LDAC is a registered trademark of Sony Corporation. This software is not affiliated with or endorsed by Sony.
