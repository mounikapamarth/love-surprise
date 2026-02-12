<!DOCTYPE html>
<html>
<head>
<title>My Little Surprise ❤️</title>

<style>
    body {
        margin: 0;
        padding: 0;
        font-family: 'Segoe UI', sans-serif;
        background: linear-gradient(to right, #ff9a9e, #fad0c4);
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        text-align: center;
        color: white;
    }

    .card {
        background: rgba(255, 255, 255, 0.2);
        padding: 30px;
        border-radius: 20px;
        backdrop-filter: blur(10px);
        box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        width: 400px;
        position: relative;
    }

    button {
        padding: 10px 20px;
        border: none;
        border-radius: 30px;
        font-size: 16px;
        cursor: pointer;
        margin: 10px;
        transition: 0.3s;
    }

    .yes {
        background: #ff4b5c;
        color: white;
    }

    .no {
        background: white;
        color: #ff4b5c;
        position: absolute;
    }

    .hidden {
        display: none;
        margin-top: 20px;
        font-size: 18px;
        animation: fadeIn 1s ease-in-out;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(10px); }
        to { opacity: 1; transform: translateY(0); }
    }
</style>
</head>

<body>

<div class="card">
    <h2>Hi My Love ❤️</h2>

    <p>
        I have something very important to ask you… 😌💕
    </p>

    <h3>Will You Be Mine Forever? 💍❤️</h3>

    <button class="yes" onclick="sayYes()">Yes ❤️</button>
    <button class="no" id="noBtn">No 🙈</button>

    <div id="loveMessage" class="hidden">
        😍 Yaaayyyyy!!! 😍 <br><br>

        You just made me the happiest person alive ❤️ <br><br>

        I promise to annoy you forever,  
        love you endlessly,  
        and stay with you always 😌💕 <br><br>

        I Love You So Much ❤️
    </div>

    <!-- Song -->
    <audio id="song" loop>
        <source src="raatan-lambiyan.mp3" type="audio/mpeg">
    </audio>
</div>

<script>

// NO button runs away 😏
const noBtn = document.getElementById("noBtn");

noBtn.addEventListener("mouseover", moveButton);
noBtn.addEventListener("click", moveButton);

function moveButton() {
    const x = Math.random() * 300;
    const y = Math.random() * 200;

    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}

// YES button action ❤️
function sayYes() {
    document.getElementById("loveMessage").style.display = "block";
    document.getElementById("song").play();
}

</script>

</body>
</html>
