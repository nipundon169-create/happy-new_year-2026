<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy New Year 2026 💖</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:'Poppins', sans-serif;
}

body{
  height:100vh;
  background: linear-gradient(135deg,#ffdde1,#ee9ca7);
  overflow:hidden;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  color:#fff;
}

.container{
  z-index:5;
  padding:25px;
  background:rgba(255,255,255,0.18);
  backdrop-filter:blur(14px);
  border-radius:22px;
  animation:fadeIn 2s ease;
  max-width:90%;
}

h1{
  font-size:2.2rem;
  text-shadow:0 0 15px #fff;
}

h2{
  font-size:3.8rem;
  color:#fff4b0;
  margin:10px 0;
  animation:pulse 2s infinite;
}

.message{
  font-size:1.05rem;
  line-height:1.6;
  margin-top:12px;
}

.name{
  margin-top:14px;
  font-size:1.15rem;
  color:#ffe6f7;
}

button{
  margin-top:18px;
  padding:10px 20px;
  border:none;
  border-radius:25px;
  background:#fff;
  color:#ee5a9c;
  font-size:1rem;
  cursor:pointer;
}

@keyframes pulse{
  0%{ transform:scale(1); }
  50%{ transform:scale(1.05); }
  100%{ transform:scale(1); }
}

@keyframes fadeIn{
  from{ opacity:0; transform:translateY(30px); }
  to{ opacity:1; transform:translateY(0); }
}

/* Floating hearts & stars */
.float{
  position:absolute;
  bottom:-20px;
  font-size:20px;
  animation:floatUp linear infinite;
  opacity:0.8;
}

@keyframes floatUp{
  from{
    transform:translateY(0) translateX(0);
    opacity:1;
  }
  to{
    transform:translateY(-110vh) translateX(30px);
    opacity:0;
  }
}

/* Confetti */
.confetti{
  position:absolute;
  width:8px;
  height:8px;
  top:-10px;
  animation:fall linear infinite;
}

@keyframes fall{
  to{
    transform:translateY(110vh) rotate(360deg);
  }
}

/* Firework */
.firework{
  position:absolute;
  width:5px;
  height:5px;
  border-radius:50%;
  animation:explode 2s ease-out;
}

@keyframes explode{
  from{ transform:scale(1); opacity:1; }
  to{ transform:scale(25); opacity:0; }
}
</style>
</head>

<body>

<!-- Music -->
<audio id="music" loop>
  <source src="https://cdn.pixabay.com/audio/2022/03/15/audio_1c0b76f5bb.mp3" type="audio/mpeg">
</audio>

<div class="container">
  <h1>🎀 Happy New Year 🎀</h1>
  <h2>2026</h2>

  <div class="message">
    “Hasti reh na… bilkul waise hi jaise tu naturally karti hai 💕<br>
    Teri excitement meri favourite cheez hai ✨<br>
    Aur jab tera mood thoda sa bhi off hota hai na,<br>
    toh mera dil bhi chup-sa ho jaata hai 🥺<br>
    Isliye apna khayal rakha kar 🌸<br>
    Aur haan… <b>mujhe ‘haan’ jaldi kar de</b> 😌💗<br>
    Aur mujhe zyada kilsaya mat kar 😋”
  </div>

  <div class="name">— From Harshita 💖</div>
  <button onclick="playMusic()">🎵 Tap for Music</button>
</div>

<script>
function playMusic(){
  document.getElementById('music').play();
}

/* Floating hearts & stars */
const emojis = ["💖","💕","💗","✨","⭐","🌟"];
setInterval(()=>{
  const e = document.createElement("div");
  e.className = "float";
  e.innerText = emojis[Math.floor(Math.random()*emojis.length)];
  e.style.left = Math.random()*100 + "vw";
  e.style.fontSize = (Math.random()*15 + 15) + "px";
  e.style.animationDuration = (Math.random()*4 + 6) + "s";
  document.body.appendChild(e);
  setTimeout(()=>e.remove(),10000);
},300);

/* Confetti */
for(let i=0;i<30;i++){
  const c=document.createElement('div');
  c.className='confetti';
  c.style.left=Math.random()*100+'vw';
  c.style.animationDuration=(Math.random()*3+3)+'s';
  c.style.background=`hsl(${Math.random()*360},100%,80%)`;
  document.body.appendChild(c);
}

/* Fireworks */
function firework(){
  const f=document.createElement('div');
  f.className='firework';
  f.style.left=Math.random()*100+'vw';
  f.style.top=Math.random()*100+'vh';
  f.style.background=`hsl(${Math.random()*360},100%,70%)`;
  document.body.appendChild(f);
  setTimeout(()=>f.remove(),2000);
}
setInterval(firework,500);
</script>

</body>
</html>
