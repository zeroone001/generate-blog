---
title: 怎么让一个 div 水平垂直居中
date: 2019-04-13 12:00:45
tags:
- html
- css
categories: css
---
div 标签居中显示的一些归类总结
<!-- more -->
#### 结构
```html
<div class="parent"><div class="child"></div></div>
```
#### 样式
1.
```css
div.parent {
    display: flex;
    justify-content: center;
    align-items: center;
}
```
2.
```css
div.parent {
    position: relative;
}
div.child {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
/* 或者 */
div.child {
    width: 50px;
    height: 10px;
    position: absolute;
    top: 50%;
    left: 50%;
    margin-left: -25px;
    margin-top: -5px;
}
/* 或 */
div.child {
    width: 50px;
    height: 10px;
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    margin: auto;
}
```
3.
```css
div.parent {
    display: grid;
}
div.child {
    justify-self: center;
    align-self: center;
}
```
4.
```css
div.parent{
  display:flex;
}
div.child{
  margin:auto;
}
```
#### 参考资料
- [资料1](https://github.com/Advanced-Frontend/Daily-Interview-Question/issues/92)


