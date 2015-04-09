title: "利用 hexo 搭建博客"
date: 2015-04-08 17:01:35
tags:
---

## 搭建教程
参考了[Hexo Document](http://hexo.io/docs/) 和 [Hexo在github上构建免费的Web应用](http://blog.fens.me/hexo-blog-github/)


## 遇到的问题
利用 'hexo deploy' 到 github 项目 'https://github.com/Shany100/hexo-blog.git' 中会出现 'error: RPC failed; result=56, HTTP code = 200'的问题。然后根据网上提供的方案，在 /.git/config 文件中添加了以下字符段：
``` bash
[http]
	postBuffer = 524288000
```
也没用达到预期的效果。还是报了问题。

## 解决了
把 github 项目由 https 改成了 'git@github.com:Shany100/hexo-blog.git'，提交后是成功的。
- hexo 的版本是
<pre>
D:\dcloud\workspace\blog>hexo version
hexo: 3.0.1
os: Windows_NT 6.1.7601 win32 x64
http_parser: 1.0
node: 0.10.32
v8: 3.14.5.9
ares: 1.9.0-DEV
uv: 0.10.28
zlib: 1.2.3
modules: 11
openssl: 1.0.1i
</pre>

## 注意
添加多说评论时，在本地环境如果是localhost的 需要注意发布到线上时分享出去的路径。"Thread Key" 唯一性。
