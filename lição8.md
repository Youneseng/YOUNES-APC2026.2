```#Avaliação
World.frameRate = 10;
//1) Add the draw loop block to the bottom of this program.
//2) Move any blocks that need to be inside the draw loop.
var salt = createSprite(200,200);
salt.setAnimation("salt");
salt.rotation = 180;

function draw() {
  background("skyblue");
  drawSprites();
  salt.y = randomNumber(195,205);
}
```

```#Desafio
World.frameRate = 30;
var catou = createSprite(200,200);
catou.setAnimation("catou");

function draw() {
  background("green");
  drawSprites();
  catou.x = randomNumber(195,205);
  catou.y = randomNumber(195,205);
  catou.rotation = randomNumber(-5,5);
}
```
