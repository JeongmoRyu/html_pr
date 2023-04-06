# web layout practice


```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="semantic.css">
  <title>Layout Practice</title>
</head>
<body>
  <div class="container">
    <div class="header"><strong>header</strong></div>
    <div class="nav"><strong>nav</strong></div>
    <div class="section"><strong>section</strong>
      <div class="article1"><strong>article1</strong></div>
      <div class="article2"><strong>article2</strong></div>
    </div>
    <div class="aside"><strong>aside</strong></div>
    <div class="footer"><strong>footer</strong></div>
  
  </div>
  
</body>
</html>
```

```css
/* 아래 코드는 수정하지 않습니다. */
body {
  font-family: Arial;
  width: 800px;
}

.container {
  width: 800px;
}
.header {
  border: 1px solid black;
  background-color: lightgray;
  margin: 4px;
  padding: 4px;
  text-align: center;
  font-size: 25px;

}
.nav {
  border: 1px solid black;
  background-color: lightgray;
  margin: 4px;
  padding: 4px;
  font-size: 20px;

}
.section {
  float: left;
  width: 68%;
  height: 300px;

  margin: 2px;
  
  margin-left: 4px;
  padding: 4px;

  border: 1px solid black;
  background-color: lightgray;
  font-size: 20px;

}

.aside { 
  float: right;
  width: 28%;
  height: 300px;
  margin: 2px;
  margin-right: 4px;
  padding: 4px;
  border: 1px solid black;
  background-color: lightgray;
  font-size: 20px;

}
.article1 {
  border: 4px;
  height: 50px;
  margin: 4px;
  margin-top: 10px;
  background-color: white;
  border: 1px solid black;
  font-size: 20px;

}
.article2 {
  border: 4px;
  height: 50px;
  margin: 4px;

  background-color: white;
  border: 1px solid black;
  font-size: 20px;

}

.footer {
  border: 1px solid black;
  background-color: lightgray;
  margin: 4px;
  padding: 4px;
  clear: both;
  font-size: 20px;

}

```

![Untitled](https://www.notion.so/web_layout_pr-eb3b1218b2f34fa583688fbfb2503ee3?pvs=4#74450a8b2c154e289e82e37078df95c2)