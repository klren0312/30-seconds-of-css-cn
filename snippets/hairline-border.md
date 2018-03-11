### Hairline border

给一个元素一个等于1像素宽的边框，可以看的很尖锐清脆

#### HTML

```html
<div class="hairline-border">text</div>
```

#### CSS

```css
.hairline-border {
  box-shadow: 0 0 0 1px;
}

@media (min-resolution: 2dppx) {
  .hairline-border {
    box-shadow: 0 0 0 0.5px;
  }
}

@media (min-resolution: 3dppx) {
  .hairline-border {
    box-shadow: 0 0 0 0.33333333px;
  }
}

@media (min-resolution: 4dppx) {
  .hairline-border {
    box-shadow: 0 0 0 0.25px;
  }
}
```

#### Demo

<div class="snippet-demo">
  <p class="snippet-demo__hairline-border">Text with a hairline border around it.</p>
</div>

<style>
.snippet-demo__hairline-border {
  box-shadow: 0 0 0 1px;
}

@media (min-resolution: 2dppx) {
  .snippet-demo__hairline-border {
    box-shadow: 0 0 0 0.5px;
  }
}

@media (min-resolution: 3dppx) {
  .snippet-demo__hairline-border {
    box-shadow: 0 0 0 0.33333333px;
  }
}

@media (min-resolution: 4dppx) {
  .snippet-demo__hairline-border {
    box-shadow: 0 0 0 0.25px;
  }
}
</style>

#### 解释

1. `box-shadow`, 当只使用spread属性的时候, 会增加可以使用子元素\*的伪边框.
2. 使用`@media (min-resolution: ...)` 来检查设备的分辨率 (`1dppx` = 96 DPI),
   设置`box-shadow` 的spread属性等于 `1 / dppx`.

#### 浏览器兼容性

<span class="snippet__support-note">⚠️ 需要完全支持替代语法和javascript用户代理检查.</span>

* https://caniuse.com/#feat=css-boxshadow
* https://caniuse.com/#feat=css-media-resolution

<hr>

\*Chrome 不支持子元素的  `border`变量. Safari 不支持子元素的`box-shadow`. Firefox 的子元素都支持.

<!-- tags: visual -->
