# Personal Software Setup With Ansible - Windows + WSL

This code is to set up a new system on a fresh install of Windows. If you want to use this, please add or remove any software you like after pulling

## Prerequisites

1. Install WSL
2. Set up a virtual environment with python in your WSL distro
3. Install ansible via pip/pip3
4. Install ansible-dev-tools
    - `pip3 install ansible-dev-tools`

## VS Code Extension

Once VS Code is installed, you can install the ansible extension. To make use of the virtual environment afterwards, use the command palette and search for `Ansible: Set Python Interpreter` and browse to your python executable file inside your virtual environment. Otherwise, the extension can't run ansible related commands for you. If you get notices that ansible-lint is failing, make sure ansible-lint is installed via ansible-dev-tools or separately.

**Alternatively** Add a `settings.json` file to a `.vscode` folder and add the following lines

```json
{
    "ansible.python.interpreterPath": "/home/zsext/.venv/bin/python3.12"
}
```
