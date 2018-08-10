# list

```html
<div class="x-list">
    <div class="x-list-header">header</div>
    <div class="x-list-body">
        <div class="x-list-item x-list-item-middle">
            <div class="x-list-thumb">
                <img src="https://zos.alipayobjects.com/rmsportal/dNuvNrtqUztHCwM.png">
            </div>
            <div class="x-list-line x-list-line-multiple">
                <div class="x-list-content">Title
                    <div class="x-list-brief" style="">subtitle</div>
                </div>
                <div class="x-list-extra">extra content</div>
                <div class="x-list-arrow x-list-arrow-horizontal" aria-hidden="true"></div>
            </div>
        </div>
    </div>
    <div class="x-list-footer">footer</div>
</div>
```
```css
.x-list-header {
    padding: 15px 15px 9px;
    font-size: 14px;
    color: #888;
    width: 100%;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
}

.x-list-footer {
    padding: 9px 15px 15px;
    font-size: 14px;
    color: #888
}

.x-list-body {
    position: relative;
    background-color: #fff;
}

.x-list-body:before {
    content: " ";
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    height: 1px;
    border-top: 1px solid #e5e5e5;
    color: #e5e5e5;
    -webkit-transform-origin: 0 0;
    transform-origin: 0 0;
    -webkit-transform: scaleY(0.5);
    transform: scaleY(0.5);
    z-index: 2;
}

.x-list-body:after {
    content: " ";
    position: absolute;
    left: 0;
    bottom: 0;
    right: 0;
    height: 1px;
    border-bottom: 1px solid #e5e5e5;
    color: #e5e5e5;
    -webkit-transform-origin: 0 100%;
    transform-origin: 0 100%;
    -webkit-transform: scaleY(0.5);
    transform: scaleY(0.5);
    z-index: 2;
}

.x-list-item {
    position: relative;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    padding-left: 15px;
    min-height: 44px;
    background-color: #fff;
    vertical-align: middle;
    overflow: hidden;
    -webkit-transition: background-color .2s;
    transition: background-color .2s;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
}

.x-list-thumb:first-child {
    margin-right: 15px;
}

.x-list-item img {
    width: 22px;
    height: 22px;
    vertical-align: middle;
}

.x-list-line {
    position: relative;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-flex: 1;
    -webkit-flex: 1;
    -ms-flex: 1;
    flex: 1;
    -webkit-align-self: stretch;
    -ms-flex-item-align: stretch;
    align-self: stretch;
    padding-right: 15px;
    overflow: hidden;
}

.x-list-item:not(:last-child) .x-list-line:after {
    content: " ";
    position: absolute;
    left: 0;
    bottom: 0;
    right: 0;
    height: 1px;
    border-top: 1px solid #e5e5e5;
    color: #e5e5e5;
    -webkit-transform-origin: 0 100%;
    transform-origin: 0 100%;
    -webkit-transform: scaleY(0.5);
    transform: scaleY(0.5);
}

.x-list-item.x-list-item-top .x-list-line {
    -webkit-box-align: start;
    -webkit-align-items: flex-start;
    -ms-flex-align: start;
    align-items: flex-start;
}

.x-list-item.x-list-item-middle .x-list-line {
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
}

.x-list-item.x-list-item-bottom .x-list-line {
    -webkit-box-align: end;
    -webkit-align-items: flex-end;
    -ms-flex-align: end;
    align-items: flex-end;
}

.x-list-line.x-list-line-multiple {
    padding: 12.5px 15px 12.5px 0;
}

.x-list-line.x-list-line-multiple .x-list-content,
.x-list-line.x-list-line-multiple .x-list-extra {
    padding-top: 0;
    padding-bottom: 0;
}

.x-list-content {
    -webkit-box-flex: 1;
    -webkit-flex: 1;
    -ms-flex: 1;
    flex: 1;
    color: #000;
    font-size: 17px;
    text-align: left;
}

.x-list-extra {
    -webkit-flex-basis: 36%;
    -ms-flex-preferred-size: 36%;
    flex-basis: 36%;
    color: #888;
    font-size: 16px;
    text-align: right;
}

.x-list-content,
.x-list-extra {
    line-height: 1.5;
    width: auto;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    padding-top: 7px;
    padding-bottom: 7px;
}

.x-list-brief {
    color: #888;
    font-size: 15px;
    line-height: 1.5;
    margin-top: 6px;
    width: auto;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}

.x-list-arrow {
    position: relative;
    padding-right: 18px;
    color: #808080;
    visibility: hidden;
}

.x-list-arrow:after {
    content: " ";
    display: inline-block;
    height: 6px;
    width: 6px;
    border-width: 2px 2px 0 0;
    border-color: #C8C8CD;
    border-style: solid;
    -webkit-transform: matrix(0.71, 0.71, -0.71, 0.71, 0, 0);
    transform: matrix(0.71, 0.71, -0.71, 0.71, 0, 0);
    position: relative;
    top: -2px;
    position: absolute;
    top: 50%;
    right: 2px;
}

.x-list-arrow-horizontal.x-list-arrow:after {
    margin-top: -4px;
    visibility: visible;
}

.x-list-arrow-vertical.x-list-arrow:after {
    -webkit-transform: rotate(315deg);
    -ms-transform: rotate(315deg);
    transform: rotate(315deg);
    margin-top: -2px;
    visibility: visible;
}
```