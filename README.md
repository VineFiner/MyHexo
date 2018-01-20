# My Hexo
```
	echo "# MyHexo" >> README.md
	git init
	git add README.md
	git commit -m "first commit"
	git remote add origin https://github.com/VineFiner/MyHexo.git
	git push -u origin master

	git remote add origin https://github.com/VineFiner/MyHexo.git
	git push -u origin master
```
# 第一步
- 添加远端

 ```
	git init
```
- 添加内容

 ```
	git add README.md
```
- 添加远端

```
	git remote add origin https://github.com/VineFiner/MyHexo.git
```
- 推送远端

```
	git push -u origin master
```
# 第二步

- 安装Node.js
- 这里使用HomeBrew进行安装

```
	brew install node
```
- 安装Hexo

```
	npm install -g hexo
```
- 卸载Hexo

```
	npm uninstall -g hexo
```
## 这里我们使用GitHub进行托管

* 这里是GitHub的特性

```
	git chekcout -b gh-pages
	
```

1、创建工作目录

```
	mkdir blog
	cd blog
	hexo init
```
* 或者

```
	hexo init blog
```
2、安装依赖包

```
	npm install
```

3、预览本地博客

- 创建、预览

```
	hexo s -g
```

- 创建、预览

```
	hexo g
	hexo s
```
- 这里会有提示、我们直接在浏览器中输入网站就可以看到本地网站网页了。

- 这里的自动部署是需要我们安装git插件的。

```
	npm install hexo-deployer-git --save
	
	修改deploy
	
	type：git
	repo：git@github.com:VineFiner/MyHexo.git
	branch：gh-pages

	因为我们是本地项目、所以这里我们需要修改

	url: http://yoursite.com/MyHexo
	root: /MyHexo

```

- 一般问题处理

```
	hexo clean
	hexo d -g
```
- 这里我们需要使用SSH进行链接

```
	ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
4、或者手动推送文件到GitHub

* 这里我们推送的是生成的public文件夹里面的内容。

```
	git add .
	git commit -m "Initial hexo"
	git push origin gh-pages
```
5、预览这个现在生成的网站
	[https://vinefiner.github.io/MyHexo/](https://vinefiner.github.io/MyHexo/)

###基本命令使用

```
	hexo g = hexo generate  #生成
	hexo s = hexo server  #启动本地预览
	hexo d = hexo deploy  #远程部署

	hexo n "文章标题" = hexo new "文章标题"  #新建一篇博文

	hexo s -g  #等同先输入hexo g，再输入hexo s
	hexo d -g  #等同先输入hexo g，再输入hexo d
```
