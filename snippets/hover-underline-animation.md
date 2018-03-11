### Hover underline animation

制作一个当文本被选中的时候的动态下划线

<small>**来源:** https://flatuicolors.com/</small>

#### HTML

```html
<p class="hover-underline-animation">Hover this text to see the effect!</p>
```

#### CSS

```css
.hover-underline-animation {
  display: inline-block;
  position: relative;
  color: #0087ca;
}
.hover-underline-animation::after {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #0087ca;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}
.hover-underline-animation:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}
```

#### Demo

<div class="snippet-demo">
  <p class="snippet-demo__hover-underline-animation">Hover this text to see the effect!</p>
</div>

<style>
.snippet-demo__hover-underline-animation {
  display: inline-block;
  position: relative;
  color: #0087ca;
}
.snippet-demo__hover-underline-animation::after {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #0087ca;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}
.snippet-demo__hover-underline-animation:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}
</style>

#### 解释

1. `display: inline-block` 给块级元素 `p` 一个 `inline-block`属性，防止下划线跨越整个父级元素，而不是仅仅是文本内容
2. `position: relative` 在元素上为伪元素建立一个相对定位的上下文.
3. `::after` 定义一个伪元素.
4. `position: absolute` 让伪元素脱离文档流，让他相对于父元素定位
5. `width: 100%` 确定伪元素达到宽度和文本长度一致
6. `transform: scaleX(0)` 将伪元素的x轴缩放初始化为0，这样它就没有宽度也就不可见
7. `bottom: 0` 和 `left: 0` 将它定位在区域的左下.
8. `transition: transform 0.25s ease-out` 意思是将在0.25s内转变 `transform`，并且使用`ease-out` 的过度效果.
9. `transform-origin: bottom right` 意思是转变的锚点指向区域的右下.
10. `:hover::after` 使用 `scaleX(1)` 将宽度转变成100%, 然后改变`transform-origin`
    到 `bottom left` ，这要锚点就被反转，当不选中的时候，就会转变到另一个方向

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没有警告.</span>

* https://caniuse.com/#feat=transforms2d
* https://caniuse.com/#feat=css-transitions

<!-- tags: animation -->
