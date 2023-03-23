# web_elements_inheritance


![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/3227a3c2-f6f5-422f-919a-32cfe23eacbe/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230323%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230323T003954Z&X-Amz-Expires=86400&X-Amz-Signature=21d50cd7558f85765ce8ac0afa465a1876801026653bd98fb3aea340ac21aeec&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

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
      width : 400px;
      height: 200px;
      border: 2px solid black;
      color: red;
      text-align: center;
      font-size: 20px;
    }

    
    .inner-box {
      width : 200px;
      height: 100px;
      color: initial;
      border : inherit;	
      text-align: initial;	
    }

  </style>
</head>
<body>
  <div class="outer-box">
    <div>
      <span>첫 번째</span>
    </div>
    <div class="inner-box">
      <span>두 번째</span>
    </div>
  </div>
</body>
</html>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/2ea87888-bae8-4853-b636-8beeb0818cc3/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230323%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230323T004011Z&X-Amz-Expires=86400&X-Amz-Signature=4116fa36df90b838db8d9c93156dc676c794fc7047dec1fbe6966b80eff95eb3&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)