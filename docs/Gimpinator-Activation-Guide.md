<details>
<summary>🧙‍♂️ Gimpinator EX Plugin for GIMP 3.x – RH Legacy Verified</summary>

<p><strong>Stable Horde Integration • Local Model Ready • Confirmed on Windows 11 – September 2025</strong></p>

<hr>

<h3>🛡️ RH Legacy Crest – Symbolic Activation</h3>
<p>This plugin scroll was authored by RangerHawk Studios.<br>
Every glyph tested. Every sidetrack archived.</p>
<img src="https://rangerhawk.github.io/assets/Crest.png" alt="RH Legacy Crest">

<hr>

<h3>🌱 What Is Gimpinator EX?</h3>
<p>Gimpinator EX lets you generate AI images directly inside GIMP using text prompts.<br>
It supports <strong>Stable Horde</strong> (a free, online distributed backend) and <strong>optional local model scaffolding</strong> via separate tools.<br>
<em>Note: Stable Horde is an online service. Local model support refers to independent configurations not connected to Stable Horde.</em></p>

<hr>

<h3>📦 Installation Guide (Beginner-Friendly)</h3>

<details>
<summary>🧰 Beginner Setup – RangerHawk Version</summary>

<ol>
<li><strong>Download the Plugin</strong><br>
<a href="https://rangerhawk.github.io/plugins/gimpinator_ex/Gimpinator-EX.zip">RangerHawk Gimpinator EX ZIP</a><br>
No renaming or manual edits required. Folder structure and username references are already corrected.</li>

<li><strong>Unzip and Move</strong><br>
Extract to:<br>
<code>C:\Users\USERNAME\AppData\Roaming\GIMP\3.0\plug-ins\</code><br>
Confirm files:<br>
<ul>
<li>gimpinator_ex.py</li>
<li>gimpinator_config.json (optional)</li>
</ul></li>

<li><strong>Check File Permissions</strong><br>
Right-click each file → Properties<br>
Uncheck “Read-only” and click “Unblock” if present.</li>

<li><strong>Create Config File (Optional)</strong><br>
Get a Stable Horde API key:<br>
<a href="https://stablehorde.net">https://stablehorde.net</a><br>
Create <code>gimpinator_config.json</code> with:<br>
<pre>{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }</pre></li>

<li><strong>Install Python</strong><br>
<a href="https://www.python.org/downloads/">Download Python 3.10+</a><br>
Check “Add Python to PATH” during setup.<br>
Use <code>where python</code> in Command Prompt to verify.</li>
</ol>
</details>

<hr>

<h3>🧠 Advanced Activation Guide</h3>

<details>
<summary>🧪 Expert Setup – Manual Configuration</summary>

<ul>
<li><strong>Folder Structure</strong><br>
<code>C:\Users\USERNAME\AppData\Roaming\GIMP\3.0\plug-ins\gimpinator_ex</code></li>

<li><strong>Python Environment</strong><br>
<code>pip install requests pillow PyGObject</code><br>
Optional:<br>
<code>pip install diffusers transformers torch accelerate</code></li>

<li><strong>Plugin Script Requirements</strong><br>
Start of file:<br>
<code>#!/usr/bin/env python3</code><br>
Required imports:<br>
<pre>
import gi  
gi.require_version("Gimp", "3.0")  
from gi.repository import Gimp, GimpUi, GObject, GLib, Gio, Gtk  
import sys, os, json
</pre>
Plugin class:<br>
<pre>
class Gimpinator(Gimp.PlugIn):  
    def do_query_procedures(self):  
        return ["plug-in-gimpinator-ex"]
</pre>
Main invocation:<br>
<code>Gimp.main(Gimpinator.__gtype__, sys.argv)</code></li>

<li><strong>Menu Path</strong><br>
Filters → Gimpinator → Gimpinator EX<br>
Optional:<br>
<code>proc.add_menu_path("&lt;Image&gt;/Filters/AI")</code></li>
</ul>
</details>

<hr>

<h3>🧾 Notes</h3>
<ul>
<li>Tested on GIMP 3.0 with Python 3.13</li>
<li>Confirmed working on Windows 11</li>
<li>Appears under Filters → Gimpinator → Gimpinator EX</li>
<li>RangerHawk version uses USERNAME placeholder and correct folder structure</li>
<li>Stable Horde is online-only; local model support is separate</li>
<li>This guide is archived in <code>/plugins/gimpinator_ex/</code></li>
</ul>

<hr>

<h3>🧙 Contributor</h3>
<p>Joe Molnar<br>
Founder of RangerHawk Studios<br>
Creative systems architect and mythic plugin ritualist</p>

<hr>

<h3>🪶 RH Legacy Footer</h3>
<p>This scroll was forged in the legacy archive of RangerHawk Studios.<br>
Every plugin tested. Every sidetrack preserved.<br>
May it guide future creators toward prompt invocation and plugin sovereignty.</p>

<p>This scroll was co-forged using AI assistance, but the structure, sequence, and symbolic intent are authored by Joe Molnar of RangerHawk Studios.<br>
Every step reflects a larger vision of mythic onboarding and creative sovereignty.</p>

</details>
