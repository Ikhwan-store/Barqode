<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Auto Play Lagu Full Volume</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #000;
            font-family: Arial, sans-serif;
        }
        .box {
            padding: 25px 50px;
            background-color: #ff0000;
            color: white;
            border-radius: 10px;
            cursor: pointer;
            font-size: 24px;
            font-weight: bold;
            text-align: center;
            box-shadow: 0 0 15px rgba(255, 0, 0, 0.7);
            transition: all 0.3s;
        }
        .box:hover {
            background-color: #ff3333;
            transform: scale(1.05);
        }
    </style>
</head>
<body>
    <div class="box" onclick="playLoudAsFuck()">
        BUKA
    </div>

    <audio id="song" src="https://files.catbox.moe/8wanjw.mp3"></audio>

    <script>
        function playLoudAsFuck() {
            const audio = document.getElementById('song');
            audio.volume = 1.0; // Volume 100% (full blast)
            audio.play()
                .then(() => {
                    console.log("Lagu diputar keras-keras, anjing!");
                })
                .catch(error => {
                    console.error("Gagal muter:", error);
                    alert("Browser nge-block autoplay! Buka di Chrome & izinkan autoplay.");
                });
        }
    </script>
</body>
</html>
