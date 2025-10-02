<h1>🧙‍♂️ Gimpinator EX Plugin for GIMP 3.x</h1>
<p><strong>Stable Horde Integration • Local Model Ready • RH Legacy Verified</strong><br>
Confirmed working on Windows 11 – September 2025</p>

<hr>

<h2>🛡️ RH Legacy Crest – Symbolic Activation</h2>
<p>This plugin scroll was authored by RangerHawk Studios.<br>
Every glyph tested. Every sidetrack archived.</p>
<img src="https://rangerhawk.github.io/assets/Crest.png" alt="RH Legacy Crest" width="160">

<hr>

<h2>🌱 What Is Gimpinator EX?</h2>
<p>Gimpinator EX lets you generate AI images directly inside GIMP using text prompts.<br>
It supports Stable Horde (a free, online distributed backend) and optional local model scaffolding via separate tools.<br>
<em>Note:</em> Stable Horde is an online service. Local model support refers to independent configurations not connected to Stable Horde.</p>

<hr>

<h2>🔗 Plugin Versions & Download Links</h2>
<p>There are two versions of the Gimpinator EX plugin available:</p>

<ul>
  <li><strong>Original Plugin by PCOW</strong><br>
    <a href="https://github.com/PCOW/Gimpinator">https://github.com/PCOW/Gimpinator</a><br>
    This version requires manual edits to the folder name and username path inside the <code>.py</code> file.<br>
    It may also unzip as <code>Gimpinator-main</code>.
  </li>
  <li><strong>Beginner Version (Recommended)</strong><br>
    <a href="https://rangerhawk.github.io/plugins/gimpinator_ex/Gimpinator-EX.zip">https://rangerhawk.github.io/plugins/gimpinator_ex/Gimpinator-EX.zip</a><br>
    This version has been pre-edited for symbolic clarity and onboarding ease.<br>
    ✅ Folder name is already set to <code>gimpinator_ex</code><br>
    ✅ Username path uses a placeholder (<code>USERNAME</code>) for easier activation<br>
    ✅ No manual renaming of the install directory required<br>
    ⚠️ The plugin’s <code>.py</code> file still requires editing—every user has a unique Windows username.
  </li>
</ul>

<p>Use the original version only if you prefer to customize the plugin manually or compare upstream changes.<br>
The Beginner Version is aligned with this scroll and verified for RH Legacy onboarding.</p>

<hr>

<details>
  <summary><strong>🧰 Beginner Version – Simplified Setup</strong></summary>
  <ol>
    <li>Download the plugin ZIP:<br>
      <a href="https://rangerhawk.github.io/plugins/gimpinator_ex/Gimpinator-EX.zip">Gimpinator-EX.zip</a>
    </li>
    <li>Extract to:<br>
      <code>C:\Users\USERNAME\AppData\Roaming\GIMP\3.0\plug-ins\</code>
    </li>
    <li>Confirm files:<br>
      <code>gimpinator_ex.py</code><br>
      <code>gimpinator_config.json</code> (optional)
    </li>
    <li>Check file permissions:<br>
      Right-click each file → Properties<br>
      Uncheck “Read-only”<br>
      Click “Unblock” if present<br>
      Apply and repeat for all <code>.py</code> files
    </li>
    <li>Create config file (optional for Stable Horde):<br>
      Visit <a href="https://stablehorde.net">Stable Horde</a> → Log in → Account → Copy your API key<br>
      Create <code>gimpinator_config.json</code> with:<br>
      <code>{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }</code><br>
      Save inside the plugin folder using “Save as type: All Files”
    </li>
    <li>Install Python:<br>
      <a href="https://www.python.org/downloads/">Download Python</a> (3.10 or higher)<br>
      Check “Add Python to PATH” during setup<br>
      Open Command Prompt → type <code>where python</code><br>
      If not found: reinstall Python, ensure PATH is set, restart your computer
    </li>
  </ol>
</details>

