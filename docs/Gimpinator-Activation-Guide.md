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
Visit: https://github.com/PCOW/Gimpinator  
Click the green “Code” button → “Download ZIP”  

If you downloaded the **RangerHawk Studios version**, the folder structure and username references are already corrected.  
No renaming or manual edits are required unless you’re using the original ZIP from PCOW.

---

### 2. Unzip and Move  
Extract the ZIP to:  
C:\Users\USERNAME\AppData\Roaming\GIMP\3.0\plug-ins\  

If using the original PCOW ZIP, it may create a folder named `Gimpinator-main`.  
Rename it to `gimpinator_ex` if needed.  

Inside that folder, confirm you have:  
- gimpinator_ex.py  
- gimpinator_config.json (optional)

---

### 3. Edit the Plugin File (PCOW Version Only)  
Open `gimpinator_ex.py` in Notepad++ or any text editor.  
Find the line near the top:  
sys.path.append(r"C:\Users\OlafW\AppData\Local\Programs\Python\Python313\Lib\site-packages")  

Replace `OlafW` with your actual Windows username.  
To find it:  
Open Command Prompt → type `echo %USERNAME%` → press Enter  

If you downloaded the RangerHawk version, this line already uses `USERNAME` as a placeholder.

---

### 4. Check File Permissions  
Right-click each plugin file → Properties  
- Uncheck “Read-only”  
- Click “Unblock” if present  
Apply and repeat for all `.py` files.

---

### 5. Create Config File (Optional for Stable Horde)  
To use Stable Horde, get a free API key:  
- Go to https://stablehorde.net  
- Log in via Discord, GitHub, etc.  
- Click your username → Account → Copy your API key  

Create a file named `gimpinator_config.json` with this content:  
{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }  

Save it inside the `gimpinator_ex` folder using “Save as type: All Files”.

---

### 6. Install Python  
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

---

### 🐍 Python Environment  
Python 3.10 or higher required  
Install dependencies:  
pip install requests pillow PyGObject  

Optional for local model scaffolding:  
pip install diffusers transformers torch accelerate

---

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

---

### 🧭 Menu Path  
Filters → Gimpinator → Gimpinator EX  

Optional grouping:  
proc.add_menu_path("<Image>/Filters/AI")

---

### 🔐 Optional Config File  
{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }

---

## 🧾 Notes  
- Tested on GIMP 3.0 with Python 3.13  
- Confirmed working on Windows 11  
- Appears under Filters → Gimpinator → Gimpinator EX  
- RangerHawk version uses `USERNAME` placeholder and correct folder structure  
- Stable Horde is online-only; local model support is separate  
- Consider adding this guide to your README or onboarding scroll

---

## 🧙 Contributor  
Joe Molnar  
Founder of RangerHawk Studios  
Creative systems architect and mythic plugin ritualist

---

## 🪶 RH Legacy Footer  
This scroll was forged in the legacy archive of RangerHawk Studios.  
Every plugin tested. Every sidetrack preserved.  
May it guide future creators toward prompt invocation and plugin sovereignty.  

This scroll was co-forged using AI assistance, but the structure, sequence, and symbolic intent are authored by Joe Molnar of RangerHawk Studios.  
Every step reflects a larger vision of mythic onboarding and creative sovereignty.
