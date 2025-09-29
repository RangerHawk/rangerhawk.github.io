# 🧙‍♂️ Gimpinator EX Plugin for GIMP 3.x

Stable Horde Integration • Local Model Ready • RH Legacy Verified  
Confirmed working on Windows 11 – September 2025

## 🛡️ RH Legacy Crest – Symbolic Activation

This plugin scroll was authored by RangerHawk Studios.  
Every glyph tested. Every sidetrack archived.  
Symbolic crest placeholder:  
[Insert crest image or ASCII glyph]

## 🌱 What Is Gimpinator EX?

Gimpinator EX is a plugin that lets you generate AI images directly inside GIMP using text prompts.  
It supports Stable Horde (free distributed backend) and optional local model scaffolding.

## 📦 Installation Guide (Beginner-Friendly)

### 1. Download the Plugin

Go to: https://github.com/PCOW/Gimpinator  
Click the green box that says “Code” and select “Download ZIP”

### 2. Unzip and Move

Extract the ZIP to:  
C:\Users\<UserName>\AppData\Roaming\GIMP\3.0\plug-ins

**Note:**  
Inside this download you will find a file named `gimpinator_ex.py`. You will need to edit this file.  
(Suggested editing with Notepad++ https://notepad-plus-plus.org/downloads/, but Windows Notepad will work fine.)

The USERNAME in this file is incorrect. Near the top of the file you will find a line:  
`sys.path.append(r"C:\Users\OlafW\AppData\Local\Programs\Python\Python313\Lib\site-packages")`  
Replace `OlafW` or `USERNAME` with your actual Windows username.

To find your Windows username:  
Open Command Prompt → type: `echo %USERNAME%` → press Enter  
Use the name it displays to replace `USERNAME` in the plugin file.

Rename the extracted folder to: `Gimpinator_ex`

Inside that folder, confirm you have:  
• gimpinator_ex.py  
• gimpinator_config.json (optional)

This optional config file stores your Stable Horde API key. It does not connect to GitHub.  
If it’s missing, you can create one manually using the instructions below.

### 3. Check File Permissions

Right-click each file → Properties  
• Uncheck “Read-only”  
• Click “Unblock” if present  
Apply and repeat for all plugin files (.py)

### 4. Create Config File (Optional for Stable Horde)

To use Stable Horde, you’ll need a free API key.

How to get one:  
- Go to https://stablehorde.net  
- Click "Login" in the top right  
- Sign in using Discord, GitHub, or another method  
- Click your username → go to "Account"  
- Scroll down to find your API key and copy it

### 5. Create the Config File

- Open Notepad or Notepad++  
- Paste this into the file (replace `your-key-here` with your actual API key):  
`{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }`  
- Click File → Save As  
- Name the file: `gimpinator_config.json`  
- Set "Save as type" to "All Files"  
- Save it inside the `Gimpinator_ex` folder

### 6. Install Python

Go to: https://www.python.org/downloads/  
Install Python 3.10 or higher  
Check “Add Python to PATH” during setup

### 7. Verify Python Installation

Open Command Prompt → type: `where python`  
This will show you where Python is installed.

If it doesn’t appear:  
• You may need to reinstall Python  
• Double-check folder path and file names  
• Ensure Python is installed and added to PATH  
• Restart your computer

## 🧠 Advanced Activation Guide (Fully Restored)

### 📁 Folder Structure

Plugin folder:  
C:\Users\<YourName>\AppData\Roaming\GIMP\3.0\plug-ins\Gimpinator_ex

Contents:  
• gimpinator_ex.py  
• gimpinator_config.json (optional)

### 🐍 Python Environment

Python 3.10 or higher is required.

Install dependencies:  
`pip install requests pillow PyGObject`

Optional for local model scaffolding:  
`pip install diffusers transformers torch accelerate`

### ⚙️ Plugin Script Requirements

Start of file:  
`#!/usr/bin/env python3`

Required imports:  
`import gi`  
`gi.require_version("Gimp", "3.0")`  
`from gi.repository import Gimp, GimpUi, GObject, GLib, Gio, Gtk`  
`import sys`  
`import os`  
`import json`

Plugin class:  
`class Gimpinator(Gimp.PlugIn):`  
`    def do_query_procedures(self):`  
`        return ["plug-in-gimpinator-ex"]`

Main invocation:  
`Gimp.main(Gimpinator.__gtype__, sys.argv)`

### 🧭 Menu Path

Appears under:  
Filters → Gimpinator → Gimpinator EX

Optional grouping:  
`proc.add_menu_path("<Image>/Filters/AI")`

### 🔐 Optional Config File

Contents of `gimpinator_config.json`:  
`{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }`

## 🧾 Notes

Tested on GIMP 3.0 with Python 3.13  
Confirmed working on Windows 11  
Plugin appears under Filters → Gimpinator → Gimpinator EX  
Consider adding this guide to your README or onboarding scroll

## 🧙 Contributor

Joe Molnar  
Founder of RangerHawk Studios  
Creative systems architect and mythic plugin ritualist

## 🪶 RH Legacy Footer

This scroll was forged in the legacy archive of RangerHawk Studios.  
Every plugin tested. Every sidetrack preserved.  
May it guide future creators toward prompt invocation and plugin sovereignty.

This scroll was co-forged using AI assistance, but the structure, sequence, and symbolic intent are authored by Joe Molnar of RangerHawk Studios.  
Every step reflects a larger vision of mythic onboarding and creative sovereignty.
