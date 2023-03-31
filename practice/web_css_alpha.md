# web css +alpha

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    * {
      color: black;
    }
    p + p {
      color: red;
    }

    p ~ span {
      color: green;
    }

    .box ~ span {
      color: green;
    }
		/* 이곳에 코드를 작성합니다. */

  </style>
</head>
<body>
  <span>0</span> 
  <p>1</p>
  <p>2</p>
  <span>3</span>
  <p>4</p>
  <div class="box">
    <p>5</p>
  </div>
  <article>기사</article>
  <ul>
    <li>6</li>
    <li>7</li>
    <li>8</li>
  </ul>
  <span>9</span>
</body>
</html>
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/59600e30-f82b-4e9d-955a-1ccc96929567/Untitled.png)
![image](https://file.notion.so/f/s/59600e30-f82b-4e9d-955a-1ccc96929567/Untitled.png?id=5af0f118-61d5-4081-988d-eb8fe78971fd&table=block&spaceId=f826548c-dfb0-4cf8-95d5-a414595fcdae&expirationTimestamp=1680307610993&signature=4N7NhaoCq9BfgsB14_P53BUuydMrLSULOrXBhJtDNRw&downloadName=Untitled.png)