
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday My Love!</title>
<style>
  /* Basic Reset */
  * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
  body {
    background: linear-gradient(to right, #ffafbd, #ffc3a0);
    overflow-x: hidden;
    scroll-behavior: smooth;
    color: #fff;
  }

  /* Section Styling */
  section {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 50px 20px;
    text-align: center;
    position: relative;
  }

  h1 {
    font-size: 3em;
    margin-bottom: 20px;
    color: #fff;
    text-shadow: 2px 2px 10px #ff4081;
    animation: glow 2s infinite alternate;
  }

  @keyframes glow {
    from { text-shadow: 2px 2px 10px #ff4081, 0 0 20px #ff4081; }
    to { text-shadow: 2px 2px 20px #ff4081, 0 0 40px #ff4081; }
  }

  p {
    font-size: 1.3em;
    max-width: 800px;
    margin: 10px 0;
    line-height: 1.8;
  }

  .heart {
    position: absolute;
    font-size: 2em;
    color: #ff69b4;
    animation: floatUp 5s linear infinite;
  }

  @keyframes floatUp {
    0% { transform: translateY(0) scale(1); opacity: 1; }
    100% { transform: translateY(-1000px) scale(0.5); opacity: 0; }
  }

  /* Buttons */
  .btn {
    padding: 15px 30px;
    margin: 20px;
    border: none;
    border-radius: 30px;
    background: #ff4081;
    color: #fff;
    font-size: 1.2em;
    cursor: pointer;
    transition: 0.3s;
  }

  .btn:hover {
    transform: scale(1.1);
    background: #ff79b0;
  }

  /* Heart background animation container */
  .hearts-container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    overflow: hidden;
    z-index: 0;
  }
</style>
</head>
<body>

<div class="hearts-container" id="heartsContainer"></div>

<section style="background: linear-gradient(to right, #ffafbd, #ffc3a0);">
  <h1>Happy Birthday My Love ❤️</h1>
  <p>Today is your special day, and I just want to tell you how much you mean to me. From the first moment I met you, my life became brighter and my heart fuller.</p>
  <p>Every smile of yours lights up my world, and every laugh makes my soul dance. I love you more than words can ever express.</p>
  <button class="btn" onclick="scrollToNext(this)">Next</button>
</section>

<section style="background: linear-gradient(to right, #fbc2eb, #a6c1ee);">
  <h1>To The One Who Holds My Heart 💖</h1>
  <p>With every beat of my heart, I think of you. Your presence in my life is like the sun breaking through the clouds, filling everything with warmth and love.</p>
  <p>I promise to stand by you, to make you laugh, to hold you when you cry, and to love you endlessly through every moment of life.</p>
  <button class="btn" onclick="scrollToNext(this)">Next</button>
</section>

<section style="background: linear-gradient(to right, #ffecd2, #fcb69f);">
  <h1>You Are My Everything 🌹</h1>
  <p>Every memory with you is a treasure. Every moment spent with you is a blessing. I can’t imagine my life without your love, your smile, and your soul.</p>
  <p>Thank you for being you. Thank you for loving me. And thank you for making my life magical just by being in it.</p>
  <button class="btn" onclick="scrollToNext(this)">Next</button>
</section>

<section style="background: linear-gradient(to right, #a1c4fd, #c2e9fb);">
  <h1>Forever and Always 💞</h1>
  <p>No matter where life takes us, my heart will always be yours. You are my partner, my best friend, and my greatest adventure.</p>
  <p>I love you more each day, and I can’t wait to make endless memories with you. Happy birthday, my love!</p>
  <button class="btn" onclick="scrollToTop()">Back to Top</button>
</section>

<script>
  // Scroll to next section
  function scrollToNext(button) {
    const currentSection = button.parentElement;
    const nextSection = currentSection.nextElementSibling;
    if (nextSection) nextSection.scrollIntoView({ behavior: 'smooth' });
  }

  // Scroll to top
  function scrollToTop() {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  // Hearts animation
  const heartsContainer = document.getElementById('heartsContainer');

  function createHeart() {
    const heart = document.createElement('div');
    heart.className = 'heart';
    heart.style.left = Math.random() * 100 + 'vw';
    heart.style.fontSize = (Math.random() * 30 + 20) + 'px';
    heart.innerText = '❤️';
    heartsContainer.appendChild(heart);

    setTimeout(() => {
      heartsContainer.removeChild(heart);
    }, 5000);
  }

  setInterval(createHeart, 300);
</script>

</body>
</html>
