<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Anniversary Bebi!</title>
    
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Load Cute Google Fonts: Mali and Quicksand -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Mali:ital,wght@0,500;0,600;0,700;1,500&family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* Base styling */
        body {
            font-family: 'Quicksand', sans-serif;
            background: linear-gradient(135deg, #FFF0F5 0%, #E6E6FA 100%);
            color: #4A4A4A;
            /* Allow scrolling on tiny screens just in case, but aim for perfect center */
            overflow-x: hidden; 
            overflow-y: auto;
        }
        
        .font-kawaii {
            font-family: 'Mali', cursive;
        }

        /* Gentle floating animation */
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-15px) rotate(2deg); }
        }
        .animate-float {
            animation: float 4s ease-in-out infinite;
        }

        /* Sparkle/Star twinkle animation */
        @keyframes twinkle {
            0%, 100% { opacity: 0.2; transform: scale(0.8); }
            50% { opacity: 1; transform: scale(1.2); }
        }
        .animate-twinkle {
            animation: twinkle 3s ease-in-out infinite;
        }

        /* Hover bounce for buttons */
        .hover-bounce {
            transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275), box-shadow 0.3s ease;
        }
        .hover-bounce:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 30px -10px rgba(255, 105, 180, 0.4);
        }

        /* Reveal Transitions */
        .fade-out {
            opacity: 0;
            transform: translateY(-30px) scale(0.9);
            transition: all 0.6s cubic-bezier(0.4, 0, 0.2, 1);
            pointer-events: none;
        }

        .fade-in-up {
            opacity: 0;
            transform: translateY(40px);
            transition: all 0.8s cubic-bezier(0.34, 1.56, 0.64, 1);
        }
        .fade-in-up.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* Cute tooltip arrow */
        .tooltip-arrow::after {
            content: '';
            position: absolute;
            top: 100%;
            left: 50%;
            margin-left: -6px;
            border-width: 6px;
            border-style: solid;
            border-color: #fff transparent transparent transparent;
        }
    </style>
