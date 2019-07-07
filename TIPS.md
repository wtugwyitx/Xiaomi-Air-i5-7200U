# 安装

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