## CSS入门
#### 12.1 css入门
* css引入方式
  * 元素内嵌样式
  ```html
  <p style="color:red;font-size:50px;">这是一段文本</p>
  ```
  * 文档内嵌样式
  ```html
  <style>
    p {
      color: blue;
      font-size: 40px;
    }
  </style>
  ```
  * 外部引用样式
  ```html
  <link rel="stylesheet" href="./styles/demo12.css">
  ```
* css样式表层叠优先级(从低到高, 高级别的样式覆盖低级别样式)
  * 浏览器样式（元素自身携带的样式）
  * 外部引入样式（使用<link>引入的样式）
  * 文档内嵌样式（使用\<style>元素设置）
  * 元素内嵌样式（使用style 属性设置）
* 强行设置最高优先级(!important)
```css
color: green !important;
```
* 样式的继承:样式继承只适用于元素的外观（文字、颜色、字体等）而元素在页面上的布局样式则不会被继承。
  如果继承这种样式，就必须使用强制继承：[inherit]。
```html
<p style="color:red;">这是<b>HTML5</b></p>
```
```html
<p>这是<b>HTML5</b></p>
<style type="text/css">
p { 
  border: 1px solid red;
} 
b { 
  border : inherit;
}
</style>;
```
