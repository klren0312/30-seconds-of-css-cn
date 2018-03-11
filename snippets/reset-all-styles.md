### Reset all styles

用一个属性来重置所有样式到默认值.这将不会影响 `direction` 和 `unicode-bidi` 属性.

#### HTML

```html
<div class="reset-all-styles">
  <h4>Title</h4>
  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure id exercitationem nulla qui repellat laborum vitae, molestias tempora velit natus. Quas, assumenda nisi. Quisquam enim qui iure, consequatur velit sit?</p>
</div>
```

#### CSS

```css
.reset-all-styles {
  all: initial;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__reset-all-styles">
    <h3>Title</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure id exercitationem nulla qui repellat laborum vitae, molestias tempora velit natus. Quas, assumenda nisi. Quisquam enim qui iure, consequatur velit sit?</p>
  </div>
</div>

<style>
.snippet-demo__reset-all-styles {
  all: initial;
}
</style>

#### 解释

 `all` 属性允许你重置所有样式(继承或不继承)变为默认值.

#### 浏览器兼容性

<span class="snippet__support-note">⚠️ 微软的 Edge 正在考虑中.</span>

* https://caniuse.com/#feat=css-all

<!-- tags: visual -->
