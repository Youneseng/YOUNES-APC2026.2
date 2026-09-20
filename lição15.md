```var rock = createSprite(200, 350);
rock.setAnimation("rock");
rock.velocityY =  -10;
rock.rotationSpeed = 2;

function draw() {
  background("skyblue");
  rock.velocityY = rock.velocityY + 0.17;
  if (rock.y > 380){rock.velocityY = 0;rock.rotationSpeed = 0;}
  // update sprites
  
  drawSprites();
}
```
```var plane = createSprite(50, 350);
plane.setAnimation("plane");
var rock = createSprite(150, 350);
rock.setAnimation("rock");
var rockdown = createSprite(350, 100);
rockdown.setAnimation("rock_down");

// You might want to change these 
plane.velocityY = -9;
plane.velocityX = 3;

function draw() {
  background("lightblue");
  plane.velocityY = plane.velocityY + 0.19;
  // Make the Y velocity more downward
  
  drawSprites();
}
```
