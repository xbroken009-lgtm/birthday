
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>For Someone Special ♡</title>

<style>
*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

html{
    scroll-behavior:smooth;
}

body{
    background:#050507;
    color:#fff;
    font-family:Arial,sans-serif;
    overflow-x:hidden;
}

body::before{
    content:"";
    position:fixed;
    inset:0;
    z-index:-2;
    background:
        radial-gradient(circle at 20% 20%,#ff4b9125,transparent 30%),
        radial-gradient(circle at 80% 70%,#844bff22,transparent 30%);
}

/* OPENING */

.hero{
    height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:25px;
}

.hero-inner{
    max-width:800px;
    animation:fadeIn 1.6s ease;
}

.eyebrow{
    font-size:10px;
    letter-spacing:7px;
    opacity:.45;
    margin-bottom:28px;
}

h1{
    font-family:Georgia,serif;
    font-size:clamp(60px,14vw,145px);
    font-weight:400;
    line-height:.82;
}

.gradient{
    background:
        linear-gradient(
            90deg,
            #fff,
            #ff9dca,
            #c9b5ff,
            #fff
        );

    background-size:300%;

    -webkit-background-clip:text;
    color:transparent;

    animation:gradientMove 7s infinite;
}

.sub{
    font-family:Georgia,serif;
    font-style:italic;
    font-size:24px;
    opacity:.6;
    margin-top:30px;
}

button{
    margin-top:45px;
    padding:16px 34px;

    border-radius:50px;

    border:1px solid #ffffff30;

    background:#ffffff08;

    color:#fff;

    cursor:pointer;

    letter-spacing:2px;

    transition:.3s;
}

button:hover{
    transform:scale(1.06);
    background:#ffffff18;
}

/* MAIN */

#site{
    display:none;
    opacity:0;
    transition:1.5s;
}

section{
    min-height:100vh;

    display:flex;
    align-items:center;
    justify-content:center;

    padding:80px 20px;

    text-align:center;
}

.container{
    width:100%;
    max-width:900px;
}

.label{
    font-size:9px;
    letter-spacing:6px;
    text-transform:uppercase;
    opacity:.35;
    margin-bottom:24px;
}

h2{
    font-family:Georgia,serif;
    font-weight:400;
    font-size:clamp(48px,9vw,90px);
    line-height:.95;
}

.text{
    max-width:620px;
    margin:28px auto 0;
    line-height:2;
    opacity:.6;
}

/* NAME */

.name{
    font-family:Georgia,serif;
    font-style:italic;

    font-size:clamp(
        75px,
        16vw,
        170px
    );

    background:
        linear-gradient(
            120deg,
            #fff,
            #ff9dc7,
            #d3bdff,
            #fff
        );

    background-size:300%;

    -webkit-background-clip:text;

    color:transparent;

    animation:gradientMove 8s infinite;
}

/* COUNTDOWN */

.countdown{
    display:flex;

    justify-content:center;

    flex-wrap:wrap;

    gap:12px;

    margin-top:45px;
}

.time{
    width:110px;
    height:110px;

    border-radius:24px;

    background:#ffffff08;

    border:1px solid #ffffff15;

    display:flex;

    flex-direction:column;

    align-items:center;

    justify-content:center;
}

.time strong{
    font-family:Georgia,serif;
    font-size:38px;
    font-weight:400;
}

.time span{
    font-size:8px;
    letter-spacing:2px;
    text-transform:uppercase;
    opacity:.4;
    margin-top:5px;
}

/* LETTER */

.letter{
    max-width:700px;

    margin:45px auto 0;

    padding:45px 30px;

    border-radius:28px;

    background:#ffffff08;

    border:1px solid #ffffff12;
}

.letter p{
    font-family:Georgia,serif;

    font-size:21px;

    line-height:1.9;

    opacity:.75;
}

/* =========================
   GIFT
========================= */

#giftSection{
    display:none;
    min-height:100vh;
}

.gift-wrap{
    position:relative;

    margin:55px auto 0;

    width:190px;
    height:180px;

    cursor:pointer;
}

.gift-lid{
    position:absolute;

    top:18px;
    left:0;

    width:190px;
    height:48px;

    border-radius:10px;

    background:
        linear-gradient(
            135deg,
            #ff4f91,
            #ff86b5
        );

    z-index:3;

    transition:.8s;
}

.gift-box{
    position:absolute;

    top:60px;
    left:10px;

    width:170px;
    height:120px;

    border-radius:8px;

    background:
        linear-gradient(
            135deg,
            #e93779,
            #ff76aa
        );

    box-shadow:
        0 20px 50px #ff4f9140;
}

.ribbon-v{
    position:absolute;

    left:75px;
    top:0;

    width:35px;
    height:180px;

    background:#ffd7e8;

    z-index:4;
}

