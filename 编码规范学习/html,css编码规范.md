# HTML、CSS编码规范

## 缩进

一次缩进2个空格

```html
<ul>
  <li>Fantastic</li>
  <li>Great</li>
</ul>
```

```css
.example {
  color: blue;
}
```

## 大小写

以下都应该用小写：

HTML元素名称， 属性， 属性值， CSS选择器， 属性， 属性值。

```html
<!-- Not recommended -->
<A HREF="/">HOME</A>
```

```html
<!-- Recommended -->
<img src="google.png" alt="Google" />
```

```css
/* Not recommended */
color: #E5E5E5;
```

```css
/* Recommended */
color: #e5e5e5;
```

## 结尾空格

结尾空格不仅多余，而且在比较代码时会更麻烦。

## 通用元规范

### 任务项

用TODO来标记待办事项(建一个大的JIRA任务，用来整理暂时不做的需求、bug)，而不是用一些其他的标记，像@@。

```html
<!-- TODO: remove optional tags -->
<ul>
  <li>Apples</li>
  <li>Oranges</li>
</ul>
```

## 多媒体元素降级

 对于像图片、视频、canvas 动画等多媒体元素，确保提供其他可访问的内容。图片可以使用替代文本（alt），视频和音频可以使用文字版本。 

```html
<!-- Not recommended -->
<img src="spreadsheet.png">
```

```html
<!-- Recommended -->
<img src="spreadsheet.png" alt="Spreadsheet screenshot.">
```

## type属性

 在引用样式表和脚本时，不要指定 type 属性，除非不是 CSS 或 JavaScript。

```html
<!-- Not recommended -->
<link rel="stylesheet" href="//www.google.com/css/maia.css"
  type="text/css">
<script src="//www.google.com/js/gweb/analytics/autotrack.js"
  type="text/javascript"></script>
```



```html
<!-- Recommended -->
<link rel="stylesheet" href="//www.google.com/css/maia.css">
<script src="//www.google.com/js/gweb/analytics/autotrack.js"></script>
```

## HTML引号

 属性值用双引号。 

```html
<!-- Not recommended -->
<a class='maia-button maia-button-secondary'>Sign in</a>
```

```html
<!-- Recommended -->
<a class="maia-button maia-button-secondary">Sign in</a>
```

## ID和Class命名

```css
/* Not recommended: meaningless */
#yee-1901 {}

/* Not recommended: presentational */
.button-green {}
.clear {}
```

``` css
/* Recommended: specific */
#gallery {}
#login {}
.video {}

/* Recommended: generic */
.aux {}
.alt {}
```

## 选择器

```css
/* Not recommended */
ul#example {}
div.error {}
```

```css
/* Recommended */
#example {}
.error {}
```

## 属性简写

 尽量使用 CSS 中可以简写的属性 (如 font)，可以提高编码效率以及代码可读性。 

``` css
/* Not recommended */
border-top-style: none;
font-family: palatino, georgia, serif;
font-size: 100%;
line-height: 1.6;
padding-bottom: 2em;
padding-left: 1em;
padding-right: 1em;
padding-top: 0;
```

``` css
/* Recommended */
border-top: 0;
font: 100%/1.6 palatino, georgia, serif;
padding: 0 1em 2em;
```

### 可以简写的属性汇总

#### Background属性:

##### 有以下属性:

```csss
background-color: #000;
background-image: url(images/bg.gif);
background-repeat: no-repeat;
background-position: top right;
```

##### 一行简写

```css
background: #000 url(images/bg.gif) no-repeat top right;
```

### Font属性

##### 有以下属性:

``` css
font-style: italic;
font-weight: bold;
font-size: .8em;
line-height: 1.2;
font-family: Arial, sans-serif;
```

##### 一行简写

```css
font: italic bold .8em/1.2 Arial, sans-serif;
```

#### Border属性

#####  以下属性

```css
border-width: 1px;
border-style: solid;
border-color: #000;
```

##### 一行简写

```css
border: 1px solid #000;
```

#### Margin和Padding属性

##### 以下属性

```css
margin-top: 10px;
margin-right: 5px;
margin-bottom: 10px;
margin-left: 5px;
```

##### 一行简写

``` css
margin: 10px 5px 10px 5px;
```



## 0和单位

 值为 0 时不用添加单位。 

