# 各种黑苹果提示/资料整理

个人使用中总结、搜集到的内容。欢迎补充。

## 黑苹果双系统（Mojave+Catalina）

要求你的系统盘是APFS格式。在磁盘工具中选择系统盘下的容器，然后增加一个容器供Catalina使用即可。两个系统共用一个硬盘分区的空间，不需要修改分区表

## 安装过程中反复重启

* 在Clover的启动选项增加`-v`显示调试信息

* 尝试在Clover页面注入无效的platform-id如0x12345678，每次重启前都需要注入直到可以正常进入系统

## OneKeyHidpi不起作用

原因是从10.15开始，`/System`目录变成只读，导致该脚本无法修改系统文件。参考`https://github.com/xzhih/one-key-hidpi/issues/57`：

在终端执行如下命令：

```sh
sudo mount -uw /
killall Finder
```

然后再执行one-key-hidpi脚本

## 关于macOS 10.15 beta

使用中出现的bug：

* Clion、PyCharm等崩溃。使用EAP版本可以解决

* Chrome启动慢

* 接入HDMI显示器后息屏状态下WindowServer占用CPU严重

* 新安装的程序不会出现在启动台。并不是bug，而是在10.15启动台的策略更改了，只有通过Mac App Store安装的app才会自动显示。手动安装的app需要在Finder的应用程序页面手动拖拽图标到Dock的启动台上

* Safari有时候出现联网错误

* 安装新字体会在检查阶段卡很久。可以直接复制字体文件到`~/Library/Fonts/`目录

## USB插入iPad提示配件供电不足/耗电量太大已被停用

利用小米笔记本的Type-C充电口+任意一款支持充电的Type-C扩展坞，iPad插入扩展坞的USB口即可

## 关于原装nvme换成BCM无线网卡

购买转接板+BCM943602CS插入后并不能识别（原因未知，可能是转接板的问题），所以放弃。

* 转接板+网卡插入后，后盖可以合上，略有凸起，不影响使用

    * 主要影响厚度的原因是转接板上的转接头太高。有些转接板有引出USB通道的插座，也会增加厚度。网卡本身非常小

* 供内置网卡使用的天线拔下可以插到nvme位置并接入BCM无线网卡

* 即使无线网卡可以使用，蓝牙部分还是需要自行飞线USB通道。（理论上）可利用的USB位置：type-c充电口的USB通道、摄像头、左右USB 3.0口

    * 目测使用摄像头的USB通道最为划算，但是并不知道摄像头数据线的料号

## 资料/驱动链接

* USB3.0转千兆以太网卡驱动（AX88179）：<https://www.asix.com.tw/download.php?sub=driverdetail&PItemID=131>

* Realtek USB无线网卡驱动合集：<https://github.com/chris1111/Wireless-USB-Adapter-Clover>

* 在小米笔记本内置屏幕上开启HiDPI：<https://github.com/xzhih/one-key-hidpi>

* CCC，克隆APFS分区利器：<https://bombich.com/>
