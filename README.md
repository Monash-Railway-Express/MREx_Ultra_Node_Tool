# MREx Ultra Node Tool

A tool specifically designed for CAN MREx to program nodes and change variables mid operation from a gui on a computer.

## Also see
[CAN MREx](https://github.com/Monash-Railway-Express/CAN_MREx) - A CAN wrapper that is intended to adhere to most of the CAN open standards however it is specifically designed for use on the MREx locomotive

[MREx Dashboard](https://github.com/Monash-Railway-Express/MREx_Dashboard) - A dashboard to view recorded data from the CAN bus for analysis.

## Getting started

### 1. [Install Python](https://www.python.org/)

### 2. [Create virtual environment](https://docs.python.org/3/library/venv.html#how-venvs-work) (optional)

In the MREx_Ultra_Node_Tool folder in your favourite terminal.

`python -m venv venv`

### 3. [Enter virtual environment](https://docs.python.org/3/library/venv.html#how-venvs-work) (only if you completed step 2)

If you install dependencies into a virtual environment, you should enter the venv each time you want to run the application.

In the MREx_Ultra_Node_Tool folder in your favourite terminal, execute the command according to the following table. If your favourite terminal does not work, try another.

<table>
<thead>
<tr><th><p>Platform</p></th>
<th><p>Shell</p></th>
<th><p>Command to activate virtual environment</p></th>
</tr>
</thead>
<tbody>
<tr><td rowspan="4"><p>POSIX (Mac, Linux)</p></td>
<td><p>bash/zsh</p></td>
<td><p><code><span>$</span> <span>source</span> venv<span>/bin/activate</span></code></p></td>
</tr>
<tr><td><p>fish</p></td>
<td><p><code><span>$</span> <span>source</span> venv<span>/bin/activate.fish</span></code></p></td>
</tr>
<tr><td><p>csh/tcsh</p></td>
<td><p><code><span>$</span> <span>source</span> venv<span>/bin/activate.csh</span></code></p></td>
</tr>
<tr><td><p>pwsh</p></td>
<td><p><code><span>$</span> venv<span>/bin/Activate.ps1</span></code></p></td>
</tr>
<tr><td rowspan="2"><p>Windows</p></td>
<td><p>cmd.exe</p></td>
<td><p><code><span>C:\&gt;</span> venv<span>\Scripts\activate.bat</span></code></p></td>
</tr>
<tr><td><p>PowerShell</p></td>
<td><p><code><span>PS</span> <span>C:\&gt;</span> venv<span>\Scripts\Activate.ps1</span></code></p></td>
</tr>
</tbody>
</table>

### 4. Install dependencies

In the MREx_Ultra_Node_Tool folder in your favourite terminal.

`pip install -r requirements.txt`

### 5. Run the application

### 6. Bundle the application for distribution

In the MREx_Ultra_Node_Tool folder in your favourite terminal.

`pyinstaller --onefile --windowed --clean --icon=favicon.ico --add-data "favicon.ico;." MRExUltraNodeTool.py`

can skip `--clean` if only changing simple code

Your nicely packaged file can then be found at MREx_Ultra_Node_Tool/dist/MRExUltraNodeTool.exe !