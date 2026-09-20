```#Avaliação

var backdrop = createSprite(200,200);
backdrop.setAnimation("sky");
var creature = createSprite(200,250);
creature.setAnimation("creature");
creature.scale = 0.2;

function draw() {
  //shake the sprite when the mouse is pressed
  if (mouseDown()){creature.rotation = randomNumber(-5,5);}
  
  
  drawSprites();
  if (mouseDown()){creature.rotation = randomNumber(-5,5);}
  else {
  fill("black");
  textSize(40);
  text("Press the mouse to shake the creature.", 20, 50, 360, 100);
  }
  //display the text when the mouse is NOT pressed
  
}
```
```#Desafio

var bee = createSprite(200,200);
bee.setAnimation("bee");


function draw(){
  background("bleu");
  if (World.mouseX < 200){bee.x = bee.x - 3;}
  else { bee.x = bee.x +3;}
  if (World.mouseY < 200){bee.y = bee.y - 3;}
  else {bee.y = bee.y + 3;}
  drawSprites();
}
```
