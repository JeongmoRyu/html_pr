# web flexbox box

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>

    .container {
      display: flex;
      flex-direction: column-reverse;
      align-items: center;
    }

    .item {
      width: 50px;
      height: 50px;
      border: 1px solid black;
      margin: 10px;
    }

  </style>
</head>
<body>
  <div class="container">
    <span class="item">1</span>
    <span class="item">2</span>
    <span class="item">3</span>
    <span class="item">4</span>
  </div>
</body>
</html>
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d922945e-40e3-4cd0-8e92-c3f7d488f213/Untitled.png)