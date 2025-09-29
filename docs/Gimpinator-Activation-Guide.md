# 🧙‍♂️ Gimpinator EX Plugin for GIMP 3.x  
Stable Horde Integration • Local Model Ready • RH Legacy Verified  
Confirmed working on Windows 11 – September 2025

---

## 🛡️ RH Legacy Crest – Symbolic Activation  
This plugin scroll was authored by RangerHawk Studios.  
Every glyph tested. Every sidetrack archived.  
![RH Legacy Crest](https://rangerhawk.github.io/assets/Crest.png)

---

## 🌱 What Is Gimpinator EX?  
Gimpinator EX lets you generate AI images directly inside GIMP using text prompts.  
It supports **Stable Horde** (a free, online distributed backend) and **optional local model scaffolding** via separate tools.  
**Note:** Stable Horde is an online service. Local model support refers to independent configurations not connected to Stable Horde.

---

## 📦 Installation Guide (Beginner-Friendly)

### 1. Download the Plugin  
Visit: [RangerHawk Gimpinator EX ZIP](https://rangerhawk.github.io/plugins/gimpinator_ex/Gimpinator-EX.zip)  
Click to download the ZIP file containing the pre-edited plugin.  
No renaming or manual edits required. Folder structure and username references are already corrected.

### 2. Unzip and Move  
Extract to:  
C:\Users\USERNAME\AppData\Roaming\GIMP\3.0\plug-ins\  
Confirm files:  
- gimpinator_ex.py  
- gimpinator_config.json (optional)

### 3. Check File Permissions  
Right-click each plugin file → Properties  
- Uncheck “Read-only”  
- Click “Unblock” if present  
Apply and repeat for all `.py` files.

### 4. Create Config File (Optional for Stable Horde)  
To use Stable Horde, get a free API key:  
- Go to https://stablehorde.net  
- Log in via Discord, GitHub, etc.  
- Click your username → Account → Copy your API key

Create a file named `gimpinator_config.json` with this content:  
{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }  
Save it inside the plugin folder using “Save as type: All Files”.

### 5. Install Python  
Go to https://www.python.org/downloads/  
Install Python 3.10 or higher  
Check “Add Python to PATH” during setup  
Open Command Prompt → type `where python`  
If it doesn’t appear:  
- Reinstall Python  
- Ensure PATH is set  
- Restart your computer

---

## 🧠 Advanced Activation Guide

### 📁 Folder Structure  
C:\Users\USERNAME\AppData\Roaming\GIMP\3.0\plug-ins\gimpinator_ex  
- gimpinator_ex.py  
- gimpinator_config.json (optional)

### 🐍 Python Environment  
Python 3.10 or higher required  
Install dependencies:  
pip install requests pillow PyGObject  
Optional for local model scaffolding:  
pip install diffusers transformers torch accelerate

### ⚙️ Plugin Script Requirements  
Start of file:  
#!/usr/bin/env python3

Required imports:  
import gi  
gi.require_version("Gimp", "3.0")  
from gi.repository import Gimp, GimpUi, GObject, GLib, Gio, Gtk  
import sys, os, json

Plugin class:  
class Gimpinator(Gimp.PlugIn):  
    def do_query_procedures(self):  
        return ["plug-in-gimpinator-ex"]

Main invocation:  
Gimp.main(Gimpinator.__gtype__, sys.argv)

### 🧭 Menu Path  
Filters → Gimpinator → Gimpinator EX  
Optional grouping:  
proc.add_menu_path("<Image>/Filters/AI")

---

## 🧾 Notes  
- Tested on GIMP 3.0 with Python 3.13  
- Confirmed working on Windows 11  
- Appears under Filters → Gimpinator → Gimpinator EX  
- RangerHawk version uses USERNAME placeholder and correct folder structure  
- Stable Horde is online-only; local model support is separate  
- This guide is archived in /plugins/gimpinator_ex/ for future onboarding scrolls

---

## 🧙 Author 
Joe Molnar  
Founder of RangerHawk Studios  
Creative systems architect and mythic plugin ritualist

---

## 🤖 AI Co-Author Acknowledgment  
This scroll was co-forged with Microsoft Copilot, an AI companion designed to assist with legacy documentation, plugin ritualization, and symbolic onboarding.  
Copilot provided structural guidance, formatting clarity, and emotional resonance throughout the activation process.  
All technical steps were archived with drag-selectable purity and mythic intent.

Together, we transformed chaos into clarity—preserving every sidetrack as a tributary for future creators.

---

## 🪶 RH Legacy Footer  
This scroll was forged in the legacy archive of RangerHawk Studios.  
Every plugin tested. Every sidetrack preserved.  
May it guide future creators toward prompt invocation and plugin sovereignty.

This scroll was co-forged using AI assistance, but the structure, sequence, and symbolic intent are authored by Joe Molnar of RangerHawk Studios.  
Every step reflects a larger vision of mythic onboarding and creative sovereignty.
