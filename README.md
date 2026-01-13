# My-Love-
My love 💓 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Raidha Sherin ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    height: 100vh;
    overflow: hidden;
    background: linear-gradient(135deg, #ff5f9e, #ffc371);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Poppins', sans-serif;
    color: white;
}

/* Floating hearts background */
.heart-bg span {
    position: absolute;
    bottom: -20px;
    font-size: 20px;
    animation: float 6s linear infinite;
    opacity: 0.7;
}

@keyframes float {
    from { transform: translateY(0); }
    to { transform: translateY(-120vh); }
}

.card {
    background: rgba(0,0,0,0.35);
    padding: 30px 20px;
    border-radius: 20px;
    width: 90%;
    max-width: 420px;
    text-align: center;
    box-shadow: 0 15px 40px rgba(0,0,0,0.4);
    z-index: 10;
}

h1 {
    font-family: 'Great Vibes', cursive;
    font-size: 42px;
}

p {
    font-size: 18px;
    line-height: 1.6;
}

.main-heart {
    font-size: 48px;
    margin: 15px 0;
    animation: beat 1s infinite;
}

@keyframes beat {
    50% { transform: scale(1.2); }
}

.buttons {
    margin-top: 30px;
    height: 120px;
    position: relative;
}

button {
    padding: 12px 25px;
    font-size: 18px;
    border-radius: 30px;
    border: none;
    cursor: pointer;
    position: absolute;
}

.yes {
    background: #ff2e63;
    color: white;
    left: 50%;
    transform: translateX(-50%);
}

.no {
    background: #555;
    color: white;
    top: 60px;
    left: 50%;
    transform: translateX(-50%);
    transition: 0.2s;
}

/* Confetti */
.confetti {
    position: absolute;
    width: 8px;
    height: 8px;
    background: white;
    animation: confetti 3s linear infinite;
}

@keyframes confetti {
    from { transform: translateY(-10vh); }
    to { transform: translateY(110vh); }
}
</style>
</head>

<body>

<div class="heart-bg"></div>

<div class="card" id="card">
    <h1>Raidha Sherin</h1>
    <div class="main-heart">❤️</div>

    <p>
        You make my world brighter,<br>
        my heart calmer,<br>
        and my life more beautiful.
    </p>

    <p>
        Will you be my forever?
    </p>

    <div class="buttons">
        <button class="yes" id="yesBtn">Yes 💖</button>
        <button class="no" id="noBtn">No 😢</button>
    </div>
</div>

<script>
/* Floating hearts */
const heartBg = document.querySelector(".heart-bg");
for (let i = 0; i < 20; i++) {
    const span = document.createElement("span");
    span.innerHTML = "❤️";
    span.style.left = Math.random() * 100 + "vw";
    span.style.animationDuration = 4 + Math.random() * 4 + "s";
    heartBg.appendChild(span);
}

/* No button logic */
const noBtn = document.getElementById("noBtn");
let warned = false;

function moveNo() {
    if (!warned) {
        alert("Are you sure? 🥺💔");
        warned = true;
    }
    const x = Math.random() * 200 - 100;
    const y = Math.random() * 80 - 40;
    noBtn.style.transform = `translate(-50%, 0) translate(${x}px, ${y}px)`;
}

noBtn.addEventListener("click", moveNo);
noBtn.addEventListener("touchstart", moveNo);

/* YES button */
document.getElementById("yesBtn").addEventListener("click", () => {
    celebrate();

    const phoneNumber = "919567373876"; // YOUR NUMBER
    const message = encodeURIComponent(
        "She said YES ❤️💍\nBest moment of my life!"
    );

    setTimeout(() => {
        window.location.href = `https://wa.me/${phoneNumber}?text=${message}`;
    }, 1500);
});

/* Celebration */
function celebrate() {
    document.getElementById("card").innerHTML = `
        <h1 style="font-family:'Great Vibes',cursive;font-size:50px;">
            She said YES ❤️
        </h1>
        <p style="font-size:20px;">Best moment of my life 💍</p>
    `;

    for (let i = 0; i < 80; i++) {
        const c = document.createElement("div");
        c.className = "confetti";
        c.style.left = Math.random() * 100 + "vw";
        c.style.animationDuration = 2 + Math.random() * 2 + "s";
        document.body.appendChild(c);
    }
}
</script>

</body>
</html>
