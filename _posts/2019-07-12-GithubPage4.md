---
layout: post
title: （测试）使用Github Page 搭建简易博客
img: post-1.jpg
date: 2019-07-11
tag: 测试

---
## **1.注册属于你自己的Github账号**
### [https://github.com/](https://github.com/)

 

## **2.创建仓库**
登录后点击右上方头像左侧的加号，在弹出框中选择“New repository”；

创建仓库页面如下：

![图片](https://app.yinxiang.com/shard/s61/res/52e01130-3d32-4e77-8221-a4e5a22db9b9/6666666.jpeg ''图片title'')
![图片](https://app.yinxiang.com/shard/s61/res/c525d49c-687c-45bf-8fe4-19f6ebd40e41/1250458-20171017153553099-864426472.png ''图片title'')

## **3.开启Github Pages**

点击仓库上方的Settings进入仓库设置。

![图片](https://app.yinxiang.com/shard/s61/res/7dea2b86-ab46-4720-ae26-8fb33c614d29/33333333.png ''图片title'')
![图片](https://app.yinxiang.com/shard/s61/res/dfdb3d9a-38e5-427d-9237-4eea1184c56b/2222222.png ''图片title'')

## **4.下载GitHub桌面版并安装**
### [https://windows.github.com/](https://windows.github.com/)

首先你需要登录桌面版，然后依次点击点击File - Clone Repository。

在Filter框中填写刚刚你设置的地址（你的用户名.github.io）


![图片](https://app.yinxiang.com/shard/s61/res/b8760a10-0311-4ffb-96dc-e6740e073e27.jpg ''图片title'')

Clone之后就会在文稿中生成一个GitHub文件夹，文件夹的名字就是你的用户名.github.io。

## **5.选择主题并配置**

在下面网站中选择一个你喜欢的主题，下载下来。


### [http://jekyllthemes.org/](http://jekyllthemes.org/)

打开刚刚生成的GitHub文件夹，把里面除.git（这个文件夹是个隐藏文件夹）的文件都删掉，然后把你下载好的主题Copy到GitHub文件夹中。

## **6.写博文**
如果你下载的主题中含有_posts文件夹，那么把你写的文章（注意要用Markdown写）放在该文件夹内；如果没有该文件夹，那就在GitHub文件夹根目录下创建一个。
然后按下面步骤操作。

![图片](https://app.yinxiang.com/shard/s61/res/6334e96d-62c9-4bc8-a2e3-a34ec297a383.jpg ''图片title'')

## **7.搭建运行本地环境**
- 安装Ruby 
  https://rubyinstaller.org/downloads/

- 安装 Bundler 

  > gem install bundler

- 安装 Jekyll

    在 GitHub Pages 目录新建文件`Gemfile`，内容如下：

  > ```
  >   source 'https://rubygems.org'
  >      gem 'github-pages', group: :jekyll_plugins
  > ```

    执行

  > ```
  > bundler install
  > ```

- 运行 Jekyll

  > ```
  > bundle exec jekyll serve
  > ```



Server address: http://127.0.0.1:4000/



