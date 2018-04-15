### Transform Centering

在父元素中使用`position: absolute` 和 `transform: translate()` (一个替代 `flexbox` 或者`display: table`的方法)在垂直和水平方向居中子元素。与 `flexbox`相似, 这个方法不需要你知道你父元素或者子元素的宽高，所以他是一个用于响应式应用的方法。

#### HTML

```html
<div class="parent">
  <div class="child">Centered content</div>
</div>
```

#### CSS

```css
.parent {
  border: 1px solid #333;
  height: 250px;
  position: relative;
  width: 250px;
}

.child {
  left: 50%;
  position: absolute;
  top: 50%;
  transform: translate(-50%, -50%);
}
```

#### Demo
<div class="snippet-demo">
  <div class="snippet-demo__parent">
    <div class="snippet-demo__child">Centered content</div>
  </div>
</div>

<style>
.snippet-demo__parent {
  border: 1px solid #333;
  height: 250px;
  position: relative;
  width: 250px;
}
.snippet-demo__child {
  left: 50%;
  position: absolute;
  top: 50%;
  transform: translate(-50%, -50%);
}
</style>

#### 解释

1. `position: absolute` 在子元素上允许它基于包含他的区域中定位
2. `left: 50%` 和 `top: 50%` 抵消子元素在包含他的区域中左边和上边50%的距离.
3. `transform: translate(-50%, -50%)` 允许子节点的宽高被否定，他将在垂直和水平方向居中

笔记: 固定父元素的宽高是为了demo需要，其实并不需要.

#### 浏览器兼容性

<span class="snippet__support-note">⚠️ 需要添加前缀才能完全支持.</span>

* https://caniuse.com/#search=transform

<!-- tags: layout -->
