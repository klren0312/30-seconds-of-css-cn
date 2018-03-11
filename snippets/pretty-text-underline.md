### Pretty text underline

当不想下划线挡住文字下方的时候，这是一个比 `text-decoration: underline` 更好的方式。
原生实现的方式有 `text-decoration-skip-ink: auto`，但是它对于下划线只有很少的控制

#### HTML

```html
<p class="pretty-text-underline">Pretty text underline without clipping descending letters.</p>
```

#### CSS

```css
.pretty-text-underline {
  font-family: Arial, sans-serif;
  display: inline;
  font-size: 18px;
  text-shadow: 1px 1px 0 #f5f6f9, -1px 1px 0 #f5f6f9, -1px -1px 0 #f5f6f9, 1px -1px 0 #f5f6f9;
  background-image: linear-gradient(90deg, currentColor 100%, transparent 100%);
  background-position: 0 0.98em;
  background-repeat: repeat-x;
  background-size: 1px 1px;
}
.pretty-text-underline::-moz-selection {
  background-color: rgba(0, 150, 255, 0.3);
  text-shadow: none;
}
.pretty-text-underline::selection {
  background-color: rgba(0, 150, 255, 0.3);
  text-shadow: none;
}
```

#### Demo

<div class="snippet-demo">
  <p class="snippet-demo__pretty-text-underline">Pretty text underline without clipping descending letters.</p>
</div>

<style>
.snippet-demo__pretty-text-underline {
  font-family: Arial, sans-serif;
  display: inline;
  font-size: 18px !important;
  text-shadow: 1px 1px 0 #f5f6f9,
    -1px 1px 0 #f5f6f9,
    -1px -1px 0 #f5f6f9,
    1px -1px 0 #f5f6f9;
  background-image: linear-gradient(90deg, currentColor 100%, transparent 100%);
  background-position: 0 0.98em;
  background-repeat: repeat-x;
  background-size: 1px 1px;
}

.snippet-demo__pretty-text-underline::-moz-selection {
  background-color: rgba(0, 150, 255, 0.3);
  text-shadow: none;
}

.snippet-demo__pretty-text-underline::selection {
  background-color: rgba(0, 150, 255, 0.3);
  text-shadow: none;
}
</style>

#### Explanation

1. `text-shadow: ...` 有四个值用于偏移属性，覆盖了一个4x4 px区域来确保下划线有一个“厚”的覆盖了下行剪切的行的阴影。使用与背景相匹配的颜色。对于更大的字体，使用一个大的  `px` .
2. `background-image: linear-gradient(...)` 创建一个90度的当前文本颜色的渐变(`currentColor`).
3.  `background-*` 属性，将渐变大小变为1x1px，并且延x轴重复
4.  `::selection` 伪选择器确定了文本阴影不会干扰文本选择

#### 浏览器兼容性

<span class="snippet__support-note">⚠️ 下划线到文本的距离，取决于文本内部度量标准，，所以你必须确保每个人看到的字体是一样的(即不会根据os来决定系统字体).</span>

* https://caniuse.com/#feat=css-textshadow
* https://caniuse.com/#feat=css-gradients

<!-- tags: visual -->
