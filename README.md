# CubeDesk

CubeDesk 是一款 Windows / Android 智能魔方训练应用，提供竞速计时、普通魔方计时、CFOP训练、本地成绩分析与可定制成就。核心训练与数据在本地运行，支持离线使用；安卓版支持横竖屏。

## 最新正式版 · 2026-10-20

作者已验收本次双端版本，并将原安装包提升为正式发行版。保留内部构建标识，文件与验收版完全一致；GitHub发行状态为正式版。

| 平台 | 正式发行版与构建标识 | 下载 |
| --- | --- | --- |
| Android | 0.2.0（`0.2.0-preview.15`，versionCode37） | [下载安卓版](https://github.com/Jay6668/CubeDesk-Releases/releases/download/android-v0.2.0-preview.15/CubeDesk-Mobile-0.2.0-preview.15.apk) · [发行说明](https://github.com/Jay6668/CubeDesk-Releases/releases/tag/android-v0.2.0-preview.15) |
| Windows | 0.24.0（`0.24.0-preview.14`） | [下载电脑版](https://github.com/Jay6668/CubeDesk-Releases/releases/download/v0.24.0-preview.14/CubeDesk-Windows-0.24.0-preview.14.exe) · [发行说明](https://github.com/Jay6668/CubeDesk-Releases/releases/tag/v0.24.0-preview.14) |

### 国内下载

[夸克原分享](https://pan.quark.cn/s/88e2650d3fa8)，提取码 **4bdt**。打开 **10.20 正式版更新（安卓0.2.0 电脑0.24.0）**，按手机或电脑选择文件。两份安装包已包含运行所需内置成就素材，无需另找桌面素材文件。

### 本次更新

- 修复连续错步撤回和模型黑影，优化快转跟随。
- 新增、精修原创皮肤与主题、头像框，统一折方Logo及首页品牌排版。
- 压紧横竖屏页面、连接与设置面板，调整模型和成绩显示比例。
- 成绩卡绑定主题，修复切屏字号异常，保留两位小数、步数、TPS与分析入口。
- 内置成就精简为24款；可添加15秒以内视频、图片及展示时长，可删除自己的自定义素材。内置素材不提供单独删除，空间管理页面暂不开放。

### 安装与更新

- Android支持8.0及以上（arm64-v8a / x86_64），仅需智能魔方蓝牙连接，不含开发板控制功能。请同包名、同签名**覆盖安装**，不要先卸载或清除数据；建议更新前从设置导出备份。
- Windows需10/11 64位与Edge WebView2 Runtime。关闭旧版后运行新版EXE，沿用原数据目录；建议更新前导出备份。
- 设置中的更新检查优先读取[Gitee国内版本源](https://gitee.com/jiuzhijin/cubedesk-releases)，GitHub为备用。检查可关闭，失败不影响离线使用；下载和安装由用户确认。
- 新公式深度改进、独立下载网站与新型号实物验证留待后续，不把协议接入描述成所有魔方都已实测。

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


## 数据分析

成绩趋势、稳定性、转动效率、练习记录四个视角，配合折线图、数量柱状图、四分位范围、散点图、练习日历和分页记录；支持今天、近 30 天、近 3 个月等时间范围。

以下截图使用隔离的示例数据，不包含真实用户成绩。

![成绩趋势](screenshots/analysis-trend.png)
![稳定性与成绩分布](screenshots/analysis-stability.png)

## 下载校验与源码

发行附件及仓库提供`SHA256SUMS.txt`，可核对文件完整性。此公开仓库只提供下载、说明、版本信息和示例截图；源码保存在独立私有仓库，下载包不包含个人成绩或配置。
