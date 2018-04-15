### Offscreen

一个防弹的方式来完全在视觉上以及DOM定位上隐藏一个元素，同时仍然通过JavaScript允许访问和屏幕阅读器阅读它。当视觉障碍的用户需要更多上下文的时候，这个方法对于无障碍（ADA）开发非常有用。作为一个 的替代品，即替代不能被屏幕阅读器阅读的`display: none`或者占据DOM物理空间的`visibility: hidden`.

#### HTML

```html
<a class="button" href="http://pantswebsite.com">
  Learn More
  <span class="offscreen"> about pants</span>
</a>
```

#### CSS

```css
.offscreen {
  border: 0;
  clip: rect(0 0 0 0);
  height: 1px;
  margin: -1px;
  overflow: hidden;
  padding: 0;
  position: absolute;
  width: 1px;
}
```

#### Demo
<div class="snippet-demo">
  <a class="button" href="javascript:;">
    Learn More
    <span class="offscreen"> about pants</span>
  </a>
</div>

<style>
.snippet-demo__button {
  -webkit-appearance: none;
  appearance: none;
  background-color: #7983ff;
  border: none;
  border-radius: 0.25rem;
  color: #fff;
  cursor: pointer;
  display: inline-block;
  font-family: sans-serif;
  font-size: 1rem;
  padding: 0.8rem 1rem;
  text-align: center;
  text-decoration: none;
  transition: background-color 0.3s;
  width: auto;
}
.snippet-demo__button:hover { background-color: #717aef; }
.snippet-demo__offscreen {
  border: 0;
  clip: rect(0 0 0 0);
  height: 1px;
  width: 1px;
  margin: -1px;
  overflow: hidden;
  padding: 0;
  position: absolute;
}
</style>

#### 解释

1. 移出所有边框
2. 使用 `clip` 表明不会显示元素的任何部分
3. 给元素宽高都设为1px
4. 否定元素的宽高，通过使用 `margin: -1px`
5. 隐藏元素溢出的部分
6. 移出所有的内边距
7. 绝对定位元素，那样他将不能占据DOM的空间

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没有警告.</span>

(及时 `clip` 技术已经被废弃, 新的 `clip-path` 最近被非常有限的浏览器支持)

* https://caniuse.com/#search=clip

<!-- tags: layout, visual -->
