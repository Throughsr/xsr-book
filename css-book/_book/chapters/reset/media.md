# css 自适应

> 根据不能媒体设备，使用不同的样式  

```css
/* media */
/* 横屏 */
@media screen and (orientation:landscape){
}
/* 竖屏 */
@media screen and (orientation:portrait){
}
/* 窗口宽度<960,设计宽度=768 */
@media screen and (max-width:959px){
}
/* 窗口宽度<768,设计宽度=640 */
@media screen and (max-width:767px){
}
/* 窗口宽度<640,设计宽度=480 */
@media screen and (max-width:639px){
}
/* 窗口宽度<480,设计宽度=320 */
@media screen and (max-width:479px){
}
/* windows UI 贴靠 */
@media screen and (-ms-view-state:snapped){
}
/* 打印 */
@media print{
    /* 闪开闪开，我要打印啦！ */ 
}
@media 
(-webkit-min-device-pixel-ratio: 1.5), 
(min-resolution: 2dppx) { 
    /* Retina屏幕干嘛干嘛嘞... */ 
}
```
## 不同设备，显示内容宽度

```css
@media (min-width: 768px) {
  .container {
    width: 750px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 970px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1170px;
  }

```

## 不同设备(web端)，不同字体大小
```css
html {
    font-size: 16px;
}

@media screen and (min-width: 375px) {
    html {
        /* iPhone6的375px尺寸作为16px基准，414px正好18px大小, 600 20px */
        font-size: calc(100% + 2 * (100vw - 375px) / 39);
        font-size: calc(16px + 2 * (100vw - 375px) / 39);
    }
}
@media screen and (min-width: 414px) {
    html {
        /* 414px-1000px每100像素宽字体增加1px(18px-22px) */
        font-size: calc(112.5% + 4 * (100vw - 414px) / 586);
        font-size: calc(18px + 4 * (100vw - 414px) / 586);
    }
}
@media screen and (min-width: 600px) {
    html {
        /* 600px-1000px每100像素宽字体增加1px(20px-24px) */
        font-size: calc(125% + 4 * (100vw - 600px) / 400);
        font-size: calc(20px + 4 * (100vw - 600px) / 400);
    }
}
@media screen and (min-width: 1000px) {
    html {
        /* 1000px往后是每100像素0.5px增加 */
        font-size: calc(137.5% + 6 * (100vw - 1000px) / 1000);
        font-size: calc(22px + 6 * (100vw - 1000px) / 1000);
    }
}
```

