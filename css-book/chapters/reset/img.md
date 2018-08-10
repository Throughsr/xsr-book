# css 图片

## 响应式图片

```css
.img-fluid {
  display: block;
  max-width: 100%;
  height: auto;
}
```

## 图片居中铺满父元素

```css
.cover-img-box {
  width: 200px;
  height: 100px;
}

.cover-img-box img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```

## 图片保持比例居中显示，顶到父元素

```css
.reach-img-box {
  width: 100px;
  height: 100px;
  border: 1px dashed #ccc;
}

.reach-img-box img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
```

## 图片毛玻璃模糊效果

```css
.img-specl {
  -webkit-transform: scale(1.05, 1.05);
  -moz-transform: scale(1.05, 1.05);
  -ms-transform: scale(1.05, 1.05);
  -o-transform: scale(1.05, 1.05);
  transform: scale(1.05, 1.05);
  -webkit-filter: blur(8px);
  filter: blur(8px);
}
```
