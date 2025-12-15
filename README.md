iOS Disable Call Recording (Unified Tool)

![alt text](https://img.shields.io/badge/iOS-18.0--26.1-blue)


![alt text](https://img.shields.io/badge/Status-Stable-brightgreen)


![alt text](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS-lightgrey)


![alt text](https://img.shields.io/badge/Auto--Install-Yes-success)


![alt text](https://img.shields.io/badge/Author-YangJiii-orange)

A unified, automated tool to replace or disable the call‑recording notification sound (Start/Stop Disclosure) on iOS without Jailbreak, using the Books app file‑overwrite exploit.

Now with Auto-Dependency Installation & Enhanced UI!

Author: YangJiii — @duongduong0908
Original Concept: Huy Nguyen — @Little_34306

⚠️ DISCLAIMER & LEGAL NOTICE

Before using this tool, you MUST read and agree to all of the following terms:

1. Device & Data Risk

This tool modifies internal iOS files (/var/mobile/Library/CallServices/...) using a system vulnerability.

There is always a risk of device issues (boot loop, soft brick, data loss).

The author (YangJiii) takes NO responsibility for any hardware damage, software corruption, or data loss.

You use this tool entirely at your own risk.

2. Legal Notice About Call Recording

The "StartDisclosure" sound exists to comply with privacy laws in many countries.

Removing or silencing this sound may violate privacy or eavesdropping laws depending on your region.

This tool is for educational research only.

The author is not responsible for any misuse.

📂 Required Folder Structure

This tool is now a single-file solution. Ensure your folder looks like this:

code
Text
download
content_copy
expand_less
Your_Tool_Folder/
│
├── main.py                    <-- The main script (runs on both Windows & Mac)
├── uuid.txt                   <-- (Created automatically, do not delete)
│
└── Sounds/                    <-- Required Folder
    ├── StartDisclosureWithTone.m4a
    └── StopDisclosure.caf
💻 PRE-REQUISITES
1. Install Python 3

Download from: python.org

Important: Check the box "Add Python to PATH" during installation.

2. Install iTunes (Windows Only)

Required for device drivers. Download from Apple's website (avoid the Microsoft Store version if possible).

3. Connect Device

Connect your iPhone via USB.

Tap Trust on the iPhone screen if prompted.

🚀 HOW TO RUN (Windows & macOS)

You DO NOT need to manually install libraries (pymobiledevice3, colorama, etc.). The script will detect missing libraries and install them automatically.

➤ Windows

Open the folder containing the files.

Type cmd in the address bar and press Enter (or open Terminal).

Run the following command:

code
Bash
download
content_copy
expand_less
python main.py

(Note: For best results, run Command Prompt as Administrator)

➤ macOS / Linux

Open Terminal.

Navigate to the folder: cd path/to/folder

Run the command:

code
Bash
download
content_copy
expand_less
python3 main.py

(Note: If prompted for a password, enter your Mac login password to allow Tunnel creation)

🛠️ HOW IT WORKS

Auto-Install: The tool checks if pymobiledevice3 and colorama are installed. If not, it installs them and restarts itself.

Device Detection: Automatically finds your connected iPhone/iPad via USB.

UUID Extraction: Scans the Books app logs to find the hidden system UUID required for the exploit.

Tunnel Creation: For iOS 17+, it creates a secure tunnel to communicate with the device.

File Replacement: It pushes the silent audio files from the Sounds folder to the device using the backup/restore exploit logic.

❓ COMMON ISSUES & FIXES
1. "No device found"

Check your USB cable.

Ensure iTunes (Windows) or Finder (Mac) can see the device.

Tap Trust on the iPhone.

2. Script stuck at "Searching for UUID..."

Unlock your iPhone.

Open the Books (Sách) app.

Open a book inside the app. If you don't have one, download a free sample from the Book Store.

3. "Tunnel creation failed"

Unplug the cable and plug it back in.

On macOS, ensure you entered the correct sudo password if prompted.

Reboot the iPhone if the issue persists.

4. Installation Error (Windows)

If the auto-install fails with "Microsoft Visual C++" errors, please install Visual C++ Build Tools.

☕ Support

If this project helped you, consider supporting via Ko-fi ❤️
👉 https://ko-fi.com/yangjiii/goal?g=1