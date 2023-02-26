---
title: "使用ensp过程中出现的问题及解决方法"
date: 2023-02-26
draft: false
tags: 
---
### 操作系统
|系统版本|内存|硬盘|
|---|---|---|
|win11 专业版|16 G|512 G|

### ensp出现无法激活设备的问题
根据手册指示去做，如果手册内容无法解决问题问题，就去检查自己的系统是否为windows 专业版。如果是专业版看看是否启用了“hyper-V”，如果启用了在“windows powershell 管理员模式”中使用以下命令去关闭“hyper-V”  

    使用命令：bcdedit /set hypervisorlaunchtype off
此时会导致windows系统下的wsl无法使用，如果想再次启用wsl，在“windows powershell 管理员模式”中使用以下命令去开启“hyper-V”  

    使用命令：bcdedit /set hypervisorlaunchtype auto