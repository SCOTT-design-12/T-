<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For My Princess ❤️</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Trebuchet MS',sans-serif;
}

body{
background:linear-gradient(135deg,#ffd6e7,#fff0f5);
overflow:hidden;
height:100vh;
display:flex;
justify-content:center;
align-items:center;
}

.page{
display:none;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
width:100%;
height:100%;
padding:25px;
animation:fade .6s;
}

.page.active{
display:flex;
}

@keyframes fade{
from{
opacity:0;
transform:scale(.95);
}
to{
opacity:1;
transform:scale(1);
}
}

h1{
color:#ff4d88;
margin-bottom:15px;
}

h2{
color:#ff4d88;
margin-bottom:15px;
}

p{
font-size:19px;
line-height:1.7;
max-width:650px;
color:#444;
margin-bottom:20px;
}

button{

padding:15px 35px;
font-size:18px;
border:none;
border-radius:40px;
cursor:pointer;
transition:.3s;

}

.yes{

background:#ff4d88;
color:white;

}

.yes:hover{

transform:scale(1.05);

}

.no{

background:white;
color:#ff4d88;
position:absolute;

}

.teddy{

width:220px;
margin-bottom:20px;
animation:bounce 2s infinite;

}

@keyframes bounce{

0%,100%{
transform:translateY(0px);
}

50%{
transform:translateY(-12px);
}

}

.roseImage{

width:280px;
margin-top:20px;

}

.arrow{

font-size:40px;
margin-top:15px;
animation:updown 1s infinite;

}

@keyframes updown{

0%,100%{
transform:translateY(0);
}

50%{
transform:translateY(10px);
}

}

/* Envelope */

.envelope{

margin-top:25px;
position:relative;
width:220px;
height:150px;
cursor:pointer;

}

.envelope-base{

position:absolute;
bottom:0;
width:220px;
height:120px;
background:#ff7aa8;
border-radius:8px;

}

.envelope-left{

position:absolute;
left:0;
bottom:0;
width:0;
height:0;
border-left:110px solid #ff94ba;
border-top:60px solid transparent;
border-bottom:60px solid transparent;

}

.envelope-right{

position:absolute;
right:0;
bottom:0;
width:0;
height:0;
border-right:110px solid #ff94ba;
border-top:60px solid transparent;
border-bottom:60px solid transparent;

}

.flap{

position:absolute;
top:0;
left:0;
width:0;
height:0;
border-left:110px solid transparent;
border-right:110px solid transparent;
border-top:80px solid #ff5d95;
transform-origin:top;
transition:1s;

}

.letter{

position:absolute;
left:20px;
bottom:15px;
width:180px;
height:95px;
background:white;
border-radius:5px;
display:flex;
justify-content:center;
align-items:center;
font-size:18px;
font-weight:bold;
color:#ff4d88;
transition:1s;
z-index:-1;

}

.open .flap{

transform:rotateX(180deg);

}

.open .letter{

transform:translateY(-110px);
z-index:3;

}

</style>

</head>

<body>

<!-- PAGE 1 -->

<div class="page active" id="page1">

<img class="teddy" src="teddy.png">

<h1>Would yuu like to get yuur gift? ❤️</h1>

<div>

<button class="yes" onclick="nextPage(2)">
Yes
</button>

<button class="no" id="noBtn">
No
</button>

</div>

</div>

<!-- PAGE 2 -->

<div class="page" id="page2">

<h1>🌹 Roses for my Princess 🌹</h1>

<img src="roses.png" class="roseImage">

<div class="arrow">
⬇️
</div>

<p>Click the letter ❤️</p>

<div class="envelope" id="envelope">

<div class="flap"></div>

<div class="envelope-base"></div>

<div class="envelope-left"></div>

<div class="envelope-right"></div>

<div class="letter" id="letter">
Open Me ❤️
</div>

</div>

</div>
<!-- PAGE 3 -->

<!-- PAGE 4 -->

<div class="page" id="page4">

<h1>Sorry Disney...</h1>

<h2 style="color:#ff4f87; margin-top:15px;">
...but here's my favourite princess ❤️
</h2>

<img id="princessImg" src="princess.jpg" alt="My Princess">

<p style="margin-top:20px;">
Thank yuu for being yuu. ❤️
</p>

</div>

<script>

const noBtn = document.getElementById("noBtn");

noBtn.addEventListener("mouseover", moveButton);
noBtn.addEventListener("click", moveButton);

function moveButton(){

const x = Math.random() * (window.innerWidth - 120);

const y = Math.random() * (window.innerHeight - 80);

noBtn.style.left = x + "px";
noBtn.style.top = y + "px";

}

function nextPage(page){

document.querySelectorAll(".page").forEach(p=>{

p.classList.remove("active");

});

document.getElementById("page"+page).classList.add("active");

}

</script>

</body>
</html>
