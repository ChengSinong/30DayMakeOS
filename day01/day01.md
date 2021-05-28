### 安装虚拟环境

由于是在Windows10环境下，希望制作操作系统的环境是Linux环境，因此在Windows10下安装WSL2，并且在其中安装Ubuntu系统，因为CentOS不稳定，且有bug。

#### 1. 安装WSL

以管理员身份运行power shell，并键入以下命令：

``` bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

```bash
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

#### 2. 安装Ubuntu
双击someApp中的Ubuntu_xxx.appx文件，执行安装Ubuntu。安装完成后启动，设置用户及密码。

#### 4. 设置WSL2

在power shell中键入：

```bash
wsl --set-default-version 2
```

可以下载cmder作为界面使用。

### 操作系统内存分布图

![memoryMap](memoryMap.png)


git branch -m main 30dMakeOS

git fetch origin

git branch -u origin/30dMakeOS 30dMakeOS

git remote set-head origin -a