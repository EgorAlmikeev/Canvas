# Canvas
[Kodaktor](https://kodaktor.ru/95ca197)

```javascript
<html><title></title>
  <head>
    <meta name="author" content="Egor A ©2018">
  </head>
  <body>
  <script>{

  function makeCanvas(x, y) {
	const canvas = document.createElement('canvas'),
	ctx = canvas.getContext('2d'); 
    canvas.setAttribute('width', x); 
    canvas.setAttribute('height', y); 
    return { canvas, ctx };
  }
  
  const { canvas, ctx } = makeCanvas(300, 120);
  document.body.appendChild(canvas);
  
  ctx.lineWidth=2;
  ctx.strokeStyle="black";
  ctx.strokeRect(1,1,canvas.width-2,canvas.height-2);
  ctx.translate(canvas.width / 2+65, canvas.height / 2-70);
  ctx.rotate(Math.PI/2);
  
  ctx.lineWidth = 3;
  ctx.strokeStyle = 'blue';

  //буква Е
  //вертикальная линия
  ctx.moveTo(20, 10);
  ctx.lineTo(20, 100);
  //горизонтальная линия 1
  ctx.moveTo(20, 10);
  ctx.lineTo(60, 10);
  //горизонтальная линия 2
  ctx.moveTo(20, 55);
  ctx.lineTo(60, 55);
  //горизонтальная линия 3
  ctx.moveTo(20, 100);
  ctx.lineTo(60, 100);
  
  //буква А
  //горизонтальная линия 1
  ctx.moveTo(70, 10);
  ctx.lineTo(120, 10);
  //горизонтальная линия 2
  ctx.moveTo(70, 55);
  ctx.lineTo(120, 55);
  //вертикальная линия 1
  ctx.moveTo(70, 10);
  ctx.lineTo(70, 100);
  //вертикальная линия 2
  ctx.moveTo(120, 10);
  ctx.lineTo(120, 100);
  
  ctx.stroke();
  ctx.closePath();
  
  //подчеркивание
  ctx.beginPath();
  ctx.strokeStyle = 'red';
  ctx.moveTo(20, 110);
  ctx.quadraticCurveTo(110, 120, 125, 110);
  
  ctx.stroke();
  ctx.closePath();
}</script></body>
</html>
```
