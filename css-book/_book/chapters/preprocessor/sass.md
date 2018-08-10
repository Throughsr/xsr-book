# sass

# 编译sass
## 命令行编译
* 编译命令
```
sass style.sass:style.css
```
* 监听命令
```
sass --watch style.sass:style.css
```
* 查看数据类型命令
```
sass -i +回车
type-of(xxx)
```
## 编译样式
* nested, 嵌套
* compact, 紧凑
* expanded, 扩展
* compressed, 压缩
## sass与scss的区别
> sass紧凑型scss 

|      | Sass | Scss |
|------|:----:| :----:|
|注释| `/* sass` `// SASS SDSS` | `/* sass*/` `//sass //sass` |
| 嵌套`@import`| `@import "base";`| `@import base`|
| 定义混合指令 `@mixin`| `@mixin alert {color:#fff; }`| `=alert color:#fff;`|
| 引用混合样式 `@include`| `@include alert;`| `+alert`|
# 使用
## 变量  
使用 $
```
$primary-color:#fff;
$primary-border:1px solid $primary-color;
div.box {
    background-color: $primary-color;
}
h1.page-header {
    border: $primary-border;
}
```
编译为
```
div.box {
  background-color: #fff;
}

h1.page-header {
  border: 1px solid #fff;
}
```
#### 什么时候需要声明变量 
1. 该值至少出现了2次。 
2. 该值至少会被更新一次。 

## 嵌套
#### 简单嵌套
```
.nav {
    height: 100px;
    ul {
        margin: 0;
        li {
            list-style: none;
            padding: 5px;
        }
    }
}
```
编译为
```
.nav {
  height: 100px;
}
.nav ul {
  margin: 0;
}
.nav ul li {
  list-style: none;
  padding: 5px;
}
```
#### 嵌套时调用父选择器  
使用 &
```
.nav {
    height: 100px;
    ul {
        margin: 0;
        a {
            display: block;
            padding: 5px;
            &:hover {
                color: #fff;
            }
        }
        & &-text {
            font-size: 24px;
        }
    }
}
```
编译为
```
.nav {
  height: 100px;
}
.nav ul {
  margin: 0;
}
.nav ul a {
  display: block;
  padding: 5px;
}
.nav ul a:hover {
  color: #fff;
}
.nav ul .nav ul-text {
  font-size: 24px;
}
```
#### 嵌套属性
```
.nav {
    border:1px solid #000 {
        left:0;
        right:0;
    }
}
```
编译为
```
.nav {
  border: 1px solid #000;
  border-left: 0;
  border-right: 0;
}
```
## 定义混合指令 @mixin
> 用于定义可重复使用的样式
#### 结构 
```
@mixin 名字(参数1，参数2，……) {
    ……
}
```
```
@mixin clearfix {
    display: inline-block;
    &:after {
        content: ".";
        display: block;
        height: 0;
        clear: both;
        visibility: hidden;
    }
    * html & {
        height: 1px
    }
}

.btn {
    @include clearfix;
}
```
编译为
```
.btn {
  display: inline-block;
}
.btn:after {
  content: ".";
  display: block;
  height: 0;
  clear: both;
  visibility: hidden;
}
* html .btn {
  height: 1px;
}
```
#### mixin里的参数
> 如果没有参数赋值，则自动使用默认值；

> 如果用参数的命名来设置值，则顺序就不重要；
```
@mixin btn($text-color, $background) {
    color: $text-color;
    background-color: $background;
    a {
        color: $text-color;
    }
}

.btn-danger {
    @include btn(#fff, #555);
}

.btn-info {
    @include btn($background:#888, $text-color:#fff);
}
```
编译为
```
.btn-danger {
  color: #fff;
  background-color: #555;
}
.btn-danger a {
  color: #fff;
}

.btn-info {
  color: #fff;
  background-color: #888;
}
.btn-info a {
  color: #fff;
}
```
## 继承指令 @extend
> 将一个选择器下的所有样式继承给另一个选择器
```
.error {
    padding: 5px;
    color: #fff;
}
.info-error {
    @extend .error;
    color: #555;
}
```
编译为
```
.error, .info-error {
  padding: 5px;
  color: #fff;
}

.info-error {
  color: #555;
}
```
## 导入 @import
> 被导入的文件称为Partials,可用`_xxx`的方式命名 
 
```
@import "xxx";
```

## 注释 
* 多行注释 `/*xxxxx*/` ,会包含在没有压缩之后的css里面
* 单行注释 `//xxxxx` ，不会出现在css
* 强制注释 `/*! xxxx*/` ,会出现压缩之后的css里面

# 数据类型

## 数字类型，number
1. 可进行加减乘除的运算;
2. 除法运算要包在括号里，例如 `(8/2)` ;
3. 乘法运算只能一个带单位，例如  `5px * 1` ;

## 字符串，string
1. 可以用一个 `+` 连接，符号不保留；
2. 带`"xxx" + xxx` 导出的css生成带引号，反之不带引号；
3. 用 `-` 和 `/` 连接，符号会保留；
4. 没有字符的 `*` 连接；

## 颜色，color
## 列表，list
## 名值对列表，map  
#### 结构
```
$map: (项目名字：对应值，项目名字：对应值，项目名字：对应值)
```
## 布尔值，boolean
1. and,与
2. or,或
3. not,非

