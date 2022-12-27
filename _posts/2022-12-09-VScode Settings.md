---
layout: post
title: VScode Settings
toc: true
date: 2022-12-15
tags: [VScode, tool]
---

居家办公装VScode出现了问题...备注下VScode设置。

#### SSH
+ SSH config
`ctrl` + `shift` + `p`:
`Remote-SSH: Settings`, 设置config绝对路径;
`Remote-SSH: Open Configuration File`, 修改config文件内容

+ 设置从登录节点跳转至计算节点
```
Host <跳转节点，名字任意>
  HostName <登录节点IP Address>
  User <User Account>

Host <目的节点，名字任意>
  HostName <计算节点IP Address>
  User <User Account>
  ProxyCommand ssh -W %h:%p <跳转节点，名字任意>
```

#### Troubleshooting
+ vscode卡在Setting up SSH Host XX:Copying VS Code Server to host with scp
原因：下载vscode-servlet文件包失败
解决：
1. 手动下载：`https://update.code.visualstudio.com/commit:${commit_id}`/server-linux-x64/stable`

这里的`commit_id`对应远程server的目录`home/.vscode-server/bin/${commot_id}`

2. 将下载后的压缩包解压缩至对应`commit_id`目录下 `tar -zxf`
3. 重启VScode


