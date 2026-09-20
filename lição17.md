```
var coin = createSprite(200,10);
coin.setAnimation("coin_gold_1");
setCoin();

var bunny = createSprite(200,350);
bunny.setAnimation("bunny1_ready_1");

var score = 0;

function draw() {
  
  if (score < 10) {background("white");}else{drawBackground();drawClouds();drawTrees();drawFence();}
  
  if(keyDown("left")){
    bunny.x = bunny.x - 3;
  }
  
  if(keyDown("right")){
    bunny.x = bunny.x + 3;
  }
  
  if(coin.y > 400){
    setCoin();
  }
  if (coin.isTouching(bunny)){score = score + 1;setCoin();}
  
  
  textSize(20);
  text("Score: " + score, 10, 10, 100, 100);
  drawSprites();
}

function setCoin(){coin.velocityY = randomNumber(2,3);
coin.x = randomNumber(10,390);
coin.y = 10;
}

function drawBackground(){
  noStroke();
  background(rgb(0,200,255));
  fill("green");
  rect(0,380,400,20);
}

function drawTrees(){
  noStroke();
  //Draw All Trunks
  fill(rgb(150,100,0));
  rect(210,330,30,50);
  rect(290,330,30,50);
  rect(360,330,30,50);
  //Draw All Branches
  fill("green");
  regularPolygon(225,280,3,100);
  regularPolygon(305,280,3,110);
  regularPolygon(375,290,3,95);
}

function drawClouds(){
  noStroke();
  fill(rgb(255,255,255,100));
  ellipse(300,200,200,50);
  ellipse(320,200,200,70);
  ellipse(340,200,200,50);
  
  ellipse(100,100,200,50);
  ellipse(120,100,200,70);
  ellipse(140,100,200,50);  
}

function drawFence(){
  stroke("white");
  strokeWeight(5);
  line(0,360,400,360);
  line(20,350,20,380);
  line(50,350,50,380);
  line(80,350,80,380);
  line(110,350,110,380);
  line(140,350,140,380);
  line(170,350,170,380);
  line(200,350,200,380);
  line(230,350,230,380);
  line(260,350,260,380);
  line(290,350,290,380);
  line(320,350,320,380);
  line(350,350,350,380);
  line(380,350,380,380);
}
```
```
var sun = createSprite(80,60);
sun.setAnimation("sun_happy_1");

var moon = createSprite(350,70);
moon.setAnimation("sticker_28_1");

function draw() {
  if(World.mouseY > 200){
    drawScene1();
  } else {
    drawScene2();
  }
}
function drawScene1() {
  noStroke();
  background(rgb(0,200,255));
  fill("green");
  rect(0,380,400,20);
  fill(rgb(255,255,255,100));
  ellipse(300,200,200,50);
  ellipse(320,200,200,70);
  ellipse(340,200,200,50);
  ellipse(100,100,200,50);
  ellipse(120,100,200,70);
  ellipse(140,100,200,50); 
  fill(rgb(150,100,0));
  rect(210,330,30,50);
  rect(290,330,30,50);
  rect(360,330,30,50);
  fill("green");
  regularPolygon(225,280,3,100);
  regularPolygon(305,280,3,110);
  regularPolygon(375,290,3,95);
  stroke("white");
  strokeWeight(5);
  line(0,360,400,360);
  line(20,350,20,380);
  line(50,350,50,380);
  line(80,350,80,380);
  line(110,350,110,380);
  line(140,350,140,380);
  line(170,350,170,380);
  line(200,350,200,380);
  line(230,350,230,380);
  line(260,350,260,380);
  line(290,350,290,380);
  line(320,350,320,380);
  line(350,350,350,380);
  line(380,350,380,380);
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
  rect(0,380,400,20);
  fill(rgb(150,100,0));
  rect(210,330,30,50);
  rect(290,330,30,50);
  rect(360,330,30,50);
  fill("green");
  regularPolygon(225,280,3,100);
  regularPolygon(305,280,3,110);
  regularPolygon(375,290,3,95);
  stroke("white");
  strokeWeight(5);
  line(0,360,400,360);
  line(20,350,20,380);
  line(50,350,50,380);
  line(80,350,80,380);
  line(110,350,110,380);
  line(140,350,140,380);
  line(170,350,170,380);
  line(200,350,200,380);
  line(230,350,230,380);
  line(260,350,260,380);
  line(290,350,290,380);
  line(320,350,320,380);
  line(350,350,350,380);
  line(380,350,380,380);

}
```
