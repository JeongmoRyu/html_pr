# web_CSS_importancy_level


- css

```css
h2 {
  color:darkviolet !important;
  
}

p {
  color:orange
}

.blue {
  color:blue
  
}

.green {
  color:green
}

#red {
  color:red
}
```
- html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <p>1</p> <!-- 1 -->
  <p class="blue">2</p> <!-- 2 -->
  <p class="blue green">3</p> <!-- 3 -->
  <p class="green blue">4</p> <!-- 4 -->
  <p id="red" class="blue">5</p> <!-- 5 -->
  <h2 id="red" class="blue">6</h2> <!-- 6 -->
  <p id="red" class="blue" style="color: yellow;">7</p> <!-- 7 -->
  <h2 id="red" class="blue" style="color: yellow;">8</h2> <!-- 8 -->
  <link rel="stylesheet" href="web_daliy0103_1.css">
</body>

</html>
```