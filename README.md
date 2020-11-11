# html 笔记

超文本标记语言（HyperText Markup language, 简称 HTML）是一种用于创建网页的标准标记语言。

> 对于中文网页需要使用<meta charset='utf-8'>声明编码，否则会出现乱码。有些浏览器会设置 GBK 为默认编码，则需要设置为<meta charset='gbk'>

---

## 实例

```html
<!DOCTYPE html> 
<html>
<head>
<meta charset='utf-8'>
<title></title>
</head>
<body>

</body>
</html>
```

解析：
- `<!DOCTYPE html>` 声明为 HTML5 文档
- `<html></html>` HTML 页面的根元素
- `<head></head>` 头标签，里面的内容是给浏览器看的
- `<body></body>` 身体标签，里面的内容是给人看的
- `<title></title>` 在 head 里面的，文档的标题标签
- `<meta />` meta 标签声明 charset ,其他还有很多用法
- `<h1></h1>` h1-h6 6级标题的第一级
- `<p></p>` 段落标签
- `<hr />` 水平线标签
- `<br />` 换行标签

---

## HTML 文档后缀名

- .html
- .htm

以上两种没有区别（因为历史原因导致有htm后缀，因为曾经不支持4位字母的后缀名）

---

## 标签种类

- 标签一般是成对出现的，如`<html></html>`,分别叫开始标签和闭合标签。
- 也有单标签，如`<br />` 换行标签（未来的html可能要求所有标签都关闭，尽量养成好习惯吧）。 

> Tip：尽管`<P>`等同于`<p>`，但还是推荐使用小写标签。

---

## 常用标签

- 标题： `<h1></h1>` h1-h6 6级标题
- 段落： `<p></p>` 段落标签
- 链接： `<a href="https://www.baidu.com/"></a>` 链接标签，链接
- 图像： `<img src="./localhost/imgPath" width="120" height="230" alt="big boat" />` 图像标签, src 是源属性（source），长宽控制, alt 替代文本属性（**注意：每个图像都需要单独加载，慎用图片**）

---

## HTML 属性

如 `<a href="https://www.baidu.com/"></a>` 这里的 href 就是 name 的属性。  
- 属性一般有 属性值 和 属性名 组成，属性值一般用双引号引起来，当然单引号也是没有问题的。
- 属性名和属性值一般都使用小写字母（对大小写不敏感）  

---

## html 注释

`<!-- 这是一个注释 -->`  

## 格式化标签

格式化标签很多，仅需要记住几个有意思的就够了。

- `<b>` 加粗
- `<i>` 斜体
- `<sub>` 下标标签
- `<sup>` 上标标签
- `<ins>` 插入字/下划线
- `<del>` 删除线

---

## a 标签的使用

- 页面跳转：`<a href="http://www.baidu.com/" target="_blank">跳转到百度</a>`  
- 锚点链接：`<a href="#idpath">页内锚点跳转</a>` # 代表本页，后跟要跳转到元素 id  
- 下载文件：`<a href="http://www.baidu.com/img/1.png" download="一个图片.png">下载图片</a>`
    - a标签的【download】属性是在HTML5中新增的属性，它指示浏览器下载 URL 而不是导航到它，并且会提示用户将href指定的链接资源保存为本地文件。如果为【download】属性设置属性值的话，则该属性值将作为下载文件的文件名来保存文件。但如果是跨域下载文件则该属性值无效。
- 创建 email 链接：`<a href="mailto:12121212@qq.com">发邮件</a>` 
- 创建 Tel 链接：`<a href="tel:123456789">打电话</a>`  
- 防止被搜索引擎收录
    - 有时候我们并不希望a标签里的链接内容被Google或百度等搜索引擎抓取，这时候就需要使用a标签下rel属性来防止连接被收录。可以给该属性值设置为“externalnofollow”来实现该效果。【external 】属性表示这是一个相对于当前网站的外部资源，【nofollow】属性表示本文档的作者不想宣传该链接的文档。这对于外链或某些无意义链接非常有用。

---

## html 头部

