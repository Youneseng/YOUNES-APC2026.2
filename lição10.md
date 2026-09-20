```#Avaliação

var backdrop = createSprite(200,200);
backdrop.setAnimation("sci_fi");
var dinosaur = createSprite(200, 350);
dinosaur.scale = 0.2;
dinosaur.setAnimation("tyrannosaurus");

function draw() {
  //move the dinosaur up
  dinosaur.y = dinosaur.y - 5;
  if(dinosaur.y < 260){dinosaur.setAnimation("pterodactyl");}

  //if it gets to the sky, turn it into a pterodactyl

  //draw everything
  drawSprites();
}
```
```#Desafio

var balloon = createSprite(200, 200);
balloon.setAnimation("balloon");
balloon.scale = 0.1;
var pop = createSprite(200, 200);
pop.setAnimation("pop"); 
pop.visible = false;

function draw() {
  // Draw Background
  background("white");
  
  // Update Values
  balloon.scale = balloon.scale + 0.002;
  if (balloon.scale > 0.7) { 
    balloon.visible = false; 
    pop.visible = true;      
  }

  // Draw Animations
  drawSprites();
}
```
