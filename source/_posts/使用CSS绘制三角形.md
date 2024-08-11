---
title: 使用css绘制三角形

date: 2024-05-22
---

[参考掘金**CUGG**Z 使用 css 绘制三角形](https://juejin.cn/post/7075884138900750372)

## 使用 border 属性

给定一个宽度和高度都为 0 的元素，其 border 的任何值都会直接相交，我们可以利用这交点来创建三角形

```

.triangle {

    width: 0;

    height: 0;

    border: 100px solid;

    border-color: orangered skyblue gold yellowgreen;

}

```
