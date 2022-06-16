# ghidra-python-skeleton

A simple template repo to provide a VScode Ghidra python scripting environment.


## Workflow

Ghidra is a binary analysis tool. In order to do something useful, you need to add binaries to your project. 

1. [Create Ghidra Project](.vscode/tasks.json)
2. [Import binary to project](.vscode/tasks.json)
3. [Run script on binary](run_headless.py)



## Dependencies
- https://github.com/clearbluejar/ghidra-pyi-generator
  - Provides the autocomplete in VSCode
  - relies on [settings.json](.vscode/settings.json) being configured correctly (already configured in template)
- https://ghidra-sre.org/ 
  - Need to download the latest Ghidra and it's dependencies
  

## Setup

### Setup venv
```bash
python3 -m venv .env
source .env/bin/activate
```
### Install stubs
pip install ghidra_stubs
wget https://github.com/clearbluejar/ghidra-pyi-generator/releases/download/v1.0.3-10.1.4/ghidra_stubs-10.1.4.refs_heads_master-py2.py3-none-any.whl
pip install ghidra_stubs-10.1.4.refs_heads_master-py2.py3-none-any.whl
```

## Need to know

This simple skeleton runs [skeleton.py](skeleton.py) directly. It just passes it to the `HeadlessAnalyzer`.
The only way to pass some string arguments is with a properties file. 

