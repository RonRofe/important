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

## Body

### Text Direction
In order to inform the browser about the main language direction of the page, an attribute of `dir` should be attached to the `<body>` tag.


**Example**
```html
<div dir=”rtl”>
```