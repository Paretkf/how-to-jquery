# Overview

### jQuery คือ
JavaScript Library ซึ่งถูกออกแบบมาเพื่อให้การเขียน JavaScript นั้นมีความสะดวกและง่ายขึ้นเหมาะกับการใช้บน Client side ทำให้การเขียน JS ง่ายขึ้น

### ตัวอย่างการจัดการ HTML ด้วย JavaScript VS jQuery
ในการแก้ element ที่มี id="hello" และเปลี่ยนค่าใน html เป็น  "world"

**Pure JavaScript**
```js
  var el = document.getElementById("hello"); 
  el.innerHTML = "world";
 ```

**jQuery** 
```js
  $("#hello").html("world");
 ```

### การติดตั้ง
- สามารถ Download จาก website ของ jQuery ได้เลย https://jquery.com/download/
- CDN

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
    </body>
</html>
```

### การเรียกใช้งาน
- ใช้ ```$``` ในการ access jQuery
- รอให้ DOM ของ html พร้อมก่อน
```js
$(document).ready(function() {
   // jQuery code goes here
});
```
example

**html**
```HTML
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
    <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
  </head>
  <body>
    <div id="hello">Hello</div>
  </body>
</html>
```

**JavaScript**
```js
$(document).ready(function() {
   $("hello").html("World")
  });
});
```

- Syntax

  - ```$``` เรียกใช้ jQuery.
  - ```(selector)``` หา HTML elements.
  - ```action()``` ใช้ action.

example

```js
$("p").hide()  // hides all <p> elements
$(".demo").hide()  // hides all elements with class="demo"
$("#demo").hide()  // hides the element with id="demo"
```

### Selectors

syntax example
```js
$("div.menu")  // all <div> elements with class="menu"
$("p:first")  // the first <p> element
$("h1, p") // all <h1> and all <p> elements
$("div p") // all <p> elements that are descendants of a <div> element
$("*")  // all elements of the DOM
```
![Selectors](./img/selector.png "selector syntax")
