# web chessboard simulation

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .board {
      width: 800px;
      height: 800px;
      border: 2px solid black;
      font-size: 0px;
    }

    .cell {
      width: 100px;
      height: 100px;
      margin: 0px;
      padding: 0px;
      display: inline-block;
    }

    .black {
      background-color: black;

    }

    .white {
      background-color: white;

    }

  </style>
</head>
<body>
  <div class="board">
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>

    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white">
      <img src="./images/black_pawn.png" alt="흰색폰" height="100px" width="100px" >
    </div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>

    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>

    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>

    <div class="cell white">
      <img src="./images/white_queen.png" alt="흰색퀸" height="100px" width="100px" >
    </div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>

    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>

    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black"></div>

    <div class="cell black"></div>
    <div class="cell white"></div>
    <div class="cell black">
      <img src="./images/white_king.png" alt="흰색킹" height="100px" width="100px" z-index="1">
    </div>
    <div class="cell white">
      
    </div>
    <div class="cell black">
      
    </div>
    <div class="cell white">
      <img src="./images/white_rook.png" alt="흰색룩" height="100px" width="100px" >
    </div>
    <div class="cell black">
      
      
    </div>
    <div class="cell white">

    </div>

  </div>

</body>
</html>
```



![Untitled](https://th.bing.com/th/id/OIP.zuLtNKre5T4RDD8oCxSFvgHaFj?w=209&h=180&c=7&r=0&o=5&pid=1.7)