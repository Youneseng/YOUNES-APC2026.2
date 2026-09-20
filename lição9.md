```#Avaliação

var orangeFish = createSprite(400, randomNumber(0, 100));
orangeFish.setAnimation("orange_fish");
var blueFish = createSprite(250, randomNumber(0, 200));
blueFish.setAnimation("blue_fish");
var greenFish = createSprite(300, randomNumber(200, 300));
greenFish.setAnimation("green_fish");
var bubble = createSprite(randomNumber(0,400),400);
bubble.setAnimation("bubble");
bubble.scale = 0.1; 
var bubble2 = createSprite(randomNumber(0,400),400);
bubble2.setAnimation("bubble2");
bubble2.scale = 0.1; 

function draw() {
  // Draw Background
  background("navy");
  drawSprites();
  if (keyDown("left")){
  orangeFish.x = orangeFish.x - 2;
  blueFish.x = blueFish.x -3;
  greenFish.x = greenFish.x -1;
  }// Draw Animations
  bubble.y = bubble.y - 2;
  bubble2.y = bubble2.y - 2;
  drawSprites();
}
```
```#Desafio
var orangeFish = createSprite(400, randomNumber(0, 100));
orangeFish.setAnimation("orange_fish");
var blueFish = createSprite(250, randomNumber(0, 200));
blueFish.setAnimation("blue_fish");
var greenFish = createSprite(300, randomNumber(200, 300));
greenFish.setAnimation("green_fish");
var bubble = createSprite(randomNumber(0,400),400);
bubble.setAnimation("bubble");
bubble.scale = 0.1; 

function draw() {
  // Draw Background
  background("navy");
  drawSprites();
  if (keyDown("left")){
  orangeFish.x = orangeFish.x - 2;
  blueFish.x = blueFish.x -3;
  greenFish.x = greenFish.x -1;
  }// Draw Animations
  bubble.y = bubble.y - 2;
  drawSprites();
}
```
