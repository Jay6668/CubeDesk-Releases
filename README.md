# CubeDesk

CubeDesk 是一款智能魔方应用，提供 Windows 桌面版和 Android 手机版，支持竞速、普通计时、CFOP 训练和本地成绩分析。

## Android 手机版下载

[下载 CubeDesk Android · v0.1.13](https://github.com/Jay6668/CubeDesk-Releases/releases/tag/android-v0.1.13)

选择 `CubeDesk-Android-0.1.13.apk`。支持 Android 8.0 及以上（arm64-v8a / x86_64）；连接智能魔方需要蓝牙。手机版支持横竖屏，不包含开发板控制功能。

已有旧版请直接覆盖安装；不要先卸载或清除数据。建议更新前通过设置导出备份。该版本已在 vivo X100 / Android 16 实机验证，应用内版本号为 `0.1.13-preview`。

本次 0.1.13 修复系统锁定竖屏后应用仍自动旋转的问题，已由用户安装确认。

## Windows 桌面版下载

[下载 CubeDesk 0.21.0](https://github.com/Jay6668/CubeDesk-Releases/releases/tag/v0.21.0)

选择 `CubeDesk-0.21.0-Windows-x64.exe`，下载后直接运行。这是单文件应用，没有安装向导。

需要 Windows 10/11 64 位和 Microsoft Edge WebView2 Runtime。连接智能魔方时需要蓝牙适配器。

核心计时、训练、分析和内置素材可离线使用。数据保存在电脑本地；更新前可以通过应用设置导出备份。

## 0.21.0：数据分析更新

成绩趋势、稳定性、转动效率、练习记录四个独立视角，配合折线图、数量柱状图、四分位范围、散点图、练习日历和分页记录。新增今天、近 30 天和近 3 个月等时间范围；修复水墨主题下等高色块遮蔽真实趋势的问题。

截图使用隔离的示例数据，不包含真实用户成绩。

![成绩趋势](screenshots/analysis-trend.png)

![稳定性与成绩分布](screenshots/analysis-stability.png)

## 下载校验

每个版本附有 `SHA256SUMS.txt`，可用于核对文件完整性。

这个公开仓库用于发布应用下载和说明。源码保存在独立的私有仓库。
