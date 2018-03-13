### Counter

计数器再本质上是一个由CSS维持的变量，它的值的增加是由CSS规则来追踪它们的使用次数

#### HTML

```html
<ul>
  <li>List item</li>
  <li>List item</li>
  <li>List item</li>
</ul>
```

#### CSS

```css
ul {
  counter-reset: counter;
}

li::before {
  counter-increment: counter;
  content: counters(counter, '.') ' ';
}
```

#### Demo

<div class="snippet-demo">
	<div class="snippet-demo__countable-section">
    <ul>
      <li>List item</li>
      <li>List item</li>
      <li>
        List item
        <ul>
          <li>List item</li>
          <li>List item</li>
          <li>List item</li>
        </ul>
      </li>
    </ul>
  </div>
</div>

<style>
  .snippet-demo__countable-section ul {
    counter-reset: counter;
    list-style-type: none;
  }

  .snippet-demo__countable-section li::before {
    counter-increment: counter;
    content: counters(counter, '.') ' ';
  }
</style>

#### Explanation

你可以使用一些HTML特征来创建一个有序列表

1. `counter-reset` 初始化一个计数器，这个属性的值就是计数器的名称。通常计数器从0开始计数。这个属性也可以被用来修改初始值。

2. `counter-increment` 在需要计数的元素里使用. 一旦 `counter-reset` 初始化,一个定时器的值将增加或减少.

3. `counter(name, style)` 显示一个计数器的值。在 `content` 属性中使用。这个函数能接受两个参数，第一特是计数器的名字，第二个参数可以是 `decimal` 或者 `upper-roman` (默认的是`decimal` ，这是计数的数字样式，阿拉伯数字或者罗马数字).

4. `counters(counter, string, style)` 显示一个计数器的值。通常在`content` 属性中使用. 这个函数接受三个参数，第一个是计数器的名称，第二个是计数器的分隔符，可以是一个字符串，第三个参数是计数的数字样式，可以是 `decimal` 或者 `upper-roman` (默认是`decimal`).

5. 一个CSS计数器在做提纲列表中非常有用，因为一个新的计数器实例能自动创建子元素。使用 `counters()` 函数, 可以在嵌套的列表中计数.

#### 浏览器兼容性

<span class="snippet__support-note">✅ 没有警告.</span>

* https://caniuse.com/#feat=css-counters

<!-- tags: visual, other -->
