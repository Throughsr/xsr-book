# button

## btn

```css
.x-button {
  display: block;
  outline: 0 none;
  -webkit-appearance: none;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  padding: 0;
  text-align: center;
  font-size: 18px;
  height: 47px;
  line-height: 47px;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-word;
  white-space: nowrap;
  color: #000;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 5px;
  transition: color 0.15s 
        ease-in-out, background-color 0.15s 
        ease-in-out,border-color 0.15s 
        ease-in-out, box-shadow 0.15s 
        ease-in-out;
}
.x-button:before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 200%;
  height: 200%;
  border: 1px solid #ddd;
  border-radius: 10px;
  -webkit-transform-origin: 0 0;
  -ms-transform-origin: 0 0;
  transform-origin: 0 0;
  -webkit-transform: scale(0.5);
  -ms-transform: scale(0.5);
  transform: scale(0.5);
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  pointer-events: none;
}
.x-button-inline {
  display: inline-block;
  padding: 0 15px;
}
.x-button-sm {
  font-size: 13px;
  height: 30px;
  line-height: 30px;
  padding: 0 15px;
}
```

## btn-link

```css
.x-btn-link {
  border: 0;
  background-color: transparent;
  outline: none;
  cursor: pointer;
}

.x-btn-link:active {
  opacity: 0.7;
}
```
