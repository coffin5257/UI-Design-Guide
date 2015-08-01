# 初创团队 UI 设计指南

## 工具

- 一台 Mac
- Sketch ：http://pan.baidu.com/s/1eQF5ClW 密码: bw9u
- Zeplin ：https://zeplin.io/ 每个免费帐号可以建一个项目，这个主要目的是导出切图
- Skala Preview：方便在手机上实时预览
- ICON 库：sketch 支持导入 SVG/EPS 格式的矢量图
- PS AI 等 ： 辅助，[如何在4小时内学会 AI](http://www.zhihu.com/question/21378038)

当然，把这些都装上，你需要先熟悉下 MAC 系统的基本使用。

## 方法

### 规范
手机端的设计，必定要遵循一定的规范，比如屏幕就这么大，你要怎么合理展示你的内容？
关于这方面，请看：

- [移动设计指南！如何利用视觉元素有效传达信息？](http://www.uisdc.com/mobile-visual-communication-design)
- iOS 和 Android 也有相关的设计规范：
	- [iOS](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/index.html) - [[ISUX转译]iOS 8人机界面指南（一）：UI设计基础](http://isux.tencent.com/ios8-human-interface-guidelines.html)
	- [Android Design 4.4](http://adchs.github.io/index.html)
	- [Android : Material design](https://www.google.com/design/spec/material-design/introduction.html#) - [中文版点这里](http://design.1sters.com/)

### 布局方案：
- [几种典型的 iOS 应用界面的交互框架各自的优缺点是什么？](http://www.zhihu.com/question/21430811)
- [比较 Material Design 和 iOS 7 设计风格，他们各自的优缺点是什么？]( http://www.zhihu.com/question/24365423)

## 设计流程

### 产品早期

- 全程参与需求确认
- 与产品合作，制作原型，构思交互
- 沟通多用能演示的，比如草图
- 原型设计基本定型，产品、设计、技术、运营达成一致

### 视觉设计

- 风格探索
- 定制界面风格、设计规范（充分利用 Sketch Symbol 和 Shared Style 功能）
	- 参考：[实用必收！如何建立一套UI设计规范？（附众多神器）](http://www.uisdc.com/create-ui-design-guideline)
- 关键界面设计，先拿给开发用
- 细节优化

### 设计 Review

- 对设计评审，修改 bug
- 对开发实现程度进行评审，注意「和善度」，切不可把开发打倒踩着他的头问他麻不麻烦！

## Sketch 工作流：

### 预防针

- 使用指南、插件安装：[Sketch 中文网](http://sketchcn.com/)，装一个 Sketch toolbox，安装插件非常方便

- 不许出现 **位置** 和 **尺寸** 上的「半个像素」，否则会有毛边，或者尺寸计算错误，这种情况一般出现在整体放大、缩小某个元素时。
 ![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801141915.png)

- Sketch 能导入 svg 或者 eps，对位图处理能力比较一般

### 尺寸

- [UI设计师不可不知的安卓屏幕知识(原创)](http://www.zcool.com.cn/article/ZNjI3NDQ=.html)
- 如果多客户端只出一套设计，设置 Artboard 大小为 720*1280（Sketch 里的都是 px），使用 Measure 插件标注的时候选择 xhdpi（2px=1dp）
- iOS 启动图片尺寸，[iOS App图标和启动画面尺寸](http://www.jianshu.com/p/adpKye)：
	- 640x960
	- 640x1136
	- 750x1134
	- 1242x2208 

### 项目组织

- 每个 app 建一个 Sketch 文件

- 每个 app 的页面是一个 Artboard，根据顶层导航，设置不同的 page

 ![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801143525.png)

比如我这个分组方式，在 app 里的表现是这样：

 ![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801143733.png)

很显然地，整个 app 有五大板块，所以分为五个 page，每个 page 里面再来做单个页面。

**所以，用英文来命名所有需要展示出来的东西**

另外，还需要建一个 page 来建立「规范」：

 ![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801145307.png)

- 每个 page 里面，按照应用逻辑来组织 Artboard 布局

以该模块（page）第一个页面为原点：

1.同一页面的交互，横向排列，每个 Artboard 之间间距为 100 
![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801151022.png)

2.有页面跳转的，纵向扩展，间距同样为 100

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801151249.png)

3.在最前面还应该设置一个 Artboard，来放置 icons，切图

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801150809.png)

### 原子设计：把每一个元素抽离成最小的组成部分

这要求你作为一个设计师，要懂开发一个 app 的接本实现原理，比如一个列表是由一个个 item 组成的：

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801152602.png)

应该这么做：

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801153052.png)

而不是这么做：

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801153117.png)

关于这个可以看看 Sketch 预设的一些模板是怎么做的，比如这个背景页，尽管它只有部分露出来，但是页面逻辑上还是做成了全屏幕大小

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801153517.png)


### Logo 设计

- App 的 Logo 使用 Sketch 的模板

 ![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801142622.png)

在这个里面设计，然后使用插件 Icon Stamper 扩展到每一个尺寸的 Artboard 
 ![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801142814.png)
 
### 标注切图

- 使用插件 Sketch Measure 对每个页面进行标注，标注信息可以快捷键隐藏

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801163836.png)
![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801163858.png)

- icon 上使用 Slice 划分切图区域，保证同一层级的 icon 图大小是一样的：

比如这四个图本身大小是不一样的，但是全部切成 64*64 的 icon

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801164215.png)

**每次导出必须检查有没有误选不想导出的东西**

### 导出

使用一开始说的 Zeplin，新建安卓项目，将每个 page 里面的 icons Artboard 导出到 Zeplin，它能直接把 icons 生成各个尺寸的图：

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801155653.png)

看效果：

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801160004.png)

#### 9patch

- 先了解下什么是 [android 9patch](http://www.jianshu.com/p/d9fa98b4e17c)
- 其实用 Sketch 做 9patch 也可以，手动画 1px 粗的黑线即可：

 ![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801165748.png)

### 文件组织管理

- 项目根目录存放所有的 Sketch 文件
	- UI 文件（只放 app 界面相关）
	- Logo 文件
	- 引导页 文件(启动页面也放里边)

把这些分开，一是防止单个 Sketch 文件过大导致 Sketch 卡顿，二是方便团队协作分工

- 每个 page 建立一个目录，另外视情况新建这些目录：
	- `Boot page`(引导页面)
	- `Start page`(启动页面)
	- `Logo`
	- 按需添加其他目录

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801162523.png)

- 每个 page 的目录下，有一个 icons 目录，存放该页面所有的 icons

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801162719.png)

