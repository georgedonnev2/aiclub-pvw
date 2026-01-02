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


可参考官网链接（**点击下方图片可跳转**），快速了解和熟悉开发板。
[![昇腾开发板学习向导](https://www.hiascend.com/doc_center/source/zh/Atlas200IDKA2DeveloperKit/23.0.RC2/index/figure/zh-cn_image_0000002465469593.png)](https://www.hiascend.com/document/detail/zh/Atlas200IDKA2DeveloperKit/23.0.RC2/index/index.html)

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


### 通过 WSL 安装 Linux

以 WSL 安装 Linux 为例。以下步骤在 `Windows 11 专业版 24H2` 验证通过。

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

### 熟悉相关操作

以编写并运行一个 Python 程序 `hello_time.py` 为例，熟悉相关操作。

- 执行 `pwd`，确定当前目录是哪个

```bash
pwd
/home/gdv2 # 显示当前目录是 /home/gdv2
```

- 执行 `mkdir ailab`，在当前目录下创建子目录 `ailab`
```bash
mkdir ailab
```

- 执行 `cd ailab` 进入子目录，再执行 `pwd` 确认当前目录
```bash
cd ailab
pwd
/home/gdv2/ailab # 已进入子目录 ailab
```

- 执行 `vim hello_time.py` 编辑文件
```bash
vim hello_time.py
```

- 进入 `vim` 界面后，先按 `i` 键，界面左下角显示 `-- INSERT --`。把以下样例代码复制后，粘贴进去。
  
```python
import datetime

def main():
    print("=" * 40)
    print("Hello World!")
    print("=" * 40)
    
    # 获取当前时间
    now = datetime.datetime.now()
    
    # 输出不同格式的时间信息
    print(f"当前日期和时间: {now.strftime('%Y-%m-%d %H:%M:%S')}")
    print(f"当前日期: {now.strftime('%Y年%m月%d日')}")
    print(f"当前时间: {now.strftime('%H时%M分%S秒')}")
    
    # 星期几（中文）
    weekdays = ["星期一", "星期二", "星期三", "星期四", "星期五", "星期六", "星期日"]
    print(f"今天是: {weekdays[now.weekday()]}")
    
    # 时间戳
    print(f"时间戳: {int(now.timestamp())}")
    
    print("=" * 40)

if __name__ == "__main__":
    main()
```

- 粘贴完成后，按 `esc` 键，然后输入 `:wq`（会同步显示在界面左下角），再按 `回车` 键，可退出 `vim` 界面。

- 执行 `ls -l`，确保已创建文件 `hello_time.py`。
```bash
ls -l
total 4
-rw-rw-r-- 1 gdv2 gdv2 725 Dec 31 15:06 hello_time.py
```

- 执行 `python3 hello_time.py` 运行 Python 程序。
```bash
python3 hello_time.py
========================================
Hello World!
========================================
当前日期和时间: 2025-12-31 14:38:09
当前日期: 2025年12月31日
当前时间: 14时38分09秒
今天是: 星期三
时间戳: 1767163089
========================================
```

> Python 2.xx 和 Python 3.xx 差别较大，当前主要使用 Python 3.xx。执行命令时输 `python3` 而不是 `python`，是推荐的做法。

<!--  -->
## 了解 Python 编程语言

可以学习相关教程，以快速熟悉和了解 Python3。可选择合适自己的教程开展学习。此处有一个教程供参考（**点击下方图片可跳转**）
<!-- [![图片描述文字](图片URL)](链接URL) -->
[![liaoxuefeng-python3-tutorial](https://liaoxuefeng.com/books/python/introduction/cover.jpg)](https://liaoxuefeng.com/books/python/introduction/index.html)

几点提示：
- 看不大明白的章节，可以先跳过。
- 教程中的样例代码，可以尝试运行。
- 想要实现什么有意思的功能。和大模型交互，获得样例代码，然后修改后运行。

## 相关比赛

留几个题目，供同学们了解信息时参考。

- **华为ICT大赛**
  - 说说 **华为ICT大赛** 的简要情况。
  - 咱们俱乐部应该参加华为ICT大赛的那些比赛（**实践赛**、**创新赛**、……）？
  - 假定参加 **创新赛**，做什么样的作品去参赛，有可能获得奖项？
  - 需要具备什么样的 **知识和技能**，才能做出能获奖的作品？
  - 希望能在俱乐部中，获得什么形式的、哪些方面的 **训练和提升**？

<!-- [第十届华为ICT大赛创新赛学习空间](https://talent.shixizhi.huawei.com/center/privateCenter.htm?schoolId=1365189427395223554&type=studyCenter_LearningTask&sxz-lang=zh_CN&mapDetail=3&mapDetailId=1838879415425572866&freedomMapClickItemId=1838879415429767175) -->
<br>

- **昇腾AI创新大赛**
  - 说说 **昇腾AI创新大赛** 的简要情况。
  - 做什么样的作品去参赛，有可能获得奖项？

<br>

- **鲲鹏创新大赛**
  - 说说 **鲲鹏创新大赛** 的简要情况。
  - 做什么样的作品去参赛，有可能获得奖项？
  - 和 **昇腾AI创新大赛**、**华为ICT大赛** 的区别是什么？