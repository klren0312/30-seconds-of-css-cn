### 圆

使用纯CSS制作一个圆球。

#### HTML

```html
<div class="circle"></div>
```

#### CSS

```css
.circle {
  border-radius: 50%;
  width: 2rem;
  height: 2rem;
  background: #333;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__circle"></div>
</div>

<style>
.snippet-demo__circle {
  border-radius: 50%;
  width: 2rem;
  height: 2rem;
  background: #333;
}
</style>

#### 解释

`border-radius: 50%` 改变节点边框的圆角来创建一个圆。

因为一个圆要在给定的点中半径相同，所以 `width` 和 `height` 必须相同。 两个值不同会创建一个椭圆。

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没啥警告.</span>

* https://caniuse.com/#feat=border-radius

<!-- tags: visual -->
