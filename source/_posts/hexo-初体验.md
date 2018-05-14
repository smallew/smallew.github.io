---
title: hexo 初体验
date: 2018-05-12 14:27:31
tags: hexo
categories: 教程
---
## 一些必要的工具
 - Git Bash
 - node.js
 - 使用的主题：https://github.com/viosey/hexo-theme-material
 
## 博客管理流程
### 日常修改
在本地对博客进行修改（添加新博文、修改样式等等）后，通过下面的流程进行管理：
- 在有道写markdown文件，然后copy到hexo\source\_posts 下
- 依次执行 git add . | git commit -m "…" | git push origin hexo指令将改动推送到GitHub（此时当前分支应为hexo）；
然后才执行hexo g -d发布网站到master分支上。
- 本地可以用hexo g -s 启动
- localhost:4000/admin #使用了hexo-admin-qiniu 插件，可以通过这个链接管理文章
- 需要上传图片需要先上传到图床 https://portal.qiniu.com/bucket/hexo-admin/resource
---

### 本地资料丢失
当重装电脑之后，或者想在其他电脑上修改博客，可以使用下列步骤：

1. 使用git clone git@github.com:smallew/smallew.github.io.git拷贝仓库（默认分支为hexo）；
smallew.github.io文件夹下通过Git bash依次执行下列指令：npm install hexo、npm install、npm install hexo-deployer-git（记得，不需要hexo init这条指令）。
1. 主题配置文件\_config.yml 没有提交到github,需要手动从笔记copy到 smallew.github.io\themes\material


---

## 参考链接
http://crazymilk.github.io/2015/12/28/GitHub-Pages-Hexo%E6%90%AD%E5%BB%BA%E5%8D%9A%E5%AE%A2/#more （很详细说了安装过程，初次安装可以参考）
https://blog.csdn.net/wuseyukui/article/details/68059953 （说了一些坑，七牛图床的使用）
http://www.ruanyifeng.com/blog/2014/06/git_remote.html （git一些常规操作）