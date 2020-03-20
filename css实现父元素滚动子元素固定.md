实现逻辑为绝对定位是相对于最近一个拥有相对定位样式的父元素。拥有相对定位的父元素不滚动，无相对定位属性的父元素滚动，而且无相对定位属性的元素为

有相对定位属性元素的子元素。


```js
.assistor {
    position: relative; /*关键点*/
    display: block;
    width: 500px;
    height: 300px;
    margin: 100px auto 0 auto;
    background-color: #ddd;
}
.parent {
    width: 500px;
    height: 300px;
    background-color: #888;
    overflow: auto; /*关键点*/
}
.child {
    position: absolute; /*关键点*/
    width: 120px;
    height: 120px;
    margin: 100px 50px;
    background-color: #333;
}
.placeholder {
    width: 1000px;
    height: 1000px;
}
```



```html
<div class="assistor">
    <div class="parent">
      <div class="child"></div>
      <div class="placeholder"></div>
    </div>
</div>

```
