# HTML是房子，CSS是装修 {ignore}
[toc]
## 什么是HTML？

html是W3C组织定义的语言标准，用于描述网页结构的语言。
HTML：Hyper Text Markup Language

MDN：Mozilla Development Network，Mozilla开发者社区。

## 什么是CSS？

CSS是W3C定义的语言标准：CSS是用于描述页面展示的语言
CSS决定了页面长什么样子。

## 执行HTML和CSS
交给浏览器内核执行->页面

### 浏览器
1.shell:外壳
2.core:内核（JS执行引擎、渲染引擎）

### 常见浏览器内核
IE：Trident
Firefox：Gecko
Chrome：Webkit/Blink
Safari: Webkit
Opera: Presto/Blink

## 版本和兼容性
HTML5、CSS3

HTML5：2014年
CSS3：目前还没有制定完成
XHTML：可以认为是HTML的一种的一个版本，完全符合XML的规范

## 第一个网页
Emmet插件：自动生成HTML代码片段（智能补全代码）

## 注释
<!-- 注释内容 --> 可跨行

## 元素
其他叫法：标签、标记
`元素 = 起始标记（begin tag) + 结束标记（end tag）+ 元素内容 + 元素属性，`
如：
   ` <a href="http://www.baidu.com" title="百度">百度</a>
    <title>标题</title>`

`有些元素没有结束标记，这样的元素叫做：空元素`，
如：空元素的两种写法
    `<meta charset = "UTF-8">`
    `<meta charset="UTF-8" />`

## 元素的嵌套
元素不能相互嵌套
元素的分类：
`父元素、子元素、祖先元素、后代元素、兄弟元素等`


## 属性
属性 = 属性名 + 属性值
如：
   ` href="http://www.baidu.com" title="百度"`

属性的分类：
`局部属性：某些元素特有的属性`
`全局属性：所有元素通用，如title`

## 标准的文档结构
```
<!DOCTYPE html> 文档声明
<html lang="en"> 根元素，lang属性，全局属性，表示该元素内部的文字是使用哪种自然语言书写的
<head> 文档头内部的内容不会显示到页面上
    <meta charset="UTF-8"> 空元素，表示文档的元素据，即附加信息
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title> 网页标题
</head>
<body> 文档体，参与显示的元素写在其中
    
</body>
</html>
```

# 语义化
[toc]
## 1.每一个元素都有具体的含义
a元素：超链接
p元素：段落
h1元素：一级标题

## 2.所有元素与展示效果无关
`展示效果应该由CSS决定`
`因为浏览器带有默认的CSS样式，所以每个元素有一些默认样式`
**选择什么元素，取决于内容的含义，而不是显示出的效果**

## 为什么需要语义化？
1.为了搜索引擎化（SEO）
`搜索引擎：百度、搜搜、Bing、Google
每隔一段时间，搜索引擎会从整个互联网中抓取页面源代码，然后分析`

2.为了让浏览器理解网页
`方便各种插件的编写和浏览器对插件的支持，如阅读模式、语音模式等`

# 文本元素
[toc]
`HTML5中支持的元素：HTML5元素周期表（百度搜索）`
## h
h1-h6:表示一级标题-六级标题 
$为占位符，用于格式化输出
`h$*6{$级标题} => 
    <h1>1级标题</h1>
    <h2>2级标题</h2>
    <h3>3级标题</h3>
    <h4>4级标题</h4>
    <h5>5级标题</h5>
    <h6>6级标题</h6>`
## p
表示段落：```<p></p>```
乱数假文：
`lorem => 
Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iste, modi assumenda voluptatum earum corporis quia sit provident cum nulla quam nemo officiis. Ab in eos atque blanditiis! Maxime, consequuntur iste.
`
## span【无语义】
没有语义，仅用于设置样式。
1.强制需要元素的时候使用```<span></span>```
如：
```
<p>三原色包含：
    <span style = "color: red">红</span>
    <span style = "color: green">绿</span>
    <span style = "color: blue">蓝</span>
</p>
```
2，某些元素在显示时会独占一行（块级元素）->display: block，
而有些元素不会（行级元素）->display: inline。
`到了HTML5已经弃用这种说法`
## pre
预格式化文本元素
`
1.空白折叠：在源代码中的连续空白字符（空格、换行、制表符等）在页面显示时会被折叠为一个空格。
`
`
2.在pre元素内部出现的内容，会按照源代码格式显示到页面上，以防止空白折叠。
通常用于在网页中显示一些代码。
`
一般在最外面套上```<code></code>```,如：
```
<code>
    <pre>
        var i=2;
        if(i){
            console.log(i);
        }
    </pre>
</code>
```
`
3.pre元素的默认CSS样式为 white-space: pre ，来达到防止空白折叠的效果。
`

