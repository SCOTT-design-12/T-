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
font-family:Arial,Helvetica,sans-serif;
}

body{
background:#ffe6ee;
overflow:hidden;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
}

.page{
display:none;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
width:100%;
height:100%;
padding:20px;
}

.page.active{
display:flex;
}

h1{
color:#ff4f87;
margin-bottom:15px;
}

p{
font-size:20px;
max-width:700px;
line-height:1.6;
margin-bottom:20px;
}

button{
padding:15px 35px;
border:none;
border-radius:30px;
font-size:18px;
cursor:pointer;
margin:10px;
transition:.3s;
}

.yes{
background:#ff4f87;
color:white;
}

.no{
background:white;
color:#ff4f87;
position:absolute;
}

img{
max-width:300px;
border-radius:20px;
margin:20px;
}

.arrow{
font-size:40px;
animation:bounce 1s infinite;
}

@keyframes bounce{
0%,100%{transform:translateY(0);}
50%{transform:translateY(-10px);}
}

#letter{
font-size:80px;
cursor:pointer;
transition:.3s;
}

#letter:hover{
transform:scale(1.1);
}

.next{
margin-top:30px;
}

#princessImg{
width:300px;
border-radius:20px;
box-shadow:0 0 30px pink;
}
</style>

</head>

<body>

<!-- PAGE 1 -->

<div class="page active" id="page1">

<h1>🧸</h1>

<h1>Would yuu like to get yuur gift?</h1>

<div>

<button class="yes" onclick="nextPage(2)">
Yes ❤️
</button>

<button class="no" id="noBtn">
No
</button>

</div>

</div>

<!-- PAGE 2 -->

<div class="page" id="page2">

<h1>🌹 Roses for my Princess 🌹</h1>

<div style="font-size:120px;">
💐
</div>

<div class="arrow">
⬇️
</div>

<p>Click the letter ❤️</p>

<div id="letter" onclick="nextPage(3)">
💌
</div>

</div>

<!-- PAGE 3 -->

<div class="page" id="page3">

<h1>For Yuu ❤️</h1>

<p>
In a world filled with temporary connections,
shallow intentions and lustful distractions...
</p>

<p>
i want yuu baby.
Not for a moment.
Not for convenience.
Not just when things are easy.
</p>

<p>
I want yuu for something real.
I want yuur heart,
yuur mind,
yuur laughter,
yuur softness,
and even the parts of yuu
that yuu're still learning
to understand. ❤️
</p>

<p>
In all the noise of this world,
it is yuu that i want.
My eyes now only see yuu. 🧸❤️
</p>

<button class="yes next" onclick="nextPage(4)">
Next Step ❤️
</button>

</div>
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
