# badge

## 点

```css
.x-badge-dot {
  position: absolute;
  -webkit-transform: translateX(-50%);
  -ms-transform: translateX(-50%);
  transform: translateX(-50%);
  -webkit-transform-origin: 0 center;
  -ms-transform-origin: 0 center;
  transform-origin: 0 center;
  top: -4px;
  height: 8px;
  width: 8px;
  border-radius: 100%;
  background: #ff5b05;
  z-index: 10;
}
```

## 文字

```css
.x-badge-text {
  height: 18px;
  line-height: 18px;
  min-width: 9px;
  padding: 0 5px;
  text-align: center;
  font-size: 12px;
  color: #000;
  background-color: #fff;
  border: 1px solid #e3e3e3;
  white-space: nowrap;
  display: block;
  position: relative;
  -webkit-transform: translateX(0);
  -ms-transform: translateX(0);
  transform: translateX(0);
  -webkit-transform-origin: -10% center;
  -ms-transform-origin: -10% center;
  transform-origin: -10% center;
}
.x-badge-text.x-badge-pill {
  padding: 0 10px;
  border-radius: 12px;
}
.x-badge-pill.x-badge-lg {
  height: 30px;
  min-width: 70px;
  line-height: 30px;
  border-radius: 20px;
}

.x-badge-pill.x-badge-md {
  height: 24px;
  min-width: 26px;
  line-height: 24px;
  border-radius: 14px;
}

.x-badge-text.x-badge-xs {
  height: 15px;
  min-width: 9px;
  padding: 0 3px;
  line-height: 15px;
  border-radius: 2px;
}
```

## 数字

```css
.x-ordinal-icon {
  display: inline-block;
  height: 19px;
  line-height: 19px;
  min-width: 14px;
  margin-right: 10px;
  padding: 0 3px;
  text-align: center;
  font-size: 12px;
  top: -2px;
  color: #000;
  border: 1px solid #000;
  background-color: #e3e3e3;
  border-radius: 2px;
}
.x-ordinal-icon.x-ordinal-md {
  height: 25px;
  line-height: 25px;
  min-width: 16px;
  padding: 0 5px;
  font-size: 14px;
  border-radius: 6px;
  color: #fff;
  border: 1px solid #45a1ff;
  background-color: #45a1ff;
}
```

## corner

```css
.x-badge {
  position: relative;
  display: inline-block;
  line-height: 1;
  vertical-align: middle;
}
.x-badge-corner {
  width: 80px;
  padding: 8px;
  position: absolute;
  right: -32px;
  top: 8px;
  background-color: #ff5b05;
  color: #fff;
  white-space: nowrap;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
  text-align: center;
  font-size: 15px;
}
.x-coner-badge {
  height: 50px;
  width: 200px;
}
.x-badge-corner-wrapper {
  overflow: hidden;
}
```
