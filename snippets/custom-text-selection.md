### Custom text selection

改变文本选中后的样式.

#### HTML

```html
<p class="custom-text-selection">选中这个文本，即可看到样式改变</p>
```

#### CSS

```css
::selection {
  background: aquamarine;
  color: black;
}
.custom-text-selection::selection {
  background: deeppink;
  color: white;
}
```

#### Demo

<div class="snippet-demo">
  <p class="snippet-demo__custom-text-selection">选中这个文本，即可看到样式改变.</p>
</div>

<style>
.snippet-demo__custom-text-selection::selection {
  background: deeppink;
  color: white;
}
.snippet-demo__custom-text-selection::-moz-selection {
  background: deeppink;
  color: white;
}
</style>

#### 解释

`::selection` 定义一个伪选择器，用在一个文本元素被选择的时候。如果你不能联系到其他选择器，你的样式将被用到全局，所有元素被选择后都会更改。

#### 浏览器兼容性

<span class="snippet__support-note">⚠️需要完整支持前缀并且不在规范中</span>

* https://caniuse.com/#feat=css-selection

<!-- tags: visual -->
