<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>For You ❤️</title>

<style>
body {
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(135deg, #1f2c3a, #3a6073);
  overflow: hidden;
  color: white;
}

/* Intro */
#intro {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 22px;
  background: black;
  cursor: pointer;
  z-index: 10;
}

/* Character (updated) */
.character {
  position: absolute;
  bottom: 0;
  left: -250px;
  width: 260px;
  opacity: 0;
  filter: drop-shadow(0 0 15px rgba(0,150,255,0.4));
  mix-blend-mode: lighten;
}

/* Walk in */
@keyframes walkIn {
  0% { left: -250px; opacity: 0; }
  100% { left: 20px; opacity: 1; }
}

/* Idle bounce */
@keyframes idle {
  0%,100% { transform: translateY(0); }
  50% { transform: translateY(-5px); }
}

/* Hand forward */
@keyframes handForward {
  0% { transform: translateX(0); }
  100% { transform: translateX(30px); }
}

/* Settle */
@keyframes settle {
  0% { transform: translateX(30px); }
  100% { transform: translateX(0); }
}

/* Speech */
.speech {
  position: absolute;
  bottom: 240px;
  left: 200px;
  background: white;
  color: black;
  padding: 10px 15px;
  border-radius: 12px;
  display: none;
  font-size: 14px;
}

/* Letter */
.letter {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%) scale(0.8);
  background: rgba(255,255,255,0.95);
  color: black;
  padding: 25px;
  width: 85%;
  max-width: 520px;
  border-radius: 20px;
  box-shadow: 0 0 30px rgba(0,0,0,0.5);
  display: none;
}

/* Text */
#text {
  white-space: pre-line;
  font-size: 15px;
  line-height: 1.5;
}

/* Pop */
@keyframes pop {
  to { transform: translate(-50%, -50%) scale(1); }
}

/* Ending */
#ending {
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.9);
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 32px;
  opacity: 0;
  transition: opacity 2s;
}

.glow {
  animation: glow 2s infinite alternate;
}

@keyframes glow {
  from { text-shadow: 0 0 10px #4ca1af; }
  to { text-shadow: 0 0 30px #ffffff; }
}
</style>
</head>

<body>

<div id="intro" onclick="startExperience()">
✨ Tap to open your surprise 💌
</div>

<!-- ✅ YOUR IMAGE ADDED -->
<img class="character" id="char" src="https://i.imgur.com/q1Aq2or.jpeg">

<div class="speech" id="speech">hey… this is for u 💌</div>

<div class="letter" id="letter">
  <div id="text"></div>
</div>

<div id="ending">
  <div class="glow">I like you the most 💙</div>
</div>

<audio id="music" src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3"></audio>

<script>
const msg = `Hbdyy ❤️

I rlly hope u hv the best day ever. U mean sm to me fr, like more than I even say sometimes, and I’m genuinely so grateful ur in my life. U literally make my days better just by being u, even on days u don’t realize it. Even the smallest things remind me of u sometimes 😭 and I just end up smiling for no reason. I hope this yr brings u all the happiness, success, and everything you’ve been wishing for, cuz u truly deserve the best of everything.

Ik I can’t celebrate ur bday the way it shld be rn cuz of circumstances, but one day I promise I’m gonna make it up to u properly 🫶

And I just want u to know I care abt u sm… more than I probably show sometimes. I’ll always be here for u no matter what.

Now go enjoy ur day 😌💙`;

let i = 0;

function startExperience() {
  document.getElementById("intro").style.display = "none";

  let char = document.getElementById("char");
  char.style.animation = "walkIn 2s forwards";

  document.getElementById("music").play();

  setTimeout(() => {
    char.style.animation = "walkIn 2s forwards, idle 2s infinite";
  }, 2000);

  setTimeout(() => {
    char.style.animation = "handForward 0.6s forwards, idle 2s infinite";
    document.getElementById("speech").style.display = "block";
  }, 3000);

  setTimeout(() => {
    char.style.animation = "settle 0.5s forwards, idle 2s infinite";
    document.getElementById("speech").style.display = "none";

    let letter = document.getElementById("letter");
    letter.style.display = "block";
    letter.style.animation = "pop 0.8s forwards";

    typeText();
  }, 4200);
}

function typeText() {
  if (i < msg.length) {
    document.getElementById("text").innerHTML += msg.charAt(i);
    i++;
    setTimeout(typeText, 20);
  } else {
    setTimeout(showEnding, 2000);
  }
}

function showEnding() {
  document.getElementById("ending").style.opacity = 1;
}
</script>

</body>
</html>
