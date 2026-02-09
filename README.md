# Happy-Valentine-s-Day
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Love Letter for Crush 💌</title>

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&display=swap" rel="stylesheet">

<style>
/* ===== CSS ===== */

body {
  background-color: #f0e6f6;
  font-family: Arial, sans-serif;
}

.envlope-wrapper {
  height: 380px;
}

#envelope {
  position: relative;
  width: 280px;
  height: 180px;
  margin: 150px auto 0;
  background-color: #d9534f;
  border-bottom-left-radius: 6px;
  border-bottom-right-radius: 6px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.2);
  cursor: pointer;
}

.front {
  position: absolute;
  width: 0;
  height: 0;
  z-index: 3;
}

.flap {
  border-left: 140px solid transparent;
  border-right: 140px solid transparent;
  border-bottom: 82px solid transparent;
  border-top: 98px solid #d9534f;
  transform-origin: top;
}

.pocket {
  border-left: 140px solid #f5a3a2;
  border-right: 140px solid #f5a3a2;
  border-bottom: 90px solid #ff6f61;
  border-top: 90px solid transparent;
  border-bottom-left-radius: 6px;
  border-bottom-right-radius: 6px;
}

.letter {
  position: relative;
  background: white;
  width: 90%;
  height: 90%;
  margin: auto;
  top: 5%;
  border-radius: 6px;
  box-shadow: 0 2px 26px rgba(0,0,0,0.12);
  font-family: "Dancing Script", cursive;
}

.words {
  position: absolute;
  left: 10%;
  width: 80%;
  text-align: center;
}

.line1 { top: 15%; font-size: 0.9rem; }
.line2 { top: 35%; font-size: 1.2rem; }
.line3 { top: 55%; font-size: 1.2rem; }
.line4 { top: 75%; font-size: 1.2rem; }

.open .flap {
  transform: rotateX(180deg);
  transition: transform 0.4s ease;
  z-index: 1;
}

.close .flap {
  transform: rotateX(0deg);
  transition: transform 0.4s ease;
  z-index: 5;
}

.open .letter {
  transform: translateY(-100px);
  transition: transform 0.4s 0.4s ease;
}

.close .letter {
  transform: translateY(0);
  transition: transform 0.4s ease;
}

.reset {
  text-align: center;
  margin-top: 20px;
}

.reset button {
  border: 2px solid #d9534f;
  background: transparent;
  color: #d9534f;
  padding: 10px 20px;
  cursor: pointer;
  font-weight: bold;
  margin: 5px;
}

.reset button:hover {
  background: #d9534f;
  color: white;
}
</style>
</head>

<body>

<div class="envlope-wrapper">
  <div id="envelope" class="close">
    <div class="front flap"></div>
    <div class="front pocket"></div>

    <div class="letter">
      <div class="words line1">To: Crush 💖</div>
      <div class="words line2">Dear crush, you are so beautiful</div>
      <div class="words line3">Every time I see you</div>
      <div class="words line4">my world stops ✨</div>
    </div>
  </div>
</div>

<div class="reset">
  <button id="open">Open</button>
  <button id="close">Close</button>
</div>

<script>
/* ===== JavaScript ===== */

const envelope = document.getElementById("envelope");
const openBtn = document.getElementById("open");
const closeBtn = document.getElementById("close");

openBtn.onclick = () => {
  envelope.classList.remove("close");
  envelope.classList.add("open");
};

closeBtn.onclick = () => {
  envelope.classList.remove("open");
  envelope.classList.add("close");
};

envelope.onclick = () => {
  envelope.classList.toggle("open");
  envelope.classList.toggle("close");
};
</script>

</body>
</html>
