# navbar

```html
<div class="x-navbar">
    <a href="javascript:;" class="x-navbar-left">
        <span class="x-icon-arrow x-icon-arrow-left"></span>
        return
    </a>
    <div class="x-navbar-title">
        Navbar
    </div>
    <div class="x-navbar-right">
        <span class="x-icon"></span>
        more
    </div>
</div>
```
```css
.x-navbar,
.x-navbar-left,
.x-navbar-right {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -webkit-align-items: center;
    align-items: center;
}
.x-navbar {
    -ms-flex-align: center;
    height: 45px;
    background-color: #108ee9;
    color: #fff;
    flex-wrap: wrap;
} 
.x-navbar-light {
    background-color: #fff;
    color: #108ee9;
}
.x-navbar-left,
.x-navbar-right,
.x-navbar-title {
    -webkit-box-flex: 1;
    -webkit-flex: 1;
    -ms-flex: 1;
    flex: 1;
}
.x-navbar-left {
    padding-left: 15px;
    font-size: 16px;
}
.x-navbar-right {
    -webkit-box-pack: end;
    -webkit-justify-content: flex-end;
    -ms-flex-pack: end;
    justify-content: flex-end;
    padding-right: 15px;
}
.x-navbar-title {
    -ms-flex: 0 0 50%;
    flex: 0 0 50%;
    max-width: 50%;
    width: 100%;
    font-size: 18px; 
    min-height: 1px; 
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    text-align: center;
}

.x-navbar-title.x-navbar-title-lg {
    -ms-flex: 0 0 70%;
    flex: 0 0 70%;
    max-width: 70%;
}
.x-icon {
    display: inline-block;
    width: 22px;
    height: 22px;
    vertical-align: middle;
    line-height: 1; 
}
.x-navbar .x-icon-arrow {
    padding-left: 20px;
    position: relative;
}
.x-icon-arrow:after {
    content: "";
    display: inline-block;
    width: 11px;
    height: 11px;
    border: 1px solid #fff;
    border-width: 1px 0 0 1px;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left:0;
    margin: auto;
}
.x-navbar.x-navbar-light .x-icon-arrow:after {
    border-color: #ccc;
}
.x-icon-arrow-left.x-icon-arrow:after  { 
    -webkit-transform: rotate(315deg);
    transform: rotate(315deg);
}
.x-icon-arrow-top.x-icon-arrow:after  {
    -webkit-transform: rotate(315deg);
    transform: rotate(315deg);
}

```

