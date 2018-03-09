### 自定义css变量

包含特殊值的 CSS 变量可以在整个文档中使用

#### HTML

```html
<p class="custom-variables">CSS is awesome!</p>
```

#### CSS

```css
:root {
  --some-color: #da7800;
  --some-keyword: italic;
  --some-size: 1.25em;
  --some-complex-value: 1px 1px 2px whitesmoke, 0 0 1em slategray, 0 0 0.2em slategray;
}

.custom-variables {
  color: var(--some-color);
  font-size: var(--some-size);
  font-style: var(--some-keyword);
  text-shadow: var(--some-complex-value);
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__custom-variables">
    <p>CSS is awesome!</p>
  </div>
</div>

<style>
.snippet-demo__custom-variables {
  --some-color: #686868;
  --some-keyword: italic;
  --some-size: 1.25em;
  --some-complex-value: 1px 1px 2px whitesmoke, 0 0 1em slategray , 0 0 0.2em slategray;
}

.snippet-demo__custom-variables p {
  color: var(--some-color);
  font-size: var(--some-size);
  font-style: var(--some-keyword);
  text-shadow: var(--some-complex-value);
}
</style>

#### 解释

变量通过`:root` 这个CSS伪类定义到全局，这个伪类可以匹配文档树的根元素.变量也能被局限于一个选择器中，如果被定义在一个块里。 

声明一个变量，可以使用 `--variable-name:`.

在文档中使用变量，可以使用这个函数`var(--variable-name)` .

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没啥警告.</span>

* https://caniuse.com/#feat=css-variables

<!-- tags: other -->
