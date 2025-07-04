# FridaScriptGen
 
It scans an APK’s Smali code for root-detection and SSL-pinning patterns and then automatically creates Frida scripts to bypass these security checks.
 
[![License: CC BY-NC-ND 4.0](https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
  
<p align="center">
  <img width="544" alt="image" src="https://github.com/user-attachments/assets/72dbf90d-9cf7-462c-a5c7-430fe4265a81"/>
</p>
 
<p align="center">
  <img width="567" alt="image" src="https://github.com/user-attachments/assets/2e780eb5-fcdc-41ca-b1c9-7c8550d80b67"/>
</p>
 
 
## Features
- Analyzes APK for root/SSL detections and creates tailored Frida scripts
 
> **Note:** This is the lite version of the script.
 

- Currently, this is a 𝐥𝐢𝐭𝐞 𝐯𝐞𝐫𝐬𝐢𝐨𝐧 🪶 that supports 83+ root & SSL detection methods.
- 🔍 Performs Smali pattern checks and generates hooks.
- Eliminates the need to run and manage multiple scripts manually.
- 🚫 Does not support highly complex obfuscation or low-level binary checks. Not guaranteed to work for all scenarios
- 🔧 Under active development and will be improved over time.

## Usage
```bash
python3 frida-script-gen.py <apk_file> [-o output_name]
```
 
## Requirements
- Python 3.X
- androguard==3.3.5
- apktool
- rich
 
## Installation
```bash
pip3 install androguard==3.3.5 rich
```
 
## Example
```bash
python3 frida-script-gen.py app.apk
frida -U -f com.example.app -l bypass_script.js
```
