# web bootstrap class

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-GLhlTQ8iRABdZLl6O3oVMWSktQOp6b7In1Zl3/Jr59b6EGGoI1aFkw7cmDA6j6gD" crossorigin="anonymous">
  
  <style>
    .container {
    
    }
    .box1 {
      border-radius: 10px;
      margin-bottom: 10px;
    }
    .row {
      display: flex;
      margin-bottom: 10px;
    }
    .row {
      background-color: white;
      border: 1px solid black;
      justify-content: center;
    }
    .col-1{
      border: 1px solid black;
    }
    .col-4 {
      border: 1px solid black;
    }

  </style>
</head>
<body>
  <div class="container">
    <div class="box1 text-center text-light bg-success fs-1">sign in</div>
    <div class="row bg-dark" style="align-items: center; justify-content: start;">
      <img src="naver.png" alt="NAVER_LOGO" style="width: 
      50px; height: 20px;">
      <div class="col-2 text-white fs-6">프로젝트 &#9660;</div>
      <div class="col-2 text-white fs-6">그룹들 &#9660;</div>
      <div class="col-2 text-white fs-6">활동</div>
      <div class="col-2 text-white fs-6">마일스톤</div>
      <div class="col-2 text-white fs-6">스티펫</div>
    </div>

    <div class="row">
      <div class="col-4 text-center bg-light text-secondary">Prev</div>
      <div class="col-1 text-center bg-primary text-light">1</div>
      <div class="col-1 text-center bg-light ">2</div>
      <div class="col-1 text-center bg-light ">3</div>
      <div class="col-1 text-center bg-light ">4</div>
      <div class="col-4 text-center bg-light ">Next</div>

    </div>

    </div>

  </div>
  

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js" integrity="sha384-w76AqPfDkMBDXo30jS1Sgez6pr3x5MlQ1ZAGC+nuZB+EYdgRZgiwxhTBTkF7CXvN" crossorigin="anonymous"></script>
</body>
</html>
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/76e23bc3-93bb-4e5a-ac1c-fbba12e23ecd/Untitled.png)