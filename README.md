<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Resmî Özür Duyurusu</title>

<style>
body{
margin:0;
font-family:Arial,Helvetica,sans-serif;
background:linear-gradient(135deg,#ff7eb3,#ff758c,#ff9770);
min-height:100vh;
display:flex;
justify-content:center;
align-items:center;
}

.card{
background:white;
padding:40px;
border-radius:25px;
width:90%;
max-width:700px;
text-align:center;
box-shadow:0 20px 50px rgba(0,0,0,.25);
}

h1{
font-size:40px;
margin-bottom:10px;
}

.status{
font-size:24px;
color:red;
font-weight:bold;
margin-bottom:25px;
}

button{
padding:18px 35px;
font-size:22px;
border:none;
border-radius:15px;
cursor:pointer;
background:#ff4d6d;
color:white;
transition:.25s;
}

button:hover{
transform:scale(1.08);
}

#msg{
margin-top:30px;
font-size:22px;
font-weight:bold;
display:none;
}

.progress{
width:100%;
height:22px;
background:#ddd;
border-radius:20px;
overflow:hidden;
margin:20px 0;
}

.bar{
height:100%;
width:2%;
background:#4CAF50;
transition:0.6s ease;
}

footer{
margin-top:35px;
font-size:14px;
color:gray;
}
</style>

</head>

<body>

<div class="card">

<h1>🚨 Arel Industries™ 🚨</h1>

<h2>RESMÎ BASIN AÇIKLAMASI</h2>

<p>
Yapılan kapsamlı iç soruşturma sonucunda,
<b>Arel'in sevgilisinin gönlünü kırdığı</b>
tespit edilmiştir.
</p>

<p class="status">
🔴 DURUM: Kritik
</p>

<p>
Sorumlu kişi (Arel)
zorunlu sarılma eğitimine alınmış,
24 saat boyunca "Haklısın aşkım." deme cezasına çarptırılmıştır.
</p>

<div class="progress">
<div class="bar" id="bar"></div>
</div>

<p>
Affedilme İhtimali:
<b id="percent">%2</b>
</p>

<button onclick="forgive()">
💖 BENİ AFFET 💖
</button>

<div id="msg"></div>

<footer>
© 2026 Arel Industries • Sevgiliyi Üzme Departmanı
</footer>

</div>

<script>
let chance = 2;

const texts = [
"🥹 Şans arttı!",
"🥺 Bir sarılma daha lazım...",
"🥹 Çikolata öneriliyor...",
"😭 Hâlâ biraz kızgın...",
"🥰 Gülmeye başladı!",
"💖 BAŞARILI! AFFEDİLDİN!"
];

function forgive(){
chance += 20;

if(chance > 100) chance = 100;

document.getElementById("bar").style.width = chance + "%";
document.getElementById("percent").innerText = "%" + chance;

let msg = document.getElementById("msg");
msg.style.display = "block";

if(chance < 100){
let index = Math.min(Math.floor(chance / 20), texts.length - 1);
msg.innerText = texts[index];
}else{
msg.innerHTML = "🎉 Tebrikler! Affedildin.<br><br>Ödül: Sonsuz sarılma ❤️";
}
}
</script>

</body>
</html>
