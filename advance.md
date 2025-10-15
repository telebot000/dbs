# 💻 Advanced jQuery Practicals

This repository contains **Advanced jQuery Practicals** demonstrating key features like **Animation**, **Chaining**, **Callback**, **Get**, **Insert**, **Remove**, and **Empty** methods.  
All examples use the **jQuery 3.6.0 CDN** and are beginner-friendly.

---

## 🧩 1. Animation and Chaining

### ✅ 1A) Animation Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>jQuery Animation Example</title>
  <style>
    div {
      background: #ffcc00;
      height: 100px;
      width: 100px;
      position: absolute;
    }
  </style>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script>
    $(document).ready(function () {
      $("button").click(function () {
        $("div").animate({ left: '300px' }); 
      });
    });
  </script>
</head>
<body>
  <button>Start Animation</button>
  <div>This is Square</div>
</body>
</html>
```

---

### ✅ 1B) Chaining Example

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    div {
      margin-top: 10px;
      background-color: #ffcc00;
      border: dashed;
      border-width: 2px;
      height: 100px;
      width: 100px;
      position: absolute;
    }
  </style>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script>
    $(document).ready(function(){
      $("button").click(function(){
        $("div").animate({ left: '250px' }, 4000, "linear", function() {
          $(this).css({
            "background-color": "#cc00cc",
            "border-radius": "25px"
          });
        });
      });
    });
  </script>
</head>
<body>
  <button>Start Animation</button>
  <div>This is Square</div>
</body>
</html>
```

---

## ⚙️ 2. jQuery Callback and Get

### ✅ 2A) Callback Example

```html
<html>
<head>
  <title>jQuery Hide Example</title>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script>
    $(document).ready(function () {
      $("button").click(function () {
        $("div").hide("slow", function () {
          alert("Hide Successfully!");
        });
      });
    });
  </script>
</head>
<body>
  <button>Click to Hide</button>
  <div style="background-color: #ffcc00; height: 100px; width: 100px;">
    This is Div
  </div>
</body>
</html>
```

---

### ✅ 2B) jQuery Get Example

```html
<html>
<head>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script>
    $(document).ready(function () {
      $("#b1").click(function () {
        alert("Text: " + $("#hi").text());
      });
      $("#b2").click(function () {
        alert("HTML: " + $("#hi").html());
      });
    });
  </script>
</head>
<body>
  <h2 id="hi">
    This is h2 with <b>bold</b>, <i>italic</i>, <u>Underline</u> fonts.
  </h2>

  <button id="b1">Text</button>
  <button id="b2">HTML</button>
</body>
</html>
```

---

## 🧱 3. Insert, Remove, and Empty Elements

### ✅ 3A) Inserting Content

```html
<!DOCTYPE html>
<html>
<head>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script>
    $(document).ready(function() {
      $("#b1").click(function() {
        $("p").append("<b><br>This is Appended text</b>.");
      });

      $("#b2").click(function() {
        $("p").prepend("<b>This is Prepended text</b><br>");
      });
    });
  </script>
</head>
<body>
  <p><i>Default Text</i></p>
  <button id="b1">Append text</button>
  <button id="b2">Prepend text</button>
</body>
</html>
```

---

### ✅ 3B) Remove Element

```html
<!DOCTYPE html>
<html>
<head>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script>
    $(document).ready(function() {
      $("#b1").click(function() {
        $("p").remove();  // Removes all <p> elements
      });
    });
  </script>
</head>
<body>
  <p><i>Default Text</i></p>
  <button id="b1">Remove P Tag</button>
</body>
</html>
```

---

### ✅ 3C) Empty Element

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    div {
      height: 100px;
      width: 100px;
      background-color: #ffcc00;
    }
  </style>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script>
    $(document).ready(function(){
      $("button").click(function(){
        $("#d1").empty(); // Removes all content inside the div
      });
    });
  </script>
</head>
<body>
  <div id="d1">
    <h3 align="center">Some Content</h3>
  </div>
  <br>
  <button>Click to empty</button>
</body>
</html>
```

---

## 🔗 Google Drive Folder

<p align="center">
  <a href="https://drive.google.com/drive/folders/11IU72HlbofU9aE8bFCpADjf7m5H_ClYR" target="_blank">
    <img src="https://img.shields.io/badge/Open%20Google%20Drive-4285F4?style=for-the-badge&logo=google-drive&logoColor=white" alt="Google Drive Button">
  </a>
</p>

---

## 📘 Summary Table

| Topic | Function Used | Description |
|--------|----------------|--------------|
| 1A | `.animate()` | Creates custom animations |
| 1B | `.animate()`, `.css()` | Chains animation and style change |
| 2A | `.hide(callback)` | Executes callback after hide |
| 2B | `.text()`, `.html()` | Fetches text and HTML content |
| 3A | `.append()`, `.prepend()` | Adds content dynamically |
| 3B | `.remove()` | Removes elements completely |
| 3C | `.empty()` | Clears element contents only |

---

## 🧠 Author Info

**Name:** _Your Name_  
**Subject:** Advanced jQuery Practicals  
**Language Used:** HTML, CSS, jQuery 3.6.0  
