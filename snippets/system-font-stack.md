### System font stack

使用操作系统原生的字体，使其更接近原生app感觉

#### HTML

```html
<p class="system-font-stack">This text uses the system font.</p>
```

#### CSS

```css
.system-font-stack {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu,
    Cantarell, 'Helvetica Neue', Helvetica, Arial, sans-serif;
}
```

#### Demo

<div class="snippet-demo">
  <p class="snippet-demo__system-font-stack">This text uses the system font.</p>
</div>

<style>
.snippet-demo__system-font-stack {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", Helvetica, Arial, sans-serif;
}
</style>

#### 解释

浏览器查询每个能用的字体，如果能用，就使用第一个能用的字体，以及如果不能找到字体（在系统中或者定义在CSS中的）就换到下一个字体

1. `-apple-system` is San Francisco, 在 iOS和macOS (非 Chrome )
2. `BlinkMacSystemFont` is San Francisco, 使用在 macOS 的Chrome
3. `Segoe UI` 使用在 Windows 10
4. `Roboto` 使用在 Android
5. `Oxygen-Sans` 使用在 GNU+Linux
6. `Ubuntu` 使用在 Linux
7. `"Helvetica Neue"` and `Helvetica` 使用在 macOS 10.10 以及更早 (用引号包裹，因为字体名中有个空格)
8. `Arial` 支持所有操作系统的字体
9. `sans-serif` 如果其他字体都不支持，就选用sans-serif 字体  

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没有警告.</span>

<!-- tags: visual -->