``` css
margin: 0;
padding: 0;
```

## 开头的0

 值在 -1 和 1 之间时，不需要加 0。 

```css
font-size: .8em;
```

## ID和Class命名分隔符

 选择器中使用连字符可以提高可读性。 

```
/* Not recommended: does not separate the words “demo” and “image” */
.demoimage {}

/* Not recommended: uses underscore instead of hyphen */
.error_status {}
```

```css
/* Recommended */
#video-id {}
.ads-sample {}
```



## 块级内容缩进

 为了反映层级关系和提高可读性，块级内容都应缩进。 

```css
@media screen, projection {

  html {
    background: #fff;
    color: #444;
  }

}
```

## 声明结束

每行CSS都应以分号结尾

```css
/* Not recommended */
.test {
  display: block;
  height: 100px
}
```

```css
/* Recommended */
.test {
  display: block;
  height: 100px;
}
```



## 属性名结尾

 属性名和值之间都应有一个空格。 

```css
/* Not recommended */
h3 {
  font-weight:bold;
}
```

```css
/* Recommended */
h3 {
  font-weight: bold;
}
```

## 声明样式块的分割

```css
/* Not recommended: missing space */
#video{
  margin-top: 1em;
}

/* Not recommended: unnecessary line break */
#video
{
  margin-top: 1em;
}
```

```css
/* Recommended */
#video {
  margin-top: 1em;
}
```

## 选择器分隔

```css
/* Not recommended */
a:focus, a:active {
  position: relative; top: 1px;
}
```

```css
/* Recommended */
h1,
h2,
h3 {
  font-weight: normal;
  line-height: 1.2;
}
```

## 规则分隔

 规则之间都用空行隔开。 

```css
html {
  background: #fff;
}

body {
  margin: auto;
  width: 50%;
}
```

## CSS引号

 属性选择器和属性值用单引号 

```css
/* Not recommended */
html {
  font-family: "open sans", arial, sans-serif;
}
```

```css
/* Recommended */
html {
  font-family: 'open sans', arial, sans-serif;
}
```

## 行长度

每行长度不得超过120个字符，除非单行不可分割。

[建议] 对于超长的样式，在样式值的 `空格` 处或 `,` 后换行，建议按逻辑分组。

```css
/* 不同属性值按逻辑分组 */
background:
    transparent url(aVeryVeryVeryLongUrlIsPlacedHere)
    no-repeat 0 0;

/* 可重复多次的属性，每次重复一行 */
background-image:
    url(aVeryVeryVeryLongUrlIsPlacedHere)
    url(anotherVeryVeryVeryLongUrlIsPlacedHere);

/* 类似函数的属性值可以根据函数调用的缩进进行 */
background-image: -webkit-gradient(
    linear,
    left bottom,
    left top,
    color-stop(0.04, rgb(88,94,124)),
    color-stop(0.52, rgb(115,123,162))
);
```

## 属性

```css
/* Recommended */
.selector {
    margin: 0;
    padding: 0;
}

/* Not recommended */
.selector { margin: 0; padding: 0; }
```

## 属性书写顺序(我觉得挺重要的)

#### [建议] 同一 rule set 下的属性在书写时，应按功能进行分组，并以 **Formatting Model（布局方式、位置） > Box Model（尺寸） > Typographic（文本相关） > Visual（视觉效果）** 的顺序书写，以提高代码的可读性。

解释：

- Formatting Model 相关属性包括：`position` / `top` / `right` / `bottom` / `left` / `float` / `display` / `overflow` 等
- Box Model 相关属性包括：`border` / `margin` / `padding` / `width` / `height` 等
- Typographic 相关属性包括：`font` / `line-height` / `text-align` / `word-wrap` 等
- Visual 相关属性包括：`background` / `color` / `transition` / `list-style` 等

另外，如果包含 `content` 属性，应放在最前面。

```css
.sidebar {
    /* formatting model: positioning schemes / offsets / z-indexes / display / ...  */
    position: absolute;
    top: 50px;
    left: 0;
    overflow-x: hidden;

    /* box model: sizes / margins / paddings / borders / ...  */
    width: 200px;
    padding: 5px;
    border: 1px solid #ddd;

    /* typographic: font / aligns / text styles / ... */
    font-size: 14px;
    line-height: 20px;

    /* visual: colors / shadows / gradients / ... */
    background: #f5f5f5;
    color: #333;
    -webkit-transition: color 1s;
       -moz-transition: color 1s;
            transition: color 1s;
}
```

