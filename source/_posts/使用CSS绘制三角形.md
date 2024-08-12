---
title: 使用css绘制三角形

date: 2024-05-22
---

[参考掘金**CUGGZ** 使用 css 绘制三角形](https://juejin.cn/post/7075884138900750372)

## 使用 border 属性

给定一个宽度和高度都为 0 的元素，其 border 的任何值都会直接相交，我们可以利用这交点来创建三角形

```css
.triangle {
  width: 0;
  height: 0;
  border: 100px solid;
  border-color: orangered skyblue gold yellowgreen;
}
```

<br/>
<center>
<div style="
    width: 0;
    height: 0;
    border: 100px solid;
    border-color: orangered skyblue gold yellowgreen;
    "/>
</center>

<br/>

让任何三边的边框的颜色为`transparent`，则非常容易得到各种角度的三角形;

比如指向下面的三角形，可以让 border 的上边可见，其他边都设置为透明`transparent`

```css
.triangle {
  width: 0;
  height: 0;
  border-top: 50px solid skyblue;
  border-right: 50px solid transparent;
  border-left: 50px solid transparent;
}
```

以下是实现效果

<div style="display:flex;justify-content: space-between;">

<div>指向下面的</div>

<div>指向左面的</div>

<div>指向右面的</div>

<div>指向上面的</div>

</div>

<div style="display:flex;justify-content: space-between;">

<div style=" 
    width: 0;
    height: 0;
    border-top: 50px solid skyblue;
    border-right: 50px solid transparent;
    border-left: 50px solid transparent;
    border-bottom: 50px solid transparent;
    "></div>

<div style=" 
    width: 0;
    height: 0;
    border-top: 50px solid transparent;
    border-right: 50px solid skyblue;
    border-left: 50px solid transparent;
    border-bottom: 50px solid transparent;
    "></div>

<div style=" 
    width: 0;
    height: 0;
    border-top: 50px solid transparent;
    border-right: 50px solid transparent;
    border-left: 50px solid skyblue;
    border-bottom: 50px solid transparent;
    "></div>

<div style=" 
    width: 0;
    height: 0;
    border-top: 50px solid transparent;
    border-right: 50px solid transparent;
    border-left: 50px solid transparent;
    border-bottom: 50px solid skyblue;
    "></div>

</div>

也可以这样写

```css
.triangle {
  width: 0;
  height: 0;
  border-style: solid;
  border-color: transparent;
  border-width: 50px 0 50px 50px;
  border-left-color: skyblue;
}
```

<br/>
<center>

<div style="
    width:0;
    height:0;
    border-style: solid;
    border-color: transparent;
    border-width: 50px 0 50px 50px;
    border-left-color: skyblue;
  "/>

</center>

<br/>
