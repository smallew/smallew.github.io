---
title: hexo 初体验
date: 2018-05-12 14:27:31
tags: hexo
categories: 教程

---
**一些必要的工具**
 - Git
 - node.js
 - 使用的主题：https://github.com/viosey/hexo-theme-material
 
**一.大概流程**
 1. 创建仓库，smallew.github.io；
 2. 创建两个分支：master 与 hexo；
 3. 设置hexo为默认分支（因为我们只需要手动管理这个分支上的Hexo网站文件）；
 4. 使用git clone git@github.com:smallew/smallew.github.io.git拷贝仓库；
 5. 在本地smallew.github.io文件夹下通过Git bash依次执行npm install hexo、hexo init、npm
    install 和 npm install hexo-deployer-git（此时当前分支应显示为hexo）;
 6. 修改_config.yml中的deploy参数，分支应为master；
 7. 依次执行git add .、git commit -m “…”、git push origin hexo提交网站相关的文件；
 8. 执行hexo generate -d生成网站并部署到GitHub上。

**二.那些坑**
 1. 对git不熟悉走了很多弯路，例如在master像提交到hexo分支一直不成功，用下面的命令 git checkout hexo #切换到hexo

**三.参考链接**
http://crazymilk.github.io/2015/12/28/GitHub-Pages-Hexo%E6%90%AD%E5%BB%BA%E5%8D%9A%E5%AE%A2/#more （很详细说了怎么优化部署）
https://blog.csdn.net/wuseyukui/article/details/68059953 （说了一些坑）
http://www.ruanyifeng.com/blog/2014/06/git_remote.html （git一些常规操作）
https://www.zybuluo.com/mdeditor# （markdown）