<h1 align="center"> 西电腾创俱乐部Website </h1>
<p align="center">
	<img src="/.github/logo.png" width="200px"/>
</p>

<p align="center">
	<a href="https://github.com/WhiteRobe/xdtic-web/blob/master/LICENSE"><img src="https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000"/></a>
	<img src="https://img.shields.io/github/repo-size/WhiteRobe/xdtic-web.svg"/>
	<img src="https://img.shields.io/github/last-commit/WhiteRobe/xdtic-web.svg"/>
	<a href="http://hits.dwyl.io/WhiteRobe/xdtic-web"><img src="http://hits.dwyl.io/WhiteRobe/xdtic-web.svg"/></a>
</p>
<p align="center">
	<img src="https://img.shields.io/badge/Node.js-10-green.svg?logo=node.js&style=flat-square"/>
	<img src="https://img.shields.io/badge/Vue-2-green.svg?logo=vue.js&style=flat-square"/>
	<img src="https://img.shields.io/badge/Redis-5.0-red.svg?logo=redis&style=flat-square"/>
	<img src="https://img.shields.io/badge/Babel-v7-yellow.svg?logo=babel&style=flat-square"/>
	<img src="https://img.shields.io/badge/koa-2.7-black.svg"/>
	<img src="https://img.shields.io/badge/javascript-ES6-blue.svg"/>
</p>

## 介绍 Introduction

“xdtic-web/西电腾创俱乐部Website”是基于Vue和Node.js的俱乐部官网开发项目。

## 配置及文档 Configure & Document

- 网站后台架构迁移自[hypethron/院庭](https://github.com/WhiteRobe/hypethron)，因此开发文档和具体配置请参考该仓库。

> 唯一不同的是，本站点采用Vue开发，而不是React。

## 快速上手 Quick-Start

1. 基础环境 Runtime

>**(Windows)** 执行 /InitEnvironment(windows).bat 脚本，从淘宝镜像源拉取项目依赖，并完成相应配置文件的创建。

>**(Linux)** 执行 /InitEnvironment(linux).sh 脚本，从淘宝镜像源拉取项目依赖，并完成相应配置文件的创建。

2. 安装Vue脚手架

```
npm install -g @vue/cli
```

3. 编译SPA项目并启动服务器

```
npm run build-start
```
