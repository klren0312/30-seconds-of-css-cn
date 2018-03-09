### 宽高成比例

给一个元素可变的宽度，它将确保其高度保持适当的响应形式(也就是说，它的宽度和高度比例是保持不变的).

#### HTML

```html
<div class="constant-width-to-height-ratio"></div>
```

#### CSS

```css
.constant-width-to-height-ratio {
  background: #333;
  width: 50%;
  padding-top: 50%;
}
```

#### Demo

更改你的浏览器窗口，来查看元素的比例是保持不变的

<div class="snippet-demo">
  <div class="snippet-demo__constant-width-to-height-ratio"></div>
</div>

<style>
.snippet-demo__constant-width-to-height-ratio {
  background: #333;
  width: 50%;
  padding-top: 50%;
}
</style>

#### 解释

`padding-top` 使用在 `::before` 伪元素上可以使元素的高度与他的宽度成比例. `100% `意思是元素的高度永远是 `100% `的宽度, 创建了一个响应式的空间.

这个方法通常也使用在放在元素里的内容.

#### 浏览器兼容性

<span class="snippet__support-note">✅没啥警告.</span>

<!-- tags: layout -->
