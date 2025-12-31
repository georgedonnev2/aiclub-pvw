# 俱乐部招新2512-学习主题和内容建议

以终为始给出学习主题和内容的建议，供感兴趣同学参考。掌握程度视个人情况而定，后续可持续加强。参考给出的建议，至少要达到了解的程度。

最终目标：做出一款作品，在华为ICT大赛、昇腾大赛、鲲鹏大赛中，获得尽可能优异的奖项。根据该目标，需要对以下主题和内容有所了解：

- 了解华为开发板。作品通常会基于华为开发板实现。
- 了解 Linux 操作系统。华为开发板安装了 Linux 操作系统，因此也需要了解。
- 了解 Python 编程语言。通常使用 Python 编写程序实现作品。
- 了解历届比赛获奖作品。作为参考做出自己的作品，提高获奖几率。

## 初识华为开发板

当前学院有 2 种规格的华为开发板：
- 昇腾开发板。官网名称 “Atlas 200I DK A2 开发者套件”。官网链接：[昇腾开发者套件](https://www.hiascend.com/hardware/developer-kit-a2)
- 鲲鹏开发板。官网名称 “OrangePi Kunpeng Pro”。官网链接：[鲲鹏开发板](https://www.hikunpeng.com/developer/devboard)

2 种规格的开发板都带有 AI算力。可以把开发板类比为普通台式机的主机，接上显示器、插上鼠标和键盘、接上网线（或连无线网络）、就是 1 个带有 AI算力的计算机。以下简介以 **昇腾开发板** 为例。


可参考官网链接 [学习向导](https://www.hiascend.com/document/detail/zh/Atlas200IDKA2DeveloperKit/23.0.RC2/index/index.html)，快速了解和熟悉开发板。
![昇腾开发板学习向导](https://www.hiascend.com/doc_center/source/zh/Atlas200IDKA2DeveloperKit/23.0.RC2/index/figure/zh-cn_image_0000002465469593.png)

可以点击感兴趣章节学习。推荐如下章节：
- `1.认识开发者套件` 之 `了解硬件接口、规格、软件栈`。链接：[产品简介](https://www.hiascend.com/document/detail/zh/Atlas200IDKA2DeveloperKit/23.0.RC2/pd/pd_0001.html)。
- `4.启动开发者套件` 之 `硬件连线` 和 `登录`。链接：[连接启动开发者套件](https://www.hiascend.com/document/detail/zh/Atlas200IDKA2DeveloperKit/23.0.RC2/qs/qs_0010.html)。
- `4.启动开发者套件` 之 `连接外部网络`。链接：[连接外部网络](https://www.hiascend.com/document/detail/zh/Atlas200IDKA2DeveloperKit/23.0.RC2/qs/qs_0008.html)。
- `6.运行入门样例`。链接：[体验预置应用](https://www.hiascend.com/document/detail/zh/Atlas200IDKA2DeveloperKit/23.0.RC2/Getting%20Started%20with%20Application%20Development/paqe/paqe_0001.html)。
- `7.学习典型样例代码` 之 `MindX SDK入门样例讲解（接口更简单）`。链接：[MindX SDK应用开发入门](https://www.hiascend.com/document/detail/zh/Atlas200IDKA2DeveloperKit/23.0.RC2/Getting%20Started%20with%20Application%20Development/gswmsad/gswmsad_0001.html)。
- `7.学习典型样例代码` 之 `AscendCL 入门样例讲解`。链接：[AscendCL 应用开发入门](https://www.hiascend.com/document/detail/zh/Atlas200IDKA2DeveloperKit/23.0.RC2/Getting%20Started%20with%20Application%20Development/gswaad/gswaad_0001.html)。


<!--  -->
## Linux 简介

Linux 内核最初只是由芬兰人林纳斯·托瓦兹（Linus Torvalds）在赫尔辛基大学上学时出于个人爱好而编写的。

Linux 是一套免费使用和自由传播的类 Unix 操作系统，是一个基于 POSIX 和 UNIX 的多用户、多任务、支持多线程和多 CPU 的操作系统。

Linux 能运行主要的 UNIX 工具软件、应用程序和网络协议。它支持 32 位和 64 位硬件。Linux 继承了 Unix 以网络为核心的设计思想，是一个性能稳定的多用户网络操作系统。

Linux 英文解释为 Linux is not Unix。

可以有多种方式获得一个 Linux 环境用于熟悉相关操作。比如：
- WSL（Windows Subsystem for Linux，适用于 Linux 的 Windows 子系统）
- 云上买一个装 Linux 的虚机
- ……

以下以 WSL 为例。

### 通过 WSL 安装 Linux

在 Windows 系统启动 PowerShell 终端，执行
```powershell
wsl --install
```

屏幕会显示如下类似输出：
```PowerShell
正在下载: 适用于 Linux 的 Windows 子系统 2.6.3
正在安装: 适用于 Linux 的 Windows 子系统 2.6.3
已安装 适用于 Linux 的 Windows 子系统 2.6.3。
正在安装 Windows 可选组件: VirtualMachinePlatform

部署映像服务和管理工具
版本: 10.0.26100.5074

映像版本: 10.0.26100.7462

启用一个或多个功能
[==========================100.0%==========================]
操作成功完成。
请求的操作成功。直到重新启动系统前更改将不会生效。
请求的操作成功。直到重新启动系统前更改将不会生效。
```

然后重新启动 Windows 系统。再启 PowerShell 终端，执行：
```powershell
wsl --list --online
```

屏幕会显示如下类似输出：
```powershell
以下是可安装的有效分发的列表。
使用“wsl.exe --install <Distro>”安装。

NAME                            FRIENDLY NAME
Ubuntu                          Ubuntu
Ubuntu-24.04                    Ubuntu 24.04 LTS
openSUSE-Tumbleweed             openSUSE Tumbleweed
openSUSE-Leap-16.0              openSUSE Leap 16.0
SUSE-Linux-Enterprise-15-SP7    SUSE Linux Enterprise 15 SP7
SUSE-Linux-Enterprise-16.0      SUSE Linux Enterprise 16.0
kali-linux                      Kali Linux Rolling
Debian                          Debian GNU/Linux
AlmaLinux-8                     AlmaLinux OS 8
AlmaLinux-9                     AlmaLinux OS 9
AlmaLinux-Kitten-10             AlmaLinux OS Kitten 10
AlmaLinux-10                    AlmaLinux OS 10
archlinux                       Arch Linux
FedoraLinux-43                  Fedora Linux 43
FedoraLinux-42                  Fedora Linux 42
Ubuntu-20.04                    Ubuntu 20.04 LTS
Ubuntu-22.04                    Ubuntu 22.04 LTS
OracleLinux_7_9                 Oracle Linux 7.9
OracleLinux_8_10                Oracle Linux 8.10
OracleLinux_9_5                 Oracle Linux 9.5
openSUSE-Leap-15.6              openSUSE Leap 15.6
SUSE-Linux-Enterprise-15-SP6    SUSE Linux Enterprise 15 SP6
```

Linux 有很多发行版，选择相对常见的 Ubuntu 安装。版本选择 `Ubuntu-22.04` 或者 `Ubuntu-24.04`，都是 LTS（长期支持） 。以 `Ubuntu-22.04` 为例，在 PowerShell 终端中执行：
```powershell
wsl --install -d Ubuntu-22.04
```

屏幕显示类似信息如下：
```bash
wsl: 使用旧分发注册。请考虑改用基于 tar 的分发。
正在下载: Ubuntu 22.04 LTS
Ubuntu 22.04 LTS 已下载。
已成功安装分发。可以通过 “wsl.exe -d Ubuntu 22.04 LTS” 启动它
正在启动 Ubuntu 22.04 LTS...
Installing, this may take a few minutes...
Please create a default UNIX user account. The username does not need to match your Windows username.
For more information visit: https://aka.ms/wslusers
Enter new UNIX username: gdv2
New password:
Retype new password:
passwd: password updated successfully
Installation successful!
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

Welcome to Ubuntu 22.04.5 LTS (GNU/Linux 6.6.87.2-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Wed Dec 31 11:43:28 CST 2025

  System load:  0.45                Processes:             30
  Usage of /:   0.1% of 1006.85GB   Users logged in:       0
  Memory usage: 5%                  IPv4 address for eth0: 172.31.80.183
  Swap usage:   0%


This message is shown once a day. To disable it please create the
/home/gdv2/.hushlogin file.
gdv2@gdv2-winbook:~$
```
> - 屏幕提示 `Enter new UNIX username:` 时，输入一个用户名（账号名），比如 `zhangshan`、`lisi`，等。 
> - 屏幕提示 `New password:` 时，输入密码。屏幕不会有显示，是正常的。
> - 屏幕提示 `Retype new password:` 时，再输一遍刚输入的密码。屏幕不会有显示，是正常的。

安装完成后，屏幕出现提示符 `gdv2@gdv2-winbook:~$`，表示已进入了 Linux 操作系统。
> - 提示符默认格式是：`Linux用户名@计算机名称`。如何修改 Windows 系统的计算机名称（设备名称），可自行搜索，此处从略。
> - 如果上述安装过程中输入用户名是 `lisi`，计算机名称是 `mybook`，则提示符应该是 `lisi@mybook:~$`。

下次进入 Linux 操作系统环境，可以：
- 启动 PowerShell 终端，并执行命令 `wsl`。
- 或者底部搜索栏输入 `ubuntu`，然后点击 `Ubuntu 22.04.5 LTS` 类似字样的应用。