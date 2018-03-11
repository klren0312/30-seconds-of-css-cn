### Truncate text

如果文本超过一行，他将被截断，末尾用`…`代替.

#### HTML

```html
<p class="truncate-text">如果超过一行，就会被截断.</p>
```

#### CSS

```css
.truncate-text {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  width: 150px;
}
```

#### Demo

<div class="snippet-demo">
  <p class="snippet-demo__truncate-text">
    This text will be truncated if it exceeds 200px in width.
  </p>
</div>

<style>
.snippet-demo__truncate-text {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  width: 200px;
  margin: 0;
}
</style>

#### 解释

1. `overflow: hidden` 防止文本溢出他的尺寸(对于一个区域, 100% 的宽度和自适应的高度).
2. `white-space: nowrap` 防止文本超过一行的高度
3. `text-overflow: ellipsis` 如果文本超过它的尺寸，他将用省略号代替
4. `width: 200px;` 确保元素有尺寸，来知道何时转变省略号

#### 浏览器兼容性

<span class="snippet__support-note">⚠️ 只工作于一行文本.</span>

* https://caniuse.com/#feat=text-overflow

<!-- tags: layout -->
