<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>🔥 Banyu Game Center</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:Arial, sans-serif;
    min-height:100vh;
    color:white;
    background:
        radial-gradient(circle at top,#312e81 0%,#111827 45%,#020617 100%);
    overflow-x:hidden;
}

/* BACKGROUND */

body::before{
    content:"";
    position:fixed;
    width:400px;
    height:400px;
    background:#7c3aed;
    filter:blur(150px);
    opacity:.25;
    top:-150px;
    left:-100px;
    z-index:-1;
}

body::after{
    content:"";
    position:fixed;
    width:400px;
    height:400px;
    background:#06b6d4;
    filter:blur(150px);
    opacity:.2;
    bottom:-150px;
    right:-100px;
    z-index:-1;
}

/* HEADER */

header{
    text-align:center;
    padding:45px 20px 25px;
}

.logo{
    font-size:50px;
    animation:pulse 2s infinite;
}

h1{
    font-size:42px;
    margin:10px 0;
    background:linear-gradient(90deg,#22d3ee,#a78bfa,#f472b6);
    -webkit-background-clip:text;
    color:transparent;
}

.subtitle{
    color:#cbd5e1;
    font-size:17px;
}

.developer{
    margin-top:12px;
    display:inline-block;
    padding:8px 18px;
    border:1px solid #38bdf8;
    border-radius:30px;
    color:#7dd3fc;
    box-shadow:0 0 15px #0ea5e9;
}

/* GAME MENU */

.container{
    width:92%;
    max-width:1100px;
    margin:auto;
}

.games{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
    gap:22px;
    margin-top:25px;
}

/* CARD */

.game-card{
    position:relative;
    padding:28px 20px;
    border-radius:22px;
    background:rgba(255,255,255,.07);
    border:1px solid rgba(255,255,255,.15);
    backdrop-filter:blur(12px);
    text-align:center;
    overflow:hidden;
    transition:.3s;
}

/* FUSING EFFECT */

.game-card::before{
    content:"";
    position:absolute;
    width:180px;
    height:180px;
    background:linear-gradient(
        45deg,
        #00eaff,
        #8b5cf6,
        #ff00cc,
        #00eaff
    );
    background-size:300%;
    animation:fusing 4s linear infinite;
    filter:blur(35px);
    opacity:.45;
    top:-100px;
    left:-100px;
}

.game-card:hover{
    transform:translateY(-10px) scale(1.03);
    border-color:#38bdf8;
    box-shadow:
        0 0 15px #38bdf8,
        0 0 40px rgba(139,92,246,.5);
}

.game-icon{
    position:relative;
    font-size:55px;
    margin-bottom:12px;
}

.game-card h2{
    position:relative;
    margin-bottom:8px;
}

.game-card p{
    position:relative;
    color:#cbd5e1;
    margin-bottom:20px;
}

/* BUTTON */

.play{
    position:relative;
    width:100%;
    border:none;
    padding:13px;
    border-radius:12px;
    font-size:16px;
    font-weight:bold;
    color:white;
    cursor:pointer;

    background:linear-gradient(
        90deg,
        #2563eb,
        #7c3aed,
        #db2777
    );

    background-size:200%;
    animation:gradient 3s linear infinite;

    box-shadow:0 0 15px rgba(124,58,237,.7);
}

.play:hover{
    box-shadow:
        0 0 15px #22d3ee,
        0 0 30px #8b5cf6;
}

/* GAME AREA */

#gameArea{
    display:none;
    margin-top:30px;
    padding:30px;
    text-align:center;
    border-radius:25px;
    background:rgba(0,0,0,.35);
    border:1px solid rgba(255,255,255,.15);
}

#gameTitle{
    font-size:30px;
    margin-bottom:20px;
}

input{
    padding:14px;
    width:90%;
    max-width:350px;
    border:none;
    border-radius:12px;
    margin:8px;
    text-align:center;
    font-size:17px;
}

.gameBtn{
    padding:13px 25px;
    border:none;
    border-radius:12px;
    background:#22c55e;
    color:white;
    font-weight:bold;
    cursor:pointer;
    margin:8px;
}

.back{
    background:#ef4444;
}

/* FOOTER */

footer{
    text-align:center;
    margin:50px 0 25px;
    color:#94a3b8;
}

/* ANIMATION */

@keyframes fusing{
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
}

@keyframes gradient{
    0%{background-position:0%;}
    50%{background-position:100%;}
    100%{background-position:0%;}
}

@keyframes pulse{
    0%,100%{transform:scale(1);}
    50%{transform:scale(1.12);}
}

</style>
</head>

<body>

<header>

<div class="logo">🎮</div>

<h1>BANYU GAME CENTER</h1>

<p class="subtitle">
Kumpulan game seru dalam satu website
</p>

<div class="developer">
⚡ Game dibuat oleh Developer Banyu ⚡
</div>

</header>

<div class="container">

<div class="games">

<!-- GAME 1 -->

