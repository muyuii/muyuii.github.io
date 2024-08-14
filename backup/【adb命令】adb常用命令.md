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
**获取手机日志：adb logcat>本地文件**
**获取启动时间：adb shell am start -W 包名/activity名**
-W：获取启动时间 -S：启动前强行停止应用（冷启动） -R 数字：启动次数
三个参数均大写，顺序可调，-R后必须接数字
**获取内存信息：adb shell dumpsys meminfo 包名**
**Native/Dalvik的Heap信息若一直增长，可能发送内存泄漏**
*Total的PSS信息是应用真正占据内存大小***
**获取cpu信息：（推荐用top）**
**adb shell dumpsys cpuinfo(查看当前cpu占用情况）**
**adb shell top -s 9（-m：  -s：按一定顺序）**
**获取流量消耗值：**
**首先：获取userId：adb shell dumpsys packge 包名 | findstr userId**
**获取上行流量：adb shell cat proc/uis_stat/userId/tcp_snd**
**获取下行流量：adb shell cat proc/uis_stat/userId/tcp_rcv**
**稳定性测试（monkey）：adb shell monkey -p 包名 -v 次数>日志文件地址**
-p 指定包名（所有命令都在此包内执行，如不指定，则在整个系统内执行）
-v log详细程度（最高支持-v-v-v’最详细）
-s 指定序列
--throttle 单步延时（数字)（每步操作间隔，单位毫秒）
--pct-touch/motion等 点击事件