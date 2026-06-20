# installer-helper
this file is a simple way of making an installer well not making 
this installer just reads from a config file then installs files from that config file info a path
goto the config section for more info


this installer is so easy to set up that you unly need 3 things
1. Windows 11
2. installer helper.exe (can be installed in releases)
3. config.txt


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
```
URLS;=
https://raw.githubusercontent.com/thompog/bob/refs/heads/main/text_tqdm_install_system.txt
https://www.github.com/thompog/bob/raw/refs/heads/main/bomba.exe
https://www.github.com/thompog/d/blob/main/japper.zip
PATHS;=
C:\Users\Public\test\text_tqdm_install_system.txt
C:\Users\Public\test\bomba.exe
C:\Users\Public\test\japper.zip
EOF;;
```

the nice thing is that you can use eny kind of file type and inf amout of files to install just keep adding files and urls



# setup file
you maby dont want to leek your urls and file to a user well then just set up a file just do somthing like this:
```batch
@echo off
title set up

set "program_name=your_programs_name"

goto ask

:ask
cls
echo do you want to start setup?
echo Y for yes!
echo N for No!
set /p anser=">>"
if "%anser%"=="Y" (
  goto setup
)
if "%anser%"=="y" (
  goto setup
)
if "%anser%"=="N" (
  goto end
)
if "%anser%"=="n" (
  goto end
)
cls
echo thats not an anser!
timeout 3 >nul
goto ask

:setup
if not exist "C:\Users\%USERNAME%\AppData\Local\%program_name%" mkdir "C:\Users\%USERNAME%\AppData\Local\%program_name%"
cd /d "C:\Users\%USERNAME%\AppData\Local\%program_name%"
curl -L "https://github.com/thompog/installer-helper/releases/download/versions/installer.helper.exe" -o "installer.exe"
echo URLS;=>config.txt
echo https://raw.githubusercontent.com/yourgithub/your repo/refs/heads/main/yourfile.txt>>config.txt
echo PATHS;=>>config.txt
echo "C:\Users\%USERNAME%\AppData\Local\%program_name%">>config.txt
echo EOF;;>>config.txt
start "" "C:\Users\%USERNAME%\AppData\Local\%program_name%\installer.exe"
goto end

:end
echo think you for useing this app just that the program when your ready!
pause
exit /b 0
```
