---
title: ADB安装过程
date: 2026-05-29
---

安装 adb

1.下载 SDK Platform Tools,打开 Android 开发者官网下载页，选择 Mac 版本下载 zip 文件。
developer.android.com/tools/releases/platform-tools

2.解压并移动到 Applications,下载后解压 zip，然后在终端执行：
mv ~/Downloads/platform-tools /Applications/platform-tools

3.配置 PATH,让终端任意位置都能直接用 adb 命令：
echo 'export PATH="/Applications/platform-tools:$PATH"' >> ~/.zshrc
source ~/.zshrc

验证安装
adb version
看到 "Android Debug Bridge version x.x.x" 说明安装成功,若提示"无法验证开发者"，去系统设置 → 隐私与安全性 → 仍要打开
连接手机

5.手机开启开发者选项
设置 → 关于手机 → 连续点击「版本号」7次，解锁开发者选项。

6.开启 USB 调试
设置 → 开发者选项 → 打开「USB 调试」。

7.连接数据线并授权,用 Type-C 数据线连接 Mac，手机弹出「允许 USB 调试」窗口，点允许。纯充电线没有数据传输功能，插上后若手机无弹窗则需换线

8.验证连接 adb devices 看到设备序列号 + "device" 字样即连接成功,若显示 "unauthorized"，执行 adb kill-server 后重新插线授权,卸载系统应用

9查找包名
adb shell pm list packages | grep <关键词>

10.卸载
adb shell pm uninstall --user 0 <包名>
看到 "Success" 即卸载成功。
如需恢复：
adb shell cmd package install-existing <包名>