# OCDeer.css

#### 介绍
css样式库，OCdeer提供从单个功能组件到全局的动态css样式，绕过复杂的调试步骤，直接在项目中导入样式库，无须浪费太多的精力在界面设计，以腾出更多时间去专注于页面逻辑和服务功能。<br>

#### 软件架构
一个控件多种样式，所有样式打包整合为OCDeer.css，开发者仅需要在HTML引用对应类选择器即可实现效果。


#### 下载指引

1.  OCDeer.css根据具体应用组件分类样式库，分为button（按钮），text（文本），films（动画），card（卡片）
2.  详细帮助文档及css代码请查阅 **Wiki** 
3.   **帮助文档标题点击可查看样式**
 
#### 帮助文档

1.  Button类
- 1.1 [流光溢彩](https://www.ocdeer.cn/ocdeer/ocdeer/btn1.html) btn-1 <br>
    单一类选择器，直接引用class="btn-1"

```HTML
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/button.css" />
    </head>
    <body>
        <button type="button" class="btn-1">BUTTON</button>	
    </body>
</html>
```
- 1.2 [flash](http://www.ocdeer.cn/ocdeer/ocdeer/btn2.html) btn-2 <br>
    单一类选择器，直接引用class="btn-2"

```HTML
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/button.css" />
    </head>
    <body>
        <button type="button" class="btn-2">BUTTON</button>	
    </body>
</html>
```
- 1.3 [波动效果](http://www.ocdeer.cn/ocdeer/ocdeer/btn3.html) btn-3 <br>
    复合样式，该样式下有两个分类，up，left，区别于波动起点位置及颜色不同，将css中始末位置互换可达成top和right效果。<br>
    首先引用样式<div class="btn-3"></div>，然后再div标签内引用具体样式分类up或者left

```HTML
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/button.css" />
    </head>
    <body>
        <div class="btn-3">
            <button type="button" class="up">BUTTON</button>
        </div>
    </body>
</html>
```
- 1.4 [流光边框](http://www.ocdeer.cn/ocdeer/ocdeer/btn4.html) btn-4 <br>
    因为该样式是按钮边框样式，button标签自带按钮边框，所以该样式使用的是```<a>```标签而非```<button>```<br>
    边框样式使用```<span>```标签定义<br>
    引用```<a class="btn-4">```<br>
    调用四个边框样式<br>
```html
    <span></span>
    <span></span>
    <span></span>
    <span></span>
```

```HTML
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/button.css" />
    </head>
    <body>
        <a class="btn-4">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            One Button
        </a>
    </body>
</html>
```
- 1.5 [折叠双层按钮](http://www.ocdeer.cn/ocdeer/ocdeer/btn5.html) btn-5 <br>
    该样式同样使用```<span>```规定,为双层按钮，左悬停为按钮1，右悬停为按钮2<br>
    该样式分为有边框和无边框两种，使用的是```<a>```标签为无边框样式，使用```<button>```则有边框<br>
    引用```<button class="btn-5">```或```<a class="btn-5">```
    调用样式
```html
    <span>This Button1</span>
    <span>This Button2</span>
```

```HTML
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/button.css" />
    </head>
    <body>
        <button class="btn-5">
            <span>This Button1</span>
	    <span>This Button2</span>
	</button> 
    </body>
</html>
```
- 1.6 [流光边框2](https://www.ocdeer.cn/ocdeer/btn6/index6.html) btn-6 <br>
    边框样式，使用的是```<a>```标签<br>
    边框样式使用```<span>```标签定义<br>
    引用```<a href="#" class="btn-6">Button</a>```<br>
    共有三种样式<br>

```HTML
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/button.css" />
    </head>
    <body>
        <a href="#" class="btn-6">Button</a>
	<a href="#" class="btn-6">Button</a>
	<a href="#" class="btn-6">Button</a>
    </body>
</html>
```
- 1.7 [边框变色](https://www.ocdeer.cn/ocdeer/btn7/index.html) btn-7 <br>
   复合样式，首先引用样式 ```<div class="container">``` ，然后再div标签内引用button样式```<button class="btn-7">```
```HTML
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<link href="css/button.css" rel="stylesheet">
		<title></title>
	</head>
	<body>
		<div class="container">
		    <button class="btn-7">
		      <label>Button</label>
		    </button>
		 </div>
	</body>
</html>
```
- 1.8 [边框绘制](https://www.ocdeer.cn/ocdeer/abutton/btn8.html) btn-8 <br>
    首先引用样式```<div class="btn-8">```<br>
    svg定义形状元素，rect()方法创建矩形<br>
```
<svg width="240" height="60">
                  <rect
                    class="rectangle"
                    width="240"
                    height="60"
                  />
                </svg>
```
调用button字体的样式```<div class="btn" >```
```HTML
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<link href="css/button.css" rel="stylesheet">
		<title></title>
	</head>
	<body>
            <div class="btn-8">
                <svg width="240" height="60">
                  <rect
                    class="rectangle"
                    width="240"
                    height="60"
                  />
                </svg>
        <div class="btn" >
         Button
        </div>
        </div>
	</body>
</html>
```
- 1.9 [边框绘制2](https://www.ocdeer.cn/ocdeer/abutton/btn9.html) btn-9 <br>
    边框样式，使用```<a>```标签，边框样式使用```<span>```定义<br>
    引用```<a href="#" class="btn-9">```<br>
```
<a href="#" class="btn-9">
	<span>
				
	</span>
	button
</a>
```
```HTML
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/button.css" />
    </head>
    <body>
        <a href="#" class="btn-9">
	    <span>
				
	    </span>
	    button
	</a>
    </body>
</html>
```

2.  text类
- 2.1 [收缩扩展](http://www.ocdeer.cn/ocdeer/ocdeer/text1.html) text-1 <br>
    引用样式class="btn-1"<br>
    该样式默认状态下缩进状态，鼠标悬停时触发扩展效果，显示全文。<br>
    默认状态样式直接规定标签选择器，所以我们直接使用span标签即为默认样式，```<span>W</span>```
    
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
	<title></title>
	<link rel="stylesheet" type="text/css" href="css/text.css" />
    </head>
    <body>
	<div class="text-1">
	    <span>W</span>
	    <span class="s">e</span>
	    <span class="s">l</span>
	    <span class="s">c</span>
	    <span class="s">o</span>
	    <span class="s">m</span>
	    <span class="s">e</span>

	    <span>O</span>
	    <span class="s">m</span>
	    <span class="s">n</span>
	    <span class="s">i</span>
	    <span class="s">p</span>
	    <span class="s">o</span>
	    <span class="s">t</span>
	    <span class="s">e</span>
	    <span class="s">n</span>
	    <span class="s">t</span>

	    <span>C</span>
	    <span class="s">o</span>
	    <span class="s">l</span>
	    <span class="s">o</span>
	    <span class="s">r</span>

	    <span>D</span>
	    <span class="s">e</span>
	    <span class="s">e</span>
	    <span class="s">r</span>
        </div>
    </body>
</html>
```
- 2.2 [聚光灯](http://www.ocdeer.cn/ocdeer/ocdeer/text2.html) text-2 <br>
    引用class="text-2"<br>
    但在实际应用同场景中使用较为麻烦，需要调节文字内容和大小，聚光点的大小等。

    该样式的设计思路并非灯光照耀在文字上显现彩色光芒，而是提前规定好文字（这里是指背景绘制区域，为了方便大家理解称暂称文字）的色彩样式并设置镂空效果，然后生成一个圆形可视区域在文字上来回滚动播放，圆形可视区域所在的地方文字不透明，显示为我们规定好的文字色彩样式。而非圆形可视区域的文字表现为透明。

    修改文字内容：content: 'ocdeer';

    修改文字大小：font-size: 8rem; 

    修改文字默认状态下颜色：.text-2{color: #FFFFFF;}

    开发思路：

    首先设置文字颜色透明：color: transparent;

    绘制背景区域：background-image: linear-gradient(to right,#c23616,#192a56,#00d2d3,yellow,#6d214f,#2e86de,#4cd137,#e84118);<br><br>

    当值为text 的时候，代表设置了文字的镂空效果：background-clip: text;

    创建元素的可显示区域，circle表示创建了圆形，100px表示圆形的直径,0%和50%表示圆形的圆心，圆形的直径和圆形的圆心利用at关键字隔开：clip-path: circle(100px at 0% 50%);

infinite 无限次播放：animation: move 5s infinite;

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/text.css" />
    </head>
    <body>
        <h1 class="text-2">ocdeer</h1>	
    </body>
</html>
```
- 2.3 [文字分裂](http://www.ocdeer.cn/ocdeer/ocdeer/text3.html) text-3 <br>

    首先引用样式：class="text-3"

    引用text-3下的a类型class="a"（这里是类选择器a，不是a标签）

    ```<a>```标签添加链接

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/button.css" />
    </head>
    <body>
        <section>
            <div class="section_item">
                <div class="a">Welcome</div>
                <div class="a">Welcome</div>
                <a href="#">馒头拿来摸摸</a>
            </div>
        </section>
    </body>
</html>
```
3.  input类
- 3.1 [输入框-绘制](https://www.ocdeer.cn/ocdeer/input/input1.html) input-1 <br>

    首先引用样式：```<div class="input-1">```
    
    分别引用边框的上下左右四个边框的对应样式
```
<input type="text" />
<span class="left"></span>
<span class="right"></span>
<span class="top"></span>
<span class="bottom"></span>
```

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/input.css" />
    </head>
    <body>
        <div class="input-1">
	    <input type="text" />
	    <span class="left"></span>
	    <span class="right"></span>
	    <span class="top"></span>
	    <span class="bottom"></span>
	</div>
    </body>
</html>
```
- 3.2 [搜索框](https://www.ocdeer.cn/ocdeer/input/input2.html) input-2 <br>

    首先引用样式：```<div class="input-2">```
    
    引用input样式```<input type="text" class="b">```

    使用```<a>```标签绘制悬停时高亮圆圈```<a href="#" class="c">```
    
    该样式的图标为矢量图```<img src="img/input.png" style="width: 30px;">```,矢量图可从阿里巴巴矢量库下载

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/input.css" />
    </head>
    <body>
        <div class="input-2">
            <input type="text" class="b">
            <a href="#" class="c">
                <img src="img/input.png" style="width: 30px;">
            </a>
    </div>
    </body>
</html>
```

4.  films类
5.  card类


