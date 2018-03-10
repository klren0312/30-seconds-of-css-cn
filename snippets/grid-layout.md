### Grid layout

使用 `grid` 构建的网页架构.

#### HTML

```html
<div class="grid-layout">
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">
    Content
    <br>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
  </div>
  <div class="footer">Footer</div>
</div>
```

#### CSS

```css
.grid-layout {
  display: grid;
  grid-gap: 10px;
  grid-template-columns: repeat(3, 1fr);
  grid-template-areas:
    'sidebar header header'
    'sidebar content content'
    'sidebar footer  footer';
  color: white;
}
.grid-layout > div {
  background: #333;
  padding: 10px;
}
.sidebar {
  grid-area: sidebar;
}
.content {
  grid-area: content;
}
.header {
  grid-area: header;
}
.footer {
  grid-area: footer;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__grid-layout">
    <div class="box snippet-demo__grid-layout__header">Header</div>
    <div class="box snippet-demo__grid-layout__sidebar">Sidebar</div>
    <div class="box snippet-demo__grid-layout__content">Content
      <br> Lorem ipsum dolor sit amet, consectetur adipisicing elit.
    </div>
    <div class="box snippet-demo__grid-layout__footer">Footer</div>
  </div>
</div>

<style>
.snippet-demo__grid-layout {
  margin: 1em;
  display: grid;
  grid-gap: 10px;
  grid-template-columns: repeat(3, 1fr);
  grid-template-areas:
    "sidebar header header"
    "sidebar content content"
    "sidebar  footer  footer";
  background-color: #fff;
  color: white;
}
.snippet-demo__grid-layout > div {
  background: #333;
  padding: 10px;
}
.snippet-demo__grid-layout__sidebar {
    grid-area: sidebar;
}
.snippet-demo__grid-layout__content {
    grid-area: content;
}
.snippet-demo__grid-layout__header {
    grid-area: header;
}
.snippet-demo__grid-layout__footer {
    grid-area: footer;
}
</style>

#### 解释

1. `display: grid` 使用grid布局.
2. `grid-gap: 10px` 定义元素间间隔.
3. `grid-template-columns: repeat(3, 1fr)` 定义三个相同defines 3 columns of the same size.
4. `grid-template-areas` 定义grid的区域名称
5. `grid-area: sidebar` 元素使用区域的名称为`sidebar`.

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没有警告.</span>

* https://caniuse.com/#feat=css-grid

<!-- tags: layout -->