# HTML实体
[toc]
实体字符，HTML Entity,通常用于在页面中显示一些特殊符号。
1.&单词;
2.&#数字;
如：
```
小于号 < 写成 &lt; 而
大于号 > 写成 &gt; 而
一个空格  写成 &nbsp; 而
版权符号 © 写成 &copy; 而
&符号本身 & 写成 &amp; 
```

# a元素
[toc]
 ## href属性
 hyper reference（超引用），通常表示跳转地址。
### 1.跳转地址，一般会刷新页面。
### 2.跳转到某个锚点（相当于在目录中跳转到当前页面的不同位置）,一般不会刷新页面
```
a*6>{章节$}  =>  
    <a href="">章节1</a>
    <a href="">章节2</a>
    <a href="">章节3</a>
    <a href="">章节4</a>
    <a href="">章节5</a>
    <a href="">章节6</a>
```
id属性：一个全局属性，表示元素在文档中的唯一编号。
```
如，<a href="#chapter2">章节2</a>
    <p id="chapter2">lorem</p>
    当点击a标签时会跳转到对应的id锚点。
```

```
添加属性的快捷写法，如
a[href=chapter$]*6{章节$}  => 
    <a href="chapter1">章节1</a>
    <a href="chapter2">章节2</a>
    <a href="chapter3">章节3</a>
    <a href="chapter4">章节4</a>
    <a href="chapter5">章节5</a>
    <a href="chapter6">章节6</a>
```
而
```<a href="#">回到顶部</a>```
会回到顶部。

### 3.功能链接
点击后，触发某个功能
1）执行JS代码,如
```<a href="javascript: alert('你好！')">弹出你好</a>```
2）发送邮件，要求主机上需要有邮件发送软件，如
```
<a href="mailto:2594622441@qq.com">点我发送邮件</a>
```
3）拨打电话,要求主机上有拨号软件或使用移动端，如
```
<a href="tel:18233316172">点击给我拨打电话</a>
```

## target属性和title属性
targe属性表示跳转窗口位置（默认为当前窗口），取值为_self/_blan，
分别为当前窗口和新建空白窗口中打开。
如，
```
<a href="https://douyu.com" target="_blank" title="斗鱼，每个人的直播平台">斗鱼</a>
```
`其中，title为鼠标放到链接上时显示的文字，target属性默认为_self`

# 路径（地址）的写法
[toc]
## 站内资源和站外资源
1.站内资源：当前网站的资源
2.站外资源：非当前网站的资源
## 绝对路径和相对路径
`
对站内资源优先使用相对路径，
对站外资源只能使用绝对路径。
`

1.绝对路径书写格式
```
协议名://主机名:端口号/路径
schema://host:port/path
如，https://www.baidu.com
    http://127.0.0.1:5501/2
```
`协议名：http、https、file等，下一跳地址和当前页面协议相同时，可省略协议名，
主机名：域名/IP地址，
端口号：http协议默认为80，https协议默认为443，可以省略，
路径：资源的存放路径，
`
2.相对路径的书写格式
以./开头，表示当前目录(也可省略)，而../则表示上一级目录

