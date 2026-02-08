<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<title>حبزلوم و حبزلمهه</title>
<link href="https://fonts.googleapis.com/css2?family=Amiri&display=swap" rel="stylesheet">
<style>
body{
  margin:0;
  background:#0b0b0b;
  color:#fff;
  font-family:'Amiri',serif;
  text-align:center;
}
.container{
  padding:40px 15px;
}
h1{
  color:#ff5fa2;
}
button{
  background:#ff5fa2;
  border:none;
  padding:15px 25px;
  font-size:18px;
  border-radius:30px;
  color:#fff;
  cursor:pointer;
}
.msg{
  margin-top:25px;
  font-size:22px;
  opacity:0;
  transition:1s;
}
.hearts{
  position:fixed;
  top:0;left:0;
  width:100%;height:100%;
  pointer-events:none;
}
.heart{
  position:absolute;
  color:#ff5fa2;
  animation:float 6s linear infinite;
}
@keyframes float{
  0%{transform:translateY(100vh);opacity:0;}
  50%{opacity:1;}
  100%{transform:translateY(-10vh);opacity:0;}
}
</style>
</head>
<body>

<div class="container">
<h1>حبزلوم ❤️ حبزلمهه</h1>
<p>(في حب دائمًا)</p>

<button onclick="startLove()">▶ شغّل الحب</button>

<div class="msg" id="m1">بحبك من واحنا أطفال ربنا يخليكي ليا</div>
<div class="msg" id="m2">هحبك طول العمر يا نور عين جوزك 🫂</div>
<div class="msg" id="m3">بحبك يا دلوعه أبوكي 🥹</div>
<div class="msg" id="m4">وجودك في حياتي نعمة 💖</div>

<audio id="song">
<source src="https://www.youtube.com/embed/Y8sYcYkKZqI?start=55" type="audio/mpeg">
</audio>
</div>

<div class="hearts" id="hearts"></div>

<script>
function startLove(){
  document.getElementById("song").play();
  let msgs=["m1","m2","m3","m4"];
  msgs.forEach((id,i)=>{
    setTimeout(()=>{document.getElementById(id).style.opacity=1;},i*3000);
  });
}
setInterval(()=>{
  let h=document.createElement("div");
  h.className="heart";
  h.innerHTML="❤️";
  h.style.left=Math.random()*100+"%";
  h.style.fontSize=(20+Math.random()*20)+"px";
  document.getElementById("hearts").appendChild(h);
  setTimeout(()=>h.remove(),6000);
},500);
</script>

</body>
</html>
# habzlamaa