.ribbon-h{
    position:absolute;

    left:0;
    top:75px;

    width:190px;
    height:28px;

    background:#ffd7e8;

    z-index:4;
}

.gift-wrap.open .gift-lid{
    transform:
        translateY(-85px)
        rotate(-8deg);
}

.gift-wrap.open .gift-box{
    animation:boxPop .7s ease;
}

.gift-text{
    margin-top:30px;

    opacity:.55;

    font-size:12px;

    letter-spacing:2px;
}

#giftMessage{
    display:none;

    margin:45px auto 0;

    animation:reveal 1.2s ease;
}

#giftMessage h3{
    font-family:Georgia,serif;

    font-size:
        clamp(
            42px,
            8vw,
            72px
        );

    font-weight:400;

    font-style:italic;
}

#giftMessage p{
    margin-top:20px;

    line-height:2;

    opacity:.65;
}

/* PARTICLES */

.particle{
    position:fixed;

    bottom:-20px;

    pointer-events:none;

    animation:
        rise
        linear
        forwards;

    opacity:0;

    z-index:5;
}

/* FOOTER */

footer{
    text-align:center;

    padding:50px 20px;

    opacity:.25;

    font-size:9px;

    letter-spacing:4px;
}

/* ANIMATIONS */

@keyframes fadeIn{

    from{
        opacity:0;
        transform:translateY(25px);
    }

    to{
        opacity:1;
        transform:none;
    }
}

@keyframes gradientMove{

    0%,100%{
        background-position:0%;
    }

    50%{
        background-position:100%;
    }
}

@keyframes rise{

    0%{
        transform:
            translateY(0)
            rotate(0);

        opacity:0;
    }

    15%{
        opacity:.8;
    }

    100%{
        transform:
            translateY(-110vh)
            rotate(360deg);

        opacity:0;
    }
}

@keyframes boxPop{

    50%{
        transform:scale(1.08);
    }

    100%{
        transform:scale(1);
    }
}

@keyframes reveal{

    from{
        opacity:0;
        transform:translateY(25px);
    }

    to{
        opacity:1;
        transform:none;
    }
}

/* MOBILE */

@media(max-width:600px){

    .time{
        width:75px;
        height:75px;
    }

    .time strong{
        font-size:27px;
    }

    .letter{
        padding:35px 22px;
    }

    .letter p{
        font-size:19px;
    }
}
</style>
</head>

<body>

<!-- =========================
     OPENING
========================= -->

<div id="opening" class="hero">

    <div class="hero-inner">

        <div class="eyebrow">
            15 · 11 · 2026
        </div>

        <h1>
            <span class="gradient">
                For<br>
                Someone
            </span>
        </h1>

        <div class="sub">
            who deserves something beautiful ♡
        </div>

        <button onclick="enterSite()">
            OPEN ✦
        </button>

    </div>

</div>


<!-- =========================
     WEBSITE
========================= -->

<div id="site">


<!-- NAME -->

<section>

    <div class="container">

        <div class="label">
            this page belongs to
        </div>

        <div class="name">
            Centimeter
        </div>

        <p class="text">
            Yes... that nickname. 😂<br>
            I couldn't make this without putting it somewhere.
        </p>

    </div>

</section>


<!-- MESSAGE -->

<section>

    <div class="container">

        <div class="label">
            a little message
        </div>

        <h2>
            Hey, you. ♡
        </h2>

        <p class="text">
            I didn't really know what to give you,
            so I made a little corner of the internet instead.
            Nothing huge. Just something made specifically
            for your day.
        </p>

    </div>

</section>


<!-- COUNTDOWN -->

<section>

    <div class="container">

        <div class="label">
            the wait
        </div>

        <h2>
            15 November
        </h2>

        <p
            class="text"
            id="countText">

            Your day is getting closer...

        </p>


        <div class="countdown">

            <div class="time">

                <strong id="days">
                    00
                </strong>

                <span>
                    Days
                </span>

            </div>


            <div class="time">

                <strong id="hours">
                    00
                </strong>

                <span>
                    Hours
                </span>

            </div>


            <div class="time">

                <strong id="minutes">
                    00
                </strong>

                <span>
                    Minutes
                </span>

            </div>


            <div class="time">

                <strong id="seconds">
                    00
                </strong>

                <span>
                    Seconds
                </span>

            </div>

        </div>

    </div>

</section>


<!-- LETTER -->

