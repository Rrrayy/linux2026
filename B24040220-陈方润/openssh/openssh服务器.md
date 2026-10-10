# OpenSSH 服务器连接与操作验证

学号：B24040220；姓名：陈方润。

环境：Windows 本地 VS Code，远程连接 VMware 中的 Ubuntu 虚拟机。

## 一、SSH 远程连接

使用 VS Code 的 Remote SSH 插件连接虚拟机，连接名称为 `ubuntu`，登录用户为 `rr`。界面显示“已连接”和 `SSH: ubuntu`，说明 SSH 远程连接成功。

本次使用 VS Code 作为 SSH 客户端，通过虚拟机端的 SSH 服务执行远程命令。

![VS Code SSH 连接成功](屏幕截图%202026-10-10%20165450.png)

## 二、远程命令验证

在虚拟机终端中执行：

```bash
ifconfig # 查看网络信息
pwd # 查看当前目录
ls # 查看当前目录内容
mkdir njupt # 创建 njupt 目录
cd njupt # 进入该目录
touch hello.txt # 创建文本文件
ls # 确认文件已创建
echo "I love njupt" > hello.txt # 写入文本内容
cat hello.txt # 查看文件内容
```

结果：网卡 `ens33` 的 IPv4 地址为 `192.168.206.130`，初始目录为 `/home/rr`。成功创建 `/home/rr/njupt/hello.txt`，读取结果为 `I love njupt`。

![远程终端命令执行结果](屏幕截图%202026-10-10%20165621.png)

## 三、实验结果

通过 VS Code Remote SSH 成功连接 Ubuntu 虚拟机，并完成网络信息查看、目录和文件创建、文本写入与读取验证。
