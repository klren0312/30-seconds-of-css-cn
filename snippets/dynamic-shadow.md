### Dynamic shadow

创建一个与`box-shadow`类似的阴影，但是阴影颜色是基于元素自己的颜色.

#### HTML

```html
<div class="dynamic-shadow-parent">
  <div class="dynamic-shadow"></div>
</div>
```

#### CSS

```css
.dynamic-shadow-parent {
  position: relative;
  z-index: 1;
}
.dynamic-shadow {
  position: relative;
  width: 10rem;
  height: 10rem;
  background: linear-gradient(75deg, #6d78ff, #00ffb8);
}
.dynamic-shadow::after {
  content: '';
  width: 100%;
  height: 100%;
  position: absolute;
  background: inherit;
  top: 0.5rem;
  filter: blur(0.4rem);
  opacity: 0.7;
  z-index: -1;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__dynamic-shadow-parent">
    <div class="snippet-demo__dynamic-shadow"></div>
  </div>
</div>

<style>
.snippet-demo__dynamic-shadow-parent {
  position: relative;
  z-index: 1;
}
.snippet-demo__dynamic-shadow {
  position: relative;
  width: 10rem;
  height: 10rem;
  background: linear-gradient(75deg, #6d78ff, #00ffb8);
}
.snippet-demo__dynamic-shadow::after {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  background: inherit;
  top: 0.5rem;
  filter: blur(0.4rem);
  opacity: 0.7;
  z-index: -1;
}
</style>

#### 解释

这个片段需要一个复杂的上下文堆砌才能实现, 这样伪元素将被定位在元素自身的下方，并且一直可见

1. `position: relative` 在父元素上为子元素建立一个笛卡尔定位的上下文
2. `z-index: 1` 简历一个新的堆叠文本
3. `position: relative` 在子元素上建立一个伪元素定位的上下文 
4. `::after` 定义一个伪元素.
5. `position: absolute` 使伪元素脱离文档流，将其定位到相对与父元素的地方
6. `width: 100%` 和 `height: 100%` 将父元素的尺寸填充进伪元素中，使他们大小相等。
7. `background: inherit` 可以让伪元素继承他的父元素的线性渐变背景
8. `top: 0.5rem` 将伪元素从其父元素的位置向下偏移.
9. `filter: blur(0.4rem)` 将伪元素高斯模糊，从而创建一个影子的样式
10. `opacity: 0.7` 设置伪元素的透明度
11. `z-index: -1` 将伪元素定位到父元素的下层

#### 浏览器兼容

<span class="snippet__support-note">⚠️ 需要前缀才能全部兼容.</span>

* https://caniuse.com/#feat=css-filters

<!-- tags: visual -->
