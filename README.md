<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Circus Adventure</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
            font-family: 'Arial Black', sans-serif;
            overflow-y: auto;
        }

        /* Animated stars background */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: white;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }

        .container {
            position: relative;
            z-index: 10;
            text-align: center;
            padding: 40px;
            background: rgba(10, 10, 20, 0.7);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            max-width: 600px;
            margin: 40px auto;
        }

        .circus-text {
            font-size: 4.5rem;
            font-weight: 900;
            letter-spacing: 3px;
            margin-bottom: 30px;
            text-shadow: 
                3px 3px 0px rgba(0, 0, 0, 0.5),
                6px 6px 0px rgba(0, 0, 0, 0.3);
            animation: circusFloat 4s ease-in-out infinite;
            line-height: 1.3;
        }

        @keyframes circusFloat {
            0%, 100% { transform: translateY(0px) rotate(-1deg); }
            50% { transform: translateY(-20px) rotate(1deg); }
        }

        /* Colorful text with gradient and individual letter colors */
        .red {
            color: #FF1744;
            text-shadow: 0 0 20px rgba(255, 23, 68, 0.8);
        }

        .blue {
            color: #00B8FF;
            text-shadow: 0 0 20px rgba(0, 184, 255, 0.8);
        }

        .yellow {
            color: #FFD600;
            text-shadow: 0 0 20px rgba(255, 214, 0, 0.8);
        }

        /* Caine image styling */
        .caine-image {
            width: 250px;
            height: 250px;
            margin: 30px auto;
            display: block;
            animation: caineSpinBounce 3s ease-in-out infinite;
            filter: drop-shadow(0 0 30px rgba(255, 23, 68, 0.6)) drop-shadow(0 0 20px rgba(0, 184, 255, 0.4));
        }

        @keyframes caineSpinBounce {
            0%, 100% { transform: translateY(0) rotate(-2deg); }
            50% { transform: translateY(-15px) rotate(2deg); }
        }

        /* Circus lights */
        .spotlight {
            position: absolute;
            width: 400px;
            height: 400px;
            border-radius: 50%;
            opacity: 0.1;
            filter: blur(40px);
        }

        .spotlight-red {
            background: #FF1744;
            top: -100px;
            left: -100px;
            animation: moveSpotlight1 8s ease-in-out infinite;
        }

        .spotlight-blue {
            background: #00B8FF;
            bottom: -100px;
            right: -100px;
            animation: moveSpotlight2 8s ease-in-out infinite;
        }

        .spotlight-yellow {
            background: #FFD600;
            top: 50%;
            right: -100px;
            animation: moveSpotlight3 8s ease-in-out infinite;
        }

        @keyframes moveSpotlight1 {
            0%, 100% { transform: translate(0, 0); }
            50% { transform: translate(50px, 50px); }
        }

        @keyframes moveSpotlight2 {
            0%, 100% { transform: translate(0, 0); }
            50% { transform: translate(-50px, -50px); }
        }

        @keyframes moveSpotlight3 {
            0%, 100% { transform: translate(0, 0); }
            50% { transform: translate(-50px, 50px); }
        }

        /* Decorative circus elements */
        .circus-decoration {
            position: absolute;
            font-size: 3rem;
            opacity: 0.6;
            animation: bounce 2s infinite;
        }

        .decoration-1 { top: 10%; left: 5%; animation-delay: 0s; }
        .decoration-2 { top: 15%; right: 5%; animation-delay: 0.5s; }
        .decoration-3 { bottom: 15%; left: 8%; animation-delay: 1s; }
        .decoration-4 { bottom: 10%; right: 8%; animation-delay: 1.5s; }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }

        /* Confetti effect */
        .confetti {
            position: fixed;
            pointer-events: none;
            font-size: 2rem;
        }
    </style>
