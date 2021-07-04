---
title: Github搭建Hexo博客
date: 2021-07-04 21:57:42
tags:
---
## 一、环境准备：
* Node.js安装
* Git安装
* Github帐号注册

## 二、部署步骤：
### 1 在Github上新建名为**.github.io的github同名公开仓库
### 2 本地安装Hexo
`npm install -g hexo-cli`
### 3 本地创建Hexo项目
`hexo init blog   （blog是文件夹名称，可自定义命名）`
### 4 项目安装部署插件,在本地项目目录下执行以下命令
`npm install hexo-deployer-git --save`
### 5 在项目文件_config.yml末尾补充部署配置
```bash
deploy:
  type: git
  repo: https://github.com/LinWenLi95/LinWenLi95.github.io.git
  branch: master
注意：repo为步骤1创建的同名仓库代码地址
```
### 6 部署（根据提示输入github用户名和密码）
```bash
hexo clean && hexo g && hexo d
```
### 7 浏览器访问网址https://**.github.io,博客搭建结束
### 8 另外还需要知道Hexo的几个常用命令
1-7步骤可快速搭建一个能通过Github访问的博客，以下是Hexo常用命令说明
```bash
npm install hexo -g # 安装Hexo
npm update hexo -g # 升级Hexo

npm install hexo-deployer-git --save # 安装部署插件

hexo init <自定义博客名> # 初始化博客

hexo new "我的博客" # 新建文章 简写：hexo n "我的博客"

hexo generate # 生成静态网页代码 简写：hexo g

hexo deploy # 部署 简写：hexo d

hexo server # 启动服务预览 简写：hexo s
hexo server -s # 静态模式
hexo server -p 5000 # 更改端口（默认4000）
hexo server -i 192.168.1.1 # 自定义 IP

hexo clean # 清除缓存，若是网页正常情况下可以忽略这条命令
```
### 9 主题设置（待补充。。。）
参考：https://zhuanlan.zhihu.com/p/26625249
