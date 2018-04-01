### :not selector

 `:not` 伪选择器对于定义一组元素非常有用，同时使最后（或者指定）的元素无样式

#### HTML

```html
<ul class="css-not-selector-shortcut">
  <li>One</li>
  <li>Two</li>
  <li>Three</li>
  <li>Four</li>
  <li>Five</li>
</ul>
```

#### CSS

```css
.css-not-selector-shortcut {
  display: flex;
}

li {
  list-style-type: none;
  margin: 0;
  padding: 0 0.75rem;
}

li:not(:last-child) {
  border-right: 2px solid #d2d5e4;
}
```

#### Demo

<div class="snippet-demo">
  <ul class="snippet-demo__css-not-selector-shortcut">
    <li>One</li>
    <li>Two</li>
    <li>Three</li>
    <li>Four</li>
    <li>Five</li>
  </ul>
</div>

<style>
.snippet-demo__css-not-selector-shortcut {
  display: flex;
  padding: 0;
}

.snippet-demo__css-not-selector-shortcut li {
  list-style-type: none;
  margin: 0;
  padding: 0 0.75rem;
}

.snippet-demo__css-not-selector-shortcut li:not(:last-child) {
  border-right: 2px solid #d2d5e4
}
</style>

#### 解释

`li:not(:last-child)` 指定样式应该用于所有 `li` 元素，除了 `:last-child`.

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没有警告.</span>

* https://caniuse.com/#feat=css-sel3

<!-- tags: visual -->
