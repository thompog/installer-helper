# installer-helper
this file is a simple way of making an installer well not making 
this installer just reads from a config file then installs files from that config file info a path
goto the config section for more info


this installer is so easy to set up that you unly need 4 things
1. Windows 11
2. installer helper.exe (can be installed in releases)
3. config.txt
4. a setup file (goto the setup file section for more info)


# config 
in the same dir as the installer helper.exe make a txt file name it "config"
then inside write this:
```
URLS;=
PATHS;=
EOF;;
```

after doing that write your urls after URLS;= but befor PATHS;= kinda like this:
```
URLS;=
https://raw.githubusercontent.com/yourgithub/your repo/refs/heads/main/yourfile.txt
PATHS;=
EOF;;
```
