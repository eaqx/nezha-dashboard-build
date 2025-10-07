![](https://github.com/nezhahq/nezha/raw/master/.github/brand.svg)

![](https://img.shields.io/badge/OS-FreeBSD-blue)
![](https://img.shields.io/github/release/eaqx/nezha-dashboard-build)

## 来源

哪吒监控官方未提供 FreeBSD 的二进制安装包，交叉编译会缺少 FreeBSD C 头文件。
这里基于 GitHub 工作流来构建 FreeBSD 虚拟机进行编译。

源代码仓库地址：

[nezhahq/nezha](https://github.com/nezhahq/nezha)

编译脚本参考自：

[nezhahq/nezha](https://github.com/nezhahq/nezha)

[vfhky/nezha-build](https://github.com/vfhky/nezha-build)

## 工作方式

本编译脚本将工作分为两步完成：

1.使用 GitHub 工作流的 ubuntu 完成源码的生成文档等非编译工作并上传完成准备工作的源码到 Releases.

2.使用 [vmactions/freebsd-vm](https://github.com/vmactions/freebsd-vm) 虚拟机下载第一步准备的源码进行编译并发布 Releases.
