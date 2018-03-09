### Bouncing loader

创建一个弹跳加载动画。

#### HTML

```html
<div class="bouncing-loader">
  <div></div>
  <div></div>
  <div></div>
</div>
```

#### CSS

```css
@keyframes bouncing-loader {
  from {
    opacity: 1;
    transform: translateY(0);
  }
  to {
    opacity: 0.1;
    transform: translateY(-1rem);
  }
}
.bouncing-loader {
  display: flex;
  justify-content: center;
}
.bouncing-loader > div {
  width: 1rem;
  height: 1rem;
  margin: 3rem 0.2rem;
  background: #8385aa;
  border-radius: 50%;
  animation: bouncing-loader 0.6s infinite alternate;
}
.bouncing-loader > div:nth-of-type(2) {
  animation-delay: 0.2s;
}
.bouncing-loader > div:nth-of-type(3) {
  animation-delay: 0.4s;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__bouncing-loader">
  	<div></div>
    <div></div>
    <div></div>
  </div>
</div>

<style>
@keyframes bouncing-loader {
  from {
    opacity: 1;
    transform: translateY(0);
  }
  to {
    opacity: 0.1;
    transform: translateY(-1rem);
  }
}
.snippet-demo__bouncing-loader {
  display: flex;
  justify-content: center;
}
.snippet-demo__bouncing-loader > div {
  width: 1rem;
  height: 1rem;
  margin: 3rem 0.2rem;
  background: #8385aa;
  border-radius: 50%;
  animation: bouncing-loader 0.6s infinite alternate;
}
.snippet-demo__bouncing-loader > div:nth-child(2) {
  animation-delay: 0.2s;
}
.snippet-demo__bouncing-loader > div:nth-child(3) {
  animation-delay: 0.4s;
}
</style>

#### 解释

注意: `1rem` 就是 `16px`.

1. `@keyframes`定义一个有两个状态的动画, 改变节点的透明度 `opacity`, 以及在2D平面的翻转`transform: translateY()`.

2. `.bouncing-loader`是跳动圆圈的父容器，以及使用 `display: flex`
   和 `justify-content: center` 来将它们定位到中间.

3. 使用 `.bouncing-loader > div`, 我们赋给`div`相同样式. 给 `div`的长宽为 `1rem`, 使用 `border-radius: 50%` 改变圆角.

4. `margin: 3rem 0.2rem` 给每个圆球上下间隔 `3rem` 以及左右间隔为 `0.2rem` 所以他们不会直接碰到各自, 这也给他们喘气的空间。

5. `animation`是下面三个特性的整合写法 `animation-name`, `animation-duration`, `animation-iteration-count`, `animation-direction` 。

6. `animation-delay` 用来让第二个和第三个 `div`的效果分开, 所以这样每个圆球的动作都不会在同一个时间开始.

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没啥警告</span>

* https://caniuse.com/#feat=css-animation

<!-- tags: animation -->
