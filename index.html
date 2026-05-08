<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TEST PRO - Final User Build</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <script src="https://www.gstatic.com/firebasejs/10.8.1/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.8.1/firebase-database-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.8.1/firebase-auth-compat.js"></script>

    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap');
        .hidden { display: none !important; }
        .glass { background: rgba(255, 255, 255, 0.05); backdrop-filter: blur(20px); border: 1px solid rgba(255, 255, 255, 0.08); }
        .nav-btn { color: #64748b; transition: 0.3s; }
        .nav-active { color: #818cf8 !important; transform: translateY(-3px); }
        
        #splash-screen { transition: opacity 0.6s ease-out; z-index: 9999; }
        .loader-grow { animation: grow 3s forwards linear; width: 0%; }
        @keyframes grow { from { width: 0%; } to { width: 100%; } }
        
        /* NEW: MODERN TRAIN BANNER CSS */
        .modern-banner {
            background: linear-gradient(135deg, #4f46e5 0%, #1e1b4b 100%);
            position: relative;
            overflow: hidden;
            border-radius: 2rem;
            padding: 28px;
            box-shadow: 0 15px 35px rgba(30, 27, 75, 0.5);
            min-height: 160px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        .banner-pattern {
            position: absolute; inset: 0; opacity: 0.1;
            background-image: repeating-linear-gradient(45deg, #ffffff 0px, #ffffff 2px, transparent 2px, transparent 15px);
            z-index: 0;
        }
        .banner-train {
            position: absolute; right: -20px; bottom: 0; width: 180px; z-index: 10;
            filter: drop-shadow(-10px 10px 15px rgba(0,0,0,0.6));
        }
        .banner-glow {
            position: absolute; right: 20px; bottom: 20px; width: 100px; height: 100px;
            background: rgba(165, 180, 252, 0.4); filter: blur(30px); z-index: 1; border-radius: 50%;
        }
        .banner-btn {
            background: white; color: #1e1b4b; padding: 10px 24px; border-radius: 99px;
            font-weight: 900; font-size: 11px; width: fit-content; margin-top: 14px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3); transition: 0.2s; position: relative; z-index: 20;
            text-transform: capitalize;
        }
        .banner-btn:active { transform: scale(0.95); }

        .sub-card { height: 100px; border-radius: 1.8rem; display: flex; flex-direction: column; align-items: center; justify-content: center; border-bottom: 4px solid #6366f1; transition: transform 0.2s; cursor: pointer; }
        .sub-card:active { transform: scale(0.95); }
        
        .q-circle { width: 35px; height: 35px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 11px; font-weight: 900; border: 1px solid rgba(255,255,255,0.1); cursor: pointer; }
        .q-answered { background: #22c55e !important; border: none; color: white; }
        .q-marked { background: #8b5cf6 !important; border: none; color: white; }
        .q-current { border: 2px solid #818cf8; transform: scale(1.1); }
        #q-sidebar { transition: 0.4s cubic-bezier(0.4, 0, 0.2, 1); right: -100%; }
        #q-sidebar.open { right: 0; }

        body { background-color: #0b0e14; color: white; font-family: 'Inter', sans-serif; overflow-x: hidden; -webkit-tap-highlight-color: transparent; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .auth-input { background: rgba(255, 255, 255, 0.04) !important; border: 1px solid rgba(255, 255, 255, 0.1) !important; color: white !important; outline: none; padding: 20px 24px; border-radius: 24px; width: 100%; font-size: 16px; margin-bottom: 12px;}
        
        .p-tab-btn { padding: 12px 0; font-weight: 900; font-size: 8px; text-transform: uppercase; border-bottom: 2px solid transparent; flex: 1; text-align: center; color: #475569; }
        .p-tab-active { color: #818cf8; border-bottom-color: #818cf8; }
        .task-bar { height: 6px; background: rgba(255,255,255,0.05); border-radius: 10px; overflow: hidden; }
        .task-fill { height: 100%; background: #818cf8; transition: 0.5s; }
        
        .opt-btn { transition: all 0.2s; }
        .opt-btn:active { transform: scale(0.98); background: rgba(79, 70, 229, 0.5); }
    </style>
</head>
<body class="no-scrollbar">

    <!-- SPLASH SCREEN -->
    <div id="splash-screen" class="fixed inset-0 bg-[#0b0e14] flex flex-col items-center justify-center text-center">
        <div class="w-20 h-20 bg-indigo-600 rounded-[2.2rem] flex items-center justify-center shadow-2xl mb-6 animate-pulse"><i class="fas fa-bolt text-4xl text-white"></i></div>
        <h1 class="text-4xl font-black italic uppercase text-white tracking-tighter">TEST PRO</h1>
        <p class="text-[9px] font-bold text-indigo-400 tracking-[0.3em] mt-2 uppercase">Ready For The Battle</p>
        <div class="w-60 h-1 bg-white/5 rounded-full mt-16 overflow-hidden relative"><div class="h-full bg-indigo-500 loader-grow"></div></div>
        <div class="absolute bottom-10 opacity-60 text-[10px] font-black uppercase tracking-widest text-white text-center w-full">Powered By Anmol Yogi</div>
    </div>

    <!-- GLOBAL ALERT MODAL -->
    <div id="app-modal" class="hidden fixed inset-0 z-[8000] bg-black/90 backdrop-blur-md flex items-center justify-center p-6 text-center text-white">
        <div class="glass w-full max-w-sm rounded-[3rem] p-10 border border-indigo-500/30 transform transition-all scale-100">
            <div id="modal-icon" class="text-5xl mb-6 text-yellow-400"><i class="fas fa-info-circle"></i></div>
            <h3 id="modal-title" class="text-xl font-black uppercase italic mb-2 text-white">Notice</h3>
            <p id="modal-msg" class="text-slate-300 text-[12px] leading-relaxed font-bold mb-10"></p>
            <button onclick="closeAppModal()" class="w-full bg-indigo-600 py-4 rounded-2xl font-black text-[10px] uppercase shadow-xl text-white active:scale-95">Continue</button>
        </div>
    </div>

    <!-- MAIN APP WRAPPER -->
    <div id="main-app" class="hidden h-screen overflow-y-auto pb-24">
        <!-- HEADER -->
        <header class="p-5 flex justify-between items-center sticky top-0 bg-[#0b0e14]/95 backdrop-blur-md z-50 border-b border-white/5">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 rounded-xl bg-indigo-600 flex items-center justify-center shadow-lg"><i class="fas fa-user-astronaut text-sm text-white"></i></div>
                <div>
                    <h2 id="display-name" class="text-xs font-black uppercase text-white">PLAYER</h2>
                    <p class="text-[9px] text-green-400 font-bold uppercase mt-0.5 tracking-tighter" id="user-level">Beginner</p>
                </div>
            </div>
            <div class="glass px-3 py-1.5 rounded-xl flex items-center gap-2 border-yellow-500/20">
                <i class="fas fa-coins text-yellow-400 text-xs"></i><span id="user-coins" class="text-xs font-black text-white">0</span>
            </div>
        </header>

        <!-- HOME TAB -->
        <div id="tab-home" class="tab-content px-5 pt-4">
            
            <!-- NEW MODERN BANNER -->
            <div class="modern-banner mb-8">
                <div class="banner-pattern"></div>
                <div class="banner-glow"></div>
                
                <!-- Track Lines SVG -->
                <svg class="absolute right-0 bottom-0 w-48 h-full opacity-20 z-0" viewBox="0 0 200 100" preserveAspectRatio="none">
                    <path d="M40 100 L160 0 M70 100 L190 0 M100 100 L220 0" stroke="white" stroke-width="4" stroke-dasharray="10 5" fill="none"/>
                </svg>
                
                <!-- Bullet Train SVG -->
                <svg class="banner-train" viewBox="0 0 200 100" xmlns="http://www.w3.org/2000/svg">
                    <!-- Train Body (Sleek curve) -->
                    <path d="M 20 75 C 5 75, -5 60, 10 50 C 40 25, 100 15, 160 15 C 185 15, 195 30, 195 55 C 195 75, 180 80, 160 80 L 40 80 Z" fill="url(#trainGrad)"/>
                    <!-- Dark Window Area -->
                    <path d="M 40 60 C 25 60, 20 50, 30 42 C 55 28, 100 25, 145 25 C 155 25, 160 32, 160 45 C 160 58, 150 60, 140 60 L 40 60 Z" fill="#0b0e14"/>
                    <!-- Front Light Glow Effect -->
                    <circle cx="20" cy="65" r="4" fill="#ffffff" filter="blur(1px)"/>
                    <circle cx="20" cy="65" r="8" fill="rgba(255,255,255,0.4)" filter="blur(3px)"/>
                    
                    <defs>
                        <linearGradient id="trainGrad" x1="0%" y1="0%" x2="100%" y2="0%">
                            <stop offset="0%" stop-color="#e0e7ff" />
                            <stop offset="100%" stop-color="#818cf8" />
                        </linearGradient>
                    </defs>
                </svg>

                <div class="relative z-20 w-2/3">
                    <h3 id="ban-title" class="text-3xl font-black italic text-white tracking-tight leading-none mb-1">FJN</h3>
                    <p id="ban-subtitle" class="text-[10px] text-indigo-200 font-bold uppercase tracking-widest mb-2">Daily Dose Test</p>
                    <button onclick="playBannerQuiz()" class="banner-btn">Start Quiz</button>
                </div>
            </div>

            <h3 class="text-[10px] font-black text-slate-500 uppercase tracking-[0.2em] mb-4 ml-1">Practice Subjects</h3>
            <div id="subjects-grid" class="grid grid-cols-2 gap-3 mb-10 text-white"></div>
        </div>

        <!-- BATTLE TAB -->
        <div id="tab-battle" class="tab-content hidden px-5 pt-4 text-white">
            <h2 class="text-xl font-black italic uppercase tracking-tighter mb-6">Battle Lobbies</h2>
            <div id="contests-list" class="flex flex-col gap-4"></div>
        </div>

        <!-- NEWS TAB -->
        <div id="tab-news" class="tab-content hidden px-5 pt-4 text-white">
            <h2 class="text-xl font-black italic uppercase mb-6">Updates & GK</h2>
            <div id="news-list" class="flex flex-col gap-3"></div>
        </div>

        <!-- PROFILE TAB -->
        <div id="tab-profile" class="tab-content hidden px-5 pt-10 text-white">
            <div class="flex flex-col items-center mb-8 text-center relative">
                <div class="w-20 h-20 rounded-[2rem] bg-indigo-600 flex items-center justify-center text-3xl mb-3 shadow-2xl mx-auto"><i class="fas fa-user-ninja"></i></div>
                <h2 id="profile-name" class="text-xl font-black uppercase italic tracking-tighter">USERNAME</h2>
                
                <div class="flex gap-2 mt-3">
                    <button onclick="openEditProfile()" class="text-[9px] text-indigo-400 font-bold bg-indigo-500/10 px-4 py-2 rounded-full border border-indigo-500/20 active:scale-95"><i class="fas fa-pencil-alt mr-1"></i> Edit Profile</button>
                    <!-- NEW: ABOUT APP BUTTON -->
                    <button onclick="openAboutApp()" class="text-[9px] text-yellow-400 font-bold bg-yellow-500/10 px-4 py-2 rounded-full border border-yellow-500/20 active:scale-95"><i class="fas fa-info-circle mr-1"></i> About App</button>
                </div>
            </div>
            
            <div class="grid grid-cols-3 gap-2 mb-8 text-center">
                <div class="glass p-3 rounded-2xl border-b-2 border-indigo-600"><div id="p-wins" class="text-lg font-black italic">0</div><p class="text-[6px] text-slate-500 font-black uppercase">Tests Won</p></div>
                <div class="glass p-3 rounded-2xl border-b-2 border-yellow-600"><div id="p-coins" class="text-lg font-black italic">0</div><p class="text-[6px] text-slate-500 font-black uppercase">Coins</p></div>
                <div onclick="switchProfileTab('mistakes')" class="glass p-3 rounded-2xl border-b-2 border-red-500 active:scale-95 cursor-pointer"><div id="p-mistakes" class="text-lg font-black text-red-500">0</div><p class="text-[6px] text-slate-500 font-black uppercase">Mistakes</p></div>
            </div>
            
            <div class="flex border-b border-white/5 mb-6 overflow-x-auto no-scrollbar">
                <button onclick="switchProfileTab('missions')" id="p-btn-missions" class="p-tab-btn p-tab-active">Missions</button>
                <button onclick="switchProfileTab('history')" id="p-btn-history" class="p-tab-btn">History</button>
                <button onclick="switchProfileTab('mistakes')" id="p-btn-mistakes" class="p-tab-btn">Mistakes</button>
                <button onclick="switchProfileTab('starred')" id="p-btn-starred" class="p-tab-btn">Saved</button>
                <button onclick="switchProfileTab('world')" id="p-btn-world" class="p-tab-btn">Ranks</button>
            </div>
            
            <div id="p-section-missions" class="space-y-4 pb-6">
                <div class="glass p-5 rounded-[2.5rem] border-indigo-500/20 bg-indigo-600/5 mb-4 text-white"><p class="text-[9px] font-black text-indigo-400 uppercase tracking-widest mb-1">Refer & Earn</p><div class="flex items-center justify-between"><span id="my-refer-code" class="font-black text-white tracking-widest text-lg uppercase">CODE</span><button onclick="shareApp()" class="text-indigo-400 text-xl active:scale-90"><i class="fas fa-share-alt"></i></button></div></div>
                <div id="task-container" class="space-y-2"></div>
                <button onclick="logout()" class="w-full p-4 border border-red-500/10 text-red-500 rounded-2xl font-black text-[9px] uppercase mt-10 active:scale-95">Logout Account</button>
            </div>
            <div id="p-section-history" class="hidden space-y-2 pb-6"></div>
            <div id="p-section-mistakes" class="hidden space-y-3 pb-6"></div>
            <div id="p-section-starred" class="hidden space-y-3 pb-6"></div>
            <div id="p-section-world" class="hidden space-y-2 pb-6 text-white"></div>
        </div>
    </div>

    <!-- TEST ARENA (GAMEPLAY) -->
    <div id="game-arena" class="hidden fixed inset-0 z-[4000] bg-[#0b0e14] flex flex-col">
        <header class="p-4 bg-slate-900/50 flex items-center justify-between border-b border-white/5">
            <div class="flex flex-col text-white"><div id="game-timer" class="text-base font-black text-yellow-500">00:00</div><p class="text-[7px] text-slate-500 font-black">TOTAL TIME</p></div>
            <div class="flex flex-col items-center text-white"><div id="q-timer" class="text-xs font-black">00:00</div><p class="text-[7px] text-slate-500 font-black">THIS QUESTION</p></div>
            <div class="flex gap-2">
                <button onclick="saveCurrentQuestion()" class="w-9 h-9 glass rounded-xl flex items-center justify-center text-yellow-400 active:scale-90"><i class="fas fa-star text-xs"></i></button>
                <button onclick="toggleSidebar()" class="w-9 h-9 bg-indigo-600 rounded-xl flex items-center justify-center text-white active:scale-90"><i class="fas fa-th-large text-xs"></i></button>
            </div>
        </header>
        <div class="px-4 py-2 flex justify-between bg-white/5 border-b border-white/5 text-[8px] font-black uppercase text-white">
            <div><span class="text-green-500">+1.0 Marks</span> <span class="text-red-500 ml-2">-0.33 Marks</span></div>
            <div class="text-indigo-400" id="q-number-display">Question 1</div>
        </div>
        <main class="flex-1 p-6 flex flex-col overflow-y-auto">
            <h2 id="q-box" class="text-[17px] font-bold mb-8 leading-snug text-white"></h2>
            <div id="opts-grid" class="flex flex-col gap-3"></div>
        </main>
        <footer class="p-4 bg-slate-900 grid grid-cols-3 gap-2">
            <button onclick="markForReview()" class="glass py-4 rounded-xl font-black text-[9px] uppercase text-indigo-400 active:scale-95">Mark</button>
            <button onclick="clearSelection()" class="glass py-4 rounded-xl font-black text-[9px] uppercase text-slate-500 active:scale-95">Clear</button>
            <button onclick="saveAndNext()" class="bg-indigo-600 py-4 rounded-xl font-black text-[9px] uppercase text-white active:scale-95">Next</button>
        </footer>
        
        <div id="q-sidebar" class="fixed top-0 bottom-0 w-4/5 max-w-xs bg-[#0f172a] z-[4100] p-6 flex flex-col text-white shadow-2xl">
            <div class="flex justify-between items-center mb-8"><h3 class="font-black text-sm uppercase">Grid Map</h3><button onclick="toggleSidebar()"><i class="fas fa-times text-xl"></i></button></div>
            <div class="flex gap-2 mb-4 text-[8px] uppercase text-slate-400 font-bold justify-around">
                <span class="text-green-500"><i class="fas fa-circle"></i> Answered</span>
                <span class="text-purple-500"><i class="fas fa-circle"></i> Marked</span>
            </div>
            <div id="palette-grid" class="flex-1 grid grid-cols-4 gap-3 overflow-y-auto content-start"></div>
            <button onclick="confirmSubmit()" class="w-full bg-red-600 py-4 rounded-2xl font-black text-xs uppercase mt-6 active:scale-95 shadow-lg shadow-red-600/30">Submit Test</button>
        </div>
    </div>

    <!-- RESULT & REPORT ARENA -->
    <div id="report-arena" class="hidden fixed inset-0 z-[5500] bg-[#0b0e14] flex flex-col overflow-y-auto p-8 text-center text-white">
        <h2 class="text-2xl font-black italic mb-6">TEST ANALYSIS</h2>
        <div class="flex justify-center mb-6"><div id="stat-circle" class="w-32 h-32 rounded-full flex items-center justify-center p-2"><div class="w-full h-full bg-[#0b0e14] rounded-full flex items-center justify-center relative z-10 font-black text-3xl" id="final-acc">0%</div></div></div>
        <div class="grid grid-cols-2 gap-3 mb-8 text-center">
            <div class="glass p-4 rounded-2xl border-b-2 border-indigo-500"><p class="text-[9px] text-slate-400 uppercase font-bold">Total Score</p><p class="text-2xl font-black text-indigo-400 mt-1" id="rep-final">0</p></div>
            <div class="glass p-4 rounded-2xl border-b-2 border-yellow-500"><p class="text-[9px] text-slate-400 uppercase font-bold">Time Taken</p><p class="text-2xl font-black text-yellow-500 mt-1" id="rep-total-time">0m</p></div>
        </div>
        <h3 class="text-left text-xs font-black uppercase mb-3 text-slate-400">Question Timeline</h3>
        <div id="analysis-list" class="text-left flex flex-col gap-3 mb-10"></div>
        <button onclick="document.getElementById('report-arena').classList.add('hidden')" class="bg-indigo-600 py-4 rounded-2xl font-black text-sm uppercase shadow-xl shadow-indigo-600/30 w-full mb-4">Close Report</button>
    </div>

    <!-- AUTHENTICATION SCREEN -->
    <div id="auth-screen" class="hidden fixed inset-0 z-[2000] bg-[#0b0e14] flex flex-col p-8 overflow-y-auto text-center text-white">
        <div class="mt-20 mb-12">
            <h2 id="auth-title" class="text-4xl font-black italic uppercase">ACCESS PRO</h2>
            <p class="text-slate-400 text-xs mt-2 font-bold">Login to continue your journey</p>
        </div>
        <div class="space-y-4">
            <div id="name-field" class="hidden"><input type="text" id="user-name" placeholder="Full Name" class="auth-input"></div>
            <input type="email" id="user-email" placeholder="Email Address" class="auth-input">
            <input type="password" id="user-pass" placeholder="Password" class="auth-input">
        </div>
        <button onclick="handleAuth()" class="w-full bg-indigo-600 py-5 rounded-[2.5rem] font-black text-sm uppercase shadow-xl shadow-indigo-600/20 mt-10 text-white active:scale-95" id="auth-btn-text">Login</button>
        <p class="text-center mt-12 text-[11px] text-slate-400 font-bold uppercase" id="auth-toggle-text">Don't have an account? <button onclick="toggleAuthMode()" class="text-indigo-400 font-black ml-1 border-b border-indigo-400 pb-0.5">Sign Up Here</button></p>
    </div>

    <!-- BOTTOM NAVIGATION -->
    <nav class="fixed bottom-0 left-0 right-0 h-20 bg-[#0f172a] border-t border-white/5 flex items-center justify-around z-50 rounded-t-[2.5rem] shadow-[0_-10px_40px_rgba(0,0,0,0.5)]">
        <button onclick="switchTab('tab-home')" id="nav-home" class="nav-btn flex flex-col items-center gap-1 nav-active"><i class="fas fa-house-chimney text-lg mb-1"></i><span class="text-[8px] font-black uppercase">Home</span></button>
        <button onclick="switchTab('tab-battle')" id="nav-battle" class="nav-btn flex flex-col items-center gap-1"><i class="fas fa-fire text-lg mb-1"></i><span class="text-[8px] font-black uppercase">Battle</span></button>
        <button onclick="switchTab('tab-news')" id="nav-news" class="nav-btn flex flex-col items-center gap-1"><i class="fas fa-newspaper text-lg mb-1"></i><span class="text-[8px] font-black uppercase">News</span></button>
        <button onclick="switchTab('tab-profile')" id="nav-profile" class="nav-btn flex flex-col items-center gap-1"><i class="fas fa-circle-user text-lg mb-1"></i><span class="text-[8px] font-black uppercase">Profile</span></button>
    </nav>

    <!-- OVERLAYS (Tests List, News, Edit Profile) -->
    <div id="test-overlay" class="hidden fixed inset-0 z-[400] bg-[#0b0e14] flex flex-col p-6 overflow-y-auto text-white">
        <div class="flex items-center mb-8 gap-4">
            <button onclick="closeOverlay('test-overlay')" class="w-10 h-10 glass rounded-full flex items-center justify-center text-white active:scale-90"><i class="fas fa-arrow-left"></i></button>
            <h2 class="text-lg font-black uppercase italic" id="overlay-subject-title">Tests</h2>
        </div>
        <div id="test-btns-box" class="flex flex-col gap-4 text-white"></div>
    </div>
    
    <div id="news-overlay" class="hidden fixed inset-0 z-[450] bg-[#0b0e14] flex flex-col p-8 overflow-y-auto text-white">
        <button onclick="closeOverlay('news-overlay')" class="w-10 h-10 glass rounded-full mb-8 flex items-center justify-center text-white active:scale-90"><i class="fas fa-arrow-left"></i></button>
        <h1 id="news-full-title" class="text-2xl font-black italic mb-6 uppercase text-indigo-400"></h1>
        <div id="news-full-desc" class="text-slate-300 leading-relaxed text-sm whitespace-pre-wrap pb-20"></div>
    </div>

    <!-- EDIT PROFILE MODAL -->
    <div id="edit-profile-modal" class="hidden fixed inset-0 z-[9000] bg-black/90 backdrop-blur-md flex items-center justify-center p-6 text-white">
        <div class="glass w-full max-w-sm rounded-[3rem] p-8 border border-white/10 shadow-2xl">
            <div class="text-4xl text-center mb-4 text-indigo-400"><i class="fas fa-user-edit"></i></div>
            <h3 class="text-lg font-black uppercase italic text-center mb-6">Update Profile</h3>
            <input type="text" id="edit-name" placeholder="Full Name" class="auth-input !mb-3">
            <input type="password" id="edit-pass" placeholder="New Password (Leave blank to keep same)" class="auth-input !mb-6">
            <button onclick="saveProfile()" class="w-full bg-indigo-600 py-4 rounded-2xl font-black text-xs uppercase shadow-xl mb-3 active:scale-95">Save Changes</button>
            <button onclick="closeOverlay('edit-profile-modal')" class="w-full glass py-4 rounded-2xl font-black text-xs uppercase text-slate-400 active:scale-95">Cancel</button>
        </div>
    </div>

    <!-- NEW: ABOUT APP MODAL -->
    <div id="about-app-modal" class="hidden fixed inset-0 z-[9000] bg-black/90 backdrop-blur-md flex flex-col items-center justify-center p-6 text-white">
        <div class="glass w-full max-w-sm rounded-[3rem] p-8 border border-indigo-500/30 shadow-2xl text-center relative overflow-hidden">
            <!-- Decorative background element -->
            <div class="absolute -top-10 -right-10 w-32 h-32 bg-indigo-600/20 rounded-full blur-2xl"></div>
            
            <div class="w-20 h-20 bg-indigo-600 rounded-[2rem] flex items-center justify-center shadow-2xl mx-auto mb-4 relative z-10"><i class="fas fa-bolt text-4xl text-white"></i></div>
            <h2 class="text-3xl font-black italic uppercase tracking-tighter mb-1 relative z-10">TEST PRO</h2>
            <p class="text-[10px] text-indigo-400 font-bold tracking-widest mb-6 relative z-10">Version 1.0.0</p>
            
            <div class="text-xs text-slate-300 font-bold leading-relaxed mb-8 relative z-10 bg-black/20 p-4 rounded-2xl">
                Ultimate mock test platform for serious aspirants. Experience real-time live battles, premium test series, detailed analysis, and earn coins to unlock advanced features.
            </div>
            
            <div class="text-[9px] font-black uppercase tracking-widest text-slate-500 mb-6 relative z-10">
                Created & Powered By<br>
                <span class="text-white text-base tracking-normal italic mt-1 block">Anmol Yogi</span>
            </div>
            
            <button onclick="closeOverlay('about-app-modal')" class="w-full bg-indigo-600 py-4 rounded-2xl font-black text-xs uppercase shadow-xl active:scale-95 relative z-10">Close</button>
        </div>
    </div>

    <!-- JAVASCRIPT -->
    <script>
        // NOTE: Please secure these keys from Firebase Console later
        const firebaseConfig = {
          apiKey: "AIzaSyCHkjvsVwRZwKs6Fup-WarqYOyyIE0FzOQ",
          authDomain: "my-app-94006.firebaseapp.com",
          databaseURL: "https://my-app-94006-default-rtdb.firebaseio.com",
          projectId: "my-app-94006",
          storageBucket: "my-app-94006.appspot.com",
          messagingSenderId: "752915121988",
          appId: "1:752915121988:web:1ea1432a7c17311b407911",
          measurementId: "G-7VPX13R6BQ"
        };
        firebase.initializeApp(firebaseConfig);
        const db = firebase.database(), auth = firebase.auth();

        let currentUser = null, currentTestName = 'Test', globalTimerInterval = null, qTimerInterval = null, shareMessageTemplate = "";
        let gS = { idx: 0, qs: [], answers: {}, status: [], timeSpent: [], qSec: 0, totalSec: 0 };
        const todayKey = new Date().toISOString().split('T')[0];

        // 1. AUTHENTICATION & INITIALIZATION
        auth.onAuthStateChanged(user => {
            if (user) {
                currentUser = user;
                document.getElementById('auth-screen').classList.add('hidden');
                document.getElementById('main-app').classList.remove('hidden');
                setTimeout(() => { document.getElementById('splash-screen').classList.add('hidden'); }, 2000);
                initAllData(user.uid);
                checkDailyBonus(user.uid);
            } else {
                setTimeout(() => { document.getElementById('splash-screen').classList.add('hidden'); document.getElementById('auth-screen').classList.remove('hidden'); }, 2000);
            }
        });

        let isSignUpMode = false;
        function toggleAuthMode() {
            isSignUpMode = !isSignUpMode;
            document.getElementById('name-field').classList.toggle('hidden');
            document.getElementById('auth-title').innerText = isSignUpMode ? "CREATE ACCOUNT" : "ACCESS PRO";
            document.getElementById('auth-btn-text').innerText = isSignUpMode ? "Sign Up" : "Login";
            document.getElementById('auth-toggle-text').innerHTML = isSignUpMode 
                ? `Already have an account? <button onclick="toggleAuthMode()" class="text-indigo-400 font-black ml-1 border-b border-indigo-400 pb-0.5">Login Here</button>` 
                : `Don't have an account? <button onclick="toggleAuthMode()" class="text-indigo-400 font-black ml-1 border-b border-indigo-400 pb-0.5">Sign Up Here</button>`;
        }

        function handleAuth() { 
            const em = document.getElementById('user-email').value, ps = document.getElementById('user-pass').value, nm = document.getElementById('user-name').value; 
            if(!em || !ps) return showAppAlert("Error", "Please fill email and password.", "fa-exclamation-triangle text-red-500"); 
            document.getElementById('auth-btn-text').innerText = "Processing...";
            if(isSignUpMode){ 
                if(!nm) { document.getElementById('auth-btn-text').innerText = "Sign Up"; return showAppAlert("Error", "Please enter your name.", "fa-user text-red-500"); }
                auth.createUserWithEmailAndPassword(em,ps).then(r=>{ 
                    db.ref('users/'+r.user.uid).set({name:nm, email:em, coins:50, wins:0}); 
                }).catch(e=> { showAppAlert("Signup Failed", e.message, "fa-times text-red-500"); document.getElementById('auth-btn-text').innerText = "Sign Up"; }); 
            } else { 
                auth.signInWithEmailAndPassword(em,ps).catch(e=> { showAppAlert("Login Failed", e.message, "fa-lock text-red-500"); document.getElementById('auth-btn-text').innerText = "Login"; }); 
            } 
        }

        function logout() { auth.signOut().then(() => location.reload()); }

        function initAllData(uid) {
            loadUserData(uid); loadSubjects(); loadNews(); loadBattleContests();
            loadDailyMissions(uid); loadHistory(uid); loadStarred(uid); loadMistakes(uid); loadRanking();
            loadAdminShareMsg();
            document.getElementById('my-refer-code').innerText = uid.substring(0, 6).toUpperCase();
        }

        // 2. DATA LOADING & SMART ICONS
        function loadUserData(uid) { 
            db.ref('users/'+uid).on('value', s => { 
                const d = s.val(); 
                if(d){ 
                    document.getElementById('display-name').innerText=d.name || "Player"; 
                    document.getElementById('profile-name').innerText=d.name || "Player"; 
                    document.getElementById('user-coins').innerText=d.coins || 0; 
                    document.getElementById('p-wins').innerText=d.wins || 0; 
                    document.getElementById('p-coins').innerText=d.coins || 0; 
                    let level = "Rookie";
                    if(d.wins > 5) level = "Amateur";
                    if(d.wins > 20) level = "Pro";
                    if(d.wins > 50) level = "Legend";
                    document.getElementById('user-level').innerText = level;
                } 
            }); 
            db.ref('mistake_bank/'+uid).on('value', s => { const p = document.getElementById('p-mistakes'); if(p) p.innerText = s.numChildren() || 0; }); 
        }

        // EDIT PROFILE FUNCTIONS
        function openEditProfile() {
            document.getElementById('edit-name').value = document.getElementById('profile-name').innerText;
            document.getElementById('edit-pass').value = '';
            document.getElementById('edit-profile-modal').classList.remove('hidden');
        }

        function saveProfile() {
            const newName = document.getElementById('edit-name').value.trim();
            const newPass = document.getElementById('edit-pass').value.trim();
            if(!newName) return showAppAlert("Error", "Name cannot be empty", "fa-exclamation-circle text-red-400");
            
            db.ref(`users/${currentUser.uid}/name`).set(newName);
            
            if(newPass.length > 0) {
                if(newPass.length < 6) return showAppAlert("Error", "Password must be at least 6 characters", "fa-lock text-red-400");
                currentUser.updatePassword(newPass).then(() => {
                    showAppAlert("Success", "Profile & Password Updated!", "fa-check-circle text-green-400");
                    closeOverlay('edit-profile-modal');
                }).catch(e => {
                    if(e.code === 'auth/requires-recent-login') showAppAlert("Security Requirement", "Please logout and login again to change password.", "fa-shield-alt text-yellow-400");
                    else showAppAlert("Error", e.message, "fa-times-circle text-red-400");
                });
            } else {
                showAppAlert("Success", "Profile Name Updated!", "fa-check-circle text-green-400");
                closeOverlay('edit-profile-modal');
            }
        }

        // NEW: ABOUT APP Modal Control
        function openAboutApp() {
            document.getElementById('about-app-modal').classList.remove('hidden');
        }

        function getSmartIcon(subjectName) {
            let name = subjectName.toLowerCase();
            if(name.includes('math') || name.includes('quant') || name.includes('ganit') || name.includes('reason') || name.includes('logic')) return 'fa-calculator text-blue-400';
            if(name.includes('sci') || name.includes('phys') || name.includes('chem') || name.includes('bio') || name.includes('vigyan')) return 'fa-flask text-green-400';
            if(name.includes('hist') || name.includes('itihaas')) return 'fa-landmark text-yellow-500';
            if(name.includes('geo') || name.includes('bhugol')) return 'fa-globe-americas text-teal-400';
            if(name.includes('eng') || name.includes('hindi') || name.includes('lang') || name.includes('vyakaran')) return 'fa-language text-pink-400';
            if(name.includes('gk') || name.includes('general') || name.includes('current')) return 'fa-lightbulb text-yellow-300';
            if(name.includes('comp') || name.includes('tech')) return 'fa-laptop-code text-indigo-400';
            if(name.includes('pol') || name.includes('civics') || name.includes('samvidhan')) return 'fa-scale-balanced text-orange-400';
            return 'fa-book-open text-white'; 
        }

        function loadSubjects() {
            db.ref('subjects').on('value', snap => {
                const grid = document.getElementById('subjects-grid'); if(!grid) return; grid.innerHTML = '';
                if(!snap.exists()) { grid.innerHTML = `<p class="col-span-2 text-center text-xs text-slate-500 py-4">No subjects added yet.</p>`; return; }
                snap.forEach(sub => {
                    const d = sub.val();
                    const iconClass = d.icon || getSmartIcon(d.name); 
                    grid.innerHTML += `<div onclick="loadTests('${sub.key}', '${d.name}')" class="glass sub-card p-4 text-center" style="border-bottom: 4px solid ${d.color || '#6366f1'}"><i class="fas ${iconClass} mb-3 text-2xl drop-shadow-lg"></i><div class="font-black text-[10px] uppercase text-white tracking-wide">${d.name}</div></div>`;
                });
            });
        }

        function loadTests(id, name) { 
            currentTestName = name; 
            document.getElementById('overlay-subject-title').innerText = name;
            db.ref('tests/'+id).once('value', s => { 
                const box = document.getElementById('test-btns-box'); box.innerHTML = ''; 
                if(!s.exists()) { box.innerHTML = `<p class="text-center text-xs text-slate-500 py-10">No tests available right now.</p>`; return; }
                
                let testsArr = [];
                s.forEach(t => { if(t.val() && t.val().name) testsArr.push(t.val()); });
                
                testsArr.reverse().forEach(t => { 
                    const qsLen = t.questions ? t.questions.length : 0;
                    const qData = JSON.stringify(t.questions || []).replace(/'/g, "&#39;"); 
                    
                    const feeValue = t.fee || 0;
                    const feeUI = feeValue > 0 ? `<span class="bg-yellow-500/20 text-yellow-400 px-2 py-0.5 rounded ml-2 font-black border border-yellow-500/30"><i class="fas fa-lock text-[8px]"></i> ${feeValue} 🪙</span>` : `<span class="bg-green-500/10 text-green-400 px-1.5 py-0.5 rounded ml-2 font-black text-[8px]">FREE</span>`;
                    
                    box.innerHTML += `<button onclick='attemptStartTest(${qData}, ${t.duration||10}, "${t.name}", ${feeValue})' class="glass p-5 rounded-3xl flex justify-between items-center w-full mb-3 text-white active:scale-95 transition-transform"><div class="text-left"><div class="font-black text-sm uppercase text-white flex items-center">${t.name} ${feeUI}</div><p class="text-[9px] text-indigo-400 font-black mt-2 uppercase">${t.duration||10} MINS • ${qsLen} Qs</p></div><div class="w-10 h-10 bg-indigo-600 rounded-full flex items-center justify-center"><i class="fas fa-play text-white"></i></div></button>`; 
                }); 
            }); 
            document.getElementById('test-overlay').classList.remove('hidden'); 
        }

        function loadNews() { 
            db.ref('news_feed').on('value', snap => { 
                const list = document.getElementById('news-list'); if(!list) return; list.innerHTML = ''; 
                if(!snap.exists()) { list.innerHTML = `<p class="text-center text-xs text-slate-500 py-4">No latest news.</p>`; return; }
                let newsArr = []; snap.forEach(n => { if(n.val() && n.val().title) newsArr.push(n.val()); });
                newsArr.reverse().forEach(d => { 
                    const div = document.createElement('div'); div.className = "glass p-4 rounded-2xl mb-2 flex justify-between items-center active:scale-95 transition-transform cursor-pointer border-l-4 border-indigo-500"; div.innerHTML = `<div class="text-[12px] font-bold w-[90%] text-white leading-snug">${d.title}</div><i class="fas fa-chevron-right text-slate-500 text-xs"></i>`; div.onclick = () => { document.getElementById('news-full-title').innerText = d.title; document.getElementById('news-full-desc').innerText = d.desc; document.getElementById('news-overlay').classList.remove('hidden'); }; list.appendChild(div); 
                }); 
            }); 
        }

        function loadBattleContests() {
            db.ref('contests').on('value', s => {
                const list = document.getElementById('contests-list'); if(!list) return; list.innerHTML = '';
                if(!s.exists()) { list.innerHTML = '<div class="glass p-8 rounded-3xl text-center"><i class="fas fa-ghost text-4xl text-slate-600 mb-3"></i><p class="text-xs text-slate-400 font-bold uppercase">No Live Battles</p></div>'; return; }
                let battlesArr = []; s.forEach(c => { if(c.val() && c.val().name) battlesArr.push(c.val()); });
                battlesArr.reverse().forEach(d => {
                    const totalQs = d.questions ? d.questions.length : 0;
                    const qData = JSON.stringify(d.questions || []).replace(/'/g, "&#39;");
                    list.innerHTML += `<div class="glass p-6 rounded-3xl mb-3 text-white border border-indigo-500/30 relative overflow-hidden">
                        <div class="absolute top-0 right-0 bg-red-500 text-[8px] font-black px-3 py-1 rounded-bl-xl uppercase animate-pulse">LIVE</div>
                        <div class="mb-4 mt-2">
                            <h3 class="text-lg font-black italic uppercase text-white">${d.name}</h3>
                            <p class="text-[10px] font-black text-indigo-400 uppercase mt-1"><i class="far fa-clock"></i> ${d.duration || 10} MINS</p>
                        </div>
                        <div class="flex justify-between items-center">
                            <p class="text-xl font-black text-yellow-400">${totalQs} <span class="text-[9px] text-slate-400 uppercase">Qs</span></p>
                            <button onclick='attemptStartTest(${qData}, ${d.duration||10}, "${d.name}", 0)' class="bg-indigo-600 px-8 py-3 rounded-xl font-black text-[11px] uppercase shadow-lg shadow-indigo-600/40 text-white active:scale-95">Join Battle</button>
                        </div>
                    </div>`;
                });
            });
        }

        // 3. QUIZ ENGINE & ENTRY FEE GATEWAY
        function attemptStartTest(qs, dur, name, fee) {
            if(fee > 0) {
                db.ref(`users/${currentUser.uid}/coins`).once('value', s => {
                    let currentCoins = s.val() || 0;
                    if(currentCoins >= fee) {
                        if(confirm(`This is a Premium Test.\nPay ${fee} Coins to unlock?`)) {
                            db.ref(`users/${currentUser.uid}/coins`).set(currentCoins - fee).then(() => {
                                showAppAlert("Unlocked!", `Paid ${fee} coins. Good luck!`, "fa-unlock text-green-400");
                                startGame(qs, dur, name);
                            });
                        }
                    } else {
                        showAppAlert("Insufficient Coins", `You need ${fee} coins to unlock this test. Play free tests to earn coins!`, "fa-coins text-yellow-400");
                    }
                });
            } else { startGame(qs, dur, name); }
        }

        function startGame(qs, dur, name) {
            if(!qs || qs.length === 0) return showAppAlert("Oops", "No questions in this test.", "fa-info-circle text-yellow-400");
            currentTestName = name;
            gS = { idx:0, qs, answers:{}, status:new Array(qs.length).fill('unseen'), timeSpent:new Array(qs.length).fill(0), qSec:0, totalSec:0 };
            document.getElementById('game-arena').classList.remove('hidden'); 
            document.getElementById('test-overlay').classList.add('hidden');
            loadQ(); startTimers(dur); updatePalette();
        }

        function loadQ() {
            const q = gS.qs[gS.idx]; document.getElementById('q-box').innerText = q.q;
            document.getElementById('q-number-display').innerText = `Question ${gS.idx + 1} of ${gS.qs.length}`;
            const grid = document.getElementById('opts-grid'); grid.innerHTML = '';
            
            q.o.forEach((o, index) => {
                const isSelected = gS.answers[gS.idx] === o;
                const b = document.createElement('button'); 
                b.className = `glass opt-btn p-4 rounded-2xl text-left font-bold text-sm text-white flex items-center gap-3 ${isSelected ? 'bg-indigo-600 border-indigo-400' : ''}`;
                const alpha = ['A', 'B', 'C', 'D'][index] || '-';
                b.innerHTML = `<span class="w-6 h-6 rounded-full flex items-center justify-center text-[10px] font-black ${isSelected?'bg-white text-indigo-600':'bg-white/10 text-slate-400'}">${alpha}</span> <span class="flex-1">${o}</span>`;
                b.onclick = () => { gS.answers[gS.idx] = o; gS.status[gS.idx] = 'answered'; loadQ(); updatePalette(); };
                grid.appendChild(b);
            });
            gS.qSec = 0;
        }

        function startTimers(totalMins) {
            let totalS = totalMins * 60;
            if(globalTimerInterval) clearInterval(globalTimerInterval); if(qTimerInterval) clearInterval(qTimerInterval);
            globalTimerInterval = setInterval(() => {
                if(totalS <= 0) { confirmSubmit(true); return; }
                let m = Math.floor(totalS/60), s = totalS%60;
                document.getElementById('game-timer').innerText = `${m.toString().padStart(2,'0')}:${s.toString().padStart(2,'0')}`;
                totalS--; gS.totalSec++;
            }, 1000);
            qTimerInterval = setInterval(() => { 
                gS.qSec++; gS.timeSpent[gS.idx]++; 
                let m=Math.floor(gS.qSec/60), s=gS.qSec%60; 
                document.getElementById('q-timer').innerText = `${m.toString().padStart(2,'0')}:${s.toString().padStart(2,'0')}`; 
            }, 1000);
        }

        function clearSelection() { delete gS.answers[gS.idx]; gS.status[gS.idx] = 'unseen'; loadQ(); updatePalette(); }
        function markForReview() { gS.status[gS.idx] = 'marked'; updatePalette(); saveAndNext(); }
        function saveAndNext() { if(gS.idx < gS.qs.length - 1) { gS.idx++; loadQ(); updatePalette(); } else { showAppAlert("End of Test", "Check grid to review or Submit.", "fa-flag-checkered text-indigo-500"); toggleSidebar(); } }
        function updatePalette() { 
            const grid = document.getElementById('palette-grid'); if(!grid) return; grid.innerHTML = ''; 
            gS.qs.forEach((_, i) => { 
                const div = document.createElement('div'); div.className = `q-circle ${gS.status[i] === 'answered' ? 'q-answered' : gS.status[i] === 'marked' ? 'q-marked' : ''} ${gS.idx === i ? 'q-current' : ''}`; div.innerText = i + 1; 
                div.onclick = () => { gS.idx = i; loadQ(); if(window.innerWidth < 768) toggleSidebar(); }; 
                grid.appendChild(div); 
            }); 
        }
        function toggleSidebar() { document.getElementById('q-sidebar').classList.toggle('open'); }

        function confirmSubmit(auto = false) {
            if(auto || confirm("Are you sure you want to submit the test?")) {
                if(globalTimerInterval) clearInterval(globalTimerInterval); if(qTimerInterval) clearInterval(qTimerInterval);
                document.getElementById('game-arena').classList.add('hidden'); document.getElementById('q-sidebar').classList.remove('open');
                showFinalReport(gS);
            }
        }

        function showFinalReport(s) {
            document.getElementById('report-arena').classList.remove('hidden');
            let gained = 0, neg = 0, correctCount = 0; let list = document.getElementById('analysis-list'); list.innerHTML = '';
            
            s.qs.forEach((q, i) => {
                const ans = s.answers[i]; const isCorrect = ans === q.a;
                let statusText = "Unattempted", statusColor = "text-slate-400 border-slate-700";
                if(ans) { 
                    if(isCorrect) { gained += 1; correctCount++; statusText = "Correct"; statusColor = "text-green-500 border-green-500/50"; } 
                    else { neg += 0.33; db.ref(`mistake_bank/${currentUser.uid}`).push({ q: q.q, cor: q.a, wrongAns: ans }); statusText = "Wrong"; statusColor = "text-red-500 border-red-500/50"; } 
                }
                list.innerHTML += `<div class="glass p-4 rounded-2xl flex flex-col gap-2 text-white border border-t-0 border-r-0 border-b-0 border-l-4 ${statusColor}">
                    <div class="flex justify-between items-center w-full"><span class="text-[10px] font-black uppercase ${statusColor.split(' ')[0]}">${statusText}</span><span class="text-[9px] font-bold text-slate-400"><i class="far fa-clock"></i> ${s.timeSpent[i]}s</span></div>
                    <p class="text-[11px] font-bold mt-1">${q.q}</p>
                    ${!isCorrect && ans ? `<p class="text-[10px] text-green-400 font-bold bg-green-500/10 p-2 rounded-lg mt-1">Ans: ${q.a}</p>` : ''}
                </div>`;
            });
            
            const net = (gained - neg).toFixed(2); const acc = s.qs.length > 0 ? Math.round((correctCount / s.qs.length) * 100) : 0;
            document.getElementById('final-acc').innerText = acc + "%"; document.getElementById('rep-final').innerText = net;
            document.getElementById('rep-total-time').innerText = Math.floor(s.totalSec/60) + "m " + (s.totalSec%60) + "s";
            document.getElementById('stat-circle').style.background = `conic-gradient(#22c55e 0deg ${acc*3.6}deg, #ef4444 0deg 360deg)`;
            
            db.ref(`user_tasks/${currentUser.uid}/${todayKey}/count`).transaction(c => (c || 0) + 1);
            db.ref(`user_tasks/${currentUser.uid}/${todayKey}/correct`).transaction(c => (c || 0) + correctCount);
            
            const historyLog = { testName: currentTestName, acc, score: net, totalSec: s.totalSec, date: new Date().toLocaleString(), logs: s.qs.map((q,idx)=>({q:q.q, a:q.a, userAns:s.answers[idx], status:s.answers[idx]===q.a?'correct':s.answers[idx]?'wrong':'unseen', timeSpent:s.timeSpent[idx]})) };
            db.ref('user_history/'+currentUser.uid).push(historyLog);
            if(acc >= 80) db.ref('users/'+currentUser.uid+'/wins').transaction(w => (w||0)+1);
        }

        // 4. PROFILE, TASKS, HISTORY & LEADERBOARD
        function loadDailyMissions(uid) {
            db.ref(`user_tasks/${uid}/${todayKey}`).on('value', snap => {
                const d = snap.val()||{count:0, correct:0, claimed:[]}; const list = document.getElementById('task-container'); if(!list) return;
                const tasks = [ { id: 1, t: 'Starter', goal: 2, cur: d.count||0, unit: 'Tests', rew: 10 }, { id: 2, t: 'Challenger', goal: 5, cur: d.count||0, unit: 'Tests', rew: 30 }, { id: 3, t: 'Quick Shot', goal: 5, cur: d.correct||0, unit: 'Correct', rew: 15 }, { id: 4, t: 'Sniper', goal: 20, cur: d.correct||0, unit: 'Correct', rew: 50 } ];
                list.innerHTML = '';
                tasks.forEach(task => {
                    const pr = Math.min((task.cur/task.goal)*100, 100); const isClaimed = d.claimed && d.claimed.includes(task.id); const canClaim = task.cur >= task.goal && !isClaimed;
                    list.innerHTML += `<div class="glass p-4 rounded-2xl flex justify-between items-center text-white mb-2"><div class="w-[65%]"><p class="text-[10px] font-black uppercase">${task.t} <span class="text-[8px] text-slate-400">(${task.cur}/${task.goal} ${task.unit})</span></p><div class="task-bar mt-2"><div class="task-fill" style="width: ${pr}%"></div></div></div><button onclick="claimTask(${task.id}, ${task.rew})" ${!canClaim?'disabled':''} class="px-3 py-2 rounded-xl text-[9px] font-black uppercase ${isClaimed?'bg-green-500/10 text-green-500 border border-green-500/30':'bg-indigo-600 shadow-lg text-white '+(!canClaim?'opacity-30':'animate-pulse active:scale-90')}">${isClaimed?'Done':task.rew+' 🪙'}</button></div>`;
                });
            });
        }
        function claimTask(id, rew) { db.ref(`users/${currentUser.uid}/coins`).transaction(c => (c||0) + rew); db.ref(`user_tasks/${currentUser.uid}/${todayKey}/claimed`).transaction(cl => { if(!cl) cl = []; cl.push(id); return cl; }); showAppAlert("Mission Passed!", `You received ${rew} Coins!`, "fa-gift text-yellow-400"); }
        
        function loadHistory(uid) { 
            db.ref('user_history/'+uid).limitToLast(15).on('value', s => { 
                const list = document.getElementById('p-section-history'); if(!list) return; list.innerHTML = ''; 
                if(!s.exists()) { list.innerHTML = `<p class="text-center text-xs text-slate-500 py-6">No test history found.</p>`; return; } 
                let arr = []; s.forEach(h => arr.push(h.val())); 
                arr.reverse().forEach(v => { 
                    const card = document.createElement('div'); card.className = `glass p-5 rounded-3xl border-l-4 ${v.acc>=80?'border-green-500':'border-indigo-600'} mb-2 flex justify-between items-center cursor-pointer active:scale-95 transition-transform`;
                    card.innerHTML = `<div><div class="text-[11px] font-black uppercase text-white">${v.testName}</div><div class="text-[8px] text-slate-400 mt-1">${v.date}</div></div><div class="text-right"><div class="text-sm font-black text-white">${v.score} <span class="text-[8px] text-slate-500">Pts</span></div><div class="text-[9px] font-black ${v.acc>=80?'text-green-400':'text-indigo-400'}">${v.acc}% ACC</div></div>`;
                    card.onclick = () => {
                        document.getElementById('report-arena').classList.remove('hidden'); document.getElementById('final-acc').innerText = v.acc + "%"; document.getElementById('rep-final').innerText = v.score; document.getElementById('rep-total-time').innerText = Math.floor((v.totalSec||0)/60) + "m " + ((v.totalSec||0)%60) + "s"; document.getElementById('stat-circle').style.background = `conic-gradient(#22c55e 0deg ${v.acc*3.6}deg, #ef4444 0deg 360deg)`;
                        let aList = document.getElementById('analysis-list'); aList.innerHTML = '';
                        if(v.logs) { v.logs.forEach((l, i) => { let statusText = "Unattempted", statusColor = "text-slate-400 border-slate-700"; if(l.status === 'correct') { statusText = "Correct"; statusColor = "text-green-500 border-green-500/50"; } else if(l.status === 'wrong') { statusText = "Wrong"; statusColor = "text-red-500 border-red-500/50"; } aList.innerHTML += `<div class="glass p-4 rounded-2xl flex flex-col gap-2 text-white border border-t-0 border-r-0 border-b-0 border-l-4 ${statusColor}"><div class="flex justify-between items-center w-full"><span class="text-[10px] font-black uppercase ${statusColor.split(' ')[0]}">${statusText}</span><span class="text-[9px] font-bold text-slate-400"><i class="far fa-clock"></i> ${l.timeSpent||0}s</span></div><p class="text-[11px] font-bold mt-1">${l.q}</p>${l.status === 'wrong' ? `<p class="text-[10px] text-green-400 font-bold bg-green-500/10 p-2 rounded-lg mt-1">Ans: ${l.a}</p>` : ''}</div>`; }); } 
                        else { aList.innerHTML = `<p class="text-xs text-slate-500 text-center py-4">Detailed analysis not available for this legacy test.</p>`; }
                    }; list.appendChild(card);
                }); 
            }); 
        }
        
        function loadMistakes(uid) { db.ref(`mistake_bank/${uid}`).limitToLast(20).on('value', s => { const list = document.getElementById('p-section-mistakes'); if(!list) return; list.innerHTML = ''; if(!s.exists()) { list.innerHTML = `<p class="text-center text-xs text-slate-500 py-6">Great! No mistakes recorded yet.</p>`; return; } let arr = []; s.forEach(m => arr.push({...m.val(), key: m.key})); arr.reverse().forEach(m => { list.innerHTML += `<div class="glass p-5 rounded-3xl relative text-white mb-2 border border-red-500/20"><div class="text-[11px] font-bold text-white pr-6">${m.q}</div><div class="mt-3 flex gap-2 flex-wrap"><span class="text-[8px] font-black px-2 py-1 bg-red-500/20 text-red-400 rounded-lg">Your Ans: ${m.wrongAns || '-'}</span><span class="text-[8px] font-black px-2 py-1 bg-green-500/20 text-green-400 rounded-lg">Correct: ${m.cor}</span></div><button onclick="db.ref('mistake_bank/${currentUser.uid}/${m.key}').remove()" class="absolute top-4 right-4 text-slate-500 hover:text-red-500"><i class="fas fa-trash"></i></button></div>`; }); }); }
        function loadStarred(uid) { db.ref(`saved_questions/${uid}`).on('value', s => { const list = document.getElementById('p-section-starred'); if(!list) return; list.innerHTML = ''; if(!s.exists()) { list.innerHTML = `<p class="text-center text-xs text-slate-500 py-6">No saved questions.</p>`; return; } s.forEach(m => { list.innerHTML += `<div class="glass p-5 rounded-3xl relative text-white mb-2 border border-yellow-500/20"><div class="text-[11px] font-bold text-white pr-6">${m.val().q}</div><div class="text-[9px] text-green-400 bg-green-500/10 inline-block px-2 py-1 rounded-lg font-black mt-3">Ans: ${m.val().cor}</div><button onclick="db.ref('saved_questions/${currentUser.uid}/${m.key}').remove()" class="absolute top-4 right-4 text-yellow-500/50 hover:text-yellow-500"><i class="fas fa-star"></i></button></div>`; }); }); }
        
        function loadRanking() { 
            db.ref('users').on('value', s => { 
                const list = document.getElementById('p-section-world'); if(!list) return; list.innerHTML = ''; 
                if(!s.exists()) { list.innerHTML = `<p class="text-center text-xs text-slate-500 py-6">No ranked players yet.</p>`; return;}
                let rs = []; s.forEach(u => { let val = u.val(); if(val && val.name) rs.push({ name: val.name, wins: val.wins || 0, uid: u.key }); }); 
                rs.sort((a, b) => b.wins - a.wins);
                rs.slice(0, 20).forEach((u, i) => { 
                    const isMe = (currentUser && currentUser.uid === u.uid); const clr = i===0?'text-yellow-400 text-lg':i===1?'text-slate-300 text-base':i===2?'text-orange-400 text-sm':'text-white text-xs'; const meBorder = isMe ? 'border-2 border-indigo-500 bg-indigo-900/30' : 'border border-white/10';
                    list.innerHTML += `<div class="glass p-4 rounded-2xl flex justify-between items-center text-white mb-2 ${meBorder}"><div class="flex items-center gap-3"><span class="font-black w-6 text-center ${clr}">#${i+1}</span><div class="font-bold text-[11px] uppercase">${u.name} ${isMe ? '<span class="text-indigo-400 text-[8px] ml-1">(YOU)</span>' : ''}</div></div><div class="text-[9px] font-black bg-white/5 px-3 py-1.5 rounded-lg">${u.wins} WINS</div></div>`; 
                }); 
            }); 
        }

        // 5. UTILS 
        function switchTab(t) { document.querySelectorAll('.tab-content').forEach(x => x.classList.add('hidden')); document.getElementById(t).classList.remove('hidden'); document.querySelectorAll('.nav-btn').forEach(btn => btn.classList.toggle('nav-active', btn.id === 'nav-' + t.split('-')[1])); window.scrollTo(0,0); }
        function switchProfileTab(t) { ['missions','history','mistakes','starred','world'].forEach(id => { const s = document.getElementById('p-section-'+id); const b = document.getElementById('p-btn-'+id); if(s) s.classList.toggle('hidden', id !== t); if(b) b.classList.toggle('p-tab-active', id === t); }); }
        function showAppAlert(title, msg, iconClass) { document.getElementById('modal-title').innerText = title; document.getElementById('modal-msg').innerText = msg; if(iconClass) document.getElementById('modal-icon').innerHTML=`<i class="fas ${iconClass}"></i>`; document.getElementById('app-modal').classList.remove('hidden'); }
        function closeAppModal() { document.getElementById('app-modal').classList.add('hidden'); }
        function closeOverlay(id) { document.getElementById(id).classList.add('hidden'); }
        function saveCurrentQuestion() { const q = gS.qs[gS.idx]; if(currentUser && q) { db.ref(`saved_questions/${currentUser.uid}`).push({ q: q.q, cor: q.a }); showAppAlert("Saved to Vault!", "Question saved in your profile.", "fa-star text-yellow-400"); } }
        
        db.ref('daily_dose').on('value', snap => { const d = snap.val(); if(d) { document.getElementById('ban-title').innerText = d.title; document.getElementById('ban-subtitle').innerText = (d.duration || 10) + " Mins Special"; window.banQs = d.questions || []; window.banDur = d.duration || 10; } });
        function playBannerQuiz() { if(window.banQs && window.banQs.length > 0) attemptStartTest(window.banQs, window.banDur, "Daily Dose", 0); else showAppAlert("Info", "Today's dose is coming soon!", "fa-clock text-indigo-400"); }
        function checkDailyBonus(uid) { db.ref(`users/${uid}/last_reward`).once('value', s => { if(s.val() !== todayKey){ setTimeout(() => { showAppAlert("Daily Login Bonus", "+10 Coins added to your wallet!", "fa-gift text-yellow-400"); }, 3000); db.ref(`users/${uid}/coins`).transaction(c=>(c||0)+10); db.ref(`users/${uid}/last_reward`).set(todayKey); } }); }
        function loadAdminShareMsg() { db.ref('admin_settings/share_msg').on('value', s => { shareMessageTemplate = s.val() || "Play Battles on TEST PRO! Use my referral code: [CODE]"; }); }
        function shareApp() { const c = currentUser.uid.substring(0, 6).toUpperCase(); const msg = shareMessageTemplate.replace("[CODE]", c); if(navigator.share) navigator.share({title:'TEST PRO', text: msg}); else window.open(`https://api.whatsapp.com/send?text=${encodeURIComponent(msg)}`); }
    </script>
</body>
</html>
