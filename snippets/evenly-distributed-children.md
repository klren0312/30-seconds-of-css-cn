### Evenly distributed children

子元素均匀分布在父元素里

#### HTML

```html
<div class="evenly-distributed-children">
  <p>Item1</p>
  <p>Item2</p>
  <p>Item3</p>
</div>
```

#### CSS

```css
.evenly-distributed-children {
  display: flex;
  justify-content: space-between;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__evenly-distributed-children">
    <p>Item1</p>
    <p>Item2</p>
    <p>Item3</p>
  </div>
</div>

<style>
.snippet-demo__evenly-distributed-children {
  display: flex;
  width: 100%;  
  justify-content: space-between;
}
</style>

#### 解释

1. `display: flex` 应用flex布局.
2. `justify-content: space-between` 将子元素水平方向均匀分布. 第一个子元素定位在页面的左边缘，最后一个元素定位在页面右边缘。

或者使用 `justify-content: space-around` 来使子元素从他们周围分散，而不是他们之间分散.

#### 浏览器兼容性
<span class="snippet__support-note">⚠️ 需要前缀才能完全支持.</span>

* https://caniuse.com/#feat=flexbox

<!-- tags: layout -->
