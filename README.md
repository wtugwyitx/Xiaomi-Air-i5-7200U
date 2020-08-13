# 小米笔记本Air 13.3 7代黑苹果配置

支持的设备型号：i5-7200U，BIOS版本为`XMAKB3M0P0504`。理论上其他BIOS版本如0304、0705也可兼容。

支持的版本：

* macOS Catalina 10.15.x

* macOS Big Sur 11.0 Beta

# 快速上手指南

本项目已全面转向OpenCore，目前支持到macOS Big Sur。Clover版本只支持到10.15.4且不再更新。个人维护能力有限，如果你有能力更新Clover相关配置，请直接提交Pull Request！

如何使用：

将本项目中EFI_OC文件夹内的两个文件夹复制到系统硬盘的ESP分区中的EFI目录下，并使用bootice工具将BOOTx64.efi添加到系统启动项。请自行使用macserial工具生成可用序列号（System UUID、MLB、Serial Number）然后填写到`OC/config.plist`文件中的对应位置（文件中搜索MLB即可找到）。

issue页面可查看更多说明，包括：

* 解锁CFG锁

* 调整BIOS的DVMT大小

* 开启HiDPI

* 如何支持Apple Music

# 同机型讨论群

* 533801737

# 捐赠

EFI更新不易，给作者加个🍗

| Wechat| Alipay | PayPal |
| - | - | - |
| ![wechat](img/wechat.png) | ![alipay](img/alipay.png) | [![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=XY2PW7DUBTWXE&source=url) |

# LICENSE

BSD

**使用本项目文件风险和后果自负**
