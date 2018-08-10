# flex 布局

## flex 上中下布局

```css
.layout-root,
body,
html {
  height: 100%;
}

.layout {
  height: 100%;
  display: -webkit-box;
  display: -moz-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  flex-direction: column;
  -webkit-box-direction: normal;
  -webkit-box-orient: vertical;
  -ms-flex-direction: column;
  -webkit-flex-direction: column;
}

.layout-bd {
  flex: 1;
  -ms-flex: 1;
  -webkit-flex: 1;
  overflow-y: auto;
  -webkit-overflow-scrolling: touch;
}
```

## flex 栅格化系统

```css
.x-flexbox {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
}

.x-flexbox-item {
  /* -webkit-box-sizing: border-box;
    box-sizing: border-box; */
  -webkit-box-flex: 1;
  -webkit-flex: 1;
  -ms-flex: 1;
  flex: 1;
}

.x-flexbox.x-flex-column {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-align: stretch;
    align-items: stretch;
    -ms-flex-direction: column;
    flex-direction: column;
}

.x-flexbox.x-flexbox-wrap {
    -webkit-flex-wrap: wrap;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
}

.x-col-1 {
    -ms-flex: 0 0 8.333333%;
    flex: 0 0 8.333333%;
    max-width: 8.333333%
}

.x-col-2 {
    -ms-flex: 0 0 16.666667%;
    flex: 0 0 16.666667%;
    max-width: 16.666667%
}

.x-col-3 {
    -ms-flex: 0 0 25%;
    flex: 0 0 25%;
    max-width: 25%
}

.x-col-4 {
    -ms-flex: 0 0 33.333333%;
    flex: 0 0 33.333333%;
    max-width: 33.333333%
}

.x-col-5 {
    -ms-flex: 0 0 41.666667%;
    flex: 0 0 41.666667%;
    max-width: 41.666667%
}

.x-col-6 {
    -ms-flex: 0 0 50%;
    flex: 0 0 50%;
    max-width: 50%
}

.x-col-7 {
    -ms-flex: 0 0 58.333333%;
    flex: 0 0 58.333333%;
    max-width: 58.333333%
}

.x-col-8 {
    -ms-flex: 0 0 66.666667%;
    flex: 0 0 66.666667%;
    max-width: 66.666667%
}

.x-col-9 {
    -ms-flex: 0 0 75%;
    flex: 0 0 75%;
    max-width: 75%
}

.x-col-10 {
    -ms-flex: 0 0 83.333333%;
    flex: 0 0 83.333333%;
    max-width: 83.333333%
}

.x-col-11 {
    -ms-flex: 0 0 91.666667%;
    flex: 0 0 91.666667%;
    max-width: 91.666667%
}

.x-col-12 {
    -ms-flex: 0 0 100%;
    flex: 0 0 100%;
    max-width: 100%
}
```

## flex 流式布局

```css
.stream-flex-box {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: start;
    -webkit-align-items: flex-start;
    -ms-flex-align: start;
    align-items: flex-start;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
}
.stream-flex-item {
    -webkit-box-flex: 0;
    -ms-flex: 0 0 25%;
    flex: 0 0 25%;
    max-width: 25%;
    box-sizing: border-box;
}
```

## flex 水平滑动
> 适用于图片水平列表滑动

```css
.level-flex-box {
  display: flex;
  width: 100%;
  padding: 0 10px;
  box-sizing: border;
  overflow-x: scroll;
  -webkit-overflow-scrolling: touch;
}

.level-flex-item {
  flex-shrink: 0;
  margin-right: 10px;
  width: 100px;
}
```

## flex 属性
| 属性 | 描述 |
|---|---|
| `flex-grow` | 扩展比率，父元素多出来的处理方法 |
| `flex-shrink` | 收缩比率，父元素不足的处理方法 |
| `flex-basis` | width的替代品 |