<section>

    <div class="container">

        <div class="label">
            a little letter
        </div>

        <h2>
            For your birthday.
        </h2>


        <div class="letter">

            <p>

                I hope you get everything
                you're wishing for.

                I hope there are a ridiculous
                number of reasons for you
                to smile this year.

                <br><br>

                And even though this is just
                a small website, I spent time
                making it because I wanted
                your birthday to have
                something a little different.

                <br><br>

                So...

                <br><br>

                Happy Birthday,
                Centimeter. ♡

            </p>

        </div>

    </div>

</section>


<!-- =========================
     BIRTHDAY GIFT
========================= -->

<section id="giftSection">

    <div class="container">

        <div class="label">
            your birthday surprise
        </div>

        <h2>
            Your gift is here. 🎁
        </h2>

        <p class="text">
            Tap the gift to open it.
        </p>


        <div
            class="gift-wrap"
            id="gift"
            onclick="openGift()">

            <div class="gift-lid"></div>

            <div class="gift-box"></div>

            <div class="ribbon-v"></div>

            <div class="ribbon-h"></div>

        </div>


        <div class="gift-text">
            TAP THE GIFT ♡
        </div>


        <div id="giftMessage">

            <h3>
                Happy Birthday,
                Centimeter! ❤️
            </h3>

            <p>

                I hope today gives you
                at least one moment
                you'll never forget.

                <br><br>

                You deserve a beautiful
                year ahead. ♡

            </p>

        </div>

    </div>

</section>


<footer>

    MADE WITH ♡ · 15 / 11

</footer>

</div>


<script>

/* =========================
   OPEN WEBSITE
========================= */

function enterSite(){

    document
        .getElementById("opening")
        .style.display="none";

    const site =
        document.getElementById("site");

    site.style.display="block";

    setTimeout(
        () => site.style.opacity="1",
        50
    );

    window.scrollTo(0,0);

    createParticles(30);
}


/* =========================
   COUNTDOWN
========================= */

let birthdayReached = false;

function countdown(){

    const now = new Date();

    let year =
        now.getFullYear();

    let birthday =
        new Date(
            year,
            10,
            15,
            0,
            0,
            0
        );

    /*
       November = month 10
    */

    if(now > birthday){

        birthday =
            new Date(
                year + 1,
                10,
                15,
                0,
                0,
                0
            );

    }

    const difference =
        birthday - now;


    document
        .getElementById("days")
        .textContent =
        String(
            Math.floor(
                difference /
                86400000
            )
        ).padStart(2,"0");


    document
        .getElementById("hours")
        .textContent =
        String(
            Math.floor(
                difference /
                3600000
            ) % 24
        ).padStart(2,"0");


    document
        .getElementById("minutes")
        .textContent =
        String(
            Math.floor(
                difference /
                60000
            ) % 60
        ).padStart(2,"0");


    document
        .getElementById("seconds")
        .textContent =
        String(
            Math.floor(
                difference /
                1000
            ) % 60
        ).padStart(2,"0");


    /*
       Birthday moment
    */

    if(
        difference <= 1000 &&
        !birthdayReached
    ){

        birthday();
    }

}


/* =========================
   BIRTHDAY REVEAL
========================= */

function birthday(){

    birthdayReached = true;


    document
        .getElementById("countText")
        .textContent =
        "IT'S YOUR DAY! ❤️";


    const gift =
        document.getElementById(
            "giftSection"
        );

    gift.style.display="flex";


    createParticles(80);


    setTimeout(
        () => {

            gift.scrollIntoView({
                behavior:"smooth"
            });

        },
        1200
    );

}


/* =========================
   OPEN GIFT
========================= */

function openGift(){

    const gift =
        document.getElementById(
            "gift"
        );


    gift.classList.add("open");


    createParticles(60);


    setTimeout(
        () => {

            document
                .getElementById(
                    "giftMessage"
                )
                .style.display =
                "block";

        },
        700
    );

}


/* =========================
   PARTICLES
========================= */

function createParticle(){

    const particle =
        document.createElement("div");

    particle.className =
        "particle";


    const symbols = [
        "♡",
        "✦",
        "✧",
        "♥",
        "🎉"
    ];


    particle.textContent =
        symbols[
            Math.floor(
                Math.random() *
                symbols.length
            )
        ];


    particle.style.left =
        Math.random() * 100 +
        "vw";


    particle.style.fontSize =
        10 +
        Math.random() * 18 +
        "px";


    particle.style.animationDuration =
        5 +
        Math.random() * 7 +
        "s";


    document.body.appendChild(
        particle
    );


    setTimeout(
        () => particle.remove(),
        13000
    );

}


function createParticles(amount){

    for(
        let i=0;
        i<amount;
        i++
    ){

        setTimeout(
            createParticle,
            i * 45
        );

    }

}


/* =========================
   START
========================= */

setInterval(
    createParticle,
    1500
);

setInterval(
    countdown,
    1000
);

countdown();

</script>

</body>
</html>