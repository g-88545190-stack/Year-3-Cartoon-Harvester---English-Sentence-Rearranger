<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Year 3 Cartoon Harvester - English Sentence Rearranger</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Quicksand:wght@500;600;700&display=swap" rel="stylesheet">
    <!-- Canvas Confetti -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        fredoka: ['"Fredoka One"', 'cursive'],
                        quicksand: ['"Quicksand"', 'sans-serif']
                    },
                    colors: {
                        brand: {
                            purple: '#8B5CF6',
                            pink: '#EC4899',
                            yellow: '#F59E0B',
                            green: '#10B981',
                            blue: '#3B82F6',
                            dark: '#1E1B4B'
                        }
                    },
                    animation: {
                        'bounce-slow': 'bounce 2s infinite',
                        'float': 'float 3s ease-in-out infinite',
                        'pulse-glow': 'pulseGlow 2s infinite',
                        'harvest-pop': 'harvestPop 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275)'
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0px) rotate(0deg)' },
                            '50%': { transform: 'translateY(-10px) rotate(3deg)' }
                        },
                        pulseGlow: {
                            '0%, 100%': { boxShadow: '0 0 15px rgba(236, 72, 153, 0.6)' },
                            '50%': { boxShadow: '0 0 30px rgba(245, 158, 11, 0.9)' }
                        },
                        harvestPop: {
                            '0%': { transform: 'scale(0.3) rotate(-10deg)', opacity: '0' },
                            '50%': { transform: 'scale(1.2) rotate(5deg)', opacity: '1' },
                            '100%': { transform: 'scale(1) rotate(0deg)', opacity: '1' }
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            font-family: 'Quicksand', sans-serif;
            background: linear-gradient(135deg, #2e1065 0%, #4c1d95 35%, #831843 100%);
            min-height: 100vh;
            color: #ffffff;
            user-select: none;
            overflow-x: hidden;
        }

        .glass-panel {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 2px solid rgba(255, 255, 255, 0.25);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(8px);
            border: 2px solid rgba(255, 255, 255, 0.3);
        }

        .word-tile {
            transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 6px 0 rgba(0, 0, 0, 0.25);
        }

        .word-tile:active {
            transform: translateY(4px);
            box-shadow: 0 2px 0 rgba(0, 0, 0, 0.25);
        }

        .phone-viewport {
            max-width: 430px;
            height: 880px;
            max-height: 92vh;
            border-radius: 40px;
            border: 8px solid #312e81;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.7);
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: rgba(0,0,0,0.2);
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb {
            background: rgba(255,255,255,0.4);
            border-radius: 10px;
        }
    </style>
</head>
<body class="flex flex-col items-center justify-between min-h-screen p-2 sm:p-4">

    <!-- TOP CONTROL BAR -->
    <header class="w-full max-w-5xl flex flex-wrap items-center justify-between gap-2 mb-3 px-3 py-2 rounded-2xl glass-panel z-20">
        <div class="flex items-center gap-3">
            <div class="bg-gradient-to-tr from-amber-400 to-pink-500 p-2.5 rounded-xl shadow-lg">
                <i class="fa-solid font-fredoka fa-wheat-awn text-2xl text-white"></i>
            </div>
            <div>
                <h1 class="font-fredoka text-lg sm:text-xl text-yellow-300 leading-none">Cartoon Harvester</h1>
                <p class="text-xs text-indigo-200">Year 3 English (KSSR / Super Minds)</p>
            </div>
        </div>

        <div class="flex items-center gap-2">
            <!-- View Mode Switcher -->
            <button id="viewToggleBtn" onclick="toggleViewMode()" class="px-3 py-1.5 rounded-xl bg-indigo-950/60 hover:bg-indigo-900 border border-indigo-400/40 text-xs font-bold text-indigo-200 flex items-center gap-1.5 transition">
                <i id="viewIcon" class="fa-solid fa-mobile-screen text-pink-400 text-sm"></i>
                <span id="viewText">Phone View</span>
            </button>

            <!-- Gallery Button -->
            <button onclick="openGallery()" class="px-3 py-1.5 rounded-xl bg-pink-600/80 hover:bg-pink-500 border border-pink-300/50 text-xs font-bold text-white flex items-center gap-1.5 shadow-md transition">
                <i class="fa-solid fa-box-open text-yellow-300"></i>
                <span>Harvested (<span id="galleryCount">0</span>/90)</span>
            </button>

            <!-- Teacher / Cheat Dashboard -->
            <button onclick="openTeacherModal()" class="p-2 rounded-xl bg-purple-900/70 hover:bg-purple-800 border border-purple-400/40 text-purple-200 text-xs transition" title="Teacher Settings">
                <i class="fa-solid fa-chalkboard-user text-base"></i>
            </button>
        </div>
    </header>

    <!-- MAIN GAME CONTAINER -->
    <main id="gameContainer" class="w-full max-w-4xl flex-1 flex flex-col justify-between transition-all duration-300 relative my-auto">
        <div id="appViewport" class="w-full h-full flex flex-col justify-between p-3 sm:p-5 rounded-3xl glass-panel relative overflow-hidden">
            
            <!-- HEADER LEVEL & SCORE INFO -->
            <div class="flex items-center justify-between mb-2">
                <!-- Level Selector Badge -->
                <div class="flex items-center gap-2">
                    <span id="levelBadge" class="px-3 py-1 rounded-full text-xs font-fredoka bg-gradient-to-r from-emerald-500 to-teal-600 text-white shadow-md uppercase tracking-wider">
                        Level 1: Easy
                    </span>
                    <span class="text-xs text-indigo-200 font-semibold">Q: <span id="currentQNum">1</span>/30</span>
                </div>

                <!-- Mute Sound -->
                <button onclick="toggleAudio()" id="audioBtn" class="p-1.5 rounded-lg bg-indigo-900/50 text-indigo-200 hover:text-white text-xs">
                    <i class="fa-solid fa-volume-high" id="audioIcon"></i>
                </button>
            </div>

            <!-- LEVEL PROGRESS BAR -->
            <div class="w-full bg-indigo-950/60 rounded-full h-3 mb-4 p-0.5 border border-indigo-400/30 overflow-hidden">
                <div id="progressBar" class="bg-gradient-to-r from-yellow-400 via-pink-500 to-purple-500 h-full rounded-full transition-all duration-500" style="width: 3.33%;"></div>
            </div>

            <!-- CARTOON CHARACTER CARD (HARVEST TARGET) -->
            <div class="relative w-full mb-3">
                <div id="characterCard" class="w-full p-3 sm:p-4 rounded-2xl glass-card flex items-center gap-3 sm:gap-4 relative overflow-hidden border border-amber-300/40">
                    <!-- Dynamic Character Avatar SVG -->
                    <div id="charAvatarContainer" class="relative w-20 h-20 sm:w-24 sm:h-24 flex-shrink-0 flex items-center justify-center bg-indigo-900/50 rounded-2xl border-2 border-amber-400/60 p-1 shadow-inner animate-float">
                        <!-- SVG graphic will load dynamically -->
                    </div>

                    <!-- Character Quote / Hint -->
                    <div class="flex-1 min-w-0">
                        <div class="flex items-center justify-between">
                            <span id="charMovie" class="text-[10px] sm:text-xs font-bold uppercase tracking-wider text-pink-300 bg-pink-950/60 px-2 py-0.5 rounded-md border border-pink-500/30">
                                Disney Movie
                            </span>
                            <span id="charHarvestStatus" class="text-[10px] text-amber-300 font-bold flex items-center gap-1">
                                <i class="fa-solid fa-wheat-awn"></i> Ready to Harvest
                            </span>
                        </div>
                        <h2 id="charName" class="font-fredoka text-base sm:text-lg text-yellow-300 truncate mt-0.5">Character Name</h2>
                        <p id="charHint" class="text-xs text-indigo-100 italic line-clamp-2 mt-1 bg-indigo-900/30 p-1.5 rounded-lg border border-indigo-500/20">
                            "Help me fix this mixed up sentence!"
                        </p>
                    </div>
                </div>
            </div>

            <!-- SENTENCE BUILDING ZONE (SELECTED WORDS) -->
            <div class="flex-1 flex flex-col justify-center mb-3">
                <div class="text-xs font-bold text-indigo-200 uppercase tracking-widest mb-1.5 flex items-center justify-between px-1">
                    <span><i class="fa-solid fa-pen-ruler text-amber-400 mr-1"></i> Your Sentence:</span>
                    <span id="wordCountBadge" class="text-[10px] bg-indigo-900/80 text-indigo-300 px-2 py-0.5 rounded-md">0 words</span>
                </div>
                
                <div id="targetZone" class="min-h-[90px] sm:min-h-[110px] w-full p-2.5 sm:p-3 rounded-2xl bg-indigo-950/70 border-2 border-dashed border-indigo-400/50 flex flex-wrap items-center align-content-start gap-2 shadow-inner transition-colors">
                    <!-- Selected word tiles appear here -->
                    <p id="emptyHint" class="text-indigo-400 text-xs italic m-auto pointer-events-none text-center">
                        Tap words from below to arrange the sentence in correct order!
                    </p>
                </div>
            </div>

            <!-- WORD BANK ZONE (JUMBLED WORDS) -->
            <div class="mb-4">
                <div class="text-xs font-bold text-indigo-200 uppercase tracking-widest mb-1.5 px-1">
                    <i class="fa-solid fa-cubes text-pink-400 mr-1"></i> Jumbled Word Tiles:
                </div>
                <div id="sourceZone" class="min-h-[80px] w-full p-2.5 rounded-2xl bg-indigo-900/40 border border-indigo-500/30 flex flex-wrap items-center justify-center gap-2">
                    <!-- Word tiles generated here -->
                </div>
            </div>

            <!-- ACTION BUTTONS -->
            <div class="flex items-center gap-2">
                <button onclick="undoLastWord()" class="flex-1 py-2.5 sm:py-3 rounded-xl bg-slate-700/80 hover:bg-slate-600 border border-slate-400/40 text-white font-bold text-xs sm:text-sm flex items-center justify-center gap-1.5 active:scale-95 transition">
                    <i class="fa-solid fa-rotate-left text-amber-300"></i> Undo
                </button>
                <button onclick="clearSentence()" class="flex-1 py-2.5 sm:py-3 rounded-xl bg-red-900/80 hover:bg-red-800 border border-red-400/40 text-white font-bold text-xs sm:text-sm flex items-center justify-center gap-1.5 active:scale-95 transition">
                    <i class="fa-solid fa-trash-can text-red-300"></i> Clear
                </button>
                <button onclick="checkAnswer()" class="flex-[2] py-2.5 sm:py-3 rounded-xl bg-gradient-to-r from-amber-500 via-pink-500 to-purple-600 hover:from-amber-400 hover:to-purple-500 border border-amber-300/50 text-white font-fredoka text-sm sm:text-base tracking-wide flex items-center justify-center gap-2 shadow-lg active:scale-95 transition">
                    <i class="fa-solid fa-circle-check text-yellow-300 text-lg"></i> CHECK ANSWER
                </button>
            </div>

        </div>
    </main>

    <!-- FOOTER / CREDIT -->
    <footer class="text-center text-[11px] text-indigo-300/80 mt-2">
        KSSR Semakan Year 3 English Language Activity • Cartoon Harvester Edition
    </footer>

    <!-- MODAL: HARVEST GALLERY -->
    <div id="galleryModal" class="fixed inset-0 bg-black/80 backdrop-blur-md flex items-center justify-center p-3 z-50 hidden">
        <div class="bg-indigo-950 border-2 border-pink-500/50 rounded-3xl w-full max-w-2xl max-h-[85vh] flex flex-col overflow-hidden shadow-2xl">
            <!-- Modal Header -->
            <div class="p-4 bg-gradient-to-r from-purple-900 to-pink-900 flex items-center justify-between border-b border-indigo-800">
                <div class="flex items-center gap-2">
                    <i class="fa-solid fa-wheat-awn text-2xl text-yellow-400"></i>
                    <div>
                        <h3 class="font-fredoka text-lg text-yellow-300">Harvested Character Collection</h3>
                        <p class="text-xs text-indigo-200">Collect all 90 cartoon friends across 3 levels!</p>
                    </div>
                </div>
                <button onclick="closeGallery()" class="w-8 h-8 rounded-full bg-indigo-900 hover:bg-indigo-800 text-indigo-200 flex items-center justify-center font-bold">
                    &times;
                </button>
            </div>

            <!-- Level Tabs -->
            <div class="flex border-b border-indigo-800 bg-indigo-900/50">
                <button onclick="switchGalleryTab(1)" id="tabL1" class="flex-1 py-2 text-xs font-bold text-amber-300 border-b-2 border-amber-400 bg-indigo-800/40">
                    Level 1 (0/30)
                </button>
                <button onclick="switchGalleryTab(2)" id="tabL2" class="flex-1 py-2 text-xs font-bold text-indigo-400 hover:text-indigo-200">
                    Level 2 (0/30)
                </button>
                <button onclick="switchGalleryTab(3)" id="tabL3" class="flex-1 py-2 text-xs font-bold text-indigo-400 hover:text-indigo-200">
                    Level 3 (0/30)
                </button>
            </div>

            <!-- Gallery Grid -->
            <div id="galleryGrid" class="p-4 overflow-y-auto grid grid-cols-2 sm:grid-cols-3 gap-3 flex-1">
                <!-- Character tiles loaded dynamically -->
            </div>
        </div>
    </div>

    <!-- MODAL: LEVEL CLEARED / VICTORY CELEBRATION -->
    <div id="victoryModal" class="fixed inset-0 bg-black/85 backdrop-blur-lg flex items-center justify-center p-4 z-50 hidden">
        <div class="bg-gradient-to-b from-indigo-900 to-purple-950 border-4 border-amber-400 rounded-3xl w-full max-w-md p-6 text-center shadow-2xl relative animate-harvest-pop overflow-hidden">
            <div class="absolute -top-10 -left-10 w-32 h-32 bg-pink-500/20 rounded-full blur-2xl"></div>
            <div class="absolute -bottom-10 -right-10 w-32 h-32 bg-amber-500/20 rounded-full blur-2xl"></div>

            <div class="w-20 h-20 mx-auto mb-3 bg-amber-400/20 rounded-full border-2 border-amber-300 flex items-center justify-center text-4xl text-yellow-300 shadow-lg">
                <i class="fa-solid fa-trophy animate-bounce"></i>
            </div>

            <span class="px-3 py-1 bg-yellow-400/20 text-yellow-300 border border-yellow-400/50 rounded-full text-xs font-bold uppercase tracking-wider">
                HARVEST COMPLETE!
            </span>

            <h2 id="victoryTitle" class="font-fredoka text-2xl text-yellow-300 mt-2 mb-1">LEVEL 1 CLEARED!</h2>
            <p id="victorySub" class="text-xs text-indigo-200 mb-4">You harvested all 30 characters in this level!</p>

            <!-- Special Harvest Reward Cartoon Card -->
            <div id="victoryCharCard" class="bg-indigo-900/80 border-2 border-amber-400 p-3 rounded-2xl flex items-center gap-3 mb-5 text-left">
                <div id="victoryAvatar" class="w-16 h-16 bg-purple-950 rounded-xl p-1 border border-amber-300 flex-shrink-0">
                    <!-- SVG -->
                </div>
                <div>
                    <span class="text-[10px] text-pink-300 font-bold uppercase">Star Mascot</span>
                    <h4 id="victoryCharName" class="font-fredoka text-yellow-300 text-sm">Character</h4>
                    <p id="victoryCharQuote" class="text-[11px] text-indigo-200 italic">"Amazing job student!"</p>
                </div>
            </div>

            <button id="victoryNextBtn" onclick="nextLevelOrReset()" class="w-full py-3.5 rounded-xl bg-gradient-to-r from-amber-400 via-pink-500 to-purple-600 font-fredoka text-white text-base shadow-xl hover:brightness-110 active:scale-95 transition">
                CONTINUE TO NEXT LEVEL <i class="fa-solid fa-arrow-right ml-1"></i>
            </button>
        </div>
    </div>

    <!-- MODAL: TEACHER DASHBOARD / CHEAT CODES -->
    <div id="teacherModal" class="fixed inset-0 bg-black/80 backdrop-blur-md flex items-center justify-center p-3 z-50 hidden">
        <div class="bg-indigo-950 border-2 border-purple-400 rounded-3xl w-full max-w-lg p-5 shadow-2xl">
            <div class="flex items-center justify-between border-b border-indigo-800 pb-3 mb-4">
                <div class="flex items-center gap-2">
                    <i class="fa-solid fa-chalkboard-user text-2xl text-purple-400"></i>
                    <div>
                        <h3 class="font-fredoka text-lg text-purple-300">Teacher Dashboard</h3>
                        <p class="text-xs text-indigo-300">Classroom tools & fast navigation</p>
                    </div>
                </div>
                <button onclick="closeTeacherModal()" class="w-8 h-8 rounded-full bg-indigo-900 hover:bg-indigo-800 text-indigo-200 flex items-center justify-center font-bold">
                    &times;
                </button>
            </div>

            <div class="space-y-4 text-xs">
                <!-- Jump Level -->
                <div class="bg-indigo-900/50 p-3 rounded-xl border border-indigo-700">
                    <label class="block font-bold text-yellow-300 mb-2">Jump to Level:</label>
                    <div class="grid grid-cols-3 gap-2">
                        <button onclick="jumpToLevel(1)" class="py-2 bg-emerald-600 hover:bg-emerald-500 rounded-lg text-white font-bold">Level 1 (Easy)</button>
                        <button onclick="jumpToLevel(2)" class="py-2 bg-amber-600 hover:bg-amber-500 rounded-lg text-white font-bold">Level 2 (Medium)</button>
                        <button onclick="jumpToLevel(3)" class="py-2 bg-pink-600 hover:bg-pink-500 rounded-lg text-white font-bold">Level 3 (Hard)</button>
                    </div>
                </div>

                <!-- Jump Specific Question -->
                <div class="bg-indigo-900/50 p-3 rounded-xl border border-indigo-700">
                    <label class="block font-bold text-yellow-300 mb-1">Jump to Question Number (1-30 in current level):</label>
                    <div class="flex gap-2">
                        <input type="number" id="qNumInput" min="1" max="30" value="1" class="flex-1 bg-indigo-950 border border-indigo-600 rounded-lg px-3 py-1.5 text-white font-bold">
                        <button onclick="jumpToQuestionInput()" class="px-4 py-1.5 bg-purple-600 hover:bg-purple-500 text-white font-bold rounded-lg">Go</button>
                    </div>
                </div>

                <!-- Unlock All Characters Cheat -->
                <div class="bg-indigo-900/50 p-3 rounded-xl border border-indigo-700 flex items-center justify-between">
                    <div>
                        <span class="font-bold text-yellow-300">Unlock All Characters</span>
                        <p class="text-[10px] text-indigo-300">Unlock full gallery instantly for demonstration.</p>
                    </div>
                    <button onclick="unlockAllCharacters()" class="px-3 py-1.5 bg-amber-500 hover:bg-amber-400 text-indigo-950 font-fredoka rounded-lg text-xs">
                        Unlock All
                    </button>
                </div>

                <!-- Reset All Progress -->
                <div class="bg-indigo-900/50 p-3 rounded-xl border border-indigo-700 flex items-center justify-between">
                    <div>
                        <span class="font-bold text-red-400">Reset Game Progress</span>
                        <p class="text-[10px] text-indigo-300">Clear saved collection and scores.</p>
                    </div>
                    <button onclick="resetGameProgress()" class="px-3 py-1.5 bg-red-600 hover:bg-red-500 text-white font-bold rounded-lg text-xs">
                        Reset All
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- FEEDBACK TOAST / MESSAGE BOX -->
    <div id="feedbackToast" class="fixed bottom-6 left-1/2 -translate-x-1/2 px-5 py-3 rounded-2xl font-bold text-sm shadow-2xl flex items-center gap-2.5 z-40 transition-all duration-300 opacity-0 pointer-events-none transform translate-y-4">
        <i id="feedbackIcon" class="text-xl"></i>
        <span id="feedbackText">Feedback message</span>
    </div>

    <!-- SCRIPT LOGIC -->
    <script>
        /* ==========================================================================
           AUDIO SYSTEM (Web Audio API Procedural Sound Effects)
           ========================================================================== */
        let audioEnabled = true;
        let audioCtx = null;

        function getAudioContext() {
            if (!audioCtx) {
                audioCtx = new (window.AudioContext || window.webkitAudioContext)();
            }
            if (audioCtx.state === 'suspended') {
                audioCtx.resume();
            }
            return audioCtx;
        }

        function playSound(type) {
            if (!audioEnabled) return;
            try {
                const ctx = getAudioContext();
                const now = ctx.currentTime;

                if (type === 'pop') {
                    // Short soft pop for clicking word
                    const osc = ctx.createOscillator();
                    const gain = ctx.createGain();
                    osc.type = 'sine';
                    osc.frequency.setValueAtTime(400, now);
                    osc.frequency.exponentialRampToValueAtTime(800, now + 0.08);
                    gain.gain.setValueAtTime(0.2, now);
                    gain.gain.exponentialRampToValueAtTime(0.01, now + 0.08);
                    osc.connect(gain);
                    gain.connect(ctx.destination);
                    osc.start(now);
                    osc.stop(now + 0.08);
                } else if (type === 'correct') {
                    // Success chord chime
                    [523.25, 659.25, 783.99, 1046.50].forEach((freq, i) => {
                        const osc = ctx.createOscillator();
                        const gain = ctx.createGain();
                        osc.type = 'triangle';
                        osc.frequency.setValueAtTime(freq, now + i * 0.08);
                        gain.gain.setValueAtTime(0.15, now + i * 0.08);
                        gain.gain.exponentialRampToValueAtTime(0.001, now + i * 0.08 + 0.3);
                        osc.connect(gain);
                        gain.connect(ctx.destination);
                        osc.start(now + i * 0.08);
                        osc.stop(now + i * 0.08 + 0.3);
                    });
                } else if (type === 'wrong') {
                    // Error low double buzzer
                    const osc = ctx.createOscillator();
                    const gain = ctx.createGain();
                    osc.type = 'sawtooth';
                    osc.frequency.setValueAtTime(180, now);
                    osc.frequency.setValueAtTime(140, now + 0.12);
                    gain.gain.setValueAtTime(0.2, now);
                    gain.gain.exponentialRampToValueAtTime(0.01, now + 0.28);
                    osc.connect(gain);
                    gain.connect(ctx.destination);
                    osc.start(now);
                    osc.stop(now + 0.28);
                } else if (type === 'fanfare') {
                    // Victory level clear fanfare
                    const notes = [440, 554.37, 659.25, 880];
                    notes.forEach((freq, idx) => {
                        const osc = ctx.createOscillator();
                        const gain = ctx.createGain();
                        osc.type = 'square';
                        osc.frequency.setValueAtTime(freq, now + idx * 0.12);
                        gain.gain.setValueAtTime(0.12, now + idx * 0.12);
                        gain.gain.exponentialRampToValueAtTime(0.001, now + idx * 0.12 + 0.4);
                        osc.connect(gain);
                        gain.connect(ctx.destination);
                        osc.start(now + idx * 0.12);
                        osc.stop(now + idx * 0.12 + 0.4);
                    });
                }
            } catch (e) {
                console.log('Audio playback error:', e);
            }
        }

        function toggleAudio() {
            audioEnabled = !audioEnabled;
            const icon = document.getElementById('audioIcon');
            if (audioEnabled) {
                icon.className = 'fa-solid fa-volume-high';
                showToast('Audio Enabled', 'success');
            } else {
                icon.className = 'fa-solid fa-volume-xmark';
                showToast('Audio Muted', 'info');
            }
        }

        /* ==========================================================================
           CARTOON CHARACTER DATABASE (90 Distinct Movie Characters)
           Each character has a unique SVG illustration generator!
           ========================================================================== */
        const CARTOONS_L1 = [
            { name: "Mirabel Madrigal", movie: "Encanto", quote: "Every gift is special!", color: "#10B981", hair: "#1E1B4B", glasses: true },
            { name: "Mei Lee (Red Panda)", movie: "Turning Red", quote: "Embrace your inner red panda!", color: "#EF4444", hair: "#991B1B" },
            { name: "Ember Lumen", movie: "Elemental", quote: "Fire elements shine bright!", color: "#F59E0B", hair: "#F97316" },
            { name: "Wade Ripple", movie: "Elemental", quote: "Go with the flow!", color: "#3B82F6", hair: "#60A5FA" },
            { name: "Asha", movie: "Wish", quote: "Wish upon a star!", color: "#8B5CF6", hair: "#4C1D95" },
            { name: "Joy", movie: "Inside Out 2", quote: "Keep positive and happy!", color: "#FBBF24", hair: "#3B82F6" },
            { name: "Anxiety", movie: "Inside Out 2", quote: "I'm planning for everything!", color: "#F97316", hair: "#EA580C" },
            { name: "Sadness", movie: "Inside Out 2", quote: "It's okay to feel sad sometimes.", color: "#60A5FA", hair: "#1D4ED8", glasses: true },
            { name: "Disgust", movie: "Inside Out 2", quote: "Eww, broccoli on pizza?", color: "#34D399", hair: "#059669" },
            { name: "Anger", movie: "Inside Out 2", quote: "That is completely unfair!", color: "#DC2626", hair: "#EF4444" },
            { name: "Moana", movie: "Moana", quote: "The ocean is calling me!", color: "#EA580C", hair: "#1E1B4B" },
            { name: "Maui", movie: "Moana", quote: "You're welcome!", color: "#D97706", hair: "#27272A" },
            { name: "Stitch", movie: "Lilo & Stitch", quote: "Ohana means family!", color: "#2563EB", hair: "#1E40AF" },
            { name: "Elsa", movie: "Frozen", quote: "Let the cold never bother you!", color: "#38BDF8", hair: "#FEF08A" },
            { name: "Anna", movie: "Frozen", quote: "Love is an open door!", color: "#F43F5E", hair: "#D97706" },
            { name: "Olaf", movie: "Frozen", quote: "I like warm hugs!", color: "#F8FAFC", hair: "#78350F" },
            { name: "Nick Wilde", movie: "Zootopia", quote: "It's called a hustle, sweetheart!", color: "#EA580C", hair: "#9A3412" },
            { name: "Judy Hopps", movie: "Zootopia", quote: "Anyone can be anything!", color: "#94A3B8", hair: "#475569" },
            { name: "Baymax", movie: "Big Hero 6", quote: "I am your personal healthcare companion.", color: "#F1F5F9", hair: "#E2E8F0" },
            { name: "Hiro Hamada", movie: "Big Hero 6", quote: "That was unbelievable!", color: "#4F46E5", hair: "#0F172A" },
            { name: "Raya", movie: "Raya & Last Dragon", quote: "Trust is the key!", color: "#059669", hair: "#1E1B4B" },
            { name: "Sisu", movie: "Raya & Last Dragon", quote: "I am a dragon!", color: "#06B6D4", hair: "#A5F3FC" },
            { name: "Luca Paguro", movie: "Luca", quote: "Silenzio Bruno!", color: "#0D9488", hair: "#78350F" },
            { name: "Alberto Scorfano", movie: "Luca", quote: "Everything good is on land!", color: "#F59E0B", hair: "#B45309" },
            { name: "Meilin's Panda", movie: "Turning Red", quote: "Fluffy and confident!", color: "#DC2626", hair: "#B91C1C" },
            { name: "Bruno Madrigal", movie: "Encanto", quote: "We don't talk about Bruno!", color: "#047857", hair: "#111827" },
            { name: "Luisa Madrigal", movie: "Encanto", quote: "Surface pressure is high!", color: "#4338CA", hair: "#312E81" },
            { name: "Isabela Madrigal", movie: "Encanto", quote: "Flowers everywhere!", color: "#EC4899", hair: "#111827" },
            { name: "Star", movie: "Wish", quote: "Glow with magic!", color: "#FACC15", hair: "#FEF08A" },
            { name: "Valentino", movie: "Wish", quote: "I can talk now!", color: "#A16207", hair: "#713F12" }
        ];

        const CARTOONS_L2 = [
            { name: "Buzz Lightyear", movie: "Toy Story", quote: "To infinity and beyond!", color: "#16A34A", hair: "#7C3AED" },
            { name: "Woody", movie: "Toy Story", quote: "There's a snake in my boot!", color: "#D97706", hair: "#78350F" },
            { name: "Forky", movie: "Toy Story 4", quote: "I'm trash! No wait, I'm a toy!", color: "#E2E8F0", hair: "#EF4444" },
            { name: "Lightning McQueen", movie: "Cars", quote: "Ka-chow!", color: "#DC2626", hair: "#F59E0B" },
            { name: "Mater", movie: "Cars", quote: "Dad-gum!", color: "#B45309", hair: "#78350F" },
            { name: "Nemo", movie: "Finding Nemo", quote: "Just keep swimming!", color: "#F97316", hair: "#EA580C" },
            { name: "Dory", movie: "Finding Dory", quote: "I remember things!", color: "#2563EB", hair: "#FACC15" },
            { name: "Remy", movie: "Ratatouille", quote: "Anyone can cook!", color: "#64748B", hair: "#334155" },
            { name: "Linguini", movie: "Ratatouille", quote: "The chef made this!", color: "#F59E0B", hair: "#EA580C" },
            { name: "WALL-E", movie: "WALL-E", quote: "Eva!", color: "#CA8A04", hair: "#854D0E" },
            { name: "EVE", movie: "WALL-E", quote: "Directive confirmed.", color: "#F8FAFC", hair: "#0EA5E9" },
            { name: "Carl Fredricksen", movie: "Up", quote: "Adventure is out there!", color: "#94A3B8", hair: "#F1F5F9", glasses: true },
            { name: "Russell", movie: "Up", quote: "Wilderness explorer ready!", color: "#EAB308", hair: "#1E293B" },
            { name: "Dug", movie: "Up", quote: "Squirrel!", color: "#D97706", hair: "#B45309" },
            { name: "Mike Wazowski", movie: "Monsters, Inc.", quote: "Always watching!", color: "#84CC16", hair: "#65A30D" },
            { name: "Sulley", movie: "Monsters, Inc.", quote: "You're doing great kid!", color: "#06B6D4", hair: "#7C3AED" },
            { name: "Boo", movie: "Monsters, Inc.", quote: "Mike Wazowski!", color: "#EC4899", hair: "#1E1B4B" },
            { name: "Mr. Incredible", movie: "The Incredibles", quote: "It's showtime!", color: "#DC2626", hair: "#F59E0B" },
            { name: "Elastigirl", movie: "The Incredibles", quote: "Flexible and strong!", color: "#EA580C", hair: "#9A3412" },
            { name: "Dash", movie: "The Incredibles", quote: "Super fast speed!", color: "#EF4444", hair: "#FACC15" },
            { name: "Violet", movie: "The Incredibles", quote: "Forcefields ready!", color: "#6366F1", hair: "#1E1B4B" },
            { name: "Jack-Jack", movie: "The Incredibles", quote: "Goo goo gaga laser!", color: "#F97316", hair: "#F59E0B" },
            { name: "Frozone", movie: "The Incredibles", quote: "Where is my super suit?", color: "#0284C7", hair: "#0F172A" },
            { name: "Miguel", movie: "Coco", quote: "Un Poco Loco!", color: "#DC2626", hair: "#1E1B4B" },
            { name: "Hector", movie: "Coco", quote: "Remember me!", color: "#78350F", hair: "#27272A" },
            { name: "Dante", movie: "Coco", quote: "Woof woof!", color: "#A16207", hair: "#854D0E" },
            { name: "Joe Gardner", movie: "Soul", quote: "Enjoy the little things!", color: "#1E40AF", hair: "#0F172A", glasses: true },
            { name: "22", movie: "Soul", quote: "Finding my spark!", color: "#A7F3D0", hair: "#34D399" },
            { name: "Po", movie: "Kung Fu Panda", quote: "Skadoosh!", color: "#18181B", hair: "#F8FAFC" },
            { name: "Master Shifu", movie: "Kung Fu Panda", quote: "Inner peace!", color: "#D97706", hair: "#FEF08A" }
        ];

        const CARTOONS_L3 = [
            { name: "Toothless", movie: "How to Train Your Dragon", quote: "Friendly night fury dragon!", color: "#18181B", hair: "#09090B" },
            { name: "Hiccup", movie: "How to Train Your Dragon", quote: "Dragons are our friends!", color: "#15803D", hair: "#B45309" },
            { name: "Light Fury", movie: "How to Train Your Dragon", quote: "Sparkling and fast!", color: "#F8FAFC", hair: "#E2E8F0" },
            { name: "Shrek", movie: "Shrek", quote: "Ogres are like onions!", color: "#65A30D", hair: "#4D7C0F" },
            { name: "Donkey", movie: "Shrek", quote: "And in the morning, I'm making waffles!", color: "#78716C", hair: "#44403C" },
            { name: "Puss in Boots", movie: "Puss in Boots: The Last Wish", quote: "Fear me, if you dare!", color: "#EA580C", hair: "#9A3412" },
            { name: "Kitty Softpaws", movie: "Puss in Boots", quote: "Fast paws!", color: "#27272A", hair: "#18181B" },
            { name: "Perro", movie: "Puss in Boots: The Last Wish", quote: "Best friends forever!", color: "#D97706", hair: "#B45309" },
            { name: "Minion Kevin", movie: "Despicable Me 4", quote: "Bello! Banana!", color: "#EAB308", hair: "#2563EB" },
            { name: "Minion Stuart", movie: "Despicable Me 4", quote: "Poopaye!", color: "#FACC15", hair: "#1D4ED8", glasses: true },
            { name: "Minion Bob", movie: "Minions", quote: "King Bob!", color: "#FDE047", hair: "#1E40AF" },
            { name: "Gru", movie: "Despicable Me 4", quote: "We are going to steal the moon!", color: "#475569", hair: "#1E293B" },
            { name: "Agnes", movie: "Despicable Me", quote: "It's so fluffy I'm gonna die!", color: "#DB2777", hair: "#0F172A" },
            { name: "Alex the Lion", movie: "Madagascar", quote: "Roar! New York City!", color: "#D97706", hair: "#92400E" },
            { name: "Marty the Zebra", movie: "Madagascar", quote: "Sugar honey iced tea!", color: "#F8FAFC", hair: "#09090B" },
            { name: "Skipper", movie: "Penguins of Madagascar", quote: "Smile and wave, boys!", color: "#0F172A", hair: "#F8FAFC" },
            { name: "Kowalski", movie: "Penguins of Madagascar", quote: "Options, sir!", color: "#1E293B", hair: "#E2E8F0" },
            { name: "Private", movie: "Penguins of Madagascar", quote: "Cute and cuddly!", color: "#334155", hair: "#F1F5F9" },
            { name: "Rico", movie: "Penguins of Madagascar", quote: "Kaboom?", color: "#0F172A", hair: "#EF4444" },
            { name: "Mario", movie: "The Super Mario Bros. Movie", quote: "It's-a me, Mario!", color: "#DC2626", hair: "#2563EB" },
            { name: "Luigi", movie: "The Super Mario Bros. Movie", quote: "Let's-a go, brother!", color: "#16A34A", hair: "#1E3A8A" },
            { name: "Princess Peach", movie: "The Super Mario Bros. Movie", quote: "Peaches peaches peaches!", color: "#EC4899", hair: "#FACC15" },
            { name: "Bowser", movie: "The Super Mario Bros. Movie", quote: "Peaches, I love you!", color: "#EA580C", hair: "#DC2626" },
            { name: "Toad", movie: "The Super Mario Bros. Movie", quote: "Adventure awaits!", color: "#2563EB", hair: "#EF4444" },
            { name: "Donkey Kong", movie: "The Super Mario Bros. Movie", quote: "Banana power!", color: "#78350F", hair: "#DC2626" },
            { name: "Sonic the Hedgehog", movie: "Sonic the Hedgehog 3", quote: "Gotta go fast!", color: "#2563EB", hair: "#1D4ED8" },
            { name: "Tails", movie: "Sonic the Hedgehog", quote: "I can fly with two tails!", color: "#F59E0B", hair: "#D97706" },
            { name: "Knuckles", movie: "Sonic the Hedgehog", quote: "Unstoppable punch!", color: "#DC2626", hair: "#991B1B" },
            { name: "Shadow", movie: "Sonic the Hedgehog 3", quote: "Ultimate life form!", color: "#18181B", hair: "#DC2626" },
            { name: "Garfield", movie: "The Garfield Movie", quote: "I love lasagna and sleep!", color: "#F97316", hair: "#C2410C" }
        ];

        /* Helper to generate dynamic SVG avatar for cartoon character */
        function generateCharacterSVG(char) {
            const hasGlasses = char.glasses ? `
                <circle cx="35" cy="45" r="12" fill="none" stroke="#FACC15" stroke-width="3"/>
                <circle cx="65" cy="45" r="12" fill="none" stroke="#FACC15" stroke-width="3"/>
                <line x1="47" y1="45" x2="53" y2="45" stroke="#FACC15" stroke-width="3"/>
            ` : '';

            return `
                <svg viewBox="0 0 100 100" class="w-full h-full drop-shadow-md">
                    <!-- Background aura -->
                    <circle cx="50" cy="50" r="45" fill="${char.color}" opacity="0.2" />
                    <!-- Body/Face Base -->
                    <circle cx="50" cy="52" r="34" fill="${char.color}" />
                    <!-- Hair/Top Feature -->
                    <path d="M 20 45 Q 50 10 80 45 Q 50 25 20 45 Z" fill="${char.hair}" />
                    <!-- Eyes -->
                    <circle cx="36" cy="48" r="6" fill="#FFFFFF" />
                    <circle cx="64" cy="48" r="6" fill="#FFFFFF" />
                    <circle cx="37" cy="48" r="3" fill="#1E1B4B" />
                    <circle cx="65" cy="48" r="3" fill="#1E1B4B" />
                    <circle cx="38" cy="46" r="1" fill="#FFFFFF" />
                    <circle cx="66" cy="46" r="1" fill="#FFFFFF" />
                    <!-- Glasses if present -->
                    ${hasGlasses}
                    <!-- Cheeks -->
                    <ellipse cx="28" cy="56" rx="4" ry="2" fill="#F43F5E" opacity="0.6"/>
                    <ellipse cx="72" cy="56" rx="4" ry="2" fill="#F43F5E" opacity="0.6"/>
                    <!-- Cute Smile -->
                    <path d="M 40 62 Q 50 72 60 62" fill="none" stroke="#1E1B4B" stroke-width="3" stroke-linecap="round" />
                    <path d="M 45 65 Q 50 70 55 65" fill="#F43F5E" />
                    <!-- Star Sparkle -->
                    <polygon points="80,20 82,25 87,25 83,28 85,33 80,30 75,33 77,28 73,25 78,25" fill="#FACC15"/>
                </svg>
            `;
        }

        /* ==========================================================================
           CURRICULUM QUESTION DATABASE (90 KSSR Year 3 Questions)
           ========================================================================== */
        const QUESTIONS_LEVEL_1 = [
            // Basic Statements, Wh- Questions, simple Adjectives, short sentences (4-5 words)
            { answer: "She is playing football.", jumbled: ["football.", "is", "playing", "She"] },
            { answer: "He has a red bicycle.", jumbled: ["bicycle.", "red", "has", "He", "a"] },
            { answer: "I like sweet ice cream.", jumbled: ["ice cream.", "I", "sweet", "like"] },
            { answer: "Where is my blue bag?", jumbled: ["bag?", "blue", "Where", "my", "is"] },
            { answer: "What is your name?", jumbled: ["is", "name?", "your", "What"] },
            { answer: "They are happy children.", jumbled: ["children.", "happy", "are", "They"] },
            { answer: "The cat is sleeping.", jumbled: ["sleeping.", "cat", "is", "The"] },
            { answer: "This hat is very big.", jumbled: ["big.", "hat", "very", "is", "This"] },
            { answer: "Who is that cute girl?", jumbled: ["that", "is", "girl?", "Who", "cute"] },
            { answer: "My brother is tall.", jumbled: ["tall.", "brother", "is", "My"] },
            { answer: "We have two books.", jumbled: ["books.", "two", "have", "We"] },
            { answer: "It is a sunny day.", jumbled: ["sunny", "a", "is", "It", "day."] },
            { answer: "She wears a pink dress.", jumbled: ["pink", "wears", "a", "dress.", "She"] },
            { answer: "When is your birthday?", jumbled: ["birthday?", "your", "is", "When"] },
            { answer: "The dog runs fast.", jumbled: ["fast.", "dog", "runs", "The"] },
            { answer: "I clean my bedroom.", jumbled: ["bedroom.", "clean", "my", "I"] },
            { answer: "There is a small bird.", jumbled: ["small", "a", "is", "There", "bird."] },
            { answer: "He likes hot soup.", jumbled: ["soup.", "hot", "likes", "He"] },
            { answer: "Where do you live?", jumbled: ["live?", "you", "do", "Where"] },
            { answer: "Look at the stars.", jumbled: ["the", "at", "Look", "stars."] },
            { answer: "She can jump high.", jumbled: ["high.", "jump", "can", "She"] },
            { answer: "My mother is cooking.", jumbled: ["cooking.", "is", "mother", "My"] },
            { answer: "The ball is round.", jumbled: ["round.", "is", "ball", "The"] },
            { answer: "What are you doing?", jumbled: ["doing?", "you", "are", "What"] },
            { answer: "We drink fresh water.", jumbled: ["water.", "fresh", "drink", "We"] },
            { answer: "It is seven o'clock.", jumbled: ["o'clock.", "seven", "is", "It"] },
            { answer: "The flowers are pretty.", jumbled: ["pretty.", "flowers", "are", "The"] },
            { answer: "He is my best friend.", jumbled: ["my", "is", "He", "friend.", "best"] },
            { answer: "I love my school.", jumbled: ["school.", "my", "love", "I"] },
            { answer: "Are you hungry now?", jumbled: ["now?", "hungry", "you", "Are"] }
        ];

        const QUESTIONS_LEVEL_2 = [
            // Modals (can/must), Frequency Adverbs (always/usually), Time/Place, Past simple, Questions (6-8 words)
            { answer: "You must wash your hands before eating.", jumbled: ["hands", "must", "eating.", "before", "You", "wash", "your"] },
            { answer: "I always brush my teeth in the morning.", jumbled: ["my", "the", "in", "I", "teeth", "morning.", "always", "brush"] },
            { answer: "She went to the clinic yesterday morning.", jumbled: ["yesterday", "went", "clinic", "She", "to", "the", "morning."] },
            { answer: "We usually play badminton in the park.", jumbled: ["badminton", "park.", "usually", "in", "play", "We", "the"] },
            { answer: "He can swim across the big pool.", jumbled: ["across", "big", "can", "swim", "pool.", "He", "the"] },
            { answer: "Did you see the colorful parrot yesterday?", jumbled: ["the", "Did", "yesterday?", "parrot", "see", "you", "colorful"] },
            { answer: "They were at the library last Sunday.", jumbled: ["the", "last", "were", "library", "They", "Sunday.", "at"] },
            { answer: "Students must listen quietly in the classroom.", jumbled: ["quietly", "the", "Students", "classroom.", "listen", "must", "in"] },
            { answer: "She sometimes helps her mother in kitchen.", jumbled: ["helps", "kitchen.", "sometimes", "in", "mother", "her", "She"] },
            { answer: "Was the English test difficult for you?", jumbled: ["difficult", "the", "you?", "test", "for", "English", "Was"] },
            { answer: "We visited our grandparents last weekend.", jumbled: ["grandparents", "last", "our", "visited", "We", "weekend."] },
            { answer: "He never forgets to do his homework.", jumbled: ["to", "never", "homework.", "forgets", "do", "his", "He"] },
            { answer: "Can you help me carry this box?", jumbled: ["carry", "me", "box?", "you", "this", "help", "Can"] },
            { answer: "The children played happily at the beach.", jumbled: ["happily", "at", "played", "children", "beach.", "The", "the"] },
            { answer: "I bought a new pencil box yesterday.", jumbled: ["yesterday.", "box", "a", "pencil", "bought", "I", "new"] },
            { answer: "She must wear her helmet while riding.", jumbled: ["wear", "must", "riding.", "while", "helmet", "her", "She"] },
            { answer: "They usually ride bicycles after school hours.", jumbled: ["bicycles", "after", "hours.", "school", "ride", "They", "usually"] },
            { answer: "Where did you buy that delicious cake?", jumbled: ["buy", "delicious", "you", "Where", "cake?", "that", "did"] },
            { answer: "We can draw funny pictures on paper.", jumbled: ["on", "pictures", "funny", "draw", "paper.", "can", "We"] },
            { answer: "My father was at work all day.", jumbled: ["work", "all", "My", "was", "father", "day.", "at"] },
            { answer: "You must not run inside the hallway.", jumbled: ["not", "inside", "run", "must", "hallway.", "You", "the"] },
            { answer: "She always wakes up early on Mondays.", jumbled: ["early", "She", "Mondays.", "always", "wakes", "on", "up"] },
            { answer: "Did they clean the school field together?", jumbled: ["clean", "Did", "field", "together?", "school", "they", "the"] },
            { answer: "He drank a glass of milk yesterday.", jumbled: ["milk", "yesterday.", "glass", "a", "drank", "He", "of"] },
            { answer: "We must protect the wild forest animals.", jumbled: ["wild", "protect", "animals.", "must", "forest", "We", "the"] },
            { answer: "She was happy with her test results.", jumbled: ["test", "She", "with", "results.", "happy", "was", "her"] },
            { answer: "Do you usually eat rice for lunch?", jumbled: ["eat", "Do", "lunch?", "rice", "usually", "for", "you"] },
            { answer: "He can speak English and Bahasa Melayu.", jumbled: ["English", "Bahasa", "can", "speak", "He", "and", "Melayu."] },
            { answer: "The monkey climbed up the tall tree.", jumbled: ["up", "tree.", "climbed", "monkey", "tall", "The", "the"] },
            { answer: "They were excited about the field trip.", jumbled: ["excited", "trip.", "field", "the", "were", "about", "They"] }
        ];

        const QUESTIONS_LEVEL_3 = [
            // Compound & Complex sentences (because, and, so, but), multiple adjectives, double clauses
            { answer: "She stayed at home because it was raining heavily.", jumbled: ["because", "home", "was", "stayed", "heavily.", "She", "raining", "it", "at"] },
            { answer: "I wanted to play outside but I was very tired.", jumbled: ["to", "I", "play", "was", "tired.", "outside", "wanted", "very", "but", "I"] },
            { answer: "He studied hard so he passed his English exam easily.", jumbled: ["he", "English", "studied", "passed", "so", "easily.", "hard", "He", "his", "exam"] },
            { answer: "The smart boy answered all questions and won the prize.", jumbled: ["boy", "smart", "and", "won", "all", "The", "answered", "questions", "the", "prize."] },
            { answer: "Although it was dark, we found the path safely.", jumbled: ["was", "found", "it", "dark,", "path", "we", "the", "safely.", "Although"] },
            { answer: "She likes eating fresh apples because they are very healthy.", jumbled: ["fresh", "healthy.", "apples", "are", "because", "eating", "they", "likes", "She", "very"] },
            { answer: "My cute little puppy loves running in the big garden.", jumbled: ["little", "running", "puppy", "garden.", "My", "in", "loves", "cute", "big", "the"] },
            { answer: "He washed his hands and ate his lunch happily.", jumbled: ["ate", "hands", "and", "washed", "happily.", "lunch", "his", "He", "his"] },
            { answer: "We could not go swimming because the water was cold.", jumbled: ["go", "water", "could", "swimming", "because", "cold.", "was", "We", "not", "the"] },
            { answer: "She woke up early so she was not late for school.", jumbled: ["so", "late", "up", "early", "she", "for", "woke", "not", "school.", "was", "She"] },
            { answer: "The friendly teacher helped us write a beautiful poem today.", jumbled: ["write", "helped", "friendly", "poem", "us", "teacher", "today.", "a", "beautiful", "The"] },
            { answer: "I like painting pictures and my brother enjoys playing music.", jumbled: ["pictures", "brother", "like", "painting", "my", "I", "and", "playing", "enjoys", "music."] },
            { answer: "He dropped his ice cream so he felt very sad.", jumbled: ["felt", "his", "cream", "ice", "dropped", "so", "he", "sad.", "He", "very"] },
            { answer: "She enjoys reading storybooks because they are full of adventure.", jumbled: ["they", "enjoys", "because", "reading", "adventure.", "full", "are", "of", "She", "storybooks"] },
            { answer: "The big yellow school bus arrived early this morning.", jumbled: ["yellow", "arrived", "school", "The", "bus", "early", "big", "this", "morning."] },
            { answer: "You should wear your coat because the wind is cold.", jumbled: ["cold.", "wear", "is", "coat", "because", "wind", "should", "your", "the", "You"] },
            { answer: "We cleaned the noisy classroom and washed the dirty whiteboard.", jumbled: ["dirty", "cleaned", "classroom", "noisy", "the", "and", "We", "whiteboard.", "washed", "the"] },
            { answer: "He missed the morning bus so he walked to school.", jumbled: ["the", "he", "bus", "to", "morning", "so", "walked", "missed", "He", "school."] },
            { answer: "My mother baked a delicious chocolate cake for my birthday.", jumbled: ["baked", "chocolate", "delicious", "cake", "My", "a", "mother", "birthday.", "my", "for"] },
            { answer: "She opened the large window because the room was hot.", jumbled: ["was", "the", "large", "opened", "window", "room", "because", "hot.", "She", "the"] },
            { answer: "They wanted to go to cinema but tickets were sold out.", jumbled: ["tickets", "wanted", "sold", "out.", "to", "go", "to", "cinema", "They", "were", "but"] },
            { answer: "The brave little boy rescued the small lost kitten.", jumbled: ["rescued", "boy", "little", "lost", "brave", "small", "kitten.", "the", "The"] },
            { answer: "I like wearing comfortable shoes when I walk in park.", jumbled: ["comfortable", "when", "in", "wearing", "shoes", "I", "walk", "park.", "like", "I"] },
            { answer: "He put on his raincoat because it started to rain.", jumbled: ["started", "raincoat", "his", "because", "rain.", "on", "it", "to", "put", "He"] },
            { answer: "We finished our homework early so we watched cartoon movie.", jumbled: ["early", "watched", "so", "our", "homework", "we", "finished", "cartoon", "movie.", "We"] },
            { answer: "The fluffy white rabbit hopped quickly across the green grass.", jumbled: ["hopped", "green", "white", "grass.", "rabbit", "quickly", "fluffy", "across", "The", "the"] },
            { answer: "She bought fresh red apples and sweet yellow bananas.", jumbled: ["yellow", "fresh", "bought", "apples", "red", "bananas.", "and", "sweet", "She"] },
            { answer: "He was hungry after playing so he ate two sandwiches.", jumbled: ["playing", "two", "hungry", "so", "sandwiches.", "he", "after", "was", "ate", "He"] },
            { answer: "The students were quiet because the principal was speaking.", jumbled: ["speaking.", "because", "principal", "were", "The", "students", "quiet", "the", "was"] },
            { answer: "I love learning English because it is fun and useful.", jumbled: ["learning", "useful.", "is", "English", "fun", "love", "because", "it", "and", "I"] }
        ];

        /* ==========================================================================
           GAME STATE & LOGIC
           ========================================================================== */
        let currentLevel = 1; // 1, 2, or 3
        let currentQIndex = 0; // 0 to 29
        let currentSelectedWords = [];
        let isPhoneView = false;

        // Progress Tracking (Saved in memory / optional localStorage)
        let harvestedData = {
            1: Array(30).fill(false),
            2: Array(30).fill(false),
            3: Array(30).fill(false)
        };

        // Initialize App
        window.addEventListener('DOMContentLoaded', () => {
            loadGameData();
            renderQuestion();
            updateGalleryCount();
        });

        function getLevelQuestions() {
            if (currentLevel === 1) return QUESTIONS_LEVEL_1;
            if (currentLevel === 2) return QUESTIONS_LEVEL_2;
            return QUESTIONS_LEVEL_3;
        }

        function getLevelCartoons() {
            if (currentLevel === 1) return CARTOONS_L1;
            if (currentLevel === 2) return CARTOONS_L2;
            return CARTOONS_L3;
        }

        function renderQuestion() {
            const questions = getLevelQuestions();
            const cartoons = getLevelCartoons();
            const q = questions[currentQIndex];
            const char = cartoons[currentQIndex];

            // Reset selection state
            currentSelectedWords = [];

            // Update UI Labels
            document.getElementById('currentQNum').innerText = currentQIndex + 1;
            document.getElementById('progressBar').style.width = `${((currentQIndex + 1) / 30) * 100}%`;

            // Update Level Badge
            const lBadge = document.getElementById('levelBadge');
            if (currentLevel === 1) {
                lBadge.innerText = 'Level 1: Easy';
                lBadge.className = 'px-3 py-1 rounded-full text-xs font-fredoka bg-gradient-to-r from-emerald-500 to-teal-600 text-white shadow-md uppercase tracking-wider';
            } else if (currentLevel === 2) {
                lBadge.innerText = 'Level 2: Medium';
                lBadge.className = 'px-3 py-1 rounded-full text-xs font-fredoka bg-gradient-to-r from-amber-500 to-orange-600 text-white shadow-md uppercase tracking-wider';
            } else {
                lBadge.innerText = 'Level 3: Challenging';
                lBadge.className = 'px-3 py-1 rounded-full text-xs font-fredoka bg-gradient-to-r from-pink-600 to-purple-600 text-white shadow-md uppercase tracking-wider';
            }

            // Update Character Card
            document.getElementById('charAvatarContainer').innerHTML = generateCharacterSVG(char);
            document.getElementById('charName').innerText = char.name;
            document.getElementById('charMovie').innerText = char.movie;
            document.getElementById('charHint').innerText = `"${char.quote}"`;

            const isHarvested = harvestedData[currentLevel][currentQIndex];
            document.getElementById('charHarvestStatus').innerHTML = isHarvested ? 
                `<i class="fa-solid fa-circle-check text-emerald-400"></i> Harvested` : 
                `<i class="fa-solid fa-wheat-awn"></i> Ready to Harvest`;

            // Render Jumbled Source Word Bank
            renderWordBank(q.jumbled);
            renderSelectedSentence();
        }

        function renderWordBank(words) {
            const sourceZone = document.getElementById('sourceZone');
            sourceZone.innerHTML = '';

            words.forEach((word, index) => {
                const button = document.createElement('button');
                button.className = 'word-tile px-3.5 py-2 rounded-xl bg-gradient-to-b from-indigo-500 to-indigo-700 hover:from-indigo-400 hover:to-indigo-600 border border-indigo-300/50 text-white font-bold text-sm sm:text-base cursor-pointer shadow-md transform hover:-translate-y-0.5 active:translate-y-1 transition';
                button.innerText = word;
                button.onclick = () => selectWord(word, button);
                sourceZone.appendChild(button);
            });
        }

        function selectWord(word, btnElement) {
            playSound('pop');
            currentSelectedWords.push(word);
            btnElement.disabled = true;
            btnElement.classList.add('opacity-30', 'scale-90', 'pointer-events-none');
            renderSelectedSentence();
        }

        function renderSelectedSentence() {
            const targetZone = document.getElementById('targetZone');
            const emptyHint = document.getElementById('emptyHint');
            const wordCountBadge = document.getElementById('wordCountBadge');

            // Clear tiles except emptyHint
            targetZone.querySelectorAll('.selected-tile').forEach(e => e.remove());

            if (currentSelectedWords.length === 0) {
                if (emptyHint) emptyHint.style.display = 'block';
                wordCountBadge.innerText = '0 words';
            } else {
                if (emptyHint) emptyHint.style.display = 'none';
                wordCountBadge.innerText = `${currentSelectedWords.length} words`;

                currentSelectedWords.forEach((word, index) => {
                    const tile = document.createElement('div');
                    tile.className = 'selected-tile word-tile px-3.5 py-2 rounded-xl bg-gradient-to-b from-amber-400 to-amber-600 border border-amber-200 text-indigo-950 font-bold text-sm sm:text-base flex items-center gap-1.5 cursor-pointer shadow-md animate-bounce-slow';
                    tile.innerHTML = `<span>${word}</span> <i class="fa-solid fa-xmark text-xs opacity-60"></i>`;
                    tile.onclick = () => removeSelectedWord(index);
                    targetZone.appendChild(tile);
                });
            }
        }

        function removeSelectedWord(index) {
            playSound('pop');
            const removedWord = currentSelectedWords.splice(index, 1)[0];
            
            // Re-enable in Source Bank
            const sourceButtons = Array.from(document.getElementById('sourceZone').children);
            for (let btn of sourceButtons) {
                if (btn.innerText === removedWord && btn.disabled) {
                    btn.disabled = false;
                    btn.classList.remove('opacity-30', 'scale-90', 'pointer-events-none');
                    break;
                }
            }
            renderSelectedSentence();
        }

        function undoLastWord() {
            if (currentSelectedWords.length > 0) {
                removeSelectedWord(currentSelectedWords.length - 1);
            }
        }

        function clearSentence() {
            if (currentSelectedWords.length === 0) return;
            playSound('pop');
            currentSelectedWords = [];
            const sourceButtons = Array.from(document.getElementById('sourceZone').children);
            sourceButtons.forEach(btn => {
                btn.disabled = false;
                btn.classList.remove('opacity-30', 'scale-90', 'pointer-events-none');
            });
            renderSelectedSentence();
        }

        function checkAnswer() {
            const questions = getLevelQuestions();
            const correctSentence = questions[currentQIndex].answer;
            const userSentence = currentSelectedWords.join(' ');

            if (userSentence === '') {
                showToast('Please select words to build a sentence first!', 'warning');
                playSound('wrong');
                return;
            }

            if (userSentence === correctSentence) {
                // CORRECT ANSWER!
                playSound('correct');
                harvestedData[currentLevel][currentQIndex] = true;
                saveGameData();
                updateGalleryCount();

                showToast('Awesome! Sentence correct! Character Harvested! 🌾', 'success');

                // Trigger confetti burst
                if (typeof confetti === 'function') {
                    confetti({ particleCount: 50, spread: 60, origin: { y: 0.7 } });
                }

                // Delay to next question or Victory
                setTimeout(() => {
                    if (currentQIndex < 29) {
                        currentQIndex++;
                        renderQuestion();
                    } else {
                        // Level Cleared Victory Celebration!
                        triggerLevelVictory();
                    }
                }, 1000);

            } else {
                // WRONG ANSWER
                playSound('wrong');
                showToast('Not quite right. Try arranging the words again!', 'error');
                
                // Shake target zone animation
                const targetZone = document.getElementById('targetZone');
                targetZone.classList.add('animate-bounce');
                setTimeout(() => targetZone.classList.remove('animate-bounce'), 600);
            }
        }

        /* ==========================================================================
           VICTORY & LEVEL CLEAR CELEBRATION
           ========================================================================== */
        function triggerLevelVictory() {
            playSound('fanfare');

            // Fire massive celebratory fireworks confetti
            if (typeof confetti === 'function') {
                confetti({ particleCount: 150, spread: 100, origin: { y: 0.5 } });
                setTimeout(() => confetti({ particleCount: 100, angle: 60, spread: 55, origin: { x: 0 } }), 300);
                setTimeout(() => confetti({ particleCount: 100, angle: 120, spread: 55, origin: { x: 1 } }), 600);
            }

            const modal = document.getElementById('victoryModal');
            const cartoons = getLevelCartoons();
            const starChar = cartoons[Math.floor(Math.random() * cartoons.length)];

            document.getElementById('victoryTitle').innerText = `LEVEL ${currentLevel} CLEARED!`;
            document.getElementById('victorySub').innerText = `Congratulations! You harvested all 30 Level ${currentLevel} Cartoon Characters!`;
            
            document.getElementById('victoryAvatar').innerHTML = generateCharacterSVG(starChar);
            document.getElementById('victoryCharName').innerText = starChar.name + ` (${starChar.movie})`;
            document.getElementById('victoryCharQuote').innerText = `"${starChar.quote}"`;

            const nextBtn = document.getElementById('victoryNextBtn');
            if (currentLevel < 3) {
                nextBtn.innerHTML = `CONTINUE TO LEVEL ${currentLevel + 1} <i class="fa-solid fa-arrow-right ml-1"></i>`;
            } else {
                nextBtn.innerHTML = `YOU WON THE ENTIRE GAME! PLAY AGAIN <i class="fa-solid fa-rotate mr-1"></i>`;
            }

            modal.classList.remove('hidden');
        }

        function nextLevelOrReset() {
            document.getElementById('victoryModal').classList.add('hidden');
            if (currentLevel < 3) {
                currentLevel++;
                currentQIndex = 0;
            } else {
                currentLevel = 1;
                currentQIndex = 0;
            }
            renderQuestion();
        }

        /* ==========================================================================
           HARVESTED CARTOON GALLERY MODAL
           ========================================================================== */
        let activeGalleryTab = 1;

        function openGallery() {
            playSound('pop');
            activeGalleryTab = currentLevel;
            renderGalleryGrid();
            document.getElementById('galleryModal').classList.remove('hidden');
        }

        function closeGallery() {
            document.getElementById('galleryModal').classList.add('hidden');
        }

        function switchGalleryTab(level) {
            playSound('pop');
            activeGalleryTab = level;
            renderGalleryGrid();
        }

        function renderGalleryGrid() {
            // Update Tab active styling
            for (let i = 1; i <= 3; i++) {
                const tab = document.getElementById(`tabL${i}`);
                const count = harvestedData[i].filter(Boolean).length;
                tab.innerText = `Level ${i} (${count}/30)`;
                if (i === activeGalleryTab) {
                    tab.className = 'flex-1 py-2 text-xs font-bold text-amber-300 border-b-2 border-amber-400 bg-indigo-800/40';
                } else {
                    tab.className = 'flex-1 py-2 text-xs font-bold text-indigo-400 hover:text-indigo-200';
                }
            }

            const grid = document.getElementById('galleryGrid');
            grid.innerHTML = '';

            let list = CARTOONS_L1;
            if (activeGalleryTab === 2) list = CARTOONS_L2;
            if (activeGalleryTab === 3) list = CARTOONS_L3;

            list.forEach((char, idx) => {
                const isUnlocked = harvestedData[activeGalleryTab][idx];
                const card = document.createElement('div');
                card.className = `p-2.5 rounded-2xl border ${isUnlocked ? 'bg-indigo-900/70 border-amber-400/60' : 'bg-indigo-950/40 border-indigo-800/60 opacity-50 grayscale'} flex flex-col items-center text-center relative overflow-hidden transition`;

                card.innerHTML = `
                    <div class="w-14 h-14 sm:w-16 sm:h-16 mb-1.5 bg-indigo-950/80 rounded-xl p-1 border border-indigo-700/50 flex items-center justify-center">
                        ${isUnlocked ? generateCharacterSVG(char) : '<i class="fa-solid fa-lock text-indigo-500 text-xl"></i>'}
                    </div>
                    <span class="text-[9px] font-bold text-pink-300 uppercase">${char.movie}</span>
                    <h4 class="font-fredoka text-xs text-yellow-300 truncate w-full mt-0.5">${char.name}</h4>
                    <span class="text-[9px] text-indigo-300 italic truncate w-full mt-0.5">${isUnlocked ? char.quote : 'Locked'}</span>
                `;
                grid.appendChild(card);
            });
        }

        function updateGalleryCount() {
            const total = harvestedData[1].filter(Boolean).length +
                          harvestedData[2].filter(Boolean).length +
                          harvestedData[3].filter(Boolean).length;
            document.getElementById('galleryCount').innerText = total;
        }

        /* ==========================================================================
           TEACHER DASHBOARD & CHEATS
           ========================================================================== */
        function openTeacherModal() {
            playSound('pop');
            document.getElementById('teacherModal').classList.remove('hidden');
        }

        function closeTeacherModal() {
            document.getElementById('teacherModal').classList.add('hidden');
        }

        function jumpToLevel(lvl) {
            currentLevel = lvl;
            currentQIndex = 0;
            renderQuestion();
            closeTeacherModal();
            showToast(`Jumped to Level ${lvl}`, 'info');
        }

        function jumpToQuestionInput() {
            const inputVal = parseInt(document.getElementById('qNumInput').value);
            if (inputVal >= 1 && inputVal <= 30) {
                currentQIndex = inputVal - 1;
                renderQuestion();
                closeTeacherModal();
                showToast(`Jumped to Question ${inputVal}`, 'info');
            } else {
                showToast('Please enter a question number between 1 and 30', 'warning');
            }
        }

        function unlockAllCharacters() {
            harvestedData[1] = Array(30).fill(true);
            harvestedData[2] = Array(30).fill(true);
            harvestedData[3] = Array(30).fill(true);
            saveGameData();
            updateGalleryCount();
            renderQuestion();
            closeTeacherModal();
            showToast('All 90 Cartoon Characters Unlocked!', 'success');
        }

        function resetGameProgress() {
            harvestedData[1] = Array(30).fill(false);
            harvestedData[2] = Array(30).fill(false);
            harvestedData[3] = Array(30).fill(false);
            currentLevel = 1;
            currentQIndex = 0;
            saveGameData();
            updateGalleryCount();
            renderQuestion();
            closeTeacherModal();
            showToast('All progress reset!', 'info');
        }

        /* ==========================================================================
           VIEWPORT MODE TOGGLE (Phone vs Desktop/Tablet)
           ========================================================================== */
        function toggleViewMode() {
            playSound('pop');
            isPhoneView = !isPhoneView;
            const container = document.getElementById('gameContainer');
            const viewIcon = document.getElementById('viewIcon');
            const viewText = document.getElementById('viewText');

            if (isPhoneView) {
                container.classList.add('phone-viewport');
                viewIcon.className = 'fa-solid fa-desktop text-amber-400 text-sm';
                viewText.innerText = 'Desktop View';
                showToast('Switched to Mobile Phone View', 'info');
            } else {
                container.classList.remove('phone-viewport');
                viewIcon.className = 'fa-solid fa-mobile-screen text-pink-400 text-sm';
                viewText.innerText = 'Phone View';
                showToast('Switched to Desktop / Fullscreen View', 'info');
            }
        }

        /* ==========================================================================
           PERSISTENCE & TOAST MESSAGES
           ========================================================================== */
        function saveGameData() {
            try {
                // In-memory or optional save
                sessionStorage.setItem('cartoon_harvester_data', JSON.stringify(harvestedData));
            } catch (e) {}
        }

        function loadGameData() {
            try {
                const data = sessionStorage.getItem('cartoon_harvester_data');
                if (data) {
                    harvestedData = JSON.parse(data);
                }
            } catch (e) {}
        }

        function showToast(message, type = 'info') {
            const toast = document.getElementById('feedbackToast');
            const icon = document.getElementById('feedbackIcon');
            const text = document.getElementById('feedbackText');

            text.innerText = message;

            if (type === 'success') {
                toast.className = 'fixed bottom-6 left-1/2 -translate-x-1/2 px-5 py-3 rounded-2xl font-bold text-sm shadow-2xl flex items-center gap-2.5 z-40 transition-all duration-300 opacity-100 pointer-events-auto bg-emerald-600 text-white border border-emerald-300';
                icon.className = 'fa-solid fa-circle-check text-yellow-300 text-xl';
            } else if (type === 'error') {
                toast.className = 'fixed bottom-6 left-1/2 -translate-x-1/2 px-5 py-3 rounded-2xl font-bold text-sm shadow-2xl flex items-center gap-2.5 z-40 transition-all duration-300 opacity-100 pointer-events-auto bg-rose-600 text-white border border-rose-300';
                icon.className = 'fa-solid fa-triangle-exclamation text-yellow-300 text-xl';
            } else if (type === 'warning') {
                toast.className = 'fixed bottom-6 left-1/2 -translate-x-1/2 px-5 py-3 rounded-2xl font-bold text-sm shadow-2xl flex items-center gap-2.5 z-40 transition-all duration-300 opacity-100 pointer-events-auto bg-amber-500 text-indigo-950 border border-amber-200';
                icon.className = 'fa-solid fa-circle-exclamation text-xl';
            } else {
                toast.className = 'fixed bottom-6 left-1/2 -translate-x-1/2 px-5 py-3 rounded-2xl font-bold text-sm shadow-2xl flex items-center gap-2.5 z-40 transition-all duration-300 opacity-100 pointer-events-auto bg-indigo-900 text-white border border-indigo-400';
                icon.className = 'fa-solid fa-circle-info text-pink-400 text-xl';
            }

            setTimeout(() => {
                toast.classList.add('opacity-0', 'pointer-events-none', 'translate-y-4');
                toast.classList.remove('opacity-100', 'translate-y-0');
            }, 2500);
        }
    </script>
</body>
</html>
