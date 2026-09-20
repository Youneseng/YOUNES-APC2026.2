```var horse = createSprite(200, 150);
horse.setAnimation("horse");
horse.setCollider("circle");
var rainbow = createSprite(400, 370);
rainbow.setAnimation("rainbow");
rainbow.velocityX = -5;
rainbow.velocityY = -5;
rainbow.rotateToDirection = true;
rainbow.setCollider("circle");

function draw() {
  // draw the background
  background("skyblue");

  if (rainbow.isTouching(horse)){horse.setAnimation("unicorn");}// change the horse to a unicorn when the rainbow touches it
  
  drawSprites();
}
```
```var roller = createSprite(200, 200);
roller.scale = 2;
roller.setAnimation("roller_1");
roller.setCollider("rectangle",0,0,40,180,30);// Use .setCollider() with all 6 parameters.
roller.debug = true;
drawSprites();
```
