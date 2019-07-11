# HP_Probook_440_G6_EFI

## HP Probook 440 G6 EFI 黑苹果 HACKINTOSH

[![img](https://img.shields.io/github/stars/jinmu333/HP_Probook_440_G6_EFI.svg?logoColor=blue&style=for-the-badge)
![img](https://img.shields.io/github/forks/jinmu333/HP_Probook_440_G6_EFI.svg?logoColor=blue&style=for-the-badge)
![img](https://img.shields.io/github/last-commit/jinmu333/HP_Probook_440_G6_EFI.svg?color=blue&style=for-the-badge)](https://github.com/jinmu333/HP_Probook_440_G6_EFI)
[![img](https://img.shields.io/badge/link-996.icu-red.svg?style=for-the-badge)](https://github.com/996icu/996.ICU)

## HP Probook 440 G6 EFI for macOS Mojave

[English](README_EN.md) | [中文](README.md)

这是我使用的 HP_Probook_440_G6 的CLOVER引导文件

### 定制usb

[定制usb教程](https://blog.daliansky.net/Intel-FB-Patcher-tutorial-and-insertion-pose.html)

### 调整 macOS CPU性能

[使用方法](https://github.com/daliansky/XiaoMi-Pro/blob/master/one-key-cpufriend/README_CN.md)

### 电脑配置

| 规格     | 详细信息                                                |
| -------- | ----------------------------------------------------- |
| 电脑型号 | HP Probook 440G6 笔记本电脑                                    |
| 操作系统 | macOS Mojave 18D42                                   |
| 处理器   | 英特尔 Core i7-8565U @ 1.9GHz 八核                   |
| 内存     | 16 GB ( 海力士 DDR4 2666MHz )                           |
| 硬盘     | 海力士 (256 GB / NVME固态硬盘 )                       |
| 显卡     | 英特尔 UHD Graphics 620 (platform-id:0x3E9B0000)       |
| 显示器   | LG  1920x1080 (14 英寸)                      |
| 声卡     | ALC269 (layout-id:11)                                 |
| 网卡     | intel 9560AC CNVi                     |

### 安装镜像

**将镜像中efi替换为本仓库的EFI文件夹**
直接使用黑果小兵博客中的镜像进行安装：[【黑果小兵】macOS Mojave 10.14.3 18D42 正式版 with Clover 4859原版镜像](https://blog.daliansky.net/macOS-Mojave-10.14.3-18D42-official-version-with-Clover-4859-original-image.html)

### CLOVER

* 支持Mojave
* CPU原生支持，变频正常(最低800Mhz) 调整性能教程在后方
* 显卡仿冒UHD630，采用`Lilu+WhateverGreen`通过`Clover/device/Properties`方式注入
* 声卡为ALC236，使用 `AppleALC` ，layout-id:11，通过`Clover/device/Properties`方式注入
* 显示器亮度调节正常(重启可保存) 
* USB请自行采用`Hackintool`定制（教程在后方）
* 其它 `ACPI` 补丁修复采用 `hotpatch` 方式，文件位于 `/CLOVER/ACPI/patched`
* 电池hotpatch补丁显示电池状态正常
* 触摸板暂时为单双指
* 独显mx130 无法驱动 hdmi输出 dp未测试

### 定制 usb

[定制usb教程](https://blog.daliansky.net/Intel-FB-Patcher-tutorial-and-insertion-pose.html)

### 调整macOS CPU性能

[使用方法](https://github.com/daliansky/XiaoMi-Pro/blob/master/one-key-cpufriend/README_CN.md)

``` bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/daliansky/XiaoMi-Pro/master/one-key-cpufriend/one-key-cpufriend_cn.sh)"
```

### HIDPI

[开启方法](https://github.com/xzhih/one-key-hidpi)

``` bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"
```

 **感谢 @[冰水加劲Q](https://github.com/xzhih)**

### 内置网卡无解