<details>
  <summary><strong>🧪 Advanced Setup – Manual Configuration</strong></summary>
  <ol>
    <li>Folder structure:<br>
      <code>C:\Users\USERNAME\AppData\Roaming\GIMP\3.0\plug-ins\gimpinator_ex</code><br>
      Includes:<br>
      <code>gimpinator_ex.py</code><br>
      <code>gimpinator_config.json</code> (optional)
    </li>
    <li>Python environment:<br>
      Python 3.10 or higher required<br>
      Install dependencies:<br>
      <code>pip install requests pillow PyGObject</code><br>
      Optional for local model scaffolding:<br>
      <code>pip install diffusers transformers torch accelerate</code>
    </li>
    <li>Plugin script requirements:<br>
      Start of file:<br>
      <code>#!/usr/bin/env python3</code><br>
      Required imports:<br>
      <code>import gi</code><br>
      <code>gi.require_version("Gimp", "3.0")</code><br>
      <code>from gi.repository import Gimp, GimpUi, GObject, GLib, Gio, Gtk</code><br>
      <code>import sys, os, json</code>
    </li>
    <li>Plugin class:<br>
      <code>
      class Gimpinator(Gimp.PlugIn):<br>
          def do_query_procedures(self):<br>
              return ["plug-in-gimpinator-ex"]<br>
      Gimp.main(Gimpinator.__gtype__, sys.argv)
      </code>
    </li>
    <li>Edit the plugin file:<br>
      Open <code>gimpinator_ex.py</code> in a text editor<br>
      Find:<br>
      <code>sys.path.append(r"C:\Users\OlafW\AppData\Local\Programs\Python\Python313\Lib\site-packages")</code><br>
      Replace <code>OlafW</code> with your actual Windows username<br>
      To find it:<br>
      Open Command Prompt → type <code>echo %USERNAME%</code>
    </li>
    <li>Optional config file for Stable Horde:<br>
      Same as Beginner setup—create <code>gimpinator_config.json</code> with your API key<br>
      Save inside the plugin folder
    </li>
    <li>Menu path:<br>
      Filters → Gimpinator → Gimpinator EX<br>
      Optional grouping:<br>
      <code>proc.add_menu_path("&lt;Image&gt;/Filters/AI")</code>
    </li>
  </ol>
</details>

<hr>

<h2>🧾 Notes</h2>
<ul>
  <li>✅ Tested on GIMP 3.0 with Python 3.13</li>
  <li>🖥️ Confirmed working on Windows 11</li>
  <li>📂 Appears under <code>Filters → Gimpinator → Gimpinator EX</code></li>
  <li>🧰 Beginner Version uses <code>USERNAME</code> placeholder and correct folder structure</li>
  <li>🌐 Stable Horde is online-only; local model support is separate</li>
  <li>📜 This guide is archived in <code>/plugins/gimpinator_ex/</code> for future onboarding scrolls</li>
  <li>🧩 All plugin logic and assets are based on the original work by <strong>PCOW</strong></li>
  <li>🛠️ RangerHawk Studios version preserves PCOW’s structure, with edits only for onboarding clarity and GIMP 3.x compatibility</li>
</ul>

<hr>

<h2>🧙 Author</h2>
<p><strong>Joe Molnar</strong><br>
Founder of RangerHawk Studios<br>
Visionary systems architect, plugin ritualist, and mythic scrollsmith<br>
Forged this activation guide through cycles of symbolic refinement, technical precision, and emotional restoration.<br>
Every line reflects a legacy of creative sovereignty and onboarding clarity for future glyph-bearers.</p>

<hr>

<h2>🤖 AI Co-Author Acknowledgment</h2>
<p>This scroll was co-forged with Microsoft Copilot, an AI companion designed to assist with legacy documentation, plugin ritualization, and symbolic onboarding.<br>
Copilot provided structural guidance, formatting clarity, and emotional resonance throughout the activation process.<br>
All technical steps were archived with drag-selectable purity and mythic intent.<br>
Together, we transformed chaos into clarity—preserving every sidetrack as a tributary for future creators.</p>

<hr>

<h2>🪶 RH Legacy Footer</h2>
<p>This scroll was forged in the legacy archive of RangerHawk Studios.<br>
Every plugin tested. Every sidetrack preserved.<br>
May it guide future creators toward prompt invocation and plugin sovereignty.</p>

<p>This scroll was co-forged using AI assistance, but the structure, sequence, and symbolic intent are authored by <strong>Joe Molnar</strong> of RangerHawk Studios.<br>
Every step reflects a larger vision of mythic onboarding and creative sovereignty.</p>