## 插值语句，interpolation `#{}`

# 函数
## 数字函数
| 函数类型 | 写法 |
| ------ | :------: |
| 绝对值 | abs(xxx) |
| 四舍五入|round(xxx.xx)|
| 进一位|seil(xxx.xx)|
| 退一位|floor(xxx.xx)|
| 百分比|percentage(650px / 1000px)|
| 最大值|min(1,2,3)|
| 最小值|max(1,2,3)|

## 字符串函数
| 函数类型 | 写法 |
| ------ | :------: |
| 大写 | to-upper-case(字符串) |
| 小写 | to-lower-case(字符串) |
| 计算字符串长度 | str-length(字符串) |
| 计算指定字符串长度 | str-index(字符串,"指定字符串") |
| 指定加入字符串 | str-insert(字符串,"指定要加入的字符串"，指定位置) |

## 颜色函数
| 函数类型 | 写法 |
| ------ | :------: |
| RGB | rgb(红,绿,蓝) |
| HSL | hsl(色相,饱和度,明度) |
| 调整色相 | adjust-hue(要调整的颜色,137deg) |
| 变亮+ | lighten(要调整的颜色,50%) |
| 变暗- | darken(要调整的颜色,20%) |
| 增加颜色的纯度 | saturate(要调整理的颜色，50%) |
| 减少颜色的纯度 | desaturate(要调整理的颜色，20%) |
| 变得不透明 | opcify(要调整理的颜色，0.3) |
| 变得更透明 | transparentize(要调整理的颜色，0.2) |


## 列表函数

| 函数类型 | 写法 |
| ------ | :------: |
| 计算列表的长度 | length(列表) |
| 列表中指定的参数 | nth(列表，1) |
| 把两个列表连起来 | join(列表1,列表2,comma)/join（列表1,列表2,space）|
| 将某个值放到列表最后 | append(列表1,某个值,comma)/join(列表1,某个值,space) |
| 多个列表值转多维列表 | zip(列表1,列表2) |
| 计算某个值的位置 | index(列表，某个值) |
> comma(逗号)和space(空格)

## map函数

| 函数类型 | 写法 |
| ------ | :------: |
| 项目对应值 | map-get($map，项目) |
| 所有项目 | map-keys($map) |
| 所有值 | map-values($map) |
| 判断$map中是否有这个项目 | map-has-key($map,项目) |
| 添加新项目和值 | map-merge($map,(项目：值)) |
| 移除项目和值 | map-remove($map,(项目：值)) |


# 控制指令
## @if 
#### 结构
```
@if 条件 {……}
```
```
$classes:"danger";
.alerts {

    @if $classes == primary {
        background-color: #cce5ff;
    }
    @else if $classes == success {
        background-color: #d4edda; 
    }
    @else {
        background-color: #f8d7da;
    }
}
```
编译为
```
.alerts {
  background-color: #f8d7da;
}
```
## @for 
> 重复输出一定量的指令，且有一定的规律
#### 结构
```
@for 变量 from <开始值> through <结束值> {
    循环内容
}
@for 变量 from <开始值> to <结束值> {
    循环内容
}
```
#### 区别
* through：会包含结束值；
* to：不包含结束值；
#### 例如：
```
$size: 5;
@for $text-size from 1 through $size {
    .text-#{$text-size} {
        font-size:11px + $text-size;
    }
}
```
编译为
```
.text-1 {
  font-size: 12px;
}

.text-2 {
  font-size: 13px;
}

.text-3 {
  font-size: 14px;
}

.text-4 {
  font-size: 15px;
}

.text-5 {
  font-size: 16px;
}
```

## @each
> 生成列表里每个项目的值
#### 结构 
```
@each 变量 in 列表值 {
    ……
}
```
```
@each $classes,
$color,
$bg-color,
$boedr-color in (primary,#004085, #cce5ff, #b8daff),
(success,#155724, #d4edda,#c3e6cb),
(danger,#721c24,#f8d7da,#f5c6cb) {
    .alerts-#{$classes} {
        color: $color;
        background-color: $bg-color;
        border-color: $boedr-color;
    }
}
```
编译为
```

```

## @while
> 重复输出格式直到表达式返回结果为 false
#### 结构
```
@while 条件 {
    ……
}
```
```
$i:5;
@while $i>0 {
  .mt-#{$i} {
    margin-top: 4px * $i;
  }
  $i:$i - 1;
}
```
编译为
```
.mt-5 {
  margin-top: 20px;
}

.mt-4 {
  margin-top: 16px;
}

.mt-3 {
  margin-top: 12px;
}

.mt-2 {
  margin-top: 8px;
}

.mt-1 {
  margin-top: 4px;
}
```

# 自定义函数
#### 结构 
```
@function 名称 （参数1，参数2） {
    ……
}
```
```
$colors: (light:#fff,dark:#000);

@function color($key) {
  @return map-get($map: $colors, $key: $key);
}

body {
  background: color(dark);
}
```
编译为
```
body {
  background: #000;
}
```

# 警告和错误
- 使用@warn ，显示在命令行
- 使用@error ，显示在css文件
