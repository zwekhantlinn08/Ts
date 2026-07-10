<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Love ❤️</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}
body{height:100vh;overflow:hidden;display:flex;justify-content:center;align-items:center;background:linear-gradient(135deg,#ffe6f0,#fff6fb,#ffd9ec);}
.container{text-align:center;padding:30px;}
h1{font-size:2.5rem;color:#ff5f9f;margin-bottom:30px;line-height:1.4;}
.buttons{position:relative;height:120px;}
button{padding:15px 35px;font-size:20px;border:none;border-radius:50px;cursor:pointer;transition:.2s;box-shadow:0 8px 20px rgba(0,0,0,.15);}
#yes{background:#ff7eb6;color:white;margin-right:20px;}
#yes:hover{transform:scale(1.1);}
#no{background:white;color:#ff5f9f;position:absolute;}
.result{display:none;animation:pop .5s ease;}
.photo-container{position:relative;display:inline-block;margin-top:25px;}
.photo{width:280px;height:280px;object-fit:cover;border-radius:25px;box-shadow:0 15px 30px rgba(0,0,0,.25);}
.bear{position:absolute;right:-50px;bottom:5px;font-size:70px;transform:rotate(-15deg);animation:bounce 2s infinite;}
.message{margin-top:20px;font-size:24px;color:#ff5f9f;font-weight:bold;}
@keyframes pop{from{transform:scale(.3);opacity:0;}to{transform:scale(1);opacity:1;}}
@keyframes bounce{50%{transform:translateY(-10px) rotate(-15deg);}}
</style>
</head>
<body>
<div class="container" id="question">
<h1>sate soe pyay p lrr hin?😣😣😣😣😣</h1>
<div class="buttons">
<button id="yes">Yes 💗</button>
<button id="no">No 😤</button>
</div>
</div>
<div class="container result" id="result">
<h1>Yay!! Lein mrr lyk tk kaalyy lyyy🙈🙊🤭</h1>
<div class="photo-container">
<img src="IMG_1614.jpeg" class="photo">
<div class="bear">🐻💋</div>
</div>
<div class="message">Thank you for understanding ❤️😁</div>
</div>
<script>
const no=document.getElementById("no");
function moveButton(){
const maxX = window.innerWidth - 140;
const maxY = window.innerHeight - 100;
const newX = Math.max(10, Math.floor(Math.random() * maxX));
const newY = Math.max(10, Math.floor(Math.random() * maxY));
no.style.left = newX + "px";
no.style.top = newY + "px";
}
no.addEventListener("mouseenter",moveButton);
no.addEventListener("click",moveButton);
no.addEventListener("touchstart",function(e){
e.preventDefault();
moveButton();
});
document.getElementById("yes").onclick=()=>{
document.getElementById("question").style.display="none";
document.getElementById("result").style.display="block";
}
</script>
</body>
</html>
