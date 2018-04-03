# travis-ci 
travis ci持续集成服务，用来构建及测试在GitHub托管的代码，[官方文档](https://docs.travis-ci.com/)。
该项目演示一个简单的持续集成案例，总结在开发过程中踩过的坑以及个人心得。

[![Build Status](https://travis-ci.org/hsxyhao/travis-ci.svg?branch=master)](https://travis-ci.org/hsxyhao/travis-ci)

步骤
> 1. 登录travis ci，同步GitHub仓库
> 2. linux服务器安装travis客户端
> 3. 在服务器上git pull自己的项目，然后travis login
> 4. 编写travis脚本

坑：
> 1. ssh登录执行脚本的出现Command not found问题，可以参考该[博客](https://blog.csdn.net/whitehack/article/details/51705889),内容比较多也比较复杂
   ，我是在脚本文件的第一行修改为：#!/bin/bash --login
> 2. 安装travis客户端时，需要还需要安装其依赖环境
> 3. 在使用travis客户端登录完项目之后，一定要将解码文件id_rsa.enc上传至github上，travis ci使用ssh免密登录时要使用

详细过程都是参考几篇博客的

参考链接：
1. [Travis CI 系列：自动化部署博客](https://segmentfault.com/a/1190000011218410)
2. [利用travis-ci持续部署nodejs应用](https://cnodejs.org/topic/5885f19c171f3bc843f6017e)
3. [ssh连接远程主机执行脚本的环境变量问题](https://blog.csdn.net/whitehack/article/details/51705889)