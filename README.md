有些零散的笔记并不适合塞在博客里，在我的预想中博客应该是更加具有技术性的文章，着重于原创包含着自己的解决思路。
但是有些从别的地方摘抄过来的解决方案或者有价值的代码段应该放到哪里呢？搭建一个个人维基或者个人笔记是一个好点子。

#### 原因

选择 docsify 来搭建个人笔记管理有以下几个原因:

- 使用运行时渲染

	这样直接存放一个 index.html + 一堆 md 在仓库即可，多平台也不需要安装其他的工具去 build，python 开一个
httpserver 就可以预览。同时我这是发布在 github pages 上的，其他人发现了错误可以很方便 pr（虽然估计没人看）

- 拥有足够的 API 

	实际上我只需要代码高亮和基本的 md 渲染这两个功能，后者包括扩充的 mermaid 和 latex 渲染，这两点 docsify 都支持。
利用 prim 可以轻松渲染我喜欢的 onedark 配色，虽然又需要引入 js（知道不好，但一把梭属实香）

- 支持中文搜索

	这是很重要的一个功能，毕竟我只打算写一份中文版本的笔记


#### 最后

**如果有看到的朋友发现错误，欢迎 pr 帮我改正！**

或者直接联系我:

Email: [Gmail](mailto:ownbyzjuyk@gmail.com) | [Edu](mailto:zjuyk@zju.edu.cn)

Telegram: [@zjuyk](https://t.me/zjuyk)

GPG: [F84D36A73BF39DC8](https://github.com/zjuyk.gpg)
