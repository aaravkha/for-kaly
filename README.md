<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday, Kaly 🤍</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap');

  body {
    font-family: 'Poppins', sans-serif;
    background: #fefefe;
    color: #3b2f2f;
    text-align: center;
    margin: 0;
    padding: 0;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  .section {
    max-width: 700px;
    padding: 40px 20px;
    border-radius: 20px;
    background: #ffffff;
    box-shadow: 0 8px 20px rgba(0,0,0,0.08);
    display: none;
    animation: fadeIn 1s ease-in-out;
  }

  .active { display: block; }

  h1 {
    font-size: 2em;
    color: #ffffff; /* White text for header */
    background-color: #dcdcdc; /* subtle gray background so white text visible */
    padding: 15px;
    border-radius: 12px;
    margin-bottom: 20px;
  }

  p {
    font-size: 1.1em;
    line-height: 1.7em;
    color: #4a3c3c;
  }

  button {
    background-color: #ffffff;
    border: 2px solid #dcdcdc;
    padding: 12px 25px;
    border-radius: 15px;
    font-size: 1.1em;
    cursor: pointer;
    color: #3b2f2f;
    font-weight: 600;
    margin-top: 20px;
    transition: 0.3s;
  }

  button:hover {
    background-color: #f0f0f0;
    transform: scale(1.05);
  }

  #reason {
    margin-top: 40px;
    font-size: 1.2em;
    min-height: 120px;
    line-height: 1.8em;
  }

  .fade { opacity: 0; transition: 0.3s; }

  @keyframes fadeIn {
    from {opacity:0;}
    to {opacity:1;}
  }
</style>
</head>
<body>

<!-- Opening Section -->
<div id="opening" class="section active">
  <h1>Happy Birthday, Kaly 🤍</h1>
  <p>
    I don’t say this often maybe because words have never been my strongest language.<br>
    But if I could put it into something tangible, it would be this.<br>
    Click below to see 23 reasons why I love you, one by one.
  </p>
  <button onclick="showReasons()">💌 Show me 💌</button>
</div>

<!-- 23 Reasons Section -->
<div id="reasons-section" class="section">
  <h1>23 Reasons Why I Love You</h1>
  <div id="reason">because you always smell like something warm and familiar.</div>
  <button onclick="nextReason()">💘 Next Reason 💘</button>
  <p style="margin-top: 50px; font-style: italic;">— khalil</p>
</div>

<script>
  const reasons = [
    "because you always smell like something warm and familiar.",
    "because you’re so damn curious about everything — even about why the moon looks bigger in december.",
    "because you see the best in people, even when they don’t. even when it hurts you.",
    "because you don’t give up on people too fast. it’s something i both admire and worry about.",
    "because you treat love like something sacred. not something to win, or to own.",
    "because you don’t need big gestures to show you care. your consistency says it all.",
    "because you make the most mundane days feel worth remembering.",
    "because you bring life into routines. suddenly my habits don’t feel repetitive anymore.",
    "because when i’m quiet, you never force me to talk. you just sit close.",
    "because you somehow understand my silence better than my words.",
    "because you never made me feel guilty for being quiet.",
    "because you never try to fix me, you just stay. and somehow that’s what heals me.",
    "because you’ve seen me at my lowest and didn’t flinch.",
    "because you never made me feel like i had to be perfect.",
    "because you say “aku sayang kamu” in that tone that sounds like a promise.",
    "because you trust me — and that’s something i’ll always protect.",
    "because you believe in me more than i do sometimes.",
    "because you make me want to be better not because you asked me to, but because being loved by you feels like something i want to deserve.",
    "because you look at the world with this kind of wonder that i lost a long time ago.",
    "because even in silence, even in distance, it’s still you i find myself coming home to.",
    "because you never stopped choosing me. even when it wasn’t easy.",
    "because you’re you. and that’s enough reason for everything else.",
    "because with you, everything finally makes sense."
  ];

  let currentReason = 0;

  function showReasons() {
    document.getElementById('opening').classList.remove('active');
    document.getElementById('reasons-section').classList.add('active');
    document.getElementById('reason').innerText = reasons[currentReason];
  }

  function nextReason() {
    currentReason++;
    if(currentReason >= reasons.length) currentReason = 0;
    const reasonDiv = document.getElementById('reason');
    reasonDiv.classList.add('fade');
    setTimeout(() => {
      reasonDiv.innerText = reasons[currentReason];
      reasonDiv.classList.remove('fade');
    }, 300);
  }
</script>
</body>
</html>
