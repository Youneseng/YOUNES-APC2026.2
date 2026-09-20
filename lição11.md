```#Avaliação

var backdrop = createSprite(200,200);
backdrop.setAnimation("rainbow");
var flyer = createSprite(200,200);
flyer.setAnimation("wing_bot");

function draw() {
  if (keyDown("left")){flyer.x = flyer.x - 3;}//move left when the left arrow is pressed
  if (keyDown("right")){flyer.x = flyer.x + 3;}
  if (keyDown("up")){flyer.y = flyer.y - 3;}//move right when the right arrow is pressed
  if (keyDown("down")){flyer.y = flyer.y + 3;}
  //move up when the up arrow is pressed
  
  //move down when the down arrow is pressed
  
  drawSprites();
}
```
```#Desafio

var bug = createSprite(200, 200);
bug.setAnimation("fly");

function draw() {
  //Draw Background
  background("white");
  
  // Update Values
  if(keyDown("up")){
    bug.setAnimation("flyu");
    bug.y = bug.y - 5;

  }
  if(keyDown("down")){
    bug.setAnimation("flyd");
    bug.y = bug.y + 5;

  }
  if(keyDown("left")){
    bug.setAnimation("fly");
    bug.x = bug.x - 5;

  }
  if(keyDown("right")){
    bug.setAnimation("flyr");
    bug.x = bug.x + 5;

  }

  //Draw Animations
  drawSprites();
}
```
