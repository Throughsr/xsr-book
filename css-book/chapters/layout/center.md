# 水平垂直居中

## 元素水平居中

```css
.x-margin-center {
  margin: 0 auto;
}
```

## 元素水平垂直居中

```css
/* 父元素知宽度，子元素未知宽度*/
.x-transform-center {
  display: block;
  position: relative;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
/* 父子元素都知宽高*/
.x-position-center {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  width: 100px;
  height: 100px;
  margin: auto;
}
/* flex布局 */
.x-flex-center {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
  -webkit-box-pack: center;
  -webkit-justify-content: center;
  -ms-flex-pack: center;
  justify-content: center;
}
/* 表格布局 */
.x-table-center {
  display: table;
}
.x-table-center {
  display: table-cell;
  text-align: center;
  vertical-align: middle;
}
```
