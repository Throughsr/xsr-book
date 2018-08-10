# notice

```html
<div class="x-notice-bar">
        <div class="x-notice-bar-icon">
            <div class="x-icon"></div>
        </div>
        <div class="x-notice-bar-content">
            <div class="x-notice-bar-marquee-wrap" style="overflow: hidden;">
                <div class="x-notice-bar-marquee">
                        notice
                </div>
            </div>
        </div>
        <div class="x-notice-bar-operation">
            <div class="x-icon"></div>
        </div>
    </div>
```
```css
.x-notice-bar {
    background-color: #fefcec;
    height: 36px;
    overflow: hidden;
    font-size: 14px;
    line-height: 36px;
    color: #f76a24;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
}
.x-notice-bar-icon,
.x-notice-bar-operation {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
}
.x-notice-bar-icon {
    margin-left: 15px;
}
.x-notice-bar-icon + div {
    margin-left: 5px;
}
.x-notice-bar-content {
    -webkit-box-flex: 1;
    -webkit-flex: 1;
    -ms-flex: 1;
    flex: 1;
    width: 100%;
    margin: auto 15px;
    width: auto;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
.x-notice-bar-marquee {
    position: relative;
    white-space: nowrap;
    display: inline-block;
    padding: 0 7.5px;
}
.x-notice-bar-operation {
    padding-right: 8px;
}
```