</head>
<!-- min-h-screen and flex center guarantee the content is perfectly middle-aligned and not cut off -->
<body class="flex flex-col items-center justify-center min-h-screen w-full relative p-4">

    <!-- Soft background decorative blobs -->
    <div class="fixed top-10 left-10 w-72 h-72 bg-pink-200 rounded-full mix-blend-multiply filter blur-3xl opacity-40 animate-pulse -z-10"></div>
    <div class="fixed bottom-10 right-10 w-80 h-80 bg-purple-200 rounded-full mix-blend-multiply filter blur-3xl opacity-40 animate-pulse -z-10" style="animation-delay: 2s;"></div>

    <!-- Background Twinkling Stars -->
    <div class="fixed top-1/4 left-1/4 text-pink-300 animate-twinkle text-2xl -z-10">✨</div>
    <div class="fixed top-1/3 right-1/4 text-purple-300 animate-twinkle text-xl -z-10" style="animation-delay: 1s;">✨</div>
    <div class="fixed bottom-1/4 left-1/3 text-pink-400 animate-twinkle text-lg -z-10" style="animation-delay: 1.5s;">✨</div>

    <!-- Main Wrapper to hold both states -->
    <main class="relative z-10 w-full max-w-md flex flex-col items-center justify-center min-h-[400px]">
        
        <!-- Step 1: The Interactive Envelope -->
        <div id="envelope-container" class="flex flex-col items-center cursor-pointer group w-full" onclick="revealGift()">
            
            <!-- Cute Tooltip -->
            <div class="mb-6 bg-white px-5 py-3 rounded-2xl shadow-sm tooltip-arrow relative animate-bounce">
                <p class="font-kawaii text-pink-500 font-bold text-lg tracking-wide">Open me, bebi! 💌</p>
            </div>
            
            <!-- Kawaii Envelope SVG -->
            <div class="animate-float">
                <svg width="240" height="180" viewBox="0 0 220 160" fill="none" xmlns="http://www.w3.org/2000/svg" class="drop-shadow-2xl">
                    <!-- Back flap/inner envelope -->
                    <path d="M10 40 H210 V140 C210 148 202 150 195 150 H25 C18 150 10 148 10 140 V40 Z" fill="#F3E8FF"/>
                    
                    <!-- Main body -->
                    <path d="M10 50 L110 110 L210 50 V140 C210 148 202 150 195 150 H25 C18 150 10 148 10 140 V50 Z" fill="#FDF4FF"/>
                    
                    <!-- Side folds (shadows) -->
                    <path d="M10 50 L90 100 L10 150 Z" fill="#FCE7F3" opacity="0.6"/>
                    <path d="M210 50 L130 100 L210 150 Z" fill="#FCE7F3" opacity="0.6"/>

                    <!-- Top Flap -->
                    <path d="M10 40 L110 105 L210 40" stroke="#FFFFFF" stroke-width="8" stroke-linecap="round" stroke-linejoin="round"/>
                    
                    <!-- Cute Ribbon/Bow Seal (Hello Kitty / Kuromi inspired) -->
                    <g transform="translate(110, 105)">
                        <!-- Left Loop -->
                        <path d="M -5 0 C -25 -20, -35 15, -5 5" fill="#F472B6" stroke="#BE185D" stroke-width="1.5"/>
                        <!-- Right Loop -->
                        <path d="M 5 0 C 25 -20, 35 15, 5 5" fill="#F472B6" stroke="#BE185D" stroke-width="1.5"/>
                        <!-- Center Knot -->
                        <circle cx="0" cy="2" r="6" fill="#EC4899" stroke="#BE185D" stroke-width="1.5"/>
                    </g>
                </svg>
            </div>
        </div>

        <!-- Step 2: The Reveal Content (Initially hidden) -->
        <!-- Added pt-14 (padding top) so the absolutely positioned cat doesn't clip outside the container boundaries -->
        <div id="reveal-container" class="hidden flex-col items-center w-full fade-in-up mt-8">
            
            <div class="relative w-full bg-white/90 backdrop-blur-lg border-4 border-pink-200 rounded-[2.5rem] shadow-2xl pt-14 pb-8 px-6 sm:px-8 text-center mt-12">
                
                <!-- Cute Peeking Cat SVG -->
                <!-- Moved down slightly using -top-12 instead of -top-16 to ensure it stays in view -->
                <div class="absolute -top-12 left-1/2 transform -translate-x-1/2 drop-shadow-md z-20">
                    <svg width="120" height="72" viewBox="0 0 100 60" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <!-- Ears -->
                        <path d="M 25 60 L 25 15 Q 30 5 45 25 Z" fill="#FFFFFF"/>
                        <path d="M 75 60 L 75 15 Q 70 5 55 25 Z" fill="#FFFFFF"/>
                        <!-- Inner Ears (Pink) -->
                        <path d="M 28 50 L 28 25 Q 32 18 40 32 Z" fill="#FBCFE8"/>
                        <path d="M 72 50 L 72 25 Q 68 18 60 32 Z" fill="#FBCFE8"/>
                        <!-- Head -->
                        <path d="M 15 60 Q 50 -10 85 60 Z" fill="#FFFFFF"/>
                        <!-- Eyes -->
                        <circle cx="38" cy="40" r="4" fill="#374151"/>
                        <circle cx="62" cy="40" r="4" fill="#374151"/>
                        <!-- Nose/Mouth (Kawaii '3' shape) -->
                        <path d="M 48 45 Q 50 48 50 45 Q 50 48 52 45" stroke="#374151" fill="none" stroke-width="2" stroke-linecap="round"/>
                        <circle cx="50" cy="43" r="1.5" fill="#F472B6"/>
                        <!-- Blush -->
                        <ellipse cx="30" cy="45" rx="5" ry="2.5" fill="#FBCFE8" opacity="0.9"/>
                        <ellipse cx="70" cy="45" rx="5" ry="2.5" fill="#FBCFE8" opacity="0.9"/>
                        <!-- Paws hanging over the edge -->
                        <rect x="30" y="55" width="12" height="15" rx="6" fill="#FFFFFF" stroke="#E5E7EB" stroke-width="1.5"/>
                        <rect x="58" y="55" width="12" height="15" rx="6" fill="#FFFFFF" stroke="#E5E7EB" stroke-width="1.5"/>
                    </svg>
                </div>

                <h1 class="font-kawaii text-3xl sm:text-4xl text-pink-500 mb-5 font-bold drop-shadow-sm leading-tight">
                    Happy Anniversary, Bebi! 💕
                </h1>
                
                <p class="text-gray-700 mb-8 text-base sm:text-lg font-medium leading-relaxed px-2">
                    i love you so much bebi. happy 2 years. everyday flows by so fast with you. i can't wait to celebrate with you bebi. you deserve this! im sorry for also dirtying your car 🥺
                </p>

                <!-- The Gift Button -->
                <a href="https://www.groupon.com/gifts/vs-1b5b8bdfb64e5388d341d22390c9949e5ddc9ed6" 
                   target="_blank" 
                   rel="noopener noreferrer"
                   class="inline-flex items-center justify-center px-6 sm:px-8 py-4 text-lg sm:text-xl font-bold text-white bg-gradient-to-r from-pink-400 to-purple-400 rounded-full hover-bounce focus:outline-none shadow-lg shadow-pink-200 w-full sm:w-auto">
                    <span class="flex items-center gap-2">
                   ᕬ_ᕬ
‎                 (• ܫ •)
                /⊃🎁⊂\ Claim Your Gift!
                        <!-- Sparkle icon inline -->
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z" />
                        </svg>
                    </span>
                </a>
            </div>
        </div>
    </main>

    <script>
        function revealGift() {
            const envelope = document.getElementById('envelope-container');
            const reveal = document.getElementById('reveal-container');

            // Fade out and shrink the envelope
            envelope.classList.add('fade-out');

            // Wait for envelope to disappear, then swap display and animate the card up
            setTimeout(() => {
                // Hide envelope entirely from DOM flow
                envelope.style.display = 'none';
                
                // Show reveal container (using flex to keep it centered)
                reveal.classList.remove('hidden');
                reveal.classList.add('flex');
                
                // Force a browser reflow so the transition applies smoothly
                void reveal.offsetWidth; 
                
                // Trigger the upward bouncy animation
                reveal.classList.add('active');
            }, 550); 
        }
    </script>
</body>
</html>
