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
    `书写在style元素中，建议style元素写在head中`
2.内联样式表（元素样式表）
    `直接书写在元素的属性的位置，范围上相当于id选择`
3.外部样式表（推荐使用）
    `将样式书写到独立的CSS文件中`
    1）可以解决多个页面样式重复的问题
    2）

