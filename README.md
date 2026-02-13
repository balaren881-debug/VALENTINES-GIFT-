<!DOCTYPE html>
<html>
<head>
    <title>For My Puttu ❤️</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #ff758c, #ff7eb3);
            overflow-x: hidden;
            color: white;
        }

        h1 {
            margin-top: 60px;
            font-size: 35px;
        }

        .question {
            font-size: 24px;
            margin-top: 30px;
        }

        button {
            padding: 12px 25px;
            font-size: 18px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            margin: 15px;
        }

        #yesBtn { background-color: #28a745; color: white; }
        #noBtn { background-color: #dc3545; color: white; position: absolute; }

        .hidden { display: none; }

        .gift-box {
            background: white;
            color: black;
            padding: 15px;
            margin: 15px auto;
            width: 250px;
            border-radius: 15px;
            cursor: pointer;
            transition: 0.3s;
        }

        .gift-box:hover {
            transform: scale(1.1);
            background: #ffe6f0;
        }

    </style>
</head>

<body>

<!-- Background Music -->
<iframe width="0" height="0"
src="https://www.youtube.com/embed/H2f7MZaw3Yo?autoplay=1&loop=1&playlist=H2f7MZaw3Yo"
frameborder="0" allow="autoplay">
</iframe>

<h1>💖 Puttu 💖</h1>

<div id="step1">
    <div class="question">
        Puttu me apko bhot pyaar krta hun 🥺❤️<br><br>
        Kya aap bhi mujhse pyaar krti ho?
    </div>
    <button id="yesBtn" onclick="nextStep()">YES 😘</button>
    <button id="noBtn">NO 😏</button>
</div>

<div id="step2" class="hidden">
    <div class="question">
        Agar me chocolate hota 🍫<br>
        to kya aap mujhe pura kha leti? 😜
    </div>
    <button onclick="nextStep2()">Obviously YES 😌</button>
</div>

<div id="step3" class="hidden">
    <div class="question">
        Agar me aapko roz tang karu 😈<br>
        to kya aap mujhe fir bhi bardasht karogi? 🥺
    </div>
    <button onclick="showGifts()">Haan jaan 💖</button>
</div>

<!-- GIFT SECTION -->
<div id="gifts" class="hidden">
    <h1>🎁 Choose Your Valentine Gift 🎁</h1>

    <div class="gift-box" onclick="gift1()">
        🎟 Romantic Date Voucher
    </div>

    <div class="gift-box" onclick="gift2()">
        🍫 Lifetime Chocolate Supply
    </div>

    <div class="gift-box" onclick="gift3()">
        💌 100 Love Letters
    </div>

    <div class="gift-box" onclick="gift4()">
        💍 Future Plan Locked
    </div>
</div>

<div id="final" class="hidden">
    <h1 id="finalMessageText"></h1>
</div>

<script>

const noBtn = document.getElementById("noBtn");

noBtn.addEventListener("mouseover", function() {
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
});

function nextStep() {
    document.getElementById("step1").classList.add("hidden");
    document.getElementById("step2").classList.remove("hidden");
}

function nextStep2() {
    document.getElementById("step2").classList.add("hidden");
    document.getElementById("step3").classList.remove("hidden");
}

function showGifts() {
    document.getElementById("step3").classList.add("hidden");
    document.getElementById("gifts").classList.remove("hidden");
}

function gift1() {
    showFinal("Yayyy 😍 Romantic Date Confirmed 💖<br>Location: Wherever My Puttu Wants 😌");
}

function gift2() {
    showFinal("Chocolate hi chocolate 🍫<br>But sabse sweet to tum ho 🥺❤️");
}

function gift3() {
    showFinal("100 nahi… lifetime letters likhunga 💌<br>Har din ek naya pyaar 😘");
}

function gift4() {
    showFinal("Future Plan Locked 💍<br>Meri Puttu meri forever Valentine ❤️");
}

function showFinal(message) {
    document.getElementById("gifts").classList.add("hidden");
    document.getElementById("final").classList.remove("hidden");
    document.getElementById("finalMessageText").innerHTML = message;
}

</script>

</body>
</html>
