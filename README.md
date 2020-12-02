# mi
<!doctype html>
<html>
 <head></head>
 <body style="color: white;"> 
  <canvas id="canvas" width="400" height="400" style="background-color:#333"></canvas>
  <script>
var canvas = document.getElementById("canvas");
var ctx = canvas.getContext("2d");
var radius = canvas.height / 2;
ctx.translate(radius, radius);
radius = radius * 0.90
setInterval(drawClock, 1000);

function drawClock() {
  drawFace(ctx, radius);
  drawNumbers(ctx, radius);
  drawTime(ctx, radius);
}

function drawFace(ctx, radius) {
  var grad;
  ctx.beginPath();
  ctx.arc(0, 0, radius, 0, 2*Math.PI);
  ctx.fillStyle = 'white';
  ctx.fill();
  grad = ctx.createRadialGradient(0,0,radius*0.95, 0,0,radius*1.05);
  grad.addColorStop(0, '#333');
  grad.addColorStop(0.5, 'white');
  grad.addColorStop(1, '#333');
  ctx.strokeStyle = grad;
  ctx.lineWidth = radius*0.1;
  ctx.stroke();
  ctx.beginPath();
  ctx.arc(0, 0, radius*0.1, 0, 2*Math.PI);
  ctx.fillStyle = '#333';
  ctx.fill();
}

function drawNumbers(ctx, radius) {
  var ang;
  var num;
  ctx.font = radius*0.15 + "px arial";
  ctx.textBaseline="middle";
  ctx.textAlign="center";
  for(num = 1; num < 13; num++){
    ang = num * Math.PI / 6;
    ctx.rotate(ang);
    ctx.translate(0, -radius*0.85);
    ctx.rotate(-ang);
    ctx.fillText(num.toString(), 0, 0);
    ctx.rotate(ang);
    ctx.translate(0, radius*0.85);
    ctx.rotate(-ang);
  }
}

function drawTime(ctx, radius){
    var now = new Date();
    var hour = now.getHours();
    var minute = now.getMinutes();
    var second = now.getSeconds();
    //hour
    hour=hour%12;
    hour=(hour*Math.PI/6)+
    (minute*Math.PI/(6*60))+
    (second*Math.PI/(360*60));
    drawHand(ctx, hour, radius*0.5, radius*0.07);
    //minute
    minute=(minute*Math.PI/30)+(second*Math.PI/(30*60));
    drawHand(ctx, minute, radius*0.8, radius*0.07);
    // second
    second=(second*Math.PI/30);
    drawHand(ctx, second, radius*0.9, radius*0.02);
}

function drawHand(ctx, pos, length, width) {
    ctx.beginPath();
    ctx.lineWidth = width;
    ctx.lineCap = "round";
    ctx.moveTo(0,0);
    ctx.rotate(pos);
    ctx.lineTo(0, -length);
    ctx.stroke();
    ctx.rotate(-pos);
}
</script>  
  <title> adnanakib.com </title>
  <style>
   .primary-btn{
	color:pink;
	background-color: #8845f4;
	padding:3px 4px ;
	border-radius:22px;
	text-decoration:none ;
	} 
	.play-btn {
		position:absolute;
		top:45%;
		left:50%;
		width:35%;
		background:#886;
		color: blue;
		border:10px solid #040;
	}
	html{background:green;
	color: black;}
	akib{background: black;
	color:green;
	padding:10px 12px;}
	 </style>
  <marquee behavior="scroll" direction="right" style="color:red; background: yellow;">
   <h1> welcome akib <img src="images - 2020-11-28T211640.674-1.jpeg" height="2px" width="2px">  </img> </h1> 
  </marquee> 
  <!--?php $t = date("H");

if ($t < "10") {
  echo " good morning! Have a nice day akib";
} elseif ($t < "20") {
  echo "Haveing a good day!";
} else {
  echo " good night!have a great sleep";
}
?--> 
  <h1>zoom easy access </h1> 
  <h2>Younsus sir</h2> 
  <li>class = nine .</li> 
  <li>subject= chemistry</li> 
  <li>time= 9-10 am .</li> 
  <a class="primary-btn" href="https://us04web.zoom.us/j/8595253959?pwd=cm55ak5oTllDcW02Ym1pSHdwOE5Gdz09"> start. zoom meeting </a> 
  <h2>Ripon sir</h2> 
  <li>class = nine .</li> 
  <li>subject= physics</li> 
  <li>time= 8.30-9.30pm .</li> 
  <a class="primary-btn" href="https://us04web.zoom.us/j/7507189157?pwd=S2N4bk0wQnRWUjc0bUd0eVZJNm4zUT09">start zoom meeting</a> 
  <h2>Sufian sir</h2> 
  <li>subject=biology</li> 
  <li>time=9-10am </li> 
  <li> class=nine </li> 
  <a class="primary-btn" href="https://us04web.zoom.us/j/7590954498?pwd=dUlLU2ZsbmRGK2wxY1V3b1dCN0I4Zz09"> start zoom meeting </a> 
  <h2 style="color:red;">YMCA</h2> 
  <li>class = nine .</li> 
  <li>subject= all</li> 
  <li>time= 11.45-2.15pm .</li> 
  <a class="primary-btn" href="https://us04web.zoom.us/j/4355704793?pwd=RkJaMGgvOWkwTVN4REdTdW9xOHFmdz09">start zoom meeting</a> 
  <br> 
  <h2> Anonno Rafiq sir</h2> 
  <li>subject=bangla</li> 
  <li>time=8-9pm </li> 
  <li> class=nine </li> 
  <a class="primary-btn" href="https://us04web.zoom.us/j/5294780132?pwd=QlJwTjRWMWRSYXJQcFJWcUFlbk1hUT09">start zoom meeting</a> 
  <h2> Saiful Islam sir</h2> 
  <li>subject=physics</li> 
  <li>time=3-4pm </li> 
  <li> class=nine </li> 
  <a class="primary-btn" href="https://us04web.zoom.us/j/9764616352?pwd=aW8rK3VIT1E4eDlCbkIxYWNrREVCZz09 ">start zoom meeting</a> 
  <br> 
  <marquee behavior="scroll" direction="left" style="color:red; background: yellow;">
   <h1>welcome akib</h1>
  </marquee> 
  <footer> 
   
 </body>
</html>