## 颜色

#### [强制] RGB颜色值必须使用十六进制记号形式 `#rrggbb`。不允许使用 `rgb()`。

解释：

带有alpha的颜色信息可以使用 `rgba()`。使用 `rgba()` 时每个逗号后必须保留一个空格。

 示例： 

``` css
/* Recommended */
.success {
    box-shadow: 0 0 2px rgba(0, 128, 0, .3);
    border-color: #008000;
}

/* Not recommended */
.success {
    box-shadow: 0 0 2px rgba(0,128,0,.3);
    border-color: rgb(0, 128, 0);
}
```

#### [强制] 颜色值可以缩写时，必须使用缩写形式。均采用小写

```css
/* Not recommended */
color: #eebbcc;
```

```css
/* Recommended */
color: #ebc;
```

## 文本编排

### 字体

#### [强制] `font-family` 属性中的字体族名称应使用字体的英文 `Family Name`，其中如有空格，须放置在引号中。

解释：

所谓英文 Family Name，为字体文件的一个元数据，常见名称如下：

| 字体            | 操作系统 | Family Name         |
| --------------- | -------- | ------------------- |
| 宋体 (中易宋体) | Windows  | SimSun              |
| 黑体 (中易黑体) | Windows  | SimHei              |
| 微软雅黑        | Windows  | Microsoft YaHei     |
| 微软正黑        | Windows  | Microsoft JhengHei  |
| 华文黑体        | Mac/iOS  | STHeiti             |
| 冬青黑体        | Mac/iOS  | Hiragino Sans GB    |
| 文泉驿正黑      | Linux    | WenQuanYi Zen Hei   |
| 文泉驿微米黑    | Linux    | WenQuanYi Micro Hei |

示例：

```css
h1 {
    font-family: "Microsoft YaHei";
}
```

#### [强制] `font-family` 按「西文字体在前、中文字体在后」、「效果佳 (质量高/更能满足需求) 的字体在前、效果一般的字体在后」的顺序编写，最后必须指定一个通用字体族( `serif` / `sans-serif` )。

示例：

```
/* Display according to platform */
.article {
    font-family: Arial, sans-serif;
}

/* Specific for most platforms */
h1 {
    font-family: "Helvetica Neue", Arial, "Hiragino Sans GB", "WenQuanYi Micro Hei", "Microsoft YaHei", sans-serif;
}
```

#### [强制] `font-family` 不区分大小写，但在同一个项目中，同样的 `Family Name` 大小写必须统一。我们就按照第一个字母大写，之后小写的这种模式！

### 字重

#### [强制] `font-weight` 属性必须使用数值方式描述。

 CSS 的字重分 100 – 900 共九档，但目前受字体本身质量和浏览器的限制，实际上支持 400 和 700 两档，分别等价于关键词 normal 和 bold。 

## 响应式

#### 强制] `Media Query` 不得单独编排，必须与相关的规则一起定义。

示例：

```
/* Good */
/* header styles */
@media (...) {
    /* header styles */
}

/* main styles */
@media (...) {
    /* main styles */
}

/* footer styles */
@media (...) {
    /* footer styles */
}


/* Bad */
/* header styles */
/* main styles */
/* footer styles */

@media (...) {
    /* header styles */
    /* main styles */
    /* footer styles */
}
```

#### [强制] `Media Query` 如果有多个逗号分隔的条件时，应将每个条件放在单独一行中。

示例：

```
@media
(-webkit-min-device-pixel-ratio: 2), /* Webkit-based browsers */
(min--moz-device-pixel-ratio: 2),    /* Older Firefox browsers (prior to Firefox 16) */
(min-resolution: 2dppx),             /* The standard way */
(min-resolution: 192dpi) {           /* dppx fallback */
    /* Retina-specific stuff here */
}
```

## 兼容性

#### [强制] 带私有前缀的属性由长到短排列，按冒号位置对齐。

标准属性放在最后，按冒号对齐方便阅读，也便于在编辑器内进行多行编辑。

示例：

```
.box {
    -webkit-box-sizing: border-box;
       -moz-box-sizing: border-box;
            box-sizing: border-box;
}
```