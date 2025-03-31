# Eshika
Happy birth day

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Special Surprise For You ✨</title>
    <style>
        /* Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #f8e1f4, #e0c3f7, #c2e6ff);
            background-size: 400% 400%;
            animation: gradientBackground 15s ease infinite;
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 10;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeIn 3s forwards 0.5s;
        }

        /* Header Styles */
        header {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }

        h1 {
            font-size: 2.5rem;
            color: #6a4c93;
            margin-bottom: 15px;
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
        }

        /* Letter Section */
        .letter-container {
            background: rgba(255, 255, 255, 0.7);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 0 20px rgba(106, 76, 147, 0.3);
            margin-bottom: 40px;
            position: relative;
            overflow: hidden;
        }

        .letter-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            border-radius: 20px;
            box-shadow: inset 0 0 15px rgba(255, 215, 232, 0.7);
            pointer-events: none;
            z-index: 1;
        }

        .letter {
            font-size: 1.2rem;
            line-height: 1.6;
            color: #333;
            position: relative;
            z-index: 2;
            min-height: 200px;
        }

        .video-container {
            display: none;
            position: relative;
            width: 100%;
            padding-top: 56.25%; /* 16:9 Aspect Ratio */
            margin-bottom: 40px;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 0 20px rgba(106, 76, 147, 0.3), 0 0 30px rgba(255, 215, 232, 0.5);
        }

        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }

        /* Surprise Button */
        .surprise-button-container {
            text-align: center;
            margin: 30px 0;
            position: relative;
        }

        .surprise-button {
            background: linear-gradient(45deg, #ff9a9e, #fad0c4, #fad0c4, #a18cd1);
            background-size: 300% 300%;
            animation: gradientButton 5s ease infinite;
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
            padding: 15px 40px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 5px 20px rgba(161, 140, 209, 0.5);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            z-index: 2;
        }

        .surprise-button::before {
            content: '';
            position: absolute;
            top: -5px;
            left: -5px;
            right: -5px;
            bottom: -5px;
            border-radius: 55px;
            background: linear-gradient(45deg, #ffccf9, #b28cff, #b28cff, #9cecff);
            background-size: 300% 300%;
            animation: gradientButton 5s ease infinite;
            z-index: -1;
            opacity: 0.6;
            filter: blur(8px);
        }

        .surprise-button:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 25px rgba(161, 140, 209, 0.7);
        }

        .surprise-button:active {
            transform: translateY(1px);
        }

        /* Surprise Modal */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }

        .modal {
            background: white;
            width: 90%;
            max-width: 600px;
            border-radius: 20px;
            padding: 30px;
            position: relative;
            transform: scale(0.8);
            transition: all 0.3s ease;
            box-shadow: 0 0 30px rgba(255, 215, 232, 0.8);
            text-align: center;
        }

        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal-overlay.active .modal {
            transform: scale(1);
        }

        .modal-header {
            margin-bottom: 20px;
        }

        .modal-body {
            margin-bottom: 30px;
        }

        .modal-close {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 24px;
            color: #6a4c93;
            background: none;
            border: none;
            cursor: pointer;
        }

        /* Playlist Styling */
        .playlist {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            padding: 20px;
            max-height: 300px;
            overflow-y: auto;
        }

        .playlist-item {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
            padding: 10px;
            border-radius: 10px;
            background: rgba(240, 240, 255, 0.7);
            transition: all 0.2s ease;
        }

        .playlist-item:hover {
            background: rgba(225, 225, 255, 0.9);
            transform: translateX(5px);
        }

        .playlist-item img {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            margin-right: 15px;
            object-fit: cover;
        }

        .playlist-item-info {
            flex-grow: 1;
            text-align: left;
        }

        .playlist-item-title {
            font-weight: bold;
            color: #6a4c93;
        }

        .playlist-item-artist {
            font-size: 0.9rem;
            color: #888;
        }

        .playlist-item-play {
            background: none;
            border: none;
            color: #6a4c93;
            cursor: pointer;
            font-size: 1.2rem;
        }

        /* Back Button */
        .back-button {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 20px;
            background: rgba(255, 255, 255, 0.7);
            border: 2px solid #6a4c93;
            color: #6a4c93;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .back-button:hover {
            background: #6a4c93;
            color: white;
        }

        /* Floating Elements */
        .floating-element {
            position: absolute;
            pointer-events: none;
            opacity: 0.7;
            z-index: 1;
            animation-name: float;
            animation-timing-function: ease-in-out;
            animation-iteration-count: infinite;
            animation-direction: alternate;
        }

        /* Music Controls */
        .music-controls {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 100;
            background: rgba(255, 255, 255, 0.7);
            border-radius: 50%;
            width: 50px;
            height: 50px;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 0 10px rgba(106, 76, 147, 0.3);
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .music-controls:hover {
            transform: scale(1.1);
        }

        .music-controls i {
            color: #6a4c93;
            font-size: 24px;
        }

        /* Animations */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes gradientBackground {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }

        @keyframes gradientButton {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }

        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
            }
            100% {
                transform: translateY(-20px) rotate(5deg);
            }
        }

        /* Cursor Effect */
        .cursor-effect {
            position: absolute;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            background: rgba(255, 182, 193, 0.7);
            pointer-events: none;
            z-index: 1000;
            transform: translate(-50%, -50%);
            transition: opacity 0.5s ease;
            opacity: 0;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }

            .container {
                padding: 15px;
            }

            .letter-container {
                padding: 20px;
            }

            .letter {
                font-size: 1rem;
            }

            .surprise-button {
                font-size: 1.2rem;
                padding: 12px 30px;
            }

            .floating-element {
                max-width: 40px;
                max-height: 40px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <div class="container">
        <header>
            <h1>For My Dearest Friend ❤️</h1>
        </header>

        <div class="letter-container">
            <div class="letter" id="typed-text"></div>
        </div>

        <div class="video-container" id="video-message">
            <!-- Replace with your video embed code -->
            <iframe src="about:blank" frameborder="0" allowfullscreen></iframe>
        </div>

        <div class="surprise-button-container">
            <button class="surprise-button" id="surprise-button">
                Click for a Surprise! 🎁
            </button>
        </div>

        <div class="navigation">
            <a href="javascript:history.back()" class="back-button">
                <i class="fas fa-arrow-left"></i> Back to Birthday Cake
            </a>
        </div>
    </div>

    <!-- Modal for Surprise -->
    <div class="modal-overlay" id="modal-overlay">
        <div class="modal">
            <button class="modal-close" id="modal-close">×</button>
            <div class="modal-header">
                <h2>🎉 Your Special Surprise! 🎉</h2>
            </div>
            <div class="modal-body">
                <div class="playlist">
                    <h3 style="margin-bottom: 15px;">Songs That Remind Me of Us 💕</h3>
                    <div class="playlist-item">
                        <img src="./pic3.jpg" alt="Song cover">
                        <div class="playlist-item-info">
                            <div class="playlist-item-title">Our Favorite Memory</div>
                            <div class="playlist-item-artist">That Artist You Love</div>
                        </div>
                        <button class="playlist-item-play"><i class="fas fa-play"></i></button>
                    </div>
                    <div class="playlist-item">
                        <img src="./pic1.jpg" alt="Song cover">
                        <div class="playlist-item-info">
                            <div class="playlist-item-title">That Summer Night</div>
                            <div class="playlist-item-artist">The Adventure Band</div>
                        </div>
                        <button class="playlist-item-play"><i class="fas fa-play"></i></button>
                    </div>
                    <div class="playlist-item">
                        <img src="./pic6.jpg" alt="Song cover">
                        <div class="playlist-item-info">
                            <div class="playlist-item-title">Inside Joke Anthem</div>
                            <div class="playlist-item-artist">Laugh Out Loud</div>
                        </div>
                        <button class="playlist-item-play"><i class="fas fa-play"></i></button>
                    </div>
                    <div class="playlist-item">
                        <img src="./pic2.jpg" alt="Song cover">
                        <div class="playlist-item-info">
                            <div class="playlist-item-title">Remember When</div>
                            <div class="playlist-item-artist">The Friendship Vibes</div>
                        </div>
                        <button class="playlist-item-play"><i class="fas fa-play"></i></button>
                    </div>
                    <div class="playlist-item">
                        <img src="./pic5.jpg" alt="Song cover">
                        <div class="playlist-item-info">
                            <div class="playlist-item-title">Birthday Wishes</div>
                            <div class="playlist-item-artist">Happy Songs</div>
                        </div>
                        <button class="playlist-item-play"><i class="fas fa-play"></i></button>
                    </div>
                </div>
                <div style="margin-top: 20px;">
                    <a href="#" download class="back-button" style="background: #ffb6c1; border-color: #ffb6c1; color: white;">
                        <i class="fas fa-download"></i> Download Your Digital Gift
                    </a>
                </div>
            </div>
        </div>
    </div>

    <!-- Music Controls -->
    <div class="music-controls" id="music-toggle">
        <i class="fas fa-volume-mute" id="music-icon"></i>
    </div>

    <!-- Audio Elements -->
    <audio id="click-sound" preload="auto">
        <source src="https://cdn.pixabay.com/download/audio/2021/08/04/audio_bb630cc098.mp3?filename=cute-notification-ringtone-1-173850.mp3" type="audio/mpeg">
    </audio>
    <audio id="background-music" loop>
        <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_c8c8a73467.mp3?filename=relaxing-145038.mp3" type="audio/mpeg">
    </audio>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/typed.js/2.0.12/typed.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/canvas-confetti/1.5.1/confetti.browser.min.js"></script>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Fade in animation
            setTimeout(() => {
                document.querySelector('.container').style.opacity = 1;
            }, 500);

            // Typewriter effect for letter
            const letterContent = "My dearest friend,\n\nAs I sit here thinking about all our memories together, I can't help but smile. From our late-night talks to our spontaneous adventures, you've filled my life with so much joy and laughter. You've been my shoulder to cry on, my partner in crime, and my biggest supporter.\n\nOn your special day, I want you to know how grateful I am to have you in my life. You make every day brighter just by being you - kind, funny, and incredibly thoughtful.\n\nHappy Birthday to my favorite person in the world! Here's to many more years of friendship, laughter, and creating memories together.\n\nWith all my love,\n[Your Name]";
            
            new Typed('#typed-text', {
                strings: [letterContent],
                typeSpeed: 30,
                showCursor: true,
                cursorChar: '|',
                onComplete: function() {
                    setTimeout(() => {
                        document.querySelector('.surprise-button').classList.add('animate__animated', 'animate__pulse', 'animate__infinite');
                    }, 1000);
                }
            });

            // Create floating elements
            const floatingElements = [
                { type: 'heart', color: '#ff6b8a', size: '20px' },
                { type: 'heart', color: '#f48fb1', size: '30px' },
                { type: 'star', color: '#ffd54f', size: '25px' },
                { type: 'star', color: '#ffecb3', size: '15px' },
                { type: 'teddy', emoji: '🧸', size: '30px' },
                { type: 'sparkle', emoji: '✨', size: '25px' },
                { type: 'sparkle', emoji: '✨', size: '20px' },
                { type: 'heart', color: '#ff6b8a', size: '25px' },
                { type: 'star', color: '#ffd54f', size: '20px' },
                { type: 'teddy', emoji: '🧸', size: '25px' }
            ];

            floatingElements.forEach((element, index) => {
                createFloatingElement(element, index);
            });

            // Cursor effect
            document.addEventListener('mousemove', createCursorEffect);

            // Surprise button functionality
            const surpriseButton = document.getElementById('surprise-button');
            const modalOverlay = document.getElementById('modal-overlay');
            const modalClose = document.getElementById('modal-close');
            const clickSound = document.getElementById('click-sound');

            surpriseButton.addEventListener('click', function() {
                clickSound.play();
                modalOverlay.classList.add('active');
                confetti({
                    particleCount: 100,
                    spread: 70,
                    origin: { y: 0.6 }
                });
            });

            modalClose.addEventListener('click', function() {
                modalOverlay.classList.remove('active');
            });

            // Music controls
            const musicToggle = document.getElementById('music-toggle');
            const musicIcon = document.getElementById('music-icon');
            const backgroundMusic = document.getElementById('background-music');
            let isMusicPlaying = false;

            musicToggle.addEventListener('click', function() {
                if (isMusicPlaying) {
                    backgroundMusic.pause();
                    musicIcon.classList.remove('fa-volume-up');
                    musicIcon.classList.add('fa-volume-mute');
                } else {
                    backgroundMusic.play().catch(e => console.log('Audio play error:', e));
                    musicIcon.classList.remove('fa-volume-mute');
                    musicIcon.classList.add('fa-volume-up');
                }
                isMusicPlaying = !isMusicPlaying;
            });

            // Helper Functions
            function createFloatingElement(element, index) {
                const floatingElement = document.createElement('div');
                floatingElement.classList.add('floating-element');
                
                if (element.emoji) {
                    floatingElement.textContent = element.emoji;
                    floatingElement.style.fontSize = element.size;
                } else if (element.type === 'heart') {
                    floatingElement.innerHTML = '<i class="fas fa-heart"></i>';
                    floatingElement.style.color = element.color;
                    floatingElement.style.fontSize = element.size;
                } else if (element.type === 'star') {
                    floatingElement.innerHTML = '<i class="fas fa-star"></i>';
                    floatingElement.style.color = element.color;
                    floatingElement.style.fontSize = element.size;
                }
                
                // Random positioning
                const randomX = Math.random() * window.innerWidth;
                const randomY = Math.random() * window.innerHeight;
                floatingElement.style.left = `${randomX}px`;
                floatingElement.style.top = `${randomY}px`;
                
                // Animation duration and delay
                const duration = 5 + Math.random() * 10;
                const delay = Math.random() * 5;
                floatingElement.style.animationDuration = `${duration}s`;
                floatingElement.style.animationDelay = `${delay}s`;
                
                document.body.appendChild(floatingElement);
            }

            function createCursorEffect(e) {
                const cursorEffect = document.createElement('div');
                cursorEffect.classList.add('cursor-effect');
                cursorEffect.style.left = `${e.pageX}px`;
                cursorEffect.style.top = `${e.pageY}px`;
                document.body.appendChild(cursorEffect);
                
                setTimeout(() => {
                    cursorEffect.style.opacity = 1;
                    cursorEffect.style.transform = `translate(-50%, -50%) scale(${Math.random() * 0.5 + 0.5})`;
                    
                    setTimeout(() => {
                        cursorEffect.style.opacity = 0;
                        setTimeout(() => {
                            cursorEffect.remove();
                        }, 500);
                    }, 300);
                }, 10);
            }
        });
    </script>
</body>
</html>
