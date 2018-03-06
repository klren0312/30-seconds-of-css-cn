### Clearfix

确保元素清楚了子元素对其的影响。

###### Note: 这只有在你使用float来构建布局的情况下有用。请考虑使用一个现代的方式比如flexbox布局或者grid布局。

#### HTML

```html
<div class="clearfix">
  <div class="floated">float a</div>
  <div class="floated">float b</div>
  <div class="floated">float c</div>
</div>
```

#### CSS

```css
.clearfix::after {
  content: '';
  display: block;
  clear: both;
}

.floated {
  float: left;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__clearfix">
    <div class="snippet-demo__floated">float a</div>
    <div class="snippet-demo__floated">float b</div>
    <div class="snippet-demo__floated">float c</div>
  </div>
</div>

<style>
.snippet-demo__clearfix::after {
  content: '';
  display: block;
  clear: both;
}

.snippet-demo__floated {
  float: left;
}
</style>

#### 解释

1. `.clearfix::after` 定义一个伪元素。
2. `content: ''` 允许这个伪元素去影响布局.
3. `clear: both` 表面元素的左边，右边或者左右两边不能与邻近的浮动元素在相同的格式化上下文中。

#### 浏览器兼容性

<span class="snippet__support-note">⚠️ 这段代码要正常工作，就要确保在容器中没有未浮动的子元素，以及在清除浮动的容器时没有高浮动的元素，但是要在相同的格式化上下文中(比如 浮动的列).</span>

<!-- tags: layout -->
