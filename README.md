
[valentine.html](https://github.com/user-attachments/files/25075716/valentine.html)
<!DOCTYPE html>
<html>
<head>
  <title>Access for Spidy Only 😈</title>
  <style>
    body {
      background: linear-gradient(135deg, #ff416c, #ff4b2b);
      font-family: 'Comic Sans MS', cursive;
      text-align: center;
      color: white;
      overflow: hidden;
    }

    h1 { margin-top: 60px; font-size: 50px; }

    input {
      padding: 10px;
      font-size: 18px;
      border-radius: 20px;
      border: none;
      text-align: center;
    }

    button {
      background: black;
      border: none;
      padding: 15px 35px;
      color: white;
      font-size: 20px;
      border-radius: 30px;
      cursor: pointer;
      margin: 15px;
    }

    #noBtn { position: absolute; }

    .gallery img {
      width: 180px;
      height: 180px;
      border-radius: 20px;
      margin: 10px;
      object-fit: cover;
      border: 3px solid white;
    }

    .heart {
      position: fixed;
      font-size: 22px;
      animation: float 6s linear infinite;
    }

    @keyframes float {
      0% {bottom: -10px;}
      100% {bottom: 100vh;}
    }
  </style>
</head>
<body>

<h1>Enter Password Spidy 🔐</h1>
<p>(Hint: spidycutu)</p>

<input type="password" id="pass">
<br>
<button onclick="unlock()">Unlock 😏</button>

<div id="content" style="display:none;">
  <h1>Happy Valentine Spidy 🕷️💖</h1>
  <h2>Will you be mine forever?</h2>

  <button onclick="yes()">YES ❤️</button>
  <button id="noBtn" onmouseover="moveNo()">NO 🙄</button>

  <div class="gallery">
  <img src="spidy1.jpeg">
  <img src="spidy2.jpeg">
  <img src="spidy3.jpeg">
</div>

</div>

</div>

<div id="message"></div>

<audio id="song" src="song.mp3" loop></audio>

<script>
function unlock() {
  if (document.getElementById("pass").value == "spidycutu") {
    document.getElementById("content").style.display = "block";
    document.getElementById("song").play();
  } else {
    alert("Wrong password 😤 Go ask mummy");
  }
}

function yes() {
  document.getElementById("message").innerHTML =
  "IYE MERA BIKE HAI 😤🚲<br><br>" +
  "Spidy tu chor hai but mera chor hai.<br>" +
  "Dil bhi mera, bike bhi mera 😏❤️<br><br>" +
  "Happy Valentine jaan 💘";
}

function moveNo() {
  const noBtn = document.getElementById("noBtn");
  noBtn.style.left = Math.random()*300 + "px";
  noBtn.style.top = Math.random()*300 + "px";
}

setInterval(() => {
  const heart = document.createElement("div");
  heart.innerHTML = "😂❤️";
  heart.className = "heart";
  heart.style.left = Math.random()*100 + "vw";
  document.body.appendChild(heart);
  setTimeout(()=>heart.remove(),6000);
}, 200);
</script>

</body>
</html>
