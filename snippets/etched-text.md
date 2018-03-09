### Etched text

创建一种文本被‘蚀刻’或者浮刻在背景上的效果

#### HTML

```html
<p class="etched-text">I appear etched into the background.</p>
```

#### CSS

```css
.etched-text {
  text-shadow: 0 2px white;
  font-size: 1.5rem;
  font-weight: bold;
  color: #b8bec5;
}
```

#### Demo

<div class="snippet-demo">
  <p class="snippet-demo__etched-text">I appear etched into the background.</p>
</div>

<style>
.snippet-demo__etched-text {
  font-size: 1.5rem;
  font-weight: bold;
  color: #b8bec5;
  text-shadow: 0 2px 0 white;
}
</style>

#### 解释

`text-shadow: 0 2px white` 创建一个白色的阴影，相对于初始位置水平偏移为`0px` 和 垂直偏移为`2px` 

背景必须要比阴影更黑才能有效果

文本颜色应该稍微暗点，使它看起来像刻在背景上一样

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没有警告.</span>

* https://caniuse.com/#feat=css-textshadow

<!-- tags: visual -->
