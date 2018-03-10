### Gradient text

给文本渐变颜色.

#### HTML

```html
<p class="gradient-text">Gradient text</p>
```

#### CSS

```css
.gradient-text {
  background: -webkit-linear-gradient(pink, red);
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
}
```

#### Demo

<div class="snippet-demo">
  <p class="snippet-demo__gradient-text">
    Gradient text
  </p>
</div>

<style>
.snippet-demo__gradient-text {
  background: -webkit-linear-gradient(pink, red);
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  font-size: 2rem;
  font-weight: bold;
  margin: 0;
}
</style>

#### 解释

1. `background: -webkit-linear-gradient(...)` 给文本元素渐变效果.
2. `webkit-text-fill-color: transparent` 用透明颜色填充文本.
3. `webkit-background-clip: text` 用文本剪切背景，然后渐变背景便赋给文本颜色

#### 浏览器兼容性

<span class="snippet__support-note">⚠️ 使用了非标准属性.</span>

* https://caniuse.com/#feat=text-stroke

<!-- tags: visual -->
