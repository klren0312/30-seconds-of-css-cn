### Display Table Centering

水平和垂直方向居中一个子节点，可以通过再父节点中使用`display: table` (作为`flexbox`的替代方案).

#### HTML

```html
<div class="container">
  <div class="center">
    <span>中心内容</span>
  </div>
</div>
```

#### CSS

```css
.container {
  border: 1px solid #333;
  height: 250px;
  width: 250px;
}

.center {
  display: table;
  height: 100%;
  width: 100%;
}

.center > span {
  display: table-cell;
  text-align: center;
  vertical-align: middle;
}
```

#### Demo
<div class="snippet-demo">
  <div class="snippet-demo__container">
    <div class="snippet-demo__center">
      <span>Centered content</span>
    </div>
  </div>
</div>

<style>
.snippet-demo__container {
  border: 1px solid #333;
  height: 250px;
  width: 250px;
}
.snippet-demo__center {
  display: table;
  height: 100%;
  width: 100%;
}
.snippet-demo__center > span {
  display: table-cell;
  text-align: center;
  vertical-align: middle;
}
</style>

#### 解释

1. `display: table` 在 '.center'的节点上允许元素具有类似于 `<table>` HTML标签的行为.
2. 100%的高度和宽度在 '.center'的节点上，允许元素在他的父元素中填充可用的位置.
3. `display: table-cell` 在 '.center > span'节点上允许元素具有类似于` <td>`HTML标签的行为.
2. `text-align: center` 在 '.center > span'节点的水平方向居中子节点.
2. `vertical-align: middle` 在 '.center > span'节点的垂直方向居中子节点.

最外层的父元素(比如这个例子中的'.container' )必须由固定的长和宽.

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没有警告.</span>

* https://caniuse.com/#search=display%3A%20table

<!-- tags: layout -->
