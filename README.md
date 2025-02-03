<div align="center">
<img width="768" src="https://github.com/ranqingwen/Lede25-autobuild/blob/main/personal/logo.png"/>
<h1>OpenWrt_Build_x64</h1>
</div>

## 当前编译状态：
| 源码+版本 | 固件编译状态 | 脚本文件 | 固件下载 |
| :-------------: | :-------------: | :-------------: | :-------------: |
| [![](https://img.shields.io/badge/Lede-6.6-32C955.svg?logo=openwrt)](https://github.com/ranqingwen/Lede25-autobuild/blob/main/.github/workflows/OpenWrt_2305_x64.yml) | <a href="https://github.com/ranqingwen/Lede25-autobuild/blob/main/.github/workflows/OpenWrt_2305_x64.yml"><img src="https://github.com/ranqingwen/Lede25-autobuild/blob/main/.github/workflows/OpenWrt_2305_x64.yml/badge.svg?style=flat" /></a> | [![](https://img.shields.io/badge/脚本-配置-orange.svg?logo=apache-spark)](https://github.com/ranqingwen/Lede25-autobuild/tree/main/diy_script/lede_diy/x86) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/ranqingwen/Lede25-autobuild/releases) |


</br>

## 项目说明 [![](https://github.com/gxnas/OpenWrt_Build_x64/blob/main/personal/describes.svg)](#项目说明-)
- 固件编译使用的源代码来自：[![Lean](https://img.shields.io/badge/Lede-Lean-red.svg?style=flat&logo=appveyor)](https://github.com/coolsnowwolf/lede) 
- 项目使用 Github Actions 拉取 [Lean](https://github.com/coolsnowwolf/lede) 的 `Openwrt-23.05（内核版本6.6）` 源码仓库进行云编译
-  本库编译的x86固件为squashfs格式；
-  ext4 与squashfs 格式的区别： ext4 格式的rootfs 可以扩展磁盘空间大小，而squashfs 不能。 squashfs 格式的rootfs 可以使用重置功能（恢复出厂设置），而ext4 不能；
-  默认的固件容量：Kernel=32M、rootfs=968M，请确保安装OpenWrt的硬盘空间至少要有1G以上；
-  OpenWrt升级方法：下载好对应版本的.img.gz文件到电脑上，不需要解压，然后在你的OpenWrt菜单“系统-备份/升级”直接选择下载好的.img.gz文件上传，刷写固件；
- 🛑******最好不要跨大版本升级（比如1806升级到2305，或者6.1内核升级6.6），大版本更新建议采用全新安装方可获得最佳的体验。******

#### 使用说明：

- 🛑1、文件名带有efi字样的固件支持Uefi和Legacy两种引导方式启动，文件名不含efi的固件仅支持Legacy传统引导方式启动，请根据实际需要下载；

- 🛑 2、默认的IP地址：192.168.23.250；

- 🛑 3、默认用户名：root，无密码；

#### 4、如需要更改Openwrt默认的IP，可以用root登录SSH下输入命令 vi /etc/config/network 修改文件，需要注意的是，在SSH界面下看到有root@OpenWrt:/#开头的字样方可操作；

#### 6、安装硬盘不可低于1G；

#### 7、虚拟机安装的，请确保文件名和路径没有中文或者特殊符号，否则转换文件时有可能转换不成功。

<a href="#readme">
<img src="https://github.com/ranqingwen/Lede25-autobuild/blob/main/personal/return.svg" title="返回顶部" align="right"/>
</a>

----
- REPO_TOKEN密匙制作教程：https://git.io/jm.md
- 云编译需要 [在此](https://github.com/settings/tokens) 创建个```token```,勾选：```repo```, ```workflow```，保存所得的key
- 然后在此仓库```Settings```->```Secrets```中添加个名字为```GH_TOKEN```的Secret,填入token获得的key

- Telegram通知```Settings```->```Secrets```中添加名字为```TELEGRAM_TO```和```TELEGRAM_TOKEN```，值分别为BOT_USER _ID和BOT_TOKEN
- 企业微信机器人通知```Settings```->```Secrets```中添加个名字为```WEBHOOK_SEND_KEY```，值为企业微信机器人https://qyapi.weixin.qq.com/cgi-bin/webhook/send?key=后面的值
----
