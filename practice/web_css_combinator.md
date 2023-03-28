# web css combinator

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<style>
div{
  color : blue;
  font-size: 30px;
}

div>div{
  color : crimson;
  padding-left: 50px;
}

</style>
<body>
  <div>
    자식
    <div>
      손자
    </div>
  </div>
  <div>
    자식
  </div>
</body>
</html>
```

![Untitled](https://file.notion.so/f/s/d28d9bd2-c1b3-4596-a357-b6f2d75d2eb6/Untitled.png?id=672df0b1-ed0b-44b7-aec8-af93c970466e&table=block&spaceId=f826548c-dfb0-4cf8-95d5-a414595fcdae&expirationTimestamp=1680073184956&signature=xqeWt3MGHerKel2bac-LaIipkxovwhGwJvGbQSGxozQ&downloadName=Untitled.png)