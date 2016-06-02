# AutoOperationAppiumDemo

libs下面放着必要的jar包

http://appium.io/ 官方网站

https://github.com/appium/sample-code/tree/master/sample-code/examples 官方示例代码

cmd 下 adb devices 一定要有设备才行

如果遇到以下问题：

1. 必须得保证 appium的路径 中没有空格，有空格会出问题的。

2.
> error: Failed to start an Appium session, err was: Error: Command failed: C:\Windows\system32\cmd.exe /s /c "D:\Android\SDK\platform-tools\adb.exe -s 192.168.56.101:5555 install "D:\ProgramFiles\Appium\node_modules\appium\build\settings_apk\settings_apk-debug.apk""
> 
> info: [debug] Error: Command failed: C:\Windows\system32\cmd.exe /s /c "D:\Android\SDK\platform-tools\adb.exe -s 192.168.56.101:5555 install "D:\ProgramFiles\Appium\node_modules\appium\build\settings_apk\settings_apk-debug.apk""
> 
>     at ChildProcess.exithandler (child_process.js:751:12)
>     at ChildProcess.emit (events.js:110:17)
>     at maybeClose (child_process.js:1016:16)
>     at Process.ChildProcess._handle.onexit (child_process.js:1088:5)
> info: [debug] Responding to client with error: {"status":33,"value":{"message":"A new session could not be created. (Original error: Command failed: C:\\Windows\\system32\\cmd.exe /s /c \"D:\\Android\\SDK\\platform-tools\\adb.exe -s 192.168.56.101:5555 install \"D:\\ProgramFiles\\Appium\\node_modules\\appium\\build\\settings_apk\\settings_apk-debug.apk\"\"\n)","killed":false,"code":3221226356,"signal":null,"cmd":"C:\\Windows\\system32\\cmd.exe /s /c \"D:\\Android\\SDK\\platform-tools\\adb.exe -s 192.168.56.101:5555 install \"D:\\ProgramFiles\\Appium\\node_modules\\appium\\build\\settings_apk\\settings_apk-debug.apk\"\"","origValue":"Command failed: C:\\Windows\\system32\\cmd.exe /s /c \"D:\\Android\\SDK\\platform-tools\\adb.exe -s 192.168.56.101:5555 install \"D:\\ProgramFiles\\Appium\\node_modules\\appium\\build\\settings_apk\\settings_apk-debug.apk\"\"\n"},"sessionId":null}
> info: <-- POST /wd/hub/session 500 30396.453 ms - 841 

等，可以把它之前的命令放入 cmd下运行， 一般是  由于 adb 方面出问题，一般是命令执行出错，可以换个其他版本的 adb.exe 试试 （本人就碰到这个问题。）

