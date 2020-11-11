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
- `<div></div>` 

---

## HTML 文档后缀名

- .html
- .htm

以上两种没有区别（因为历史原因导致有htm后缀，因为曾经不支持4位字母的后缀名）

---

## 标签种类

- 标签一般是成对出现的，如`<html></html>`,分别叫开始标签和闭合标签。
- 也有单标签，如`<br />` 换行标签（未来的html可能要求所有标签都关闭，尽量养成好习惯吧）。 

> Tip：尽管<P>等同于<p>，但还是推荐使用小写标签。

---

## 常用标签

- 标题： `<h1></h1>` h1-h6 6级标题
- 段落： `<p></p>` 段落标签
- 链接： `<a href="https://www.baidu.com/"></a>` 链接标签，链接
- 图像： `<img src="./localhost/imgPath" width="120" height="230" />` 图像标签，路径、长宽控制

---

## HTML 属性

如 `<a href="https://www.baidu.com/"></a>` 这里的 href 就是 name 的属性。  
- 属性一般有 属性值 和 属性名 组成，属性值一般用双引号引起来，当然单引号也是没有问题的。
- 属性名和属性值一般都使用小写字母（对大小写不敏感）  
- 