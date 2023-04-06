# web flexbox practice

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .outer-box {
      display: flex;
      justify-content: space-between;
      border: black 1px dotted ;
      height: 200px;
      width: 600px;
    }

    .inner-box {
      border: red 1px solid;
      height: 200px;
      width: 300px;
      display: flex;
      justify-content: space-between;
    }

    .box {
      height: 100px;
      width: 100px;
      background-color: skyblue;
    }
    
  </style>
</head>
<body>
  <div class="outer-box">
    <div class="inner-box" >
      <div class="box">item1</div>
      <div class="box">item2</div>
    </div>
  </div>
</body>
</html>
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/77658280-7b11-4596-8435-073087e46ad8/Untitled.png)