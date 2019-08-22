# study
每周学习计划

## 201907

### 7月第三周

* [不是程序员的程序员](https://mp.weixin.qq.com/s/aEVRaqbuxPxeQwW3ewCqnA)
本文来自微信公众号InfoQ，是一个有关编程方面的公众号，涉及广泛，大家可以关注一下。
这篇文章主要讲的是，沟通 (communication)在我们领域的重要性。

* [同学，W3C了解一下？](https://75team.com/post/first-impression-of-w3c)
本文讲述w3c的标准是如何诞生的，以及如何加入w3c工作组。

* [前端学习路线](https://www.cnblogs.com/wu-web/p/8228340.html)
本文讲述的是前端方面的一个学习线路图，大家可以点进去了解一下，拟定一下自己的学习目标，我们不仅可以在公司学习，我们还可以通过其他学习路径自己专研。

* [菜鸟工程师的超神之路 -- 从校园到职场](https://mp.weixin.qq.com/s?__biz=MzAwMDc1ODA4Nw==&mid=2655123731&idx=1&sn=e1bcf595fad34a304f17d339701e7537&scene=0#wechat_redirect)
我认为本文最为主要的描述就是我们的心态，我们刚从学校进入职场，我们在这其中会遇到很多困难，很多挑战，面对他们，我们的心态至关重要，公司要我们来是创造价值的，我们不能为了工作而工作。

* [更好的纯CSS滚动指示器技术实现](https://www.zhangxinxu.com/wordpress/2019/06/better-css-scroll-indicator/)
本文讲诉的是有关页面中滚动条的文章，传统的css滚动指示器效果虽然方法和思路非常精妙，但是却有致命的缺陷，导致几乎无法在实际项目中应用。
致命缺陷是：
1.页面内容不能有背景色或背景图！
2.body自身也不能有背景图！
本文讲诉了更好的办法去控制它。

### 7月第四周

* [小技巧](https://www.cnblogs.com/ljwsyt/p/9516416.html)
本文讲述的是一些特殊知识的妙用，有关JavaScript的。

* [当你输入一个网址的时候，实际会发生什么?](https://www.cnblogs.com/wenanry/archive/2010/02/25/1673368.html)
本文主要讲述网络模块是如何协同工作的(url解析的过程)

* [HTML渲染过程详解](https://www.cnblogs.com/dojo-lzz/p/3983335.html)
本文主要从以下五个方面去讲解了HTML渲染的过程
1.解析HTML
2.构建DOM树
3.DOM树与CSS样式进行附着构造呈现树
4.布局
5.绘制

* [【CSS进阶】CSS 颜色体系详解](https://www.cnblogs.com/coco1s/p/5622534.html)
本文从几个方面详细的对css颜色进行了讲解，以及可以通过对颜色的一些控制，达到特定的效果等。

### 8月第一周
#### 什么是npm（npm使用介绍）
node package manager:node 包管理工具
npm是随同NodeJS一起安装的包管理工具，能解决NodeJS代码部署上的很多问题，常见的使用场景有以下几种：
+ 允许用户从NPM服务器下载别人编写的第三方包到本地使用。
+ 允许用户从NPM服务器下载并安装别人编写的命令行程序到本地使用。
+ 允许用户将自己编写的包或命令行程序上传到NPM服务器供别人使用。
由于新版的nodejs已经集成了npm，所以之前npm也一并安装好了。同样可以通过输入 "npm -v" 来测试是否成功安装。命令如下，出现版本提示表示安装成功:
```
C:\Users\Administrator>npm -v
6.2.0
```
__注意：在使用npm命令时，如果直接从国外的仓库下载依赖，下载速度很慢，甚至会下载不下来，我们可以更换npm的仓库源，提高下载速度。__

#### 怎么用npm
下载包
```
npm install <packagename>
```
删除包
```
npm unistall <packagename>
```
安装包下载安装在当前目录下node_modules特殊文件夹中。

创建npm账号
```
npm adduser
```
登录
```
npm login
```
发布
```
npm publish
```
#### 如何发布
初始化一个项目
```
npm init
```
创建一个名为XX.js文件
可利用vi编辑器
可运行一下看js文件是否成功
```
node XX.js
```
登录npm,输入创建时的账号密码邮箱
```
npm login
```
发布包
```
npm publish
```
__注意：如果项目里有部分私密的代码不想发布到npm上，可以将它写入.gitignore 或.npmignore中，上传就会被忽略了__

#### 如何修改镜像源
1、先查看自己的镜像源
可以用
```
npm config get registry
```
也可以用
```
npm config list
```
2、修改自己的镜像源
```
npm set registry https://registry.npm.taobao.org
```
如果只是临时改变源，可以这样
```
npm --registry=https://registry.npm.taobao.org
```
__注意：设置npm的源，可以设置多个源，但是只有一个是生效的（最后一个设置的为准），若公司有镜像源则可以设置为公司，也可以设置为其他的，这里以淘宝的镜像源为例__
__公司的私有地址为 http://nexushost.paas.x__

#### mac无法利用node安装sass时该怎么办
+ 第一步：检查电脑是否有brew
```
brew -v
```
若不是命令语句则说明没有，则下载homebrew，将以下链接放入终端中执行，公司的网比较差，用自己的wifi热点
``` 
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
若有，则直接进行第二步
+ 第二步：安装node，终端直接输入
```
brew install node
```
检查是否安装完成，请输入
```
node -v
```
+ 第三步：安装sass，在终端输入
```
npm install -g sass
```
npm是node的包管理工具，所以下node的时候，npm也自带下载下来了

### 8月第三周
#### HTML DOM树
通过 HTML DOM，树中的所有节点均可通过 JavaScript 进行访问。所有 HTML 元素（节点）均可被修改，也可以创建或删除节点。
#### 什么是DOM
DOM 是 W3C（万维网联盟）的标准。

DOM 定义了访问 HTML 和 XML 文档的标准：

“W3C 文档对象模型 （DOM） 是中立于平台和语言的接口，它允许程序和脚本动态地访问和更新文档的内容、结构和样式。”
W3C DOM 标准被分为 3 个不同的部分：

+ 核心 DOM - 针对任何结构化文档的标准模型
+ XML DOM - 针对 XML 文档的标准模型
+ HTML DOM - 针对 HTML 文档的标准模型

HTML DOM 是:
+ HTML 的标准对象模型
+ HTML 的标准编程接口
+ W3C 标准

HTML DOM 定义了所有 HTML 元素的对象和属性，以及访问它们的方法
**换言之，HTML DOM 是关于如何获取、修改、添加或删除 HTML 元素的标准。**
