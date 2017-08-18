## 一. HTML5概述
#### 1.1 HTML5 是什么
* HTML5 是继 HTML4.01 和 XHTML1.0 之后的超文本标记语言的最新版本。
* 其中最重要的三项技术分别为：
  * HTML5 核心规范（标签元素）
  * CSS（层叠样式表第三代）
  * JavaScript
* HTML5 核心
  * 新的语义元素
  * 增强的Web 表单
  * 音频和视频
  * 通过 JavaScript 绘图的 Canvas
#### 1.2 基本样式
* HTML基本格式
```html
<!DOCTYPE html> <!-- 文档类型声明 -->
<html lang="en"> 
<head> <!-- 文档元数据开始 -->
  <meta charset="UTF-8"> <!-- 声明字符编码 -->
  <!-- 移动设备自适应 -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- ie兼容 -->
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>基本格式</title> <!-- 设置文档标题 -->
</head>
<body> <!-- 表示 HTML 文档内容 -->
  <a href="http://www.baidu.com"></a> <!-- 一个超链接元素（标签） -->
</body>
</html> <!-- 表示 HTML 文档结束 -->
```
#### 1.3 文本元素

#### 1.4 超链接和路径
* a标签
  * href属性
  ```html
  <a href="http://www.baidu.com">百度</a>
  ```
  * target属性
    * _blank 在新窗口或标签页中打开文档
    * _parent 在父窗框组（frameset）中打开文档
    * _self 在当前窗口打开文档（默认）
    * _top 在顶层窗口打开文档
  ```html
  <a href="http://www.baidu.com" target="_blank">百度</a>
  ```
* 相对和绝对路径
  * 绝对路径
  ```html
  <a href="file:///D:/lesson1/code/index2.html">index2</a>
  ```
  * 相对路径
  ```html
  <a href="index2.html">index2</a>
  ```


