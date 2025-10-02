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

<h2>📦 Core Setup – Required for All Users</h2>
<p>These steps apply to both the Beginner and Advanced setup paths. Complete them before activating the plugin.</p>

<h3>🐍 Step 1: Install Python</h3>
<ol>
  <li>Go to <a href="https://www.python.org/downloads/">python.org/downloads</a></li>
  <li>Download Python version <strong>3.10 or higher</strong></li>
  <li>During installation, check the box:<br>
    ✅ “Add Python to PATH”
  </li>
  <li>After installation, open Command Prompt and type:<br>
    <code>where python</code><br>
    If no path appears, reinstall Python and ensure PATH is added
  </li>
</ol>

<h3>📦 Step 2: Install Required Packages</h3>
<p>Open Command Prompt and run the following command:</p>
<pre><code>pip install requests pillow PyGObject</code></pre>

<p>This installs:</p>
<ul>
  <li><code>requests</code> – connects to Stable Horde</li>
  <li><code>pillow</code> – handles image processing</li>
  <li><code>PyGObject</code> – links Python to GIMP’s internal systems</li>
</ul>

<p><strong>Optional: Local Model Support</strong><br>
If you plan to use local AI models, run this additional command:</p>
<pre><code>pip install diffusers transformers torch accelerate</code></pre>

<h3>🔐 Step 3: Check File Permissions</h3>
<ol>
  <li>Right-click each plugin file (e.g. <code>gimpinator_ex.py</code>) → Properties</li>
  <li>Uncheck “Read-only”</li>
  <li>Click “Unblock” if present</li>
  <li>Click Apply</li>
</ol>

<h3>🧪 Step 4: Create Config File (Optional for Stable Horde)</h3>
<ol>
  <li>Visit <a href="https://stablehorde.net">Stable Horde</a></li>
  <li>Log in via Discord, GitHub, etc.</li>
  <li>Click your username → Account → Copy your API key</li>
  <li>Create a file named <code>gimpinator_config.json</code> with this content:</li>
</ol>

<pre><code>{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }</code></pre>

<p>Save the file inside the plugin folder using “Save as type: All Files”</p>

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
    <li>Plugin appears in GIMP under:<br>
      <code>Filters → Gimpinator → Gimpinator EX</code>
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
    <li>Optional grouping:<br>
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
  <li>📜 This guide is archived in <code>/plugins/g
