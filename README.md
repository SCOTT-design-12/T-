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

<div class="page" id="page3">

<h1>💌 Just for Yuu ❤️</h1>

<div class="loveLetter">

<p>

In a world filled with temporary connections,
shallow intentions,
and lustful distractions...

</p>

<p>

i want yuu baby.

Not for a moment.

Not for convenience.

Not just when things are easy.

</p>

<p>

I want yuu for something real.

I want yuur heart.

I want yuur mind.

I want yuur laughter.

I want yuur softness.

And even the parts of yuu
that yuu're still learning to understand. ❤️

</p>

<p>

In all the noise of this world...

it is yuu that i want.

My eyes now only see yuu. 🧸❤️

</p>

<button class="yes" onclick="nextPage(4)">

One Last Thing ❤️

</button>

</div>

</div>

<!-- PAGE 4 -->

<div class="page" id="page4">

<div id="reveal">

<h1 id="disneyText">

Sorry Disney...

</h1>

<h2 id="princessText" style="display:none;">

...but here's my favourite princess ❤️

</h2>

<img
id="princessImg"
src="princess.jpg"
alt="Princess"
style="display:none;">

<p
id="endingText"
style="
display:none;
font-size:22px;
margin-top:25px;
color:#555;
max-width:600px;
">

Every fairytale has a princess...

<br><br>

Mine just happens to be real. ❤️

</p>

</div>

</div>

<style>

.loveLetter{

background:white;

padding:30px;

border-radius:20px;

max-width:700px;

box-shadow:0 10px 35px rgba(0,0,0,.12);

}

#page4{

background:#000;

color:white;

transition:1.5s;

}

#page4 h1{

font-size:48px;

opacity:0;

animation:fadeText 2s forwards;

}

#page4 h2{

margin-top:20px;

font-size:34px;

color:#ff7db0;

opacity:0;

}

#princessImg{

width:330px;

max-width:90%;

margin-top:35px;

border-radius:25px;

box-shadow:0 0 35px hotpink;

opacity:0;

}

#endingText{

opacity:0;

}

@keyframes fadeText{

from{

opacity:0;

transform:translateY(25px);

}

to{

opacity:1;

transform:translateY(0);

}

}

.fadeIn{

animation:fadeText 2s forwards;

}

</style>
