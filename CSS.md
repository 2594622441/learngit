# CSS为网页添加样式
[toc]
## 术语解释
```元素选择器添加样式：
<style>
    h1{
        color: red;
        background-color: lightblue;
        text-align: center;
    }
</style>
```
CSS规则 = 选择器 + 声明块
`选择器用来选中元素以确定样式的范围，声明块`

### 选择器
1.ID选择器：选中的是对应id值的元素（选中所有该元素，用的较少）
```
<style>
    #指定元素对应的id {
        color:red;
        background-color:lightblue;
        tect-align:center;
    }
</style>
```

2.元素选择器（只选择一个，用的是少）
```
<style>
    元素名称{
        color: red;
        background-color: lightblue;
        text-align: center;
    }
</style>
```
3.类选择器（用的最多）
```
<style>
    .类名称{
        color: red;
        background-color: lightblue;
        text-align: center;
    }
</style>
```


总结：
1.id选择器：#id名称{}
2.元素选择器：元素名称{}
3.类选择器：.类名称{}
### 声明块
声明块中包含许多声明（属性），每一个声明表达了某一个样式规则。

## CSS代码书写位置
1.内部样式表，
`
书写在style元素中，建议style元素写在head中
`
2.内联样式表（元素样式表），JS常用，不推荐使用
`
直接书写在元素的属性的位置，范围上相当于id选择
`
3.外部样式表（推荐使用）
`
将样式书写到独立的CSS文件中
`
    1）可以解决多个页面样式重复的问题
    2）有利于浏览器缓存，从而提高页面响应速度
    3）有利于代码分离(HTML和CSS)，便于阅读和维护

# 常见的样式声明

1.color:元素内部的文字颜色(定义好的单词/rgb/hex16进制)
2.background-color：元素背景颜色
3.font-size;元素内部文字的尺寸大小
    1）px:像素，绝对单位
    2）em：相对父元素字体大小的倍数，相对单位
    3）user agent：UA，用户代理（浏览器）
4.font-weight：文字粗细程度，取值为数字/预设值（单词）
    1）normal：默认值，400
    2）bold：加粗，700
5.font-family：文字类型，必须用户计算机中已存在的字体才有效
    1）微软雅黑
    2）宋体
    3）黑体
    4）sans-serif:非衬线字体
    。。。
6.font-style：字体样式，通常用于设置斜体字
    1）italic：倾斜
    2）i元素：默认其中的文字为倾斜字体，实际使用中用它表示一个图标（icon）
    3）strong和em元素：默认带有加粗效果，strong元素表示重要的不可忽略的，em表示强调的内容
7.text-decoration：文本修饰（给文本加线）
    1）line-through：中间加线（表示删除的del元素和表示过期的s元素的时候常用）
    2）overline：上面加线
    3）underline：下划线
8.text-indent：首行文本缩进
    1）px:像素
    2）em:字符数
9.line-height：行高，每行文本的高度
    1）px:像素
    2）em:通常不用
    3）纯数字，表示相对于当前元素的大小
    4）normal
    。。。
10.width：
11.height：
12.letter-space：



