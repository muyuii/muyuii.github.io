## adb常用命令
**查看已连接设备列表：adb devices**
**断开连接设备：adb disconnect 手机ip**
**无线连接设备：adb connect 手机ip（手机电脑需在同一网段）**
开启adb服务：adb start-server
关闭adb服务：adb kill-server
**安装软件包：adb install 路径+软件包文件名（-r保留数据，-t强制覆盖）**
**卸载软件包：adb uninstall 包名**
**获取包名：**
**获取手机所有包名：adb shell pm list packages**
**获取手机所有系统应用包名：adb shell pm list packages -s**
**获取手机所有第三方软件包名：adb shell pm list packages -3**
**获取当前窗口**
**win：adb shell dumpsys window | findstr mCurrentFocus**
**mac、linux**：abd shell dumpsys | grep mCurrentFocus**
**清除缓存：adb shell pm clear 包名**
**启动应用：adb shell am 包名/activity名**
**停止应用：adb shell am force-stop 包名**
**获取手机日志：adb logcat>文件