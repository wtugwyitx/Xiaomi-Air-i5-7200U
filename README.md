# 小米笔记本Air 13.3 7代黑苹果配置

支持的版本：

* macOS Mojave 10.14.5
* macOS Catalina 10.15 Beta (19A501i)

## 配置

* 处理器：Intel Core i5-7200U

* 内存：8GB Samsung DDR4 2133MHz

* 硬盘：Samsung NVMe SSD Controller PM961 256GB

* 集成显卡：Intel Graphics HD620

* 声卡：Realtek ALC255 with layout-id 30

* 无线网卡：Intel Wireless AC8265

## 不支持的组件

* nVidia MX150

* 指纹传感器

* Intel无线和蓝牙

* 10.15中不支持亮度控制

## TODO

* 修复10.15的亮度控制

* 更新VoodooI2C(https://github.com/alexandred/VoodooI2C/issues/132)

## 更新记录

2019-07-07:

* 更新Clover到4979
* 更新 Lilu/WhateverGreen/AppleALC/VirtualSMC/NoTouchID 
* 支持Catalina
* 增加RtWlanU驱动
* 移除导致Catalina内核崩溃的`SSDT-PNLF.aml`。同时导致亮度控制不可用

## Credits

- [Acidanthera](https://github.com/acidanthera) for providing [AppleALC](https://github.com/acidanthera/AppleALC), [Lilu](https://github.com/acidanthera/Lilu), [O[VirtualSMC](https://github.com/acidanthera/VirtualSMC), [VoodooPS2](https://github.com/acidanthera/VoodooPS2), and [WhateverGreen](https://github.com/acidanthera/WhateverGreen).
- [alexandred](https://github.com/alexandred) for providing [VoodooI2C](https://github.com/alexandred/VoodooI2C).
- [apianti](https://sourceforge.net/u/apianti), [blackosx](https://sourceforge.net/u/blackosx), [blusseau](https://sourceforge.net/u/blusseau), [dmazar](https://sourceforge.net/u/dmazar), and [slice2009](https://sourceforge.net/u/slice2009) for providing [Clover](https://sourceforge.net/projects/cloverefiboot).
- [RehabMan](https://github.com/RehabMan) for providing [EAPD-Codec-Commander](https://github.com/RehabMan/EAPD-Codec-Commander),  [OS-X-Clover-Laptop-Config](https://github.com/RehabMan/OS-X-Clover-Laptop-Config), [OS-X-Null-Ethernet](https://github.com/RehabMan/OS-X-Null-Ethernet), and [SATA-unsupported](https://github.com/RehabMan/hack-tools/tree/master/kexts/SATA-unsupported.kext).

# Donation

If this project help you reduce time to hackintosh, you can give me a cup of coffee :)

| Wechat| Alipay | PayPal |
| - | - | - |
| ![wechat](img/wechat.png) | ![alipay](img/alipay.png) | [![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=XY2PW7DUBTWXE&source=url) |