</head>
<body>
    <div class="stars" id="stars"></div>

    <!-- Spotlight effects -->
    <div class="spotlight spotlight-red"></div>
    <div class="spotlight spotlight-blue"></div>
    <div class="spotlight spotlight-yellow"></div>

    <!-- Circus decorations -->
    <div class="circus-decoration decoration-1">🎪</div>
    <div class="circus-decoration decoration-2">🎭</div>
    <div class="circus-decoration decoration-3">🎨</div>
    <div class="circus-decoration decoration-4">🎬</div>

    <!-- Main content -->
    <div class="container">
        <div class="circus-text">
            <span class="red">H</span><span class="blue">e</span><span class="yellow">l</span><span class="red">l</span><span class="blue">o</span>
            <br>
            <span class="yellow">m</span><span class="red">y</span>
            <br>
            <span class="blue">d</span><span class="yellow">e</span><span class="red">a</span><span class="blue">r</span><span class="yellow">,</span>
            <br>
            <span class="red">l</span><span class="blue">o</span><span class="yellow">o</span><span class="red">k</span><span class="blue">i</span><span class="yellow">n</span><span class="red">g</span>
            <br>
            <span class="blue">f</span><span class="yellow">o</span><span class="red">r</span>
            <br>
            <span class="yellow">a</span><span class="red">n</span>
            <br>
            <span class="blue">a</span><span class="yellow">d</span><span class="red">v</span><span class="blue">e</span><span class="yellow">n</span><span class="red">t</span><span class="blue">u</span><span class="yellow">r</span><span class="red">e</span>
        </div>
        
        <!-- Caine Image - SVG Illustration -->
        <svg class="caine-image" viewBox="0 0 200 300" xmlns="http://www.w3.org/2000/svg">
            <!-- Body -->
            <ellipse cx="100" cy="150" rx="45" ry="65" fill="#E91E63"/>
            
            <!-- Legs -->
            <rect x="80" y="210" width="12" height="55" fill="#1a1a2e" rx="6"/>
            <rect x="108" y="210" width="12" height="55" fill="#1a1a2e" rx="6"/>
            
            <!-- Shoes -->
            <ellipse cx="86" cy="270" rx="9" ry="7" fill="#FF6F00"/>
            <ellipse cx="114" cy="270" rx="9" ry="7" fill="#FF6F00"/>
            
            <!-- Arms -->
            <rect x="35" y="135" width="18" height="55" fill="#E91E63" rx="9"/>
            <rect x="147" y="135" width="18" height="55" fill="#E91E63" rx="9"/>
            
            <!-- Gloves -->
            <circle cx="44" cy="195" r="11" fill="white"/>
            <circle cx="156" cy="195" r="11" fill="white"/>
            
            <!-- Cane -->
            <line x1="156" y1="160" x2="175" y2="210" stroke="#2d2d44" stroke-width="3"/>
            <circle cx="175" cy="215" r="5" fill="#FFD700"/>
            
            <!-- Head -->
            <circle cx="100" cy="80" r="42" fill="#E91E63"/>
            
            <!-- Face outline -->
            <circle cx="100" cy="85" r="36" fill="none" stroke="#8B0A50" stroke-width="1.5"/>
            
            <!-- Eyes white -->
            <circle cx="82" cy="68" r="13" fill="white"/>
            <circle cx="118" cy="68" r="13" fill="white"/>
            
            <!-- Eyes pupils - Blue and Green -->
            <circle cx="82" cy="71" r="9" fill="#0066FF"/>
            <circle cx="118" cy="71" r="9" fill="#00AA44"/>
            
            <!-- Mouth - Big smile -->
            <path d="M 85 95 Q 100 108 115 95" stroke="#8B0A50" stroke-width="2.5" fill="none"/>
            <path d="M 85 95 L 115 95" stroke="#FF6B00" stroke-width="1.5"/>
            
            <!-- Teeth -->
            <rect x="86" y="93" width="4" height="6" fill="white" stroke="#333" stroke-width="0.5"/>
            <rect x="92" y="93" width="4" height="6" fill="white" stroke="#333" stroke-width="0.5"/>
            <rect x="98" y="93" width="4" height="6" fill="white" stroke="#333" stroke-width="0.5"/>
            <rect x="104" y="93" width="4" height="6" fill="white" stroke="#333" stroke-width="0.5"/>
            <rect x="110" y="93" width="4" height="6" fill="white" stroke="#333" stroke-width="0.5"/>
            
            <!-- Top hat -->
            <rect x="68" y="18" width="64" height="22" fill="#2d2d44" rx="2"/>
            <ellipse cx="100" cy="40" rx="34" ry="8" fill="#2d2d44"/>
            <ellipse cx="100" cy="38" rx="32" ry="6" fill="#1a1a2e"/>
            
            <!-- Hat band -->
            <rect x="68" y="38" width="64" height="3" fill="#E91E63"/>
            
            <!-- Chest decoration -->
            <rect x="82" y="120" width="36" height="18" fill="#8B0A50" rx="2"/>
            <circle cx="91" cy="129" r="2.5" fill="#FFD700"/>
            <circle cx="100" cy="129" r="2.5" fill="#FFD700"/>
            <circle cx="109" cy="129" r="2.5" fill="#FFD700"/>
        </svg>
    </div>

    <script>
        // Generate random stars
        function generateStars() {
            const starsContainer = document.getElementById('stars');
            for (let i = 0; i < 50; i++) {
                const star = document.createElement('div');
                star.className = 'star';
                star.style.left = Math.random() * 100 + '%';
                star.style.top = Math.random() * 100 + '%';
                star.style.animationDelay = Math.random() * 3 + 's';
                starsContainer.appendChild(star);
            }
        }

        // Generate confetti
        function createConfetti() {
            const confettiTypes = ['🎪', '🎭', '🎨', '🎬', '⭐', '✨'];
            for (let i = 0; i < 30; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.textContent = confettiTypes[Math.floor(Math.random() * confettiTypes.length)];
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.top = -50 + 'px';
                confetti.style.opacity = Math.random() * 0.5 + 0.5;
                
                document.body.appendChild(confetti);
                
                const duration = Math.random() * 3 + 3;
                const randomX = (Math.random() - 0.5) * 200;
                
                confetti.animate([
                    { transform: 'translateY(0) translateX(0) rotate(0)', opacity: 1 },
                    { transform: `translateY(${window.innerHeight + 50}px) translateX(${randomX}px) rotate(360deg)`, opacity: 0 }
                ], {
                    duration: duration * 1000,
                    easing: 'ease-in'
                });
                
                setTimeout(() => confetti.remove(), duration * 1000);
            }
        }

        // Initialize
        generateStars();
        createConfetti();

        // Create confetti periodically
        setInterval(createConfetti, 4000);
    </script>
</body>
</html>
