# text

## 文本溢出
```css
/* 不换行 */
.x-text-truncate {
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
}
/* 换行 */
.x-text-newline {
    word-wrap:break-word;
    word-break:normal;
}
/* 英文断行 */
.x-text-english {
    word-break:break-all;
}
```

## 文本对齐
```css
.x-text-left {
    text-align:left;
}
.x-text-right {
    text-align:right;
}
.x-text-center {
    text-align:center;
}
```

## 文字瘦高
```css
.x-text-tall { 
    display: inline-block;transform:scale(1,1.5);
}
```

## 滚动条样式
```css
/*定义滚动条高宽及背景 高宽分别对应横竖滚动条的尺寸*/  
::-webkit-scrollbar  
{  
    width: 6px;  
    height: 6px;  
    background-color: #F5F5F5;  
}  
  
/*定义滚动条轨道 内阴影+圆角*/  
::-webkit-scrollbar-track  
{  
    -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3);  
    border-radius: 10px;  
    background-color: #FFF;  
}  
  
/*定义滑块 内阴影+圆角*/  
::-webkit-scrollbar-thumb  
{  
    border-radius: 10px;  
    -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3);  
    background-color: #AAA;  
}  
```