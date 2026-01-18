# askisim-i-inn
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sana Özel 💖</title>

    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            background: linear-gradient(135deg, #ffb6c1, #ffe4ec);
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: "Segoe UI", sans-serif;
            overflow: hidden;
        }

        .container {
            background: white;
            width: 90%;
            max-width: 420px;
            padding: 25px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
            position: relative;
            z-index: 2;
        }

        .main-text {
            font-size: 17px;
            color: #444;
            line-height: 1.6;
        }

        .note {
            margin-top: 20px;
            background: #ffe6ef;
            padding: 15px;
            border-radius: 15px;
            font-size: 14px;
            color: #555;
        }

        /* Kalpler */
        .heart {
            position: absolute;
            bottom: -20px;
            font-size: 20px;
            color: #ff5c8a;
            animation: floatUp 6s linear infinite;
            opacity: 0.8;
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0) scale(1);
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) scale(1.5);
                opacity: 0;
            }
        }

        .music-note {
            margin-top: 15px;
            font-size: 12px;
            color: #888;
        }
    </style>
</head>
<body>

    <!-- MÜZİK -->
    <audio autoplay loop>
        <source src="tencereden-kapak.mp3" type="audio/mpeg">
    </audio>

    <div class="container">
        <div class="main-text">
            Her gece seni özleyerek uyuyorum ve her sabah seni daha çok severek uyanıyorum.  
            Gözlerini kapat ve huzurla uyu aşkım, seni her şeyinle çok seviyorum.
        </div>

        <div class="note">
            Bir yerden bulduğumu sanma bu siteyi, senin için yaptım.  
            Evinin direği hanımışım, benim pütüşüm.  
            Kocan Eren yaptı 💕
        </div>

        <div class="music-note">
            🎵 Kenan Doğulu – Tencereden Kapak
        </div>
    </div>

    <!-- KALP OLUŞTURMA -->
    <script>
        function createHeart() {
            const heart = document.createElement("div");
            heart.className = "heart";
            heart.innerHTML = "❤️";
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = (4 + Math.random() * 3) + "s";

            document.body.appendChild(heart);

            setTimeout(() => {
                heart.remove();
            }, 7000);
        }

        setInterval(createHeart, 500);
    </script>

</body>
</html>