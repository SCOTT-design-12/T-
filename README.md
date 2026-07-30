<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Open Me ❤️</title>

    <link rel="stylesheet" href="style.css">

    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600&family=Caveat:wght@700&display=swap" rel="stylesheet">
</head>
<body>

<div class="background"></div>

<div class="container">

    <div class="envelope" id="envelope">

        <div class="shadow"></div>

        <div class="back"></div>

        <div class="letter">

            <div class="paper">

                <h2>To My Baby ❤️</h2>

                <p>
                    in a world filled with temporary connections,
                    shallow intentions, and lustful distractions,
                    i want yuu baby!
                </p>

                <p class="continue">
                    (click anywhere to continue reading...)
                </p>

            </div>

        </div>

        <div class="front"></div>

        <div class="flap"></div>

        <span class="open-text">
            💌<br>
            open me
        </span>

    </div>

</div>

<div class="overlay" id="overlay">

    <div class="full-letter">

        <button id="close">
            ✕
        </button>

        <h1>For Yuu ❤️</h1>

        <div class="message">

            <p>
                in a world filled with temporary connections,
                shallow intentions,
                and lustful distractions,
                i want yuu baby!
            </p>

            <p>
                not for a moment,
                not for convenience,
                and not just when things are easy,
                but i want yuu for something real.
            </p>

            <p>
                i want yuur heart,
                yuur mind,
                yuur laughter,
                yuur softness,
                and EVEN the parts of yuu
                that yuu're still learning
                to understand. ❤️
            </p>

            <p>
                and if yuu're wondering whether
                yuur love would be worth giving,
                whether the lover girl era
                would be worth bringing back...
            </p>

            <p>
                in all the noise of this world,
                it is yuu that i want.
            </p>

            <h2>
                my eyes now only see yuu.
                🧸❤️
            </h2>

        </div>

    </div>

</div>

<script src="script.js"></script>

</body>
</html>
/* Google Font Backup */
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600&family=Caveat:wght@700&display=swap');

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    height:100vh;
    overflow:hidden;
    display:flex;
    justify-content:center;
    align-items:center;
    background:#f8f6f2;
    font-family:'Cormorant Garamond',serif;
    position:relative;
}

/* Newspaper-style background */

.background{
    position:absolute;
    inset:0;
    background:
        radial-gradient(circle at center,
        rgba(255,255,255,.75),
        rgba(241,239,234,.95)),
        url("https://www.transparenttextures.com/patterns/paper-fibers.png");
    background-size:cover;
    filter:brightness(1.02);
}

/* faded newspaper text */

.background::before{
    content:"THE LOVE TIMES   •   SPECIAL EDITION   •   EVERY LOVE STORY HAS A BEGINNING";
    position:absolute;
    top:40px;
    left:50%;
    transform:translateX(-50%);
    width:100%;
    text-align:center;
    font-size:18px;
    letter-spacing:7px;
    color:rgba(0,0,0,.07);
    font-weight:bold;
}

.background::after{
    content:"LOVE • MEMORIES • FOREVER • LETTERS • HEART •";
    position:absolute;
    bottom:35px;
    width:100%;
    text-align:center;
    color:rgba(0,0,0,.06);
    letter-spacing:8px;
    font-size:16px;
}

.container{
    position:relative;
    z-index:5;
}

/* Floating animation */

@keyframes float{

    0%{
        transform:translateY(0px);
    }

    50%{
        transform:translateY(-14px);
    }

    100%{
        transform:translateY(0px);
    }

}

.envelope{

    width:330px;
    height:220px;
    position:relative;
    cursor:pointer;
    animation:float 3.5s ease-in-out infinite;

}

/* shadow */

.shadow{

    position:absolute;
    bottom:-28px;
    left:50%;
    width:220px;
    height:24px;
    transform:translateX(-50%);
    border-radius:50%;
    background:rgba(0,0,0,.12);
    filter:blur(10px);

}

/* envelope body */

.back{

    position:absolute;
    width:100%;
    height:100%;
    background:#fffdf9;
    border-radius:10px;
    box-shadow:
        0 18px 35px rgba(0,0,0,.12),
        inset 0 0 25px rgba(255,255,255,.8);

}

/* lower front */

.front{

    position:absolute;
    bottom:0;

    width:100%;
    height:120px;

    background:#f2ede5;

    clip-path:polygon(0 0,50% 75%,100% 0,100% 100%,0 100%);
    border-radius:0 0 10px 10px;
}

/* flap */

.flap{

    position:absolute;

    width:100%;
    height:120px;

    background:#faf6ef;

    clip-path:polygon(0 100%,50% 0,100% 100%);
    transform-origin:top;
    transition:.9s ease;

    z-index:8;

    border-radius:10px 10px 0 0;

}

/* open animation */

.envelope.open .flap{

    transform:rotateX(180deg);

}

/* letter */

.letter{

    position:absolute;

    width:90%;
    left:5%;
    top:18px;

    transition:1s;

    z-index:4;

}

.envelope.open .letter{

    transform:translateY(-145px);

}

.paper{

    background:#fffefb;
    border-radius:8px;
    padding:25px;
    box-shadow:0 12px 25px rgba(0,0,0,.10);
    min-height:260px;

}

.paper h2{

    text-align:center;
    margin-bottom:18px;
    font-family:'Caveat',cursive;
    color:#b83d5a;
    font-size:36px;

}

.paper p{

    line-height:1.8;
    font-size:19px;
    color:#444;

}

.continue{

    margin-top:30px;
    text-align:center;
    color:#999;
    font-size:16px;
    font-style:italic;

}

/* open me */

.open-text{

    position:absolute;
    top:58%;
    left:50%;
    transform:translate(-50%,-50%);
    z-index:12;

    font-family:'Caveat',cursive;
    font-size:36px;
    color:#444;
    text-align:center;
    transition:.4s;

}

.envelope.open .open-text{

    opacity:0;

}

/* Fullscreen letter */

.overlay{

    position:fixed;
    inset:0;

    background:rgba(248,246,242,.96);

    display:flex;
    justify-content:center;
    align-items:center;

    opacity:0;
    pointer-events:none;

    transition:.6s;

    z-index:50;

}

.overlay.show{

    opacity:1;
    pointer-events:auto;

}

.full-letter{

    width:min(90%,700px);
    max-height:85vh;
    overflow:auto;

    background:#fffefc;
    padding:50px;

    border-radius:14px;

    box-shadow:0 20px 60px rgba(0,0,0,.15);

}

.full-letter h1{

    text-align:center;
    margin-bottom:35px;

    color:#b63d5d;

    font-family:'Caveat',cursive;
    font-size:52px;

}

.message p{

    margin-bottom:24px;
    font-size:22px;
    line-height:1.9;
    color:#444;

}

.message h2{

    margin-top:30px;
    text-align:center;
    font-family:'Caveat',cursive;
    font-size:44px;
    color:#d14d6d;

}

#close{

    float:right;
    border:none;
    background:none;
    font-size:30px;
    cursor:pointer;
    color:#777;
    transition:.3s;

}

#close:hover{

    transform:rotate(90deg);

}

::-webkit-scrollbar{

    width:8px;

}

::-webkit-scrollbar-thumb{

    background:#d8d2ca;
    border-radius:20px;

}
