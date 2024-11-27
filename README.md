# lexilg.github.io
Ableton's Kids DAW
<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Ableton Kids</title>

    <style>

        body {

            margin: 0;

            font-family: 'Arial', sans-serif;

            background: linear-gradient(180deg, #8c71c2, #a9d5d4);

            color: #ffffff;

        }



        header {

            display: flex;

            justify-content: space-between;

            align-items: center;

            padding: 20px;

            background-color: #4a3978;

        }



        header .nav {

            display: flex;

            gap: 15px;

        }



        header .nav a {

            text-decoration: none;

            color: #fff;

            background: #8f77ca;

            padding: 8px 15px;

            border-radius: 20px;

            font-size: 14px;

        }



        header .nav a:hover {

            background: #b998ff;

        }



        .main {

            text-align: center;

            padding: 40px;

        }



        .main .screen {

            margin: 20px auto;

            background: #c1dfec;

            border-radius: 15px;

            padding: 20px;

            max-width: 600px;

            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);

        }



        .main .keyboard {

            display: flex;

            justify-content: center;

            margin: 20px auto;

            background: #f6a7c6;

            border-radius: 15px;

            padding: 20px;

            max-width: 400px;

        }



        .main .keyboard .key {

            width: 40px;

            height: 120px;

            margin: 0 5px;

            background: #fff;

            border: 1px solid #000;

            border-radius: 5px;

            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);

            cursor: pointer;

        }



        .main .keyboard .key:active {

            background: #ddd;

        }

    </style>

</head>

<body>

    <header>

        <div class="logo">Ableton Kids</div>

        <nav class="nav">

            <a href="#">Shop</a>

            <a href="#">Education</a>

            <a href="#">Resources</a>

            <a href="#">Sponsors</a>

            <a href="#">FAQ</a>

        </nav>

    </header>



    <main class="main">

        <div class="screen">

            <h1>Now Introducing Ableton Kids!</h1>

            <p>A mini-user-friendly way to explore music production and creativity.</p>

        </div>



        <div class="keyboard" id="keyboard">

            <div class="key" data-note="C"></div>

            <div class="key" data-note="D"></div>

            <div class="key" data-note="E"></div>

            <div class="key" data-note="F"></div>

            <div class="key" data-note="G"></div>

            <div class="key" data-note="A"></div>

            <div class="key" data-note="B"></div>

        </div>

    </main>



    <script>

        const keyboard = document.getElementById('keyboard');



        keyboard.addEventListener('click', (event) => {

            if (event.target.classList.contains('key')) {

                const note = event.target.getAttribute('data-note');

                playSound(note);

            }

        });



        function playSound(note) {

            const audio = new Audio(`https://example.com/sounds/${note}.mp3`); // Replace with actual sound file URLs

            audio.play();

        }

    </script>

</body>

</html>
