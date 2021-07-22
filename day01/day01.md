<!--
 * @Author: chengsn
 * @Date: 2021-05-28 16:54:30
 * @LastEditTime: 2021-07-22 16:48:24
 * @LastEditors: chengsn
 * @Description: This is  just a test for C language.
 * @FilePath: \day01\day01.md
 * 可以输入预定的版权声明、个性签名、空行等
-->

## 30 天自制操作系统笔记--Day01

### 安装虚拟环境

由于是在 Windows10 环境下，希望制作操作系统的环境是 Linux 环境，因此在 Windows10 下安装 WSL2，并且在其中安装 Ubuntu 系统，因为 CentOS 不稳定，且有 bug。

#### 1. 安装 WSL

以管理员身份运行 power shell，并键入以下命令：

```bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

```bash
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

#### 2. 安装 Ubuntu

下载<https://aka.ms/wsl-ubuntu-1804>，安装完成后启动，设置用户及密码。

#### 4. 设置 WSL2

在 power shell 中键入：

```bash
wsl --set-default-version 2
```

可以下载 cmder 作为界面使用。

### 操作系统内存分布图

![memoryMap](memoryMap.png)
从上图可以看出，操作系统的启动区起点是从 0x07C00 开始的，从而在写操作系统时，使用语句

```bash
ORG 0x7c00
```

作为开头。这是告诉操作系统，从这个地址开始将程序装载到内存中的这个地址。
暂时先记录这些，抽时间慢慢学习并做好笔记。写一个操作系统出来。

鉴于 Windows 的 WSL2 图形界面比较捞，最近整了个树莓派，于是在树莓派上安装了 Manjaro 系统，有一说一，这个系统的图形化处理确实非常不错。于是在做了一些配置之后，手动从源码安装了 qemu-6.0.0.
