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
It supports Stable Horde (a free, online distributed backend) and optional local model scaffolding via separate tools.  
Note: Stable Horde is an online service. Local model support refers to independent configurations not connected to Stable Horde.

---

## 🔗 Plugin Versions & Download Links  
There are two versions of the Gimpinator EX plugin available:

- Original Plugin by PCOW  
  https://github.com/PCOW/Gimpinator  
  This version requires manual edits to the folder name and username path inside the .py file. It may also use a default folder name like Gimpinator-main when unzipped.

- Beginner Version (Recommended)  
  https://rangerhawk.github.io/plugins/gimpinator_ex/Gimpinator-EX.zip  
  This version has been pre-edited for symbolic clarity and onboarding ease.  
  ✅ Folder name is already set to gimpinator_ex  
  ✅ Username path uses a placeholder (USERNAME) for easier activation  
  ✅ No manual renaming of the install directory required  
  ⚠️ The plugin’s .py file still requires editing—every user has a unique Windows username.

Use the original version only if you prefer to customize the plugin manually or compare upstream changes.  
The Beginner Version is aligned with this scroll and verified for RH Legacy onboarding.

---

## 📦 Installation Guide

---

### 🧙‍♂️ Extraction Ritual: Preserve Folder Geometry

To maintain the sacred structure of this plugin archive, **do not use WinRAR** for extraction. WinRAR may flatten nested folders or misplace symbolic overlays, disrupting onboarding clarity and breaking legacy alignment.

✅ Recommended Extraction Methods  
Use one of the following tools to preserve the intended folder hierarchy:

• 🪄 **Windows Default Unzip Utility**  
  Right-click the ZIP file and choose **“Extract All…”**  
  This method typically preserves folder structure and is safe for onboarding.

• 🛡️ **7-Zip (Preferred for Legacy Scrolls)**  
  Download from the official site: https://www.7-zip.org  
  After installation:  
  1. Right-click the ZIP file.  
  2. Select **“7-Zip → Extract to ‘Gimpinator_EX\’”**  
     This ensures all assets remain bundled within the correct folder.

⚠️ Do *not* use “Extract Here” unless you are certain the archive contains a single folder.  
Misaligned glyphs and scattered assets may result in onboarding confusion.

🚫 **Avoid WinRAR**  
WinRAR may extract files without preserving folder geometry, leading to broken overlays, misplaced assets, and onboarding failure. This tool is not compatible with legacy-grade packaging rituals.

---

<details>
<summary>🧰 Beginner Version</summary>

### 1. Download the Plugin  
Visit: https://rangerhawk.github.io/plugins/gimpinator_ex/Gimpinator-EX.zip  
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
Apply and repeat for all .py files.

### 4. Create Config File (Optional for Stable Horde)  
To use Stable Horde, get a free API key:  
- Go to https://stablehorde.net  
- Log in via Discord, GitHub, etc.  
- Click your username → Account → Copy your API key

Create a file named gimpinator_config.json with this content:  
{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }  
Save it inside the gimpinator_ex folder using “Save as type: All Files”.

### 5. Install Python  
Go to https://www.python.org/downloads/  
Install Python 3.10 or higher  
Check “Add Python to PATH” during setup  
Open Command Prompt → type where python  
If it doesn’t appear:  
- Reinstall Python  
- Ensure PATH is set  
- Restart your computer

</details>

<details>
<summary>🧪 Advanced Setup – Manual Configuration</summary>

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

### 🛠️ Edit the Plugin File  
Open gimpinator_ex.py in a text editor.  
Find the line:  
sys.path.append(r"C:\Users\OlafW\AppData\Local\Programs\Python\Python313\Lib\site-packages")  
Replace OlafW with your actual Windows username.  
To find it:  
Open Command Prompt → type echo %USERNAME% → press Enter

### 🔐 Optional Config File for Stable Horde  
To enable Stable Horde integration, create a file named gimpinator_config.json with the following content:  
{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }  
Save it inside the gimpinator_ex folder using “Save as type: All Files”.  
You can obtain a free API key by logging into https://stablehorde.net and visiting your account page.

### 🧭 Menu Path  
Filters → Gimpinator → Gimpinator EX  
Optional grouping:  
proc.add_menu_path("<Image>/Filters/AI")

</details>

---

## 🧾 Notes  
- Tested on GIMP 3.0 with Python 3.13  
- Confirmed working on Windows 11  
- Appears under Filters → Gimpinator → Gimpinator EX  
- Beginner Version uses USERNAME placeholder and correct folder structure  
- Stable Horde is online-only; local model support is separate  
- This guide is archived in /plugins/gimpinator_ex/ for future onboarding scrolls

---

## 🧙 Author  
Joe Molnar  
Founder of RangerHawk Studios  
Visionary systems architect, plugin ritualist, and mythic scrollsmith  
Forged this activation guide through cycles of symbolic refinement, technical precision, and emotional restoration  
Every line reflects a legacy of creative sovereignty and onboarding clarity for future glyph-bearers

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
