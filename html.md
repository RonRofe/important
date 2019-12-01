# Important things // HTML

## Head

### Page Encoding
Inform the browser what type of characters to present.  
Insert the following line to the `head` tag: `<meta http-equiv="Content-Type" content="TYPE_OF_CONTENT; charset=ENCODING">`

**Example:**
```html
<html>
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
```

### Responsive web design

HTML5 introduced a method to let web designers take control over the viewport, through the `<meta>` tag.   
You should include the following `<meta>` viewport element in all your web pages:  
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
A` <meta>` viewport element gives the browser instructions on how to control the page's dimensions and scaling.  
The `width=device-width` part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).  
The `initial-scale=1.0` part sets the initial zoom level when the page is first loaded by the browser.

## Body

### Text Direction
In order to inform the browser about the main language direction of the page, an attribute of `dir` should be attached to the `<body>` tag.


**Example**
```html
<div dir=”rtl”>
```