# CubeDesk

CubeDesk 是一款智能魔方应用，提供 Windows 和 Android 版本，支持竞速、普通计时、CFOP 训练、本地成绩分析与可定制的成就特效。核心功能和内置素材支持离线使用。

## Android 手机版下载

[下载 CubeDesk Android 0.1.16](https://github.com/Jay6668/CubeDesk-Releases/releases/tag/android-v0.1.16)

选择 `CubeDesk-Android-0.1.16.apk`。支持 Android 8.0 及以上（arm64-v8a / x86_64），支持横竖屏；连接智能魔方需要蓝牙。手机版不包含开发板控制功能。

已有旧版请直接覆盖安装，包名和签名保持一致；不要先卸载或清除数据。建议更新前在设置里导出备份。本次构建及签名核验完成，未进行新版本手机实机检查；新增协议的验证范围见下表。此前 0.1.13 的旋转锁定修复已由用户安装确认，本次保留该策略。

## Windows 桌面版下载

[下载 CubeDesk Windows 0.23.1](https://github.com/Jay6668/CubeDesk-Releases/releases/tag/v0.23.1)

选择 `CubeDesk-0.23.1-Windows-x64.exe`，下载后直接运行。这是单文件应用，没有安装向导。需要 Windows 10/11 64 位和 Microsoft Edge WebView2 Runtime，连接智能魔方时需要蓝牙适配器。

数据保存在本机。新版沿用原数据目录，建议更新前从设置导出备份。本次已通过隔离数据目录下的封装资源检查，36 项成就素材和训练库完整。

## 多品牌三阶智能魔方：实验性适配

| 协议 / 设备系列 | 本次验证范围 |
| --- | --- |
| MoYu32 / 威龙 V10 AI | 保留原有驱动；本轮未重新进行实物验收 |
| GAN Gen1 / 356i | 合成报文、加密与读取流程离线检查 |
| GAN Gen2 | 离线检查；GAN12ui、GAN12ui FreePlay、GANic 公开抓包回放 |
| GAN Gen3 | 合成报文与连接生命周期离线检查 |
| GAN Gen4 | 离线检查；GAN i4 公开抓包回放 |
| 奇艺智能三阶 / Tornado V4 | 离线检查；奇艺、Tornado V4 公开抓包回放 |
| GiiKER / Mi Smart Cube | 离线检查；GiiKER i3SE 公开抓包回放 |
| GoCube / Rubik’s Connected | 离线检查；两类设备公开抓包回放 |
| MoYu MHC v1 | 合成报文、多通知通道与状态读取流程离线检查 |

新增协议尚未有对应型号的实际连接验收。同品牌、不同固件不保证通用；设备按实际 GATT 服务识别。部分型号可能需补充 MAC，电量与历史能力因设备而异。MHC 在读不到面状态时，需要先手工复原并同步。此轮不支持 GAN 251、计客 i2 等二阶设备。

验证合计：35 项离线检查；9 套公开抓包共 1,299 个数据包、280 步转动与原记录一致。抓包回放不能替代真实蓝牙连接测试。

协议实现参考 MIT 许可的 [gan-web-bluetooth](https://github.com/afedotov/gan-web-bluetooth) 和 [smartcube-web-bluetooth](https://github.com/poliva/smartcube-web-bluetooth)，许可随应用保留。

## 国内下载与更新提醒

国内下载：[夸克网盘](https://pan.quark.cn/s/88e2650d3fa8)，提取码 **4bdt**。

当前版本：Windows **0.23.1**、Android **0.1.16**（versionCode 17）。进入 `10.17 更新：国内更新支持（安卓0.1.16 电脑0.23.1）` 文件夹，按平台选择安装包；夸克是否要求登录或客户端，以其页面提示为准。

新版启动后可在后台检查更新，优先读取 [Gitee 公开版本信息](https://gitee.com/jiuzhijin/cubedesk-releases)，GitHub 作为备用源。设置中可以关闭自动检查、手动检查，或直接打开夸克下载入口。检查失败不影响离线使用；检查过程不上传成绩、设备地址或个人资料。复原或已有弹窗时，自动提醒会推迟展示。下载和安装仍需用户确认，不会静默安装。

较早版本需要先手动安装本次版本，才能使用国内更新源。Android 请使用同包名、同签名安装包**覆盖安装**，不要先卸载或清除数据；建议先从设置导出备份。Windows 沿用原数据目录。本次构建与签名检查已完成，未进行新版本手机实机验收；多品牌智能魔方支持仍属于实验性适配。

## 数据分析

成绩趋势、稳定性、转动效率、练习记录四个视角，配合折线图、数量柱状图、四分位范围、散点图、练习日历和分页记录；支持今天、近 30 天、近 3 个月等时间范围。

以下截图使用隔离的示例数据，不包含真实用户成绩。

![成绩趋势](screenshots/analysis-trend.png)
![稳定性与成绩分布](screenshots/analysis-stability.png)

## 下载校验

每个版本附有 `SHA256SUMS.txt`，可用于核对文件完整性。

这个公开仓库用于发布应用下载和说明。源码保存在独立的私有仓库。
