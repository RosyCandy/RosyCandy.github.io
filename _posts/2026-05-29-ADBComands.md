---
title: ADB常用指令
date: 2026-05-29
---

准备 / 连接
adb devices 查看已连接设备
adb kill-server 杀掉 adb 后台服务
adb start-server 启动 adb 后台服务
adb pair : 无线配对（Android 11+）
adb connect : 无线连接

应用管理
adb shell pm list packages 列出所有已安装包
adb shell pm list packages -3 只列第三方应用
... | grep <关键词> 过滤包名
adb shell pm uninstall --user 0 <包名> 卸载应用（当前用户，可恢复）
adb shell cmd package install-existing <包名> 恢复被卸载的系统应用
adb install <apk路径> 安装本地 APK

文件传输
adb push <本地路径> <手机路径> 推送文件到手机
adb pull <手机路径> <本地路径> 从手机拉取文件

调试 / 其他
adb shell 进入手机 shell交互环境
adb reboot 重启手机
adb reboot recovery 重启进入 recovery 模式
adb logcat 查看系统日志（调试用）
adb version 查看 adb 版本
恢复提示：--user 0 卸载可用 install-existing 恢复；彻底找回可恢复出厂设置。