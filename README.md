## Useage

```shell
$ npm install -g yo
```
```shell
$ npm install -g generator-mtb-app
```
```shell
$ yo mtb-app
```
接下来，就可以启动grunt进行愉快的编码了。
```shell
$ grunt
```
grunt 默认会启动 `watch` 模式，`less/`文件下的less文件会自动编译到`build/css/`文件下，`js/`文件夹下的js会自动压缩至`build/js/`目录下。

```shell
$ grunt build
```
`grunt build` 会自动将 带有 `data-htmlone` 属性并引用本地文件的 `<link>` 和 `<script>` 标签自动替换为 css 和js的内容。Combo到html一起。在`dest/`目录下。 详见项目 `amfe/or.htmlone`


### Info

```shell
$ yo mtb-app

     _-----_
    |       |    .--------------------------.
    |--(o)--|    |  Create your own Yeoman  |
   `---------´   |      generator with      |
    ( _´U`_ )    |       superpowers!       |
    /___A___\    '--------------------------'
     |  ~  |     
   __'.___.'__   
 ´   `  |° ´ Y ` 

? Would you mind telling me your username on Gitlab? cenan.chr
? What's the base name of your generator? app-test
   create package.json
   create Gruntfile.js
   create .editorconfig
   create .jshintrc
   create .travis.yml
   create README.md
   create .gitattributes
   create .gitignore
   create index.html
   create less/main.less
   create js/main.js
   create test/test-app.js
>> npm install start ...
```
 
生成工程模板如下:

```
|- app-name/
	|- images/
	|- js/
		- main.js
	|- less/
		- main.less
	|- node_modules/
	|- test/
	- .editorconfig
	- .gitattributes
	- .gitignore
	- .jshintrc
	- .travis.yml
	- .yo-rc.json
	- Gruntfile.js
	- index.html
	- package.json
	- README.md
```

** grunt build **

```shell
$ cd app-name
$ grunt build
```
会自动生成 `build/` 和 `dest/` 目录。
`build/` 目录 会把 `js/` 和 `less/` 目录下的 js 和 less文件分别编译压缩至 `build/js/` 和 `build/css/` 目录下
`dest/` 目录下 会 自动把 根目录下的 `.html` 和 `.htm` 文件中引入的 带 `data-onereq` 的 css link 和 js 内容压缩并Combo至 `dest/` 目录下。
