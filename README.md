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

after doing that write your urls after URLS;= but befor PATHS;= like this:
```
URLS;=
https://raw.githubusercontent.com/yourgithub/your repo/refs/heads/main/yourfile.txt
PATHS;=
EOF;;
```

after that you write your file path like this:
```
URLS;=
https://raw.githubusercontent.com/yourgithub/your repo/refs/heads/main/yourfile.txt
PATHS;=
C:\To\Your\file.txt
EOF;;
```

the end resolt shold look like kinda this:
´´´
URLS;=
https://raw.githubusercontent.com/thompog/bob/refs/heads/main/text_tqdm_install_system.txt
https://www.github.com/thompog/bob/raw/refs/heads/main/bomba.exe
https://www.github.com/thompog/d/blob/main/japper.zip
PATHS;=
C:\Users\Public\test\text_tqdm_install_system.txt
C:\Users\Public\test\bomba.exe
C:\Users\Public\test\japper.zip
EOF;;
´´´

the nice thing is that you can use eny kind of file type and inf amout of files to install just keep adding files and urls
