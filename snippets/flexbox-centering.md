### Flexbox centering

使用`flexbox`，在父元素中水平和垂直方向居中一个子元素

#### HTML

```html
<div class="flexbox-centering">
  <div class="child">Centered content.</div>
</div>
```

#### CSS

```css
.flexbox-centering {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__flexbox-centering">
    <p class="snippet-demo__flexbox-centering__child">Centered content.</p>
  </div>
</div>

<style>
.snippet-demo__flexbox-centering {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 200px;
}
</style>

#### 解释

1. `display: flex` 使用flexbox布局.
2. `justify-content: center` 使子元素水平居中
3. `align-items: center` 使子元素垂直居中

#### 浏览器兼容性

<span class="snippet__support-note">⚠️ 需要前缀才能完全支持</span>

* https://caniuse.com/#feat=flexbox

<!-- tags: layout -->
