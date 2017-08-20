## CSS入门
#### 12.1 css入门
* CSS引入方式
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
  border: inherit;
}
</style>;
```
#### 13.1 CSS选择器[上]
* 元素的分类
  * 区块：能换行的标签元素
  * 内联: 不换行的标签元素
* 基本选择器
  * 通用选择器
  ```css
  /* 通用选择器会将所有元素匹配并配置样式 */
  * {
    border: 1px solid red;
  }
  ```
  * 元素选择器
  ```css
  p { 
    color: red;
  } 
  ```
  * ID 选择器
  ```css
  #abc { 
    font-size: 20px;
  }
  <p id="abc">段落</p>
  ```
  * 类选择器
  ```css
  <b class="abc">加粗</b>
  <span class="abc">无</span>
  .abc { 
    border: 1px solid red;
  }
  ```
  * 属性选择器
  ```css
  [href] { 
    color: orange;
  }
  <!-- 匹配属性值的属性选择器 -->
  [type="password"] { 
    border: 1px solid red;
  }
  <!-- CSS3正则匹配属性选择器 -->
  <!-- ^开头 -->
  [href^="http"] { 
    color: orange;
  }
  <!-- $结尾 -->
  [href$=".com"] { 
    color: orange;
  }
  <!-- 包含指定字符的属性选择器 -->
  [href*="baidu"] { 
    color: orange;
  }
  ```
* 复合选择器
  * 分组选择器
  ```css
  p,b,i,span { 
    color: red;
  }
  ```
  * 后代选择器
  <!-- 选择<p>元素内部所有<b>元素。不在乎<b>的层次深度 -->
  ```css
  p b { 
    color: red;
  }
  ```
  * 子选择器
  ```css
  ul > li { 
    border: 1px solid red;
  }
  <ul>
    <li> 我是儿子 <ol>
            <li> 我是孙子 </li>
            <li> 我是孙子 </li>
        </ol>
    </li>
    <li> 我是儿子 </li>
    <li> 我是儿子 </li>
  </ul>
  ```
  * 相邻兄弟选择器
  <!-- 相邻兄弟选择器匹配和第一个元素相邻的第二个元素 -->
  ```css
  p + b { 
    color: red;
  }
  ```
  * 普通兄弟选择器
  <!-- 普通兄弟选择器匹配和第一个元素后面的所有元素 -->
  ```css
  p ~ b { 
    color: red;
  }
  ``` 
* 伪元素选择器
  * ::first-line 块级首行
  ```css
  ::first-line { 
    color: red;
  }
  ```
  * ::first-letter 块级首字母
  ```css
  ::first-letter { 
    color: red;
  }
  ```
  * ::before 文本前插入
  ```css
  a::before { 
    content: '点击-';
  }
  ```
  * ::after 文本后插入
  ```css
  a::after { 
    content: '-请进';
  }
  ```
  * ::selection 选中后样式
  ```css
  ::selection {
    color: red;
  }
  ```
#### 13.1 CSS选择器[下]
伪类选择器
* 结构型伪类
  * 根元素选择器
  ```css
  :root {
    border: 1px solid red;
  }
  ```
  * 子元素选择器
  ```css
  <!-- 伪类都需要加上前置选择器来限制范围 -->
  ul > li:first-child {
    color: gold;
  }
  ul > li:last-child {
    color: black;
  }
  ul > li:only-child {
    color: black;
  }
  ul > li:nth-child(2) {
    color: blue;
  }
  ul > li:nth-last-child(2) {
    color: orange;
  }
  ```
* UI伪类
```css
input:enabled {
  border: 1px solid red;
}
input:disabled {
  border: 1px solid blue;
}
input:checked {
  display: none;
}
input:valid {
  border: 3px solid green;
}
input:invalid {
  border: 1px solid red;
}
```
* 动态伪类
```css
a:link {
  color: red;
}
a:visited {
  color: orange;
}
a:hover {
  color: pink;
}
a:active {
  color: blue;
}
input:focus {
  border: 3px solid greenyellow;
}
```
* 其它伪类选择器
```css
a:not([href*="baidu"]) {
  color: pink;
}
p:empty {
  display: none;
}
:lang(en) {
  color: orange;
}
<!-- 当锚点定位到的时候 -->
:target {
  color: red;
}
```
#### 14 CSS颜色与度量单位
* 颜色
  * 颜色名称 black
  ```css
  p {
    color: red;
  }
  ```
  * 十六进制代码 #000000
  ```css
  p {
    color: #ff0000;
  }
  ```
  * 十进制代码 0,0,0
  ```css
  p {
    color: rgb(255,0,0);
  }
  ```
* 度量单位
  * 绝对长度单位
  * 相对长度单位


