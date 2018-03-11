### Overflow scroll gradient

当有很多内容需要滚动查看的时候，给溢出的元素一个渐变效果，使其更好的呈现

#### HTML

```html
<div class="overflow-scroll-gradient">
  <div class="overflow-scroll-gradient__scroller">
    Content to be scrolled
  </div>
</div>
```

#### CSS

```css
.overflow-scroll-gradient {
  position: relative;
}
.overflow-scroll-gradient::after {
  content: '';
  position: absolute;
  bottom: 0;
  width: 240px;
  height: 25px;
  background: linear-gradient(
    rgba(255, 255, 255, 0.001),
    white
  ); /* transparent keyword is broken in Safari */
  pointer-events: none;
}
.overflow-scroll-gradient__scroller {
  overflow-y: scroll;
  background: white;
  width: 240px;
  height: 200px;
  padding: 15px 0;
  line-height: 1.2;
  text-align: center;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__overflow-scroll-gradient">
    <div class="snippet-demo__overflow-scroll-gradient__scroller">
      Content to be scrolled
    </div>
  </div>
</div>

<style>
.snippet-demo__overflow-scroll-gradient {
  position: relative;
}
.snippet-demo__overflow-scroll-gradient::after {
  content: '';
  background: linear-gradient(rgba(255, 255, 255, 0.001), white);
  position: absolute;
  width: 240px;
  height: 25px;
  bottom: 0;
  pointer-events: none;
}
.snippet-demo__overflow-scroll-gradient__scroller {
  overflow-y: scroll;
  background: white;
  width: 240px;
  height: 200px;
  padding: 15px 0;
  line-height: 1.2;
  text-align: center;
}
</style>

<script>
document.querySelector('.snippet-demo__overflow-scroll-gradient__scroller').innerHTML = 'content '.repeat(100)
</script>

#### 解释

1. `position: relative` 在父元素上给伪元素建立一个相对定位的上下文
2. `::after` 定义一个伪元素
3. `background-image: linear-gradient(...)` 添加一个线性渐变，从透明变成白色(从上到下).
4. `position: absolute` 让伪元素脱离文档流，并且相对父元素定位
5. `width: 240px` 匹配滚动元素的大小 (一个有伪元素的父元素的子元素).
6. `height: 25px` 是渐变的伪元素的高,应该保持相对的小
7. `bottom: 0` 将伪元素定位在父元素的底部.
8. `pointer-events: none` 伪元素不能当作鼠标事件的目标，但是允许在它后面的文本被选择或交互.

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没有警告.</span>

* https://caniuse.com/#feat=css-gradients

<!-- tags: visual -->
