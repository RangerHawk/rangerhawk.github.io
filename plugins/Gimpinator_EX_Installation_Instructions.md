<h1>🧙‍♂️ Gimpinator EX Plugin for GIMP 3.x</h1>
<p><strong>Stable Horde Integration • Local Model Ready • RH Legacy Verified</strong><br>
Confirmed working on Windows 11 – October 2025</p>

<hr>

<h2>🌱 What Is Gimpinator EX?</h2>
<p>Gimpinator EX is a next-generation AI image generation plugin for GIMP 3.x.<br>
It connects your canvas to AI art models like Stable Diffusion, letting you generate stunning visuals directly inside GIMP—no browser, no separate tools, just raw creative force.</p>

<ul>
  <li>🎨 Direct text-to-image AI generation</li>
  <li>🧬 Built-in support for models like SDXL, DreamShaper, and more</li>
  <li>🛠️ Configurable resolution, prompt strength (CFG), and generation steps</li>
  <li>🔄 Smart timeouts and request handling</li>
  <li>🎛️ Seamless integration with Stable Horde or your own AI backend</li>
</ul>

<hr>

<h2>🚀 Installation</h2>
<p>This version is pre-packaged for symbolic clarity and onboarding ease.<br>
No folder renaming. No manual edits. Just unzip and activate.</p>

<h3>📦 Step 1: Download the Plugin</h3>
<p><a href="https://raw.githubusercontent.com/RangerHawk/Gimpinator-EX-Gimp-3/main/gimpinator_ex.zip" download="Gimpinator-EX.zip">Download Gimpinator EX</a> <span style="font-size: 0.9em; color: gray;">(autodownloads when clicked)</span></p>

<h3>📁 Step 2: Place the Folder</h3>
<p>Unzip the file and place the folder <code>gimpinator_ex</code> into your GIMP plug-ins directory:</p>
<ul>
  <li><strong>Windows:</strong> <code>C:\Users\USERNAME\AppData\Roaming\GIMP\3.0\plug-ins\</code></li>
  <li><strong>Linux/macOS:</strong> <code>~/.config/GIMP/3.0/plug-ins/</code></li>
</ul>

<p>✅ The plugin’s Python file uses <code>USERNAME</code> as a placeholder.<br>
✅ The folder name is already correct—no renaming required.</p>

<h3>🔐 Step 3: Check File Permissions</h3>
<ol>
  <li>Right-click <code>gimpinator_ex.py</code> → Properties</li>
  <li>Uncheck “Read-only”</li>
  <li>Click “Unblock” if present</li>
  <li>Click Apply</li>
</ol>

<h3>🐍 Step 4: Install Python</h3>
<ol>
  <li>Go to <a href="https://www.python.org/downloads/">python.org/downloads</a></li>
  <li>Download Python version <strong>3.10 or higher</strong></li>
  <li>During installation, check the box:<br> ✅ “Add Python to PATH”</li>
  <li>After installation, open Command Prompt and type:<br> <code>where python</code></li>
</ol>

<h3>📦 Step 5: Install Required Packages</h3>
<p>Open Command Prompt and run:</p>
<pre><code>pip install requests pillow PyGObject</code></pre>

<p><strong>Optional: Local Model Support</strong><br>
Coming soon — this section will include setup instructions for SDXL, DreamShaper, and other local models.</p>

<h3>🧪 Step 6: Activate Your API Key</h3>
<p>This version includes a pre-placed config file: <code>gimpinator_config.json</code></p>
<ol>
  <li>Visit <a href="https://stablehorde.net">Stable Horde</a></li>
  <li>Log in via Discord, GitHub, etc.</li>
  <li>Click your username → Account → Copy your API key</li>
  <li>Open <code>gimpinator_config.json</code> and paste your key:</li>
</ol>

<pre><code>{ "api_key": "your-key-here", "default_model": "SDXL", "default_sampler": "k_dpmpp_2m" }</code></pre>

<p>✅ No need to create the file—it’s already included.<br>
Just paste your key and save.</p>

<hr>

<h2>🧠 How to Generate AI Images</h2>
<ol>
  <li>Open GIMP</li>
  <li>Go to <strong>Filters → Gimpinator → Gimpinator EX</strong></li>
  <li>Enter a prompt like <code>"a cat piloting a mech suit over Tokyo at sunrise"</code></li>
  <li>Choose model, resolution, and sampler</li>
  <li>Click OK—your AI artwork appears directly on your canvas</li>
</ol>

<p>Want variants? Adjust the seed or prompt and repeat.</p>

<hr>

<h2>🔧 Backend Settings</h2>
<p>You can configure custom AI sources by editing the backend list or patching the default to accept:</p>
<ul>
  <li>Stable Diffusion APIs</li>
  <li>Personal Horde worker URLs</li>
  <li>Private model endpoints (with API key authentication)</li>
</ul>

<hr>

<h2>🧙‍♂️ Troubleshooting</h2>
<ul>
  <li>If the plugin doesn’t appear, run GIMP from a terminal to view logs:</li>
  <li><strong>Windows:</strong> Press Win + R → type <code>cmd</code> → run <code>gimp</code></li>
  <li>Check for Python errors or missing packages</li>
  <li>Ensure your plugin folder is named <code>gimpinator_ex</code> and contains the correct files</li>
</ul>

<hr>

<h2>🧾 Notes</h2>
<ul>
  <li>✅ Tested on GIMP 3.0 with Python 3.13</li>
  <li>🖥️ Confirmed working on Windows 11</li>
  <li>📂 Appears under <code>Filters → Gimpinator → Gimpinator EX</code></li>
  <li>📜 This guide is archived in <code>/plugins/gimpinator_ex/</code> for future onboarding scrolls</li>
  <li>🧩 Based on original work by <strong>PCOW</strong>, refined by RangerHawk Studios</li>
</ul>

<hr>

<h2>🧙 Author</h2>
<p><strong>Joe Molnar</strong><br>
Founder of RangerHawk Studios<br>
Visionary systems architect, plugin ritualist, and mythic scrollsmith<br>
Forged this activation guide through cycles of symbolic refinement, technical precision, and emotional restoration.</p>

<hr>

<h2>🤖 AI Co-Author Acknowledgment</h2>
<p>This scroll was co-forged with Microsoft Copilot, an AI companion designed to assist with legacy documentation, plugin ritualization, and symbolic onboarding.<br>
Together, we transformed chaos into clarity—preserving every sidetrack as a tributary.</p>
