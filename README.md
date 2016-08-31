# Zoomify

[![Join the chat at https://gitter.im/indrimuska/zoomify](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/indrimuska/zoomify?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Zoomify是一个放大图片的jquery插件，为避免图片变虚，默认会放大到原始尺寸或窗口尺寸，可以添加自定义样式控制其大小和位置。

示例页面参见demo/index.html

![Zoomify: jQuery Plugin for lightboxes](http://indrimuska.github.io/zoomify/img/zoomify-preview.png)

## Installation

```html
<script src="//cdn.bootcss.com/jquery/3.1.0/jquery.min.js"></script>
<script src="js/vendor/zoomify/dist/zoomify.min.js"></script>
<link href="css/vendor/zoomify/dist/zoomify.min.css" rel="stylesheet">
```

## Usage

Enable zoomify via JavaScript:

```javascript
$('img.myImage1').zoomify(); // Default settings
$('img.myImage2').zoomify({ duration: 1000 }); // 1s duration
```

## Options

Property | Type | Default | Description
---|---|---|---
duration | `integer` | `200` | Transition duration in milliseconds.
easing | `string` | `"linear"` | Transition property name.

Options can be passed via data attributes or JavaScript. For data attributes, append the option name to `data-`, as in `data-duration=""`.

## Methods

Method | Description
---|---
zoom | Starts a zoom-in or a zoom-out transformation depending on the state of the image.
zoomIn | Starts a zoom-in transformation.
zoomOut | Starts a zoom-out transformation.
reposition | Calculates the correct position of the image and moves it at the center of the visible part of page.

Example of call the `zoomIn()` method:
```javascript
$('#myImage').zoomify('zoomIn');
```

## Events

Event | Description
---|---
zoom-in.zoomify | Fired before each zoom-in transformation.
zoom-in-complete.zoomify | Fired after each zoom-in transformation.
zoom-out.zoomify | Fired before each zoom-out transformation.
zoom-out-complete.zoomify | Fired after each zoom-out transformation.

```javascript
$('#myImage').on('zoom-in.zoomify', function () {
    // do something...
});
```

## License

Copyright (c) 2015 Indri Muska. Licensed under the MIT license.