<div class="game-card">

<div class="game-icon">🎯</div>

<h2>Tebak Angka</h2>

<p>Tebak angka rahasia dari 1 sampai 100.</p>

<button class="play" onclick="openGame('angka')">
🔥 MAIN SEKARANG
</button>

</div>

<!-- GAME 2 -->

<div class="game-card">

<div class="game-icon">🧠</div>

<h2>Quiz</h2>

<p>Uji pengetahuanmu dengan pertanyaan seru.</p>

<button class="play" onclick="openGame('quiz')">
🔥 MAIN SEKARANG
</button>

</div>

<!-- GAME 3 -->

<div class="game-card">

<div class="game-icon">🌎</div>

<h2>Tebak Negara</h2>

<p>Tebak nama negara dari petunjuk yang diberikan.</p>

<button class="play" onclick="openGame('negara')">
🔥 MAIN SEKARANG
</button>

</div>

<!-- GAME 4 -->

<div class="game-card">

<div class="game-icon">🐾</div>

<h2>Tebak Hewan</h2>

<p>Tebak hewan berdasarkan petunjuk.</p>

<button class="play" onclick="openGame('hewan')">
🔥 MAIN SEKARANG
</button>

</div>

<!-- GAME 5 -->

<div class="game-card">

<div class="game-icon">➗</div>

<h2>Matematika</h2>

<p>Uji kemampuan perkalian dan pembagian.</p>

<button class="play" onclick="openGame('math')">
🔥 MAIN SEKARANG
</button>

</div>

<!-- GAME 6 -->

<div class="game-card">

<div class="game-icon">🧩</div>

<h2>Tebak Benda</h2>

<p>Tebak benda berdasarkan petunjuk.</p>

<button class="play" onclick="openGame('benda')">
🔥 MAIN SEKARANG
</button>

</div>

<!-- GAME 7 -->

<div class="game-card">

<div class="game-icon">⚡</div>

<h2>Reaksi Cepat</h2>

<p>Seberapa cepat kamu bisa bereaksi?</p>

<button class="play" onclick="openGame('reaksi')">
🔥 MAIN SEKARANG
</button>

</div>

<!-- GAME 8 -->

<div class="game-card">

<div class="game-icon">🔢</div>

<h2>Hitung Cepat</h2>

<p>Selesaikan soal sebelum waktunya habis.</p>

<button class="play" onclick="openGame('hitung')">
🔥 MAIN SEKARANG
</button>

</div>

</div>


<!-- AREA GAME -->

<div id="gameArea">

<h2 id="gameTitle"></h2>

<div id="gameContent"></div>

<button class="gameBtn back" onclick="closeGame()">
⬅ KEMBALI KE MENU
</button>

</div>

</div>

<footer>

© 2026 Banyu Game Center  
<br>
Dibuat oleh <b>Developer Banyu</b>

</footer>


<script>

let secretNumber;
let currentGame;
let score=0;


/* OPEN GAME */

function openGame(game){

    currentGame=game;

    document.querySelector(".games").style.display="none";

    document.getElementById("gameArea").style.display="block";

    if(game==="angka") angka();
    if(game==="quiz") quiz();
    if(game==="negara") negara();
    if(game==="hewan") hewan();
    if(game==="math") math();
    if(game==="benda") benda();
    if(game==="reaksi") reaksi();
    if(game==="hitung") hitung();
}


/* CLOSE */

function closeGame(){

    document.querySelector(".games").style.display="grid";

    document.getElementById("gameArea").style.display="none";

}


/* TEBAK ANGKA */

function angka(){

    secretNumber=Math.floor(Math.random()*100)+1;

    document.getElementById("gameTitle").innerText="🎯 Tebak Angka";

    document.getElementById("gameContent").innerHTML=`

        <p>Tebak angka 1 - 100</p>

        <input id="answer"
        type="number"
        placeholder="Masukkan angka">

        <br>

        <button class="gameBtn"
        onclick="checkAngka()">
        TEBAK
        </button>

        <p id="result"></p>

    `;

}


function checkAngka(){

    let value=Number(document.getElementById("answer").value);

    let result=document.getElementById("result");

    if(value===secretNumber){

        result.innerHTML="🎉 BENAR! Kamu berhasil!";

    }

    else if(value<secretNumber){

        result.innerHTML="⬆️ Terlalu kecil!";

    }

    else{

        result.innerHTML="⬇️ Terlalu besar!";

    }

}


/* QUIZ */

function quiz(){

    document.getElementById("gameTitle").innerText="🧠 Quiz";

    document.getElementById("gameContent").innerHTML=`

    <p>Ibukota Indonesia adalah?</p>

    <input id="answer"
    placeholder="Jawaban kamu">

    <br>

    <button class="gameBtn"
    onclick="checkQuiz()">
    JAWAB
    </button>

    <p id="result"></p>

    `;

}


