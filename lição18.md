```#Game
var knife = createSprite(-50, -50);
knife.setAnimation("knife");
knife.scale = 0.2;
knife.setCollider("rectangle", 0, 0, 50, 100, 0);

var balloon = createSprite(10, 5);
balloon.setAnimation("balloon");
balloon.scale = 0.6;
balloon.setCollider("circle", 0, 0, 50);

var Joker = createSprite(50, 315);
Joker.setAnimation("Joker");
Joker.scale = 0.5;

var pop = createSprite(-50,-50);
pop.setAnimation("pop");
pop.scale = 0.6;

var score = 0;

var gameState = "start";



var popTimer = 0;


playSound("nickpanek-metal-chipper-8-bit-heavy-metal-fusion-instrumental-351589.mp3", true);

function draw() {
  
  if (gameState == "start") {
    drawScene1();
    
    fill("black");
    rect(40, 70, 320, 230);

    fill("white");
    noStroke();
    textSize(28);
    text("BURST 24 BALLOONS", 60, 110);

    textSize(25);
    text("CONTROLS:", 140, 150);

    textSize(30);
    text("LEFT ARROW", 90, 180);
    text("RIGHT ARROW", 90, 210);
    text("SPACE TO SHOOT", 90, 240);

    textSize(28);
    text("Press ENTER to start", 80, 275);}

    if (keyWentDown("ENTER")) {
      gameState = "playing";
    }
  

  else if (gameState == "playing") {

    if (score < 16) {
      drawScene1();
    } else {
      drawScene2();
    }

  if (keyDown("LEFT_ARROW")) {
    Joker.velocityX = -4;
  } else if (keyDown("RIGHT_ARROW")) {
    Joker.velocityX = 4;
  } else {
    Joker.velocityX = 0;
  }

  if (Joker.x < 30) {
    Joker.x = 30;
  }

  if (Joker.x > 370) {
    Joker.x = 370;
  }


  if (balloon.y > 400) {
    gameState = "lose";
    drawScene1();
    drawSprites();
    
    fill("BLACK");
    noStroke();
    textSize(50);
    text("YOU LOSE!", 85, 200);

    textSize(20);
    text("Score: " + score, 150, 240);
  }

    if (keyWentDown("SPACE")) {
      knife.x = Joker.x;
      knife.y = Joker.y - 20;
      knife.velocityY = -6;
    }

    setknife();

    if (score >= 24) {
      gameState = "win";
    drawScene2() ;
    drawSprites();
    fill("white");
    noStroke();
    textSize(50);
    text("YOU WIN!", 100, 200);

    textSize(20);
    text("Score: 24", 150, 240);}
    textSize(20);
    fill("red");
    text("Score: " + score, 10, 10, 100, 100);

    drawSprites();
  }
}
function drawScene1() {
  noStroke();
  background(rgb(0, 200, 255));

  fill("green");
  rect(0, 380, 400, 20);

  fill(rgb(255, 255, 255, 100));
  ellipse(300, 200, 200, 50);
  ellipse(320, 200, 200, 70);
  ellipse(340, 200, 200, 50);

  ellipse(100, 100, 200, 50);
  ellipse(120, 100, 200, 70);
  ellipse(140, 100, 200, 50);

  fill(rgb(150, 100, 0));
  rect(210, 330, 30, 50);
  rect(290, 330, 30, 50);
  rect(360, 330, 30, 50);

  fill("green");
  regularPolygon(225, 280, 3, 100);
  regularPolygon(305, 280, 3, 110);
  regularPolygon(375, 290, 3, 95);

  stroke("white");
  strokeWeight(5);

  line(0, 360, 400, 360);
  line(20, 350, 20, 380);
  line(50, 350, 50, 380);
  line(80, 350, 80, 380);
  line(110, 350, 110, 380);
  line(140, 350, 140, 380);
  line(170, 350, 170, 380);
  line(200, 350, 200, 380);
  line(230, 350, 230, 380);
  line(260, 350, 260, 380);
  line(290, 350, 290, 380);
  line(320, 350, 320, 380);
  line(350, 350, 350, 380);
  line(380, 350, 380, 380);

  fill(255, 255, 0);
  ellipse(310, 90, 150, 150);
}

function drawScene2() {
  background(10, 15, 30);
  noStroke();

  fill(255, 250, 200);
  ellipse(100, 100, 150, 150);

  fill(10, 15, 30);
  ellipse(140, 90, 150, 150);

  fill("green");
  rect(0, 380, 400, 20);

  fill(rgb(150, 100, 0));
  rect(210, 330, 30, 50);
  rect(290, 330, 30, 50);
  rect(360, 330, 30, 50);

  fill("green");
  regularPolygon(225, 280, 3, 100);
  regularPolygon(305, 280, 3, 110);
  regularPolygon(375, 290, 3, 95);

  stroke("white");
  strokeWeight(5);

  line(0, 360, 400, 360);
  line(20, 350, 20, 380);
  line(50, 350, 50, 380);
  line(80, 350, 80, 380);
  line(110, 350, 110, 380);
  line(140, 350, 140, 380);
  line(170, 350, 170, 380);
  line(200, 350, 200, 380);
  line(230, 350, 230, 380);
  line(260, 350, 260, 380);
  line(290, 350, 290, 380);
  line(320, 350, 320, 380);
  line(350, 350, 350, 380);
  line(380, 350, 380, 380);
}

function setballoon() {
  balloon.setAnimation("balloon");
  balloon.x = randomNumber(10, 390);
  balloon.y = 5;
  if (score < 16) {balloon.velocityY = randomNumber(2, 3);}
  if (score >= 16) {balloon.velocityY = 4;}
}

function setknife() {
   if (knife.isTouching(balloon) && popTimer == 0) {
    playSound("sound://category_pop/vibrant_game_harvest_collect_bubble_pop.mp3");
    balloon.setAnimation("pop");
    balloon.velocityY = 0;
    
    score = score + 1;
    popTimer = 15;
    
    knife.x = -50;
    knife.y = -50;
    knife.velocityY = 0;
  }

  
  if (popTimer > 0) {
    popTimer = popTimer - 1;
  }

  
  if (popTimer == 0 && balloon.getAnimationLabel() == "pop") {
    setballoon();
  }


  if (knife.y < -50) {
    knife.x = -50;
    knife.y = -50;
    knife.velocityY = 0;
  }
}
```
