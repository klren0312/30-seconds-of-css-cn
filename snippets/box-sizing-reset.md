### 重置Box-sizing

重置 box-model，使`width`和 `height`不会被他们的 `border`或者`padding`影响.

#### CSS

```css
html {
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: inherit;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__box-sizing-reset">Demo</div>
</div>

<style>
.snippet-demo__box-sizing-reset {
  box-sizing: border-box;
  width: 200px;
  padding: 1.5em;
  color: #7983ff;
  font-family: sans-serif;
  background-color: white;
  border: 5px solid;
}
</style>

#### 解释

1. `box-sizing: border-box` 可以使添加的 `padding` 或者 `border`不影响组件的 `width` 或者 `height`.
2. `box-sizing: inherit`可以使一个组件遵守他父组件的  `box-sizing` 规则.

#### 浏览器兼容性

<span class="snippet__support-note">✅没啥警告.</span>

* https://caniuse.com/#feat=css3-boxsizing

<!-- tags: layout -->