function checkQuiz(){

    let answer=document
    .getElementById("answer")
    .value
    .toLowerCase();

    if(answer==="jakarta"){

        document.getElementById("result")
        .innerText="🎉 BENAR!";

    }

    else{

        document.getElementById("result")
        .innerText="❌ Salah. Coba lagi!";

    }

}


/* NEGARA */

function negara(){

    document.getElementById("gameTitle").innerText="🌎 Tebak Negara";

    document.getElementById("gameContent").innerHTML=`

    <p>Negara ini terkenal dengan Menara Eiffel.</p>

    <input id="answer"
    placeholder="Nama negara">

    <br>

    <button class="gameBtn"
    onclick="checkNegara()">
    JAWAB
    </button>

    <p id="result"></p>

    `;

}


function checkNegara(){

    let answer=document
    .getElementById("answer")
    .value
    .toLowerCase();

    document.getElementById("result").innerText=

    answer==="prancis" || answer==="perancis"

    ? "🎉 BENAR!"

    : "❌ Salah!";

}


/* HEWAN */

function hewan(){

    document.getElementById("gameTitle").innerText="🐾 Tebak Hewan";

    document.getElementById("gameContent").innerHTML=`

    <p>Aku memiliki belalai panjang. Aku siapa?</p>

    <input id="answer"
    placeholder="Nama hewan">

    <br>

    <button class="gameBtn"
    onclick="checkHewan()">
    JAWAB
    </button>

    <p id="result"></p>

    `;

}


function checkHewan(){

    let answer=document
    .getElementById("answer")
    .value
    .toLowerCase();

    document.getElementById("result").innerText=

    answer==="gajah"

    ? "🎉 BENAR!"

    : "❌ Salah!";

}


/* MATEMATIKA */

function math(){

    let a=Math.floor(Math.random()*10)+1;

    let b=Math.floor(Math.random()*10)+1;

    let answer=a*b;

    document.getElementById("gameTitle")
    .innerText="➗ Matematika";

    document.getElementById("gameContent").innerHTML=`

    <p>${a} × ${b} = ?</p>

    <input id="answer"
    type="number"
    placeholder="Jawaban">

    <br>

    <button class="gameBtn"
    onclick="checkMath(${answer})">
    JAWAB
    </button>

    <p id="result"></p>

    `;

}


function checkMath(correct){

    let value=Number(
        document.getElementById("answer").value
    );

    document.getElementById("result").innerText=

    value===correct
    ? "🎉 BENAR!"
    : "❌ Salah!";

}


/* BENDA */

function benda(){

    document.getElementById("gameTitle").innerText="🧩 Tebak Benda";

    document.getElementById("gameContent").innerHTML=`

    <p>Aku digunakan untuk melihat waktu. Aku punya jarum.</p>

    <input id="answer"
    placeholder="Nama benda">

    <br>

    <button class="gameBtn"
    onclick="checkBenda()">
    JAWAB
    </button>

    <p id="result"></p>

    `;

}


function checkBenda(){

    let answer=document
    .getElementById("answer")
    .value
    .toLowerCase();

    document.getElementById("result").innerText=

    answer==="jam"

    ? "🎉 BENAR!"

    : "❌ Salah!";

}


/* REAKSI */

function reaksi(){

    document.getElementById("gameTitle")
    .innerText="⚡ Reaksi Cepat";

    document.getElementById("gameContent").innerHTML=`

    <p>Klik tombol secepat mungkin!</p>

    <button
    class="gameBtn"
    onclick="reactionStart()">
    MULAI
    </button>

    <p id="result"></p>

    `;

}


function reactionStart(){

    let start=Date.now();

    document.getElementById("gameContent").innerHTML=`

    <button
    class="gameBtn"
    onclick="reactionEnd(${start})">
    ⚡ KLIK!
    </button>

    `;

}


function reactionEnd(start){

    let time=Date.now()-start;

    document.getElementById("gameContent").innerHTML=`

    <h2>⚡ ${time} ms</h2>

    <p>Semakin kecil waktunya semakin cepat!</p>

    <button
    class="gameBtn"
    onclick="reaksi()">
    COBA LAGI
    </button>

    `;

}


/* HITUNG CEPAT */

function hitung(){

    let a=Math.floor(Math.random()*20)+1;

    let b=Math.floor(Math.random()*20)+1;

    let answer=a+b;

    document.getElementById("gameTitle")
    .innerText="🔢 Hitung Cepat";

    document.getElementById("gameContent").innerHTML=`

    <p>${a} + ${b} = ?</p>

    <input id="answer"
    type="number"
    placeholder="Jawaban">

    <br>

    <button
    class="gameBtn"
    onclick="checkHitung(${answer})">
    JAWAB
    </button>

    <p id="result"></p>

    `;

}


function checkHitung(correct){

    let value=Number(
        document.getElementById("answer").value
    );

    document.getElementById("result").innerText=

    value===correct
    ? "🔥 BENAR!"

    : "❌ Salah!";

}

</script>

</body>
</html>
