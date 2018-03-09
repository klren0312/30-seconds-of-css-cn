### Disable selection

使内容不可选择

#### HTML

```html
<p>你可以选择我.</p>
<p class="unselectable">你不能选择我!</p>
```

#### CSS

```css
.unselectable {
  user-select: none;
}
```

#### Demo

<div class="snippet-demo">
  <p>你可以选择我.</p>
  <p class="snippet-demo__disable-selection">你不能选择我!</p>
</div>

<style>
.snippet-demo__disable-selection {
  user-select: none;
}
</style>

#### 解释

`user-select: none` 使文本不可选择.

#### 浏览器兼容性

<span class="snippet__support-note">⚠️ 需要前缀才能全部支持.</span>
<span class="snippet__support-note">⚠️ 这不是一个安全的方法，对于防止用户来复制内容</span>

* https://caniuse.com/#feat=user-select-none

<!-- tags: interactivity -->