- `<title>title标签</title>`
- `<base href="定义所有链接起始url">`
- `<meta charset="utf-8">` 描述关键字，作者，字符集等  

| 标签 | 描述 |
|:----:|:----:|
| `<head>` | 定义了文档的信息 |
| `<title>` | 定义了文档的标题 |
| `<base>` | 定义了页面链接标签的默认链接地址 |
| `<link>` | 定义了一个文档和外部资源之间的关系 |
| `<meta>` | 定义了HTML文档中的元数据 |
| `<script>` | 定义了客户端的脚本文件 |
| `<style>` | 定义了HTML文档的样式文件 |

## html 表格

可参考[教程](https://www.runoob.com/html/html-tables.html)  

## html 列表

html 支持有序列表和无序列表。

- **无序列表：用的最多的**(在很多页面的菜单栏都是用无序列表写的)

```html
<ul>
    <li></li>
    <li></li>
</ul>
```

- 有序列表 `<ol></ol>`  

---

## html 区块

html 可以通过 `<div> 和 <span>` 将元素组合起来。  

### 区块元素

大多数 html 元素被定义为 **块级元素**或**内联元素**。  
块级元素在浏览器显示时，通常会以新行来开始（和结束）。  
实例：`<h1>, <p>, <ul>, <table>`  

### 内联元素

内联元素在显示时通常不会以新行开始。  
实例：`<b>, <td>, <a>, <img>`

---

`<div>` 是块级元素，用于组合其他元素的容器。  
`<div>` 元素没有特定含义。此外，由于它属于块级元素，浏览器会在其前后显示折行。  
如果与 CSS 一同使用，`<div>` 元素可用于对大的内容块设置样式属性。  
`<div>` 元素的另一个常见的用途是文档布局。它取代了试用表格定义布局的老式方法。使用 table 元素进行文档布局不是表格的正确用法。 table 元素的作用是显示表格化的数据。  

---

`<span>` 元素时内联元素，可用作文本的容器  
`<span>` 元素也没有特定的含义。  
当与 CSS 一同使用时， `<span>` 元素可用于为部分文档设置样式属性。  

---

## html 表单和输入

html 表单用于收集不通类型的用户输入。  

```html
<form>
    input 元素
</form>
```

### input 元素的多重类型属性（type）

多数情况下被用到的表单标签是输入标签`<input>`。  
输入类型是由类型属性（type）定义的。

- `<input type="text">` 文本域（text Fields）（默认20个字符）
- `<input type="password" name="pwd">` 字符会以星号或原点显示。  
- `<input type="radio" name="sex" value="male">` 单选按钮（Radio Buttons）
- `<input type="checkbox" name="veicle" value="Bike">` 复选框（Checkboxes）
- `<input type="submit" value="Submit">` 提交按钮（Submit Button） 当用户单机确认按钮时，表单的内容会被传送到另一个文件。表单的动作属性定义了目的文件的文件名。由动作属性定义的这个文件通常会对接到的输入数据进行相关的处理。

更多[参考](https://www.runoob.com/html/html-forms.html)  

---

## iframe 框架

`<iframe src="URL" width="200" height="200"  frameborder="0"></iframe>` url、宽、高、边框  

```html
<iframe src="demo_iframe.htm" name="iframe_a"></iframe>
<p><a href="http://www.runoob.com" target="iframe_a">RUNOOB.COM</a></p>
```

显示一个目标链接的页面

## 颜色（RGB）

html 颜色由一个十六进制符号来定义，这个符号由红、绿、蓝的值组成（RGB）。  
每种颜色的最小值是0（十六进制：#00），最大值255（十六进制：#FF）  
单一颜色的两个值相同时，可以简写。（#FF4400可简写为#F40）

---

## html 字符实体

html中的预留字符必须被替换为字符实体。  
一些在键盘上找不多的字符也可以使用字符实体来替代。  

**格式：& 开始  ; 结束，如：`&lt;`就是<**  

[常用速查](https://www.runoob.com/html/html-entities.html)  

---

## url

统一资源定位器(Uniform Resource Locators)

[速查](https://www.runoob.com/html/html-url.html)  
