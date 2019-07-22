---
layout: post
title: Vue 项目配置多页面入口
img: post-1.jpg
date: 2019-07-22
tag: 技术
category:  技术

---
Vue 项目配置多入口



在Src目录下新建pages文件夹，入口页面都放在里面



![1563776718541](https://app.yinxiang.com/shard/s61/res/44a8c044-3fca-451b-a34f-7d60d80ae634/1563776718541.png)

添加入口路径

首先修改 build / utils.js文件

在底部插入以下代码

```
　　　//多页面输出配置
　　　// 与上面的多页面入口配置相同，读取pages文件夹下的对应的html后缀文件，然后放入数组中
exports.htmlPlugin = function() {
　let entryHtml = glob.sync(PAGE_PATH + '/*/*.html')
　let arr = []
　entryHtml.forEach((filePath) => {
　let filename = filePath.substring(filePath.lastIndexOf('\/') + 1, filePath.lastIndexOf('.'))
　let conf = {
　　　　// 模板来源
　	template: filePath,
　　　　// 文件名称
　	filename: filename + '.html',
　　　　// 页面模板需要加对应的js脚本，如果不加这行则每个页面都会引入所有的js脚本
　	chunks: ['manifest', 'vendor', filename],
　	inject: true
　}
　　if (process.env.NODE_ENV === 'production') {
　　　conf = merge(conf, {
　　　	minify: {
　　　	removeComments: true,
　　　	collapseWhitespace: true,
　　　	removeAttributeQuotes: true
　　　},
　　　	chunksSortMode: 'dependency'
　　　})
　　}
　　arr.push(new HtmlWebpackPlugin(conf))
　　})
　　return arr
}
```

然后修改 build / webpack.base.conf.js 文件

entry 修改为

```
 entry:utils.entries,
```

![1563777277234](https://app.yinxiang.com/shard/s61/res/966715fb-5ee4-4673-8a58-50e279859c29/1563777277234.png)



这样以后只要直接在pages里新建入口文件，就会自动遍历读取，不用再次修改配置文件



修改 build / webpack.dev.conf.js 文件

添加对应代码，例如我的pages下有 admin 和 login 两个入口

![1563777540526](https://app.yinxiang.com/shard/s61/res/3af72038-8880-43ee-8757-5fb262a27a8f/1563777537126.png)

有多少个入口就添加多少项



然后再修改 build / webpack.prod.conf.js 文件

![1563777763174](https://app.yinxiang.com/shard/s61/res/5fa02d5a-c1e6-4f60-addb-e14a3da9ee36/1563777763174.png)

至此。。多个入口配置已经完成 。





