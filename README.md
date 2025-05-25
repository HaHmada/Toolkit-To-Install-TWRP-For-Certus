<div align="center">

# Toolkit FlashTWRP For Redmi 6/6A

![Logo](https://github.com/HaHmada/assets-repository/blob/main/TWRP/TWRP.png)
</div>

# Uses Of This Tool
- Make It Easy For You To Install TWRP

# This Toolkit View
![Version 1.0](https://github.com/HaHmada/assets-repository/blob/main/TWRP/Toolkit-FlashTWRP-For-Certus.png)

> **Note**: For Now Only Support Windows 

# How To Use

1. Download The File In [Here](https://github.com/HaHmada/Toolkit-To-Install-TWRP-For-Certus/releases/ "Download Link")

2. Extract The File (With Winrar Or Other Extractor)

3. After Extract The File, Open "Toolkit FlashTWRP.bat"

4. Follow The Instructions

5. Congratulations, You Can Now Use TWRP On Your Redmi 6/6A

# You Can Make This Toolkit Yourself (Only For Windows 7 or New Version)

<details>
	 <summary><b>Click Here To Start Build</b></summary>

# Tools

- [TWRP For Certus](https://eu.dl.twrp.me/cactus/twrp-3.7.0_9-0-cactus.img "TWRP")

**Git For Windows Versions**

- [Git For Windows (32-bit)](https://objects.githubusercontent.com/github-production-release-asset-2e65be/23216272/3a299a53-faf3-4a79-b4f5-bc1b0bd64f74?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20241129%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20241129T124320Z&X-Amz-Expires=300&X-Amz-Signature=91f5e2d35ff6633fd1677dffa6ba06a7e413695db401841627db031ad54e2dd2&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3DGit-2.47.1-32-bit.exe&response-content-type=application%2Foctet-stream "Git-For-Windows_32-bit")

- [Git For Windows (64-bit)](https://objects.githubusercontent.com/github-production-release-asset-2e65be/23216272/67e30882-badc-4f28-a242-90f27d9ed99d?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20241129%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20241129T124520Z&X-Amz-Expires=300&X-Amz-Signature=6225f1644bf93572e9185340d9f49716f4ea6fd267ff34d22988782aed287675&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3DGit-2.47.1-64-bit.exe&response-content-type=application%2Foctet-stream "Git-For-Windows_64-bit")

**Notepad++ Versions**

- [Notepad++ x86 (32-bit)](https://objects.githubusercontent.com/github-production-release-asset-2e65be/33014811/cddd26c4-d387-4259-ba6c-cefba3b02e13?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20241129%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20241129T123354Z&X-Amz-Expires=300&X-Amz-Signature=f5ca99e3fa48aba1309bccdca9e3b6189e8dc052cfe78781ed4d73d2816f5c59&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3Dnpp.8.7.2.Installer.exe&response-content-type=application%2Foctet-stream "Notepad++_x86")

- [Notepad++ ARM64/x86_64 (64-bit)](https://objects.githubusercontent.com/github-production-release-asset-2e65be/33014811/a768fb53-85e0-4176-bb94-2f0a48463375?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20241129%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20241129T123713Z&X-Amz-Expires=300&X-Amz-Signature=469ddee8bc51648bad2e4ef8c8e4f3c958978c6f4bad7371d3c7cd256eb0a206&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3Dnpp.8.7.2.Installer.arm64.exe&response-content-type=application%2Foctet-stream "Notepad++_ARM64")

> **Note**: Rename twrp-3.7.0_9-0-cactus.img To recovery.img

# After You Install Everything, Follow This Steps

1. First You Have To Find A Location ("Documents" Folder Example)

2. Open CMD And Open Documents Folder In CMD

```
cd Documents
```

3. Copy This Command To CMD (If This Doesn't Work You Can Use "Git CMD")

```
git clone https://github.com/HaHmada/Toolkit-To-Install-TWRP-For-Certus.git -b TWRP
```

4. After That Close CMD

5. Put The "recovery.img" File Into The Toolkit-To-Install-TWRP-For-Certus Folder

6. Open Notepad++, And Paste In Notepad++

```
@echo off
TITLE Toolkit Flash TWRP By HaH Mada
color 37
Mode con: COLS=75 LINES=40
echo.
echo     ************************************************************
echo     *******              Toolkit Flash TWRP              *******
echo     *******                 By HaH mada                  *******
echo     ************************************************************
echo     *******                 Redmi 6/6A                   *******
echo     ************************************************************
echo.             
echo.
taskkill /f /im "adb.exe" >nul 2>nul
cd /d %~dp0adb
adb kill-server
adb start-server
echo.
echo   *******  Waiting For The Device
adb devices
echo.
pause
echo.
echo   *******  Booting Into Fastboot Mode
adb reboot bootloader
echo.
pause
echo.
echo   *******  Erase Stock Recovery
fastboot erase recovery
echo.
pause
echo.
echo   *******  Flashing Twrp Recovery
fastboot flash recovery recovery.img
echo.
pause
echo.
echo   *******  Reboot To Recovery
fastboot boot recovery.img
echo.             
echo   *******  SUCCESS!
echo   If You Can't Enter TWRP, Enter TWRP Manually With Volume Up + Power   
echo.                
ECHO.  Press ENTER to exit ...
pause  >NUL
EXIT
```

7. Once you are done, click CTRL+SHIFT+S & Following This Settings

Location: C:/Users/user/Documents/Toolkit-To-Install-TWRP-For-Certus

File name: Toolkit.bat

Save as type: All types (*.*)

8. Finish You Can Use This Toolkit

</details>

# Error Solution

If Your Devices Are Not Detected Like This

```
< waiting for any device >
```
You Must Install Driver For Redmi 6/6A, Click the Link Below

<a href="https://xiaomidriver.com/xiaomi-redmi-6a"><img src="https://img.shields.io/badge/Driver%20For-Redmi%206/6A-orange?style=flat&logo=xiaomi" /></a>
