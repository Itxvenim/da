<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Our Love Journey</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;600&family=Pacifico&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #ffe6f7, #ffb3d9, #ff99cc, #ff80bf);
            color: #333;
            overflow-x: hidden;
            line-height: 1.6;
        }
        .page {
            display: none;
            min-height: 100vh;
            padding: 20px;
            box-sizing: border-box;
            text-align: center;
        }
        .page.active {
            display: block;
        }
        .cute-box {
            width: 90%;
            max-width: 500px;
            margin: 0 auto;
            border: 3px solid #800000;
            border-radius: 20px;
            background: linear-gradient(135deg, #fdf5e6, #f5deb3, #d2b48c);
            padding: 20px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
            position: relative;
        }
        .cute-box::before {
            content: '💖';
            position: absolute;
            top: -10px;
            left: -10px;
            font-size: 1.5em;
        }
        .cute-box::after {
            content: '🌟';
            position: absolute;
            top: -10px;
            right: -10px;
            font-size: 1.5em;
        }
        .bold-text {
            font-family: 'Pacifico', cursive;
            font-size: 2.5em;
            font-weight: 400;
            margin-bottom: 20px;
            color: #8b0000;
        }
        .cute-line {
            font-size: 1.3em;
            margin: 15px 0;
            font-weight: 300;
        }
        .next-btn {
            background: linear-gradient(45deg, #ff6b6b, #ff4757);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.2em;
            font-weight: 600;
            border-radius: 30px;
            cursor: pointer;
            margin-top: 20px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            transition: transform 0.2s;
        }
        .next-btn:hover {
            transform: translateY(-2px);
        }
        .emoji {
            font-size: 2em;
            margin: 0 5px;
        }
        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.3);
            z-index: 10;
            font-family: 'Dancing Script', cursive;
            font-size: 2em;
            color: #8b0000;
        }
        .game-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
            max-width: 350px;
            margin: 0 auto;
            background: linear-gradient(135deg, #e6f7ff, #b3d9ff, #99ccff);
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
        }
        .card {
            width: 70px;
            height: 70px;
            background: linear-gradient(45deg, #fff, #ffe6f7);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-size: 2.5em;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .counter, .moves {
            font-size: 1.5em;
            margin-bottom: 20px;
            font-weight: 400;
        }
        .letter-box {
            width: 85%;
            max-width: 450px;
            height: 350px;
            margin: 0 auto;
            border: 3px solid #800000;
            border-radius: 20px;
            background: linear-gradient(135deg, #fdf5e6, #f5deb3, #d2b48c);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            position: relative;
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
        }
        .letter-display {
            font-family: 'Dancing Script', cursive;
            font-size: 1.2em;
            font-weight: 400;
            text-align: center;
            max-height: 250px;
            overflow-y: scroll;
            padding: 20px;
            line-height: 1.6;
            scrollbar-width: thin;
            scrollbar-color: #800000 #ffe6f7;
        }
        .letter-display::-webkit-scrollbar {
            width: 8px;
        }
        .letter-display::-webkit-scrollbar-track {
            background: #ffe6f7;
        }
        .letter-display::-webkit-scrollbar-thumb {
            background: #800000;
            border-radius: 4px;
        }
        .decor-emoji {
            position: absolute;
            font-size: 1.8em;
        }
        .decor-emoji.top-left { top: 10px; left: 10px; }
        .decor-emoji.top-right { top: 10px; right: 10px; }
        .decor-emoji.bottom-left { bottom: 10px; left: 10px; }
        .decor-emoji.bottom-right { bottom: 10px; right: 10px; }
        .poetry-box {
            width: 85%;
            max-width: 450px;
            height: 250px;
            margin: 0 auto;
            border: 3px solid #800000;
            border-radius: 20px;
            background: linear-gradient(135deg, #fdf5e6, #f5deb3, #d2b48c);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-size: 1.3em;
            font-weight: 600;
            text-align: center;
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
        }
        .poetry-display {
            font-family: 'Dancing Script', cursive;
            font-size: 1.5em;
            font-weight: 400;
            text-align: center;
            line-height: 1.8;
            color: #8b0000;
        }
        .final-message {
            display: none;
            font-family: 'Dancing Script', cursive;
            font-size: 1.8em;
            font-weight: 700;
            margin-top: 20px;
            color: #8b0000;
        }
        footer {
            text-align: center;
            padding: 10px;
            font-size: 0.9em;
            color: #666;
            margin-top: 20px;
        }
        @media (max-width: 600px) {
            .game-container {
                grid-template-columns: repeat(3, 1fr);
            }
            .card {
                width: 55px;
                height: 55px;
            }
            .bold-text {
                font-size: 2em;
            }
            .letter-box, .poetry-box {
                width: 90%;
                height: auto;
                min-height: 300px;
            }
            .letter-display {
                max-height: 200px;
            }
        }
    </style>
</head>
<body>
    <div class="popup" id="well-done-popup">
        Well Done! 🎉💕
    </div>

    <div id="page1" class="page active">
        <div class="cute-box">
            <div class="bold-text">Our Love Journey <span class="emoji">💖</span><span class="emoji">🌟</span></div>
            <div class="cute-line">A story of hearts and smiles <span class="emoji">😊</span><span class="emoji">❤️</span></div>
            <div class="cute-line">From friends to forever <span class="emoji">💑</span><span class="emoji">✨</span></div>
            <div class="cute-line">Let's relive the magic <span class="emoji">🥰</span><span class="emoji">🌈</span></div>
        </div>
        <button class="next-btn" onclick="nextPage(2)">Next Page <span class="emoji">➡️</span></button>
    </div>

    <div id="page2" class="page">
        <div class="bold-text">Match the Emojis Game <span class="emoji">🎮</span><span class="emoji">💕</span></div>
        <div class="counter">Remaining Pairs: <span id="remaining">6</span></div>
        <div class="moves">Moves: <span id="moves">0</span></div>
        <div class="game-container" id="game-board"></div>
        <button class="next-btn" id="game-next-btn" style="display: none;" onclick="nextPage(3)">Next Page <span class="emoji">➡️</span></button>
    </div>

    <div id="page3" class="page">
        <div class="bold-text">A Letter from My Heart <span class="emoji">💌</span><span class="emoji">🥺</span></div>
        <div class="letter-box" onclick="revealLetter()">
            <div class="decor-emoji top-left">🌸</div>
            <div class="decor-emoji top-right">💖</div>
            <div class="decor-emoji bottom-left">😘</div>
            <div class="decor-emoji bottom-right">🌹</div>
            <div class="letter-display" id="letter-text"></div>
        </div>
        <button class="next-btn" onclick="nextPage(4)">Next Page <span class="emoji">➡️</span></button>
    </div>

    <div id="page4" class="page">
        <div class="bold-text">Final Surprise <span class="emoji">🎁</span><span class="emoji">💕</span></div>
        <div class="poetry-box" onclick="revealPoetry()">
            Tap to Reveal Poetry <span class="emoji">✨</span>
        </div>
        <div class="final-message" id="final-msg">
            Love you so much Begam <span class="emoji">💖</span><span class="emoji">🥰</span><span class="emoji">😍</span><span class="emoji">🌟</span>
        </div>
        <button class="next-btn" onclick="restart()">Start Over <span class="emoji">🔄</span></button>
    </div>

    <footer>
        Made with love 💕
    </footer>

    <script>
        let currentPage = 1;

        function nextPage(page) {
            document.getElementById(`page${currentPage}`).classList.remove('active');
            currentPage = page;
            document.getElementById(`page${currentPage}`).classList.add('active');
        }

        function restart() {
            currentPage = 1;
            document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
            document.getElementById('page1').classList.add('active');
            resetGame();
            resetLetter();
            resetPoetry();
        }

        const emojis = ['😊', '❤️', '🌟', '💑', '🥰', '🌈', '😘', '🌹', '🌸', '💖', '🎮', '✨'];
        let cards = [];
        let flippedCards = [];
        let matchedPairs = 0;
        let moves = 0;

        function initGame() {
            const board = document.getElementById('game-board');
            board.innerHTML = '';
            cards = [...emojis, ...emojis].sort(() => Math.random() - 0.5);
            cards.forEach((emoji, index) => {
                const card = document.createElement('div');
                card.classList.add('card');
                card.dataset.emoji = emoji;
                card.dataset.index = index;
                card.addEventListener('click', flipCard);
                board.appendChild(card);
            });
            matchedPairs = 0;
            moves = 0;
            updateUI();
        }

        function flipCard() {
            if (flippedCards.length < 2 && !this.classList.contains('flipped') && !this.classList.contains('matched')) {
                this.classList.add('flipped');
                this.textContent = this.dataset.emoji;
                flippedCards.push(this);
                if (flippedCards.length === 2) {
                    moves++;
                    setTimeout(checkMatch, 1000);
                }
                updateUI();
            }
        }

        function checkMatch() {
            const [card1, card2] = flippedCards;
            if (card1.dataset.emoji === card2.dataset.emoji) {
                card1.classList.add('matched');
                card2.classList.add('matched');
                matchedPairs++;
                if (matchedPairs === 6) {
                    document.getElementById('game-board').style.display = 'none';
                    document.querySelector('.counter').style.display = 'none';
                    document.querySelector('.moves').style.display = 'none';
                    document.getElementById('well-done-popup').style.display = 'block';
                    setTimeout(() => {
                        document.getElementById('well-done-popup').style.display = 'none';
                        document.getElementById('game-next-btn').style.display = 'block';
                    }, 2000);
                }
            } else {
                card1.classList.remove('flipped');
                card2.classList.remove('flipped');
                card1.textContent = '';
                card2.textContent = '';
            }
            flippedCards = [];
            updateUI();
        }

        function updateUI() {
            document.getElementById('remaining').textContent = 6 - matchedPairs;
            document.getElementById('moves').textContent = moves;
        }

        function resetGame() {
            initGame();
            document.getElementById('game-board').style.display = 'grid';
            document.querySelector('.counter').style.display = 'block';
            document.querySelector('.moves').style.display = 'block';
            document.getElementById('game-next-btn').style.display = 'none';
            document.getElementById('well-done-popup').style.display = 'none';
        }

        const letterText = `Do you remember how we started, just as friends, talking about random things and sharing little moments without even realizing how special it would all become? Almost a year passed like that, and somewhere along the way, I quietly fell for you. You are so sweet and caring, and the way you always look after me means more to me than I can ever explain. I really hope you always stay this happy and smiling.
When we finally met face to face, that moment instantly became my favorite memory. Looking into your eyes felt different — your eyes, your smile, and every little thing about you felt warm and familiar, like something my heart already knew. On 25th August 2025, I finally shared what I had been holding inside for so long, and when you accepted my proposal, life suddenly felt lighter and brighter.
Since that day, everything feels more beautiful — the world looks colorful, small things make sense, and somehow, you show up in every thought and every smile. You, your kindness, your eyes,`;

        function revealLetter() {
            document.getElementById('letter-text').textContent = letterText;
        }

        function resetLetter() {
            document.getElementById('letter-text').textContent = '';
        }

        function revealPoetry() {
            const box = document.querySelector('.poetry-box');
            box.innerHTML = `<div class="poetry-display">*_اچھـا لگتـــا ہــے تیـــرا نـام میـرے نـام کـے ســـاتــھ _* 🥹❤️‍🔥<br>*_جیسـے کوئـی صبـح جـڑی ہـو کسـی شـام کـے سـاتـھ_*😌🫂</div>`;
            setTimeout(() => {
                box.style.display = 'none';
                document.getElementById('final-msg').style.display = 'block';
            }, 3000);
        }

        function resetPoetry() {
            document.querySelector('.poetry-box').innerHTML = 'Tap to Reveal Poetry <span class="emoji">✨</span>';
            document.querySelector('.poetry-box').style.display = 'flex';
            document.getElementById('final-msg').style.display = 'none';
        }

        initGame();
    </script>
</body>
</html>
