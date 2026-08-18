# birthday--website-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Allie ♡</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@500;600&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "DM Sans", sans-serif;
  color: #24171b;
  min-height: 100vh;
  overflow-x: hidden;
  background:
    radial-gradient(circle at 10% 15%, #ffb6c1 0, transparent 25%),
    radial-gradient(circle at 90% 25%, #8fc4ff 0, transparent 27%),
    linear-gradient(135deg, #fff3f5, #edf5ff);
}

/* BACKGROUND EFFECTS */

.bg {
  position: fixed;
  border-radius: 50%;
  pointer-events: none;
  z-index: -1;
  filter: blur(2px);
}

.bg1 {
  width: 250px;
  height: 250px;
  background: #ef476f;
  left: -130px;
  top: 20%;
  opacity: .25;
  animation: float 8s infinite ease-in-out;
}

.bg2 {
  width: 300px;
  height: 300px;
  background: #3185d8;
  right: -160px;
  bottom: 10%;
  opacity: .22;
  animation: float 10s infinite ease-in-out reverse;
}

@keyframes float {
  50% {
    transform: translateY(-35px);
  }
}

/* NAVIGATION */

header {
  position: fixed;
  z-index: 100;
  top: 0;
  left: 0;
  width: 100%;
  padding: 14px 6%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: rgba(255,255,255,.78);
  backdrop-filter: blur(15px);
  border-bottom: 1px solid rgba(0,0,0,.06);
}

.logo {
  color: #bd203c;
  font-weight: 700;
  cursor: pointer;
}

nav {
  display: flex;
  gap: 5px;
  overflow-x: auto;
}

nav button {
  border: 0;
  background: transparent;
  padding: 8px 12px;
  border-radius: 20px;
  cursor: pointer;
  white-space: nowrap;
}

nav button:hover {
  background: #ffe0e6;
}

/* PAGES */

.page {
  display: none;
  min-height: 100vh;
  padding: 110px 6% 70px;
  justify-content: center;
  align-items: center;
}

.page.active {
  display: flex;
  animation: pageIn .65s ease;
}

@keyframes pageIn {
  from {
    opacity: 0;
    transform: translateY(18px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.card {
  width: min(920px, 100%);
  padding: clamp(28px, 6vw, 60px);
  background: rgba(255,255,255,.9);
  border-radius: 30px;
  border: 1px solid rgba(255,255,255,.9);
  box-shadow: 0 25px 70px rgba(55,25,35,.13);
  position: relative;
  overflow: hidden;
}

.card:after {
  content: "";
  position: absolute;
  width: 180px;
  height: 180px;
  border-radius: 50%;
  background: #dcecff;
  right: -80px;
  top: -80px;
  opacity: .55;
}

h1,
h2 {
  font-family: "Playfair Display", serif;
}

h1 {
  font-size: clamp(3rem, 8vw, 6rem);
  color: #b51e39;
  line-height: .95;
}

h2 {
  font-size: clamp(2rem, 5vw, 3.4rem);
  color: #b51e39;
  margin-bottom: 20px;
}

h3 {
  margin-bottom: 12px;
}

p {
  line-height: 1.8;
  margin: 10px 0;
}

.small {
  color: #777;
  font-size: .9rem;
}

/* CAT */

.cat {
  width: 180px;
  height: 180px;
  object-fit: contain;
  animation: catFloat 4s ease-in-out infinite;
}

@keyframes catFloat {
  0%,100% {
    transform: translateY(0) rotate(-2deg);
  }
  50% {
    transform: translateY(-12px) rotate(2deg);
  }
}

.cat-area {
  text-align: center;
  margin-bottom: 20px;
}

/* BUTTON */

.main-btn {
  margin-top: 25px;
  border: none;
  padding: 14px 26px;
  border-radius: 30px;
  background: linear-gradient(100deg,#b91f3b,#e3425c);
  color: white;
  font-weight: 700;
  cursor: pointer;
  box-shadow: 0 9px 22px rgba(185,31,59,.25);
  transition: .25s;
}

.main-btn:hover {
  transform: translateY(-4px);
  box-shadow: 0 15px 30px rgba(185,31,59,.3);
}

.back {
  margin-top: 25px;
  border: 0;
  padding: 10px 18px;
  border-radius: 20px;
  background: #e8f2ff;
  cursor: pointer;
}

/* OPENING */

.center {
  text-align: center;
}

.delivery {
  display: inline-block;
  padding: 12px 20px;
  background: #e8f3ff;
  border: 1px solid #c7def8;
  border-radius: 14px;
  margin: 15px 0;
  font-weight: 700;
}

/* HOME */

.home p {
  max-width: 650px;
  margin: 15px auto;
}

.home {
  text-align: center;
}

.blue {
  color: #3478c5;
}

.menu {
  display: grid;
  grid-template-columns: repeat(4,1fr);
  gap: 15px;
  margin-top: 35px;
}

.menu-item {
  padding: 22px 14px;
  background: white;
  border: 1px solid #eadce0;
  border-radius: 20px;
  cursor: pointer;
  transition: .25s;
}

.menu-item:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 35px rgba(60,30,40,.1);
  border-color: #d93b55;
}

.menu-item strong {
  display: block;
  color: #bd233d;
  margin-bottom: 8px;
}

.menu-item span {
  color: #777;
  font-size: .85rem;
}

/* LETTER */

.letter {
  background: #fffdf8;
  border-left: 4px solid #c72a44;
  padding: clamp(25px,5vw,45px);
}

.letter p {
  font-family: Georgia, serif;
  font-size: 1.05rem;
}

.signature {
  margin-top: 30px;
  color: #bb2841;
  font-style: italic;
}

/* MUSIC */

.music {
  text-align: center;
}

.record {
  width: 175px;
  height: 175px;
  margin: 25px auto;
  border-radius: 50%;
  background:
    repeating-radial-gradient(
      circle,
      #151515 0 5px,
      #343434 6px 8px
    );
  display: grid;
  place-items: center;
  color: white;
  font-size: 3rem;
  box-shadow: 0 15px 35px rgba(0,0,0,.25);
}

.record.playing {
  animation: spin 2s linear infinite;
}

@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}

.lyrics {
  display: none;
  max-width: 600px;
  margin: 30px auto;
  padding: 30px;
  border-radius: 22px;
  background: linear-gradient(135deg,#fff0f3,#edf6ff);
  border: 1px solid #dddfe7;
}

.lyrics.show {
  display: block;
}

.lyrics p {
  font-family: Georgia, serif;
  font-size: 1.2rem;
  opacity: 0;
  animation: lyric .7s forwards;
}

.lyrics p:nth-child(1) { animation-delay: .3s; }
.lyrics p:nth-child(2) { animation-delay: 1.2s; }
.lyrics p:nth-child(3) { animation-delay: 2.1s; }
.lyrics p:nth-child(4) { animation-delay: 3s; }

@keyframes lyric {
  from {
    opacity: 0;
    transform: translateY(15px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* THOUGHTS */

.thoughts {
  display: grid;
  grid-template-columns: repeat(2,1fr);
  gap: 18px;
}

.thought {
  padding: 25px;
  background: white;
  border-radius: 20px;
  border: 1px solid #eee;
  transition: .25s;
}

.thought:hover {
  transform: scale(1.03);
}

.thought:nth-child(odd) {
  border-left: 4px solid #d52c48;
}

.thought:nth-child(even) {
  border-left: 4px solid #3981d0;
}

/* GIFT */

.gift-page {
  text-align: center;
}

.gift {
  display: inline-block;
  font-size: 7rem;
  cursor: pointer;
  animation: gift 2s infinite;
}

@keyframes gift {
  50% {
    transform: translateY(-12px) rotate(4deg);
  }
}

.final {
  display: none;
  max-width: 650px;
  margin: 30px auto 0;
}

.final.show {
  display: block;
  animation: pageIn .8s ease;
}

/* LAST */

.last {
  text-align: center;
}

.last-heart {
  font-size: 5rem;
  color: #cf2944;
  animation: heartbeat 1.2s infinite;
}

@keyframes heartbeat {
  50% {
    transform: scale(1.18);
  }
}

.labu {
  font-family: "Playfair Display", serif;
  color: #bd233d;
  font-size: 3rem;
  margin-top: 40px;
}

/* CONFETTI */

.confetti {
  position: fixed;
  width: 8px;
  height: 13px;
  top: -20px;
  z-index: 500;
  pointer-events: none;
  animation: fall 3.5s linear forwards;
}

@keyframes fall {
  to {
    transform: translateY(110vh) rotate(720deg);
    opacity: 0;
  }
}

/* MOBILE */

@media(max-width:800px) {

  header {
    flex-direction: column;
    align-items: flex-start;
    gap: 7px;
  }

  nav {
    width: 100%;
  }

  .menu {
    grid-template-columns: repeat(2,1fr);
  }

  .thoughts {
    grid-template-columns: 1fr;
  }
}

@media(max-width:500px) {

  .menu {
    grid-template-columns: 1fr;
  }

  .card {
    border-radius: 22px;
  }

  .cat {
    width: 145px;
    height: 145px;
  }

  h1 {
    font-size: 3.2rem;
  }
}
</style>
</head>

<body>

<div class="bg bg1"></div>
<div class="bg bg2"></div>

<header>

  <div class="logo" onclick="showPage('home')">
    ALLIE'S BIRTHDAY
  </div>

  <nav>
    <button onclick="showPage('home')">Home</button>
    <button onclick="showPage('letter')">Letter</button>
    <button onclick="showPage('music')">Music</button>
    <button onclick="showPage('thoughts')">Thoughts</button>
    <button onclick="showPage('gift')">Gift</button>
  </nav>

</header>


<!-- OPENING -->

<section id="opening" class="page active">

  <div class="card center">

    <div class="cat-area">

      <img
        class="cat"
        src="https://media.tenor.com/2roX3uxz_68AAAAi/cat-cute.gif"
        alt="cat">

    </div>

    <p class="small">meow.</p>

    <h1>A tiny delivery<br>for you.</h1>

    <p>
      Something small has arrived.
    </p>

    <div class="delivery">
      BIRTHDAY DELIVERY — FOR ALLIE
    </div>

    <p>Are you Allie?</p>

    <button class="main-btn" onclick="showPage('package')">
      Yes, that's me
    </button>

  </div>

</section>


<!-- PACKAGE -->

<section id="package" class="page">

  <div class="card center">

    <div class="cat-area">

      <img
        class="cat"
        src="https://media.tenor.com/2roX3uxz_68AAAAi/cat-cute.gif"
        alt="cat">

    </div>

    <p class="small">delivery confirmed.</p>

    <h2>Your birthday package has arrived.</h2>

    <p>
      I couldn't exactly send you a real gift through the screen,
      so I had to improvise.
    </p>

    <p>
      Hopefully this counts.
    </p>

    <button class="main-btn" onclick="showPage('home')">
      Open the package
    </button>

  </div>

</section>


<!-- HOME -->

<section id="home" class="page">

  <div class="card home">

    <div class="cat-area">

      <img
        class="cat"
        src="https://media.tenor.com/2roX3uxz_68AAAAi/cat-cute.gif"
        alt="cat">

    </div>

    <h2>
      Happy birthday, <span class="blue">Allie.</span>
    </h2>

    <p>
      Welcome to your little corner of the internet.
    </p>

    <p>
      I couldn't send you an actual gift,
      so I made this instead.
    </p>

    <p>
      It's not perfect, but I made it for you.
    </p>

    <div class="menu">

      <div class="menu-item" onclick="showPage('letter')">
        <strong>Letter</strong>
        <span>something I actually wanted to say</span>
      </div>

      <div class="menu-item" onclick="showPage('music')">
        <strong>Songs</strong>
        <span>a little soundtrack for today</span>
      </div>

      <div class="menu-item" onclick="showPage('thoughts')">
        <strong>Thoughts</strong>
        <span>some random things I wanted you to know</span>
      </div>

      <div class="menu-item" onclick="showPage('gift')">
        <strong>Final gift</strong>
        <span>save this one for last</span>
      </div>

    </div>

  </div>

</section>


<!-- LETTER -->

<section id="letter" class="page">

  <div class="card">

    <h2>A letter for you</h2>

    <div class="letter">

      <p>hellow Allie :D</p>

      <p>Happy birthday!!</p>

      <p>
        I honestly wasn't sure what to write because I'm
        terrible at making birthday messages sound normal.
      </p>

      <p>
        I just didn't want to send you the usual
        "happy birthday" and leave it at that,
        so I made this little website instead.
      </p>

      <p>
        It's kinda crazy that we literally met online
        and somehow ended up becoming friends.
        I never really expected we'd talk this much,
        but I'm genuinely glad we did.
      </p>

      <p>
        I really appreciate all the random conversations
        we've had, even the completely stupid ones.
        Somehow those end up being some of the funniest.
      </p>

      <p>
        I hope this year gives you more reasons to smile,
        more things to look forward to,
        and hopefully a lot less bullshit.
      </p>

      <p>
        I'm really glad I met you,
        and I'm really glad we became friends.
      </p>

      <p>
        I hope we stay friends for a really,
        really long time.
      </p>

      <p>
        Anyway, I'm going to stop before this turns
        into an entire essay.
      </p>

      <p>
        Happy birthday again, Allie.
      </p>

      <p class="signature">
        — shen
      </p>

    </div>

    <button class="back" onclick="showPage('home')">
      Back
    </button>

  </div>

</section>


<!-- MUSIC -->

<section id="music" class="page">

  <div class="card music">

    <p class="small">today's soundtrack</p>

    <h2>For the First Time</h2>

    <p>
      Mac DeMarco
    </p>

    <div class="record" id="record">
      ♪
    </div>

    <p>
      I don't know why, but this song always felt
      like it belonged here.
    </p>

    <button class="main-btn" onclick="playSong()">
      Play
    </button>

    <div class="lyrics" id="lyrics">

      <p>To all the days we were together</p>

      <p>To all the time we were apart</p>

      <p>Of each other's lives</p>

      <p>Heart to heart</p>

    </div>

    <button class="back" onclick="showPage('home')">
      Back
    </button>

  </div>

</section>


<!-- THOUGHTS -->

<section id="thoughts" class="page">

  <div class="card">

    <h2>Things I wanted you to know</h2>

    <div class="thoughts">

      <div class="thought">
        I'm really glad I met you.
      </div>

      <div class="thought">
        I hope you know you're appreciated.
      </div>

      <div class="thought">
        I hope we stay friends for a really long time.
      </div>

      <div class="thought">
        I hope this year is good to you.
      </div>

      <div class="thought">
        Keep being your silly self.
      </div>

      <div class="thought">
        I'm lucky to have you as a friend.
      </div>

    </div>

    <button class="back" onclick="showPage('home')">
      Back
    </button>

  </div>

</section>


<!-- GIFT -->

<section id="gift" class="page">

  <div class="card gift-page">

    <p class="small">one last thing</p>

    <h2>There's something here for you.</h2>

    <div
      class="gift"
      onclick="openGift()"
      id="giftBox">
      🎁
    </div>

    <p>
      Take your time.
    </p>

    <button class="main-btn" onclick="openGift()">
      Open it
    </button>

    <div class="final" id="final">

      <h2>Happy birthday, Allie.</h2>

      <p>
        I know this is just a little website,
        but I really wanted to make something for you.
      </p>

      <p>
        I'm genuinely happy that we met,
        even if it was through a screen.
      </p>

      <p>
        Thank you for all the random conversations,
        the laughs, and all the little moments we've shared.
      </p>

      <p>
        I hope you have a really good birthday
        and that this year gives you plenty of reasons
        to be happy.
      </p>

      <p>
        And whenever you're having a bad day,
        I hope you remember that someone out there
        is genuinely happy that you're here.
      </p>

      <p>
        So go enjoy your birthday.
        Eat something good.
        Have fun.
        Laugh a lot.
      </p>

      <p>
        I'm really glad I met you, Allie.
      </p>

      <button class="main-btn" onclick="showPage('last')">
        One more thing
      </button>

    </div>

  </div>

</section>


<!-- LAST -->

<section id="last" class="page">

  <div class="card last">

    <div class="last-heart">
      ♥
    </div>

    <h2>
      That's all.
    </h2>

    <p>
      I hope this little website made you smile,
      even just for a moment.
    </p>

    <p>
      Thank you for being part of my life
      and for all the memories we've made so far.
    </p>

    <p>
      Here's to more random conversations,
      stupid jokes, and good memories.
    </p>

    <p>
      Happy birthday, Allie.
    </p>

    <div class="labu">
      labu
    </div>

  </div>

</section>


<script>

function showPage(id) {

  document.querySelectorAll(".page").forEach(page => {
    page.classList.remove("active");
  });

  const page = document.getElementById(id);

  if (page) {
    page.classList.add("active");
    window.scrollTo({
      top: 0,
      behavior: "smooth"
    });
  }

}


/* MUSIC */

function playSong() {

  const record = document.getElementById("record");
  const lyrics = document.getElementById("lyrics");

  record.classList.add("playing");
  lyrics.classList.add("show");

  createConfetti(25);

}


/* GIFT */

function openGift() {

  const box = document.getElementById("giftBox");
  const final = document.getElementById("final");

  box.style.transform = "scale(1.4) rotate(8deg)";

  setTimeout(() => {
    box.style.display = "none";
    final.classList.add("show");
    createConfetti(80);
  }, 500);

}


/* CONFETTI */

function createConfetti(amount) {

  const colors = [
    "#c9233d",
    "#e44b61",
    "#3478c5",
    "#6ba5e6",
    "#ffb3c1",
    "#ffffff"
  ];

  for (let i = 0; i < amount; i++) {

    const piece = document.createElement("div");

    piece.className = "confetti";

    piece.style.left =
      Math.random() * 100 + "vw";

    piece.style.background =
      colors[Math.floor(Math.random() * colors.length)];

    piece.style.animationDuration =
      (2 + Math.random() * 2.5) + "s";

    piece.style.animationDelay =
      Math.random() * .8 + "s";

    piece.style.transform =
      "rotate(" + Math.random() * 360 + "deg)";

    document.body.appendChild(piece);

    setTimeout(() => {
      piece.remove();
    }, 5000);

  }

}


/* occasional tiny confetti when opening */

setTimeout(() => {
  createConfetti(12);
}, 1200);

</script>

</body>
</html>