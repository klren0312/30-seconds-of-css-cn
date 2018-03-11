### Popout menu

鼠标移动到元素的时候，弹出一个菜单

#### HTML

```html
<div class="reference">
  <div class="popout-menu">
    Popout menu
  </div>
</div>
```

#### CSS

```css
.reference {
  position: relative;
}
.popout-menu {
  position: absolute;
  visibility: hidden;
  left: 100%;
}
.reference:hover > .popout-menu {
  visibility: visible;
}
```

#### Demo

<div class="snippet-demo">
  <div class="snippet-demo__reference">
    <div class="snippet-demo__popout-menu">
      Popout menu
    </div>
  </div>
</div>

<style>
.snippet-demo__reference {
  background: linear-gradient(135deg, #ff4c9f, #ff7b74);
  height: 75px;
  width: 75px;
  position: relative;
  will-change: transform;
}
.snippet-demo__popout-menu {
  position: absolute;
  visibility: hidden;
  left: 100%;
  background: #333;
  color: white;
  font-size: 0.9rem;
  padding: 0.4rem 0.8rem;
  width: 100px;
  text-align: center;
}
.snippet-demo__reference:hover > .snippet-demo__popout-menu {
  visibility: visible;
}
</style>

#### 解释

1. `position: relative` 为子元素建立一个相对定位的上下文.
2. `position: absolute` 让弹出菜单脱离文档流来相对父元素定位
3. `left: 100%` 将弹出菜单向左移动到他的父元素的宽度100%
4. `visibility: hidden` 先将将弹出菜单隐藏，并且允许改变(不同于 `display: none`).
5. `.reference:hover > .popout-menu` 意思是当 `.reference` 触发, 会立即选择 `.popout-menu`这个类下的子元素，并改变它们的 `visibility` 为 `visible`,就弹出菜单 

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没有警告.</span>

<!-- tags: interactivity -->
