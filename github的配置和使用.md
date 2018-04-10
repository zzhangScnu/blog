---
date: 2018-04-09 22:43
status: public
title: github的配置和使用
---

##安装
先在电脑中安装git。到官网下载双击安装。
##设置
GitBash提供了linux的仿真环境，可以在Windows中使用linux命令。设置内容会被写入~/.gitconfig文件中保存。~表示/c/Users/Administrator，相当于linux中的用户根目录。
###设置姓名
<pre><code>git config --global user.name "name"</code></pre>
###设置邮箱
<pre><code>git config --global user.email "mail"</code></pre>
###设置SSH
1. 设置后免去每次push都要输入密码。
   该命令将生成邮箱地址的公钥存放在*id_rsa.pub*中，生成私钥存放在*id_rsa*中。
   <pre><code>ssh-keygen -t rsa -C "email"</code></pre>
2. 将公钥添加到github中个人账号setting里的key域。   
3. 该命令将本机与github进行认证。
 <pre><code>ssh -T git@github.com</code></pre>


###使用
1. 创建仓库。在github网站上创建，也可以设置分支等。
2. 将仓库同步到本地
   <pre><code>git clone 地址</code></pre>
3. 初始化仓库
  <pre><code>git init</code></pre>
4.  日常使用相关指令
    <pre><code> git status  //查看仓库状态
     git add * 或 git add 文件 //将本地文件提交到git缓存区
     git commit -m "message" //添加注释语句
     git push //将git缓存区中的文件提交到git服务器
     git log //查看提交日志
    </code></pre>