每个页面文件导出两份：原图 和 标注版，命名后面加 `measure` 以示区分

### 使用 Git 管理

- [专为设计师而写的GitHub快速入门教程](http://www.ui.cn/detail/20957.html)
- [Git 教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

#### 演示：

1.新建项目

本地建立项目目录

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801171038.png)

去我们的 Gitlab（跟 Github 类似的一个东西，但是我们私有的） 上新建一个项目

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801170524.png)

根据提示，显然我们这已经有了一个文件夹，现在需要进行一些设置

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801170648.png)

2.初始化项目

用命令行做这些操作，图形界面太难用，命令行并没有设计师们想象的那么恐怖

```bash
cd UI_Git_Test //进入项目文件夹
git init //初始化项目仓库
git remote add origin http://****/****/UI-Git-Test.git  //添加远程仓库
```
然后开始做一些基本工作，比如新建一个 sketch 文件保存到这里，再建一些必要的目录，现在目录下有这些东西

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801172012.png)

绿色表示文件夹，`.`开头的是隐藏文件，`.git` 是 `git init`命令自动生成的，`.gitignore` 是我们手动生成的，内容如下：

```
*.sketch
*.pixate
*.psd
*.ai
*.esp
```

这个文件是用来描述哪些文件可以被 git 忽视掉，不把它加到版本库。我们只需要把图片资源放到版本管理里就行了，所以让 git 把一些源文件忽视掉。

3.上传到 Gitlab 上

- 先需要添加到缓冲区

```bash
git add .  //强行添加所有的就行
```
- 然后 commit （提交)，`-m` 参数是指定提交日志，比如我们第一次提交是 `初始化项目`。

```bash
git commit -m "初始化项目"
```

**这个要跟你所做的修改一致，比如你刚导出`页面1`的图，`add` 之后，commit 日志就应该写成 `"页面1"`。再比如修改了某个 icon 的颜色，应该写 `"修改 xxx 颜色"`，甚至可以写的更细致，把颜色值写出来**

- 上传到远程 Gitlab 上

```bash
git push origin master
```

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801173807.png)

- 我们去 Gitlab 项目主页去看看，这里是你的提交日志

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801174509.png)

看文件目录
![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801174554.png)

**纳尼！！！怎么只有这一个？ Sketch 文件被忽略了没错，其他的都去哪里了？**
原来，Git 是只认文件不认目录的，我们的目录里面是空的所有直接被忽视了。

不信你在某个目录下建一个文件，再 `add` `commit` `push` 看看。

- 我们忘了一件事

在初始化项目的时候还应该新建一个 `README.md` 文件，`.md`文件是 markdown 文件，有一个在线编辑器 [作业部落](https://www.zybuluo.com/mdeditor)，左右对照，很快你就能知道什么是 markdown 。

然后我们在项目根目录下建一个 `README.md`，方便开发快速了解你的设计，内容为：

```md
# xxx 项目 UI 开发指南
--------------

## 项目结构

每个目录是对应的功能模块，里面包括 页面视觉图、页面标注图、icons

开发不听话要多打

```

然后我们再去 Gitlan 看看，根目录下的 README.md 文件能直接预览

![](http://7bv8xn.com1.z0.glb.clouddn.com/20150801180318.png)

#### 以上！通过这样的方式，你能很轻松地维护你的设计，很顺畅地跟开发沟通，另外，设计师掌握点技术相关的东西，还是很重要的。

最后，本文引用了大量互联网上的文章链接，特别感谢这些文章的作者们。