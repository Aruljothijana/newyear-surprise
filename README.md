# newyear-surprise
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Aruljothi ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
  margin:0;
  height:100vh;
  background:linear-gradient(135deg,#220033,#000);
  display:flex;
  justify-content:center;
  align-items:center;
  font-family:'Segoe UI',sans-serif;
  color:#fff;
}
.card{
  background:rgba(255,255,255,0.1);
  padding:30px;
  border-radius:22px;
  text-align:center;
  width:340px;
}
h1{color:#ff9ad5;}
.circle{
  width:120px;height:120px;
  border-radius:50%;
  border:6px solid rgba(255,154,213,0.3);
  margin:25px auto;
  display:flex;
  align-items:center;
  justify-content:center;
  position:relative;
}
.heart{
  font-size:42px;
  cursor:pointer;
}
.progress{
  position:absolute;
  inset:0;
  border-radius:50%;
  border:6px solid transparent;
  border-top-color:#ff5fa2;
  transform:rotate(-90deg);
}
.content{
  display:none;
}
img{
  width:100%;
  border-radius:15px;
  margin:12px 0;
}
.note{
  margin-top:15px;
  color:#ffd6ec;
}
</style>
</head>

<body>

<audio id="song" loop>
  <source src="https://files.catbox.moe/5g1z6y.mp3" type="audio/mpeg">
</audio>

<div class="card">
  <h1>A little surprise for you 💕</h1>
  <p>Before this year begins</p>

  <div class="circle" id="circle">
    <div class="progress" id="progress"></div>
    <div class="heart" id="heart">❤️</div>
  </div>

  <div class="content" id="content">
    <h2>Aruljothi 🌙</h2>

    <img src="photo1.jpg">
    <img src="photo2.jpg">

    <div class="note">
      ✨ Happy New Year, my love ✨<br><br>
      Every smile of yours is my favorite view,  
      every moment with you is my peace 💖<br><br>

      <b>With Love to My Daalu 💋</b><br>
      — Janaranjan
    </div>
  </div>
</div>

<script>
let timer;
const heart=document.getElementById("heart");
const content=document.getElementById("content");
const progress=document.getElementById("progress");
const song=document.getElementById("song");

heart.addEventListener("touchstart",start);
heart.addEventListener("mousedown",start);
heart.addEventListener("touchend",stop);
heart.addEventListener("mouseup",stop);

function start(){
  progress.style.animation="spin 2s linear forwards";
  timer=setTimeout(()=>{
    content.style.display="block";
    song.play();
  },2000);
}
function stop(){ clearTimeout(timer); }
</script>

<style>
@keyframes spin{
  from{transform:rotate(-90deg);}
  to{transform:rotate(270deg);}
}
</style>

</body>
</html>