# 图片元素
[toc]
##  img元素
image的缩写，为空元素,
1.src属性，如：
```
<img src="https://t8.baidu.com/it/u=3571592872,3353494284&fm=79&app=86&size=h300&n=0&g=4n&f=jpeg?sec=1594860469&t=74fdd78883e5a91753b0a1b6fe637544">
<img src="./img/solar/earth.jpg">
```
2.alt属性，当图片资源丢失或其他原因无法加载时作为替代显示的文字，
如：
```
<img src="./img/solar/earth.jpg" alt="这是一张地球图片">
```
## 和a元素联用
1.点击图片后会跳转到指定的地址，如：
```
<a href="https://t8.baidu.com/it/u=3571592872,3353494284&fm=79&app=86&size=h300&n=0&g=4n&f=jpeg?sec=1594860469&t=74fdd78883e5a91753b0a1b6fe637544">
    <img src="./img/solar/jpg" alt="这是一张太阳系的图片">
</a>
```
2.点击图片的指定区域跳转到对应的地址，点击其他区域时和a元素中的地址相同
使用map元素和它的子元素area元素(空元素)，如
```
<a href="https://t8.baidu.com/it/u=3571592872,3353494284&fm=79&app=86&size=h300&n=0&g=4n&f=jpeg?sec=1594860469&t=74fdd78883e5a91753b0a1b6fe637544">
    <img usemap="#solarMap" src="./img/solar/jpg" alt="这是一张太阳系的图片">
</a>

<map name="solarMap">
    <area shape="circle" coords="Rx,Ry,R"  href="./earth.jpg" alt="地球">
    <area shape="rect" coords="x1,x2,y1,y2" href="./moon.jpg" alt="月球">
    <area shape="ploy" coords="x1,y1,x2,y2,...xn,yn" href="./plato.jpg" alt="冥王星">
</map>
```
## 和figure元素联用
表示其中的子元素互相关
`figcaption是figure的子元素，表示标题`


# 多媒体元素
[toc]
## 1.video元素，即视频元素

```
<video src="./鸡你太美.mp4"></video>
```
### controls元素，控件的显示，默认为不显示
controls="controls"即设置为显示，
```
<video controls="controls" src="./鸡你太美.mp4"></video>
```
### 某些属性，只有两种状态：
1.不写
2.取值为属性名，但在HTML5中，可以不用书写属性值

### autoplay属性
也是一个布尔属性，自动播放
```
<video controls autoplay src="./鸡你太美.mp4"></video>
```
### muted属性
 也是一个布尔属性，静音播放
### loop属性
也是一个布尔属性，循环播放


## 2.audio元素，即音频元素
把video换成audio即可，其他一样

## 3.兼容性
1）旧版本浏览器可能不支持video和audio元素，只能用flash
2）不同的浏览器支持的音视频格式可能不一致
mp4/webm、mp3
## 4.source元素
为video和audio的子元素，是个空元素
如：
```
<video controls autoplay muted loop style="width:500px;">
    <source src="鸡你太美.mp4">
</video>
```

# 列表元素
[toc]
## 有序列表
ol: orderd list
li: list item
`li为ol的父元素`
如：
```
<ol type="i"> 表示使用罗马数字
    <li>打开冰箱门</li>
    <li>大象进去</li>
    <li>冰箱门关上</li>
</ol>
```
1.
type="1"，为默认值，使用数字
type="i"表示使用小写罗马数字，
type="I",表示使用大写罗马数字，
type="a"，表示使用小写字母
type="A"，表示使用大写字母
`推荐使用list-style-type的CSS样式来替代type`
2.
reversed属性，序号会降序显示
## 无序列表
ul: unorderd list
`只需把ol改为ul即可，其他一致`
## 定义列表
通常用于一些术语的定义
dl: definition list
dt: definition title，为dl的子元素,定义标题
dd: definition description，为dl的子元素，定义描述
如：
```
<dl>
    <dt>HTML</dt>
    <dd>超文本标记语言</dd>
</dl>
```
# 容器元素
[toc]
该元素内部用于放置其它元素，用于划分区域
## div元素
没有语义，之前都是使用div划分区域
## nav元素
表示导航

## 语义化容器元素
article元素：通常用于表示整篇文章
header元素:通常用于表示页头，也可以表示文章的头部
footer元素：通常用于表示页脚，也可以表示文章的尾部
section元素：通常用于表示文章中的章节
aside元素：通常用于表示侧边栏，即附加信息

# 元素的包含关系
[toc]
以前：块级元素可以包含行级元素，反之不可以（a元素除外）
现在：由元素的语义和内容类别决定

总结：
`
1.容器元素中可以包含任何元素
2.a元素中几乎可以包含任何元素
3.某些元素有固定的子元素，如ul->li, ol->li, dl->dt/dd
4.标题元素和段落元素不能相互嵌套，并且不能包含容器元素
`


