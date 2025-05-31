<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Arcade Mania: Game Seru Penuh Warna!</title>
<style>
  /* --- Reset & Base Styles --- */
  body {
    margin: 0; padding: 0; font-family: 'Press Start 2P', cursive, 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: #0d0d1a; /* Darker, deep blue/purple background */
    color: #e0e0ff; /* Soft white/light blue text */
    display: flex; flex-direction: column; align-items: center;
    min-height: 100vh;
    overflow-x: hidden;
    position: relative; /* For rain and general positioning */
  }

  /* --- Header --- */
  header {
    width: 100%;
    padding: 1.5rem 1rem;
    text-align: center;
    background: linear-gradient(90deg, #ff007f, #00ffff, #ff00ff); /* Brighter, more vibrant rainbow */
    background-size: 600% 600%;
    animation: rainbowHeader 15s ease infinite; /* Slower, smoother rainbow animation */
    color: #fff;
    font-size: 3rem; /* Larger font size */
    font-weight: 700;
    text-shadow: 0 0 15px rgba(255, 255, 255, 0.7); /* Stronger white glow */
    border-bottom: 5px solid #00ffff; /* Cyberpunk border */
    position: relative;
    z-index: 10;
    box-shadow: 0 5px 20px rgba(0, 255, 255, 0.5);
  }
  @keyframes rainbowHeader {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
  }

  /* --- Main Content Area --- */
  main {
    width: 100%; max-width: 960px; /* Slightly wider main content */
    padding: 2rem 1rem;
    flex-grow: 1;
    position: relative;
    z-index: 5;
  }

  /* --- Game Sections --- */
  section.game-section {
    margin-bottom: 3.5rem; /* More space between sections */
    border: 3px solid #6a05ad; /* Purple border */
    border-radius: 15px; /* More rounded corners */
    padding: 1.5rem;
    background: rgba(18, 18, 36, 0.8); /* Slightly transparent dark background */
    box-shadow: 0 0 25px rgba(106, 5, 173, 0.6); /* Purple glow */
    backdrop-filter: blur(5px); /* Subtle blur effect */
  }
  h2 {
    margin-top: 0;
    text-align: center;
    color: #00ffff; /* Cyan color */
    text-shadow: 0 0 10px #00ffff, 0 0 20px rgba(0, 255, 255, 0.5); /* Stronger cyan glow */
    margin-bottom: 1.5rem;
    font-size: 2rem;
  }
  .rules {
    font-size: 1rem;
    color: #b0b0ff; /* Lighter text for rules */
    margin-bottom: 1.5rem;
    padding: 0 1rem;
    line-height: 1.5;
  }
  .game-container {
    text-align: center;
  }

  /* --- Buttons --- */
  button {
    cursor: pointer;
    font-family: 'Press Start 2P', cursive;
    font-size: 1rem;
    padding: 0.8rem 1.5rem; /* Larger padding */
    border: none;
    border-radius: 8px;
    margin: 0.7rem;
    background: linear-gradient(45deg, #007bff, #00c0ff); /* Blueish gradient */
    color: #0d0d1a; /* Dark text on buttons */
    font-weight: 600;
    box-shadow: 0 0 15px rgba(0, 192, 255, 0.7); /* Blue glow */
    transition: all 0.3s ease-in-out; /* Smoother transition */
    text-transform: uppercase;
  }
  button:hover {
    background: linear-gradient(45deg, #00c0ff, #007bff);
    color: #fff; /* White text on hover */
    transform: translateY(-3px); /* Subtle lift effect */
    box-shadow: 0 5px 20px rgba(0, 192, 255, 0.9);
  }
  button:active {
      transform: translateY(0);
      box-shadow: 0 0 10px rgba(0, 192, 255, 0.5);
  }
  button:disabled {
      opacity: 0.6;
      cursor: not-allowed;
      box-shadow: none;
      transform: none;
  }


  /* --- Saweria Button --- */
  #saweria {
    margin-top: 4rem;
    text-align: center;
  }
  #saweria a {
    display: inline-block;
    background: linear-gradient(45deg, #f39c12, #f1c40f); /* Orange/yellow gradient */
    color: #2c3e50; /* Darker text */
    font-weight: 700;
    padding: 1rem 2.5rem; /* Larger padding */
    border-radius: 25px; /* More rounded */
    text-decoration: none;
    box-shadow: 0 0 20px #f1c40f; /* Stronger glow */
    font-size: 1.5rem; /* Larger font */
    transition: background 0.4s ease, transform 0.3s ease;
    text-transform: uppercase;
    font-family: 'Press Start 2P', cursive;
  }
  #saweria a:hover {
    background: linear-gradient(45deg, #f1c40f, #f39c12);
    transform: scale(1.05); /* Slight zoom effect */
  }

  /* --- Marquee Text --- */
  .marquee {
    width: 100%;
    overflow: hidden;
    white-space: nowrap;
    box-sizing: border-box;
    animation: marquee 15s linear infinite; /* Slower marquee */
    color: #ff00ff; /* Magenta color */
    text-shadow: 0 0 10px #ff00ff; /* Magenta glow */
    font-weight: 700;
    margin-bottom: 2rem;
    padding: 0.8rem 0;
    background-color: rgba(255, 0, 255, 0.1); /* Transparent magenta background */
    position: relative;
    z-index: 6;
    font-size: 1.1rem;
    border-top: 2px dashed #ff00ff;
    border-bottom: 2px dashed #ff00ff;
  }
  @keyframes marquee {
    0%    {transform: translateX(100%);}
    100% {transform: translateX(-100%);}
  }

  /* --- Game Output Display --- */
  .game-output {
    margin: 1.5rem auto 0 auto;
    max-width: 400px; /* Wider output area */
    min-height: 100px; /* Taller output area */
    padding: 1rem 1.5rem;
    border-radius: 10px;
    background: #0a0a1a; /* Very dark background */
    color: #00ffff; /* Cyan text */
    font-family: 'Press Start 2P', cursive;
    font-size: 1.1rem;
    box-shadow: inset 0 0 15px #00ffff; /* Stronger cyan glow inset */
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    white-space: normal; /* Allow text wrapping */
    word-break: break-word; /* Break long words */
  }

  /* --- Input Tebak Angka --- */
  #taInput {
      padding: 0.7rem;
      border-radius: 8px;
      border: 2px solid #00ffff; /* Cyan border */
      background-color: #0a0a1a; /* Dark background */
      color: #00ffff; /* Cyan text */
      font-size: 1.1rem;
      text-align: center;
      margin-right: 0.8rem;
      font-family: 'Press Start 2P', cursive;
  }
  #taInput:focus {
      outline: none;
      box-shadow: 0 0 12px #00ffff; /* Stronger glow on focus */
  }

  /* --- Tic Tac Toe Grid --- */
  .tic-tac-toe {
    display: grid;
    grid-template-columns: repeat(3, 90px); /* Larger cells */
    grid-template-rows: repeat(3, 90px);
    gap: 8px; /* Larger gap */
    justify-content: center;
    margin: 0 auto 1.5rem;
  }
  .tic-tac-toe button {
    font-size: 3rem; /* Larger X/O */
    background: #1a1a33; /* Darker cell background */
    color: #00ffff;
    border: 3px solid #00ffff; /* Stronger cyan border */
    transition: background 0.3s ease, color 0.3s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0;
    box-shadow: 0 0 8px rgba(0, 255, 255, 0.4);
  }
  .tic-tac-toe button:hover:not(:disabled) {
    background: #00ffff;
    color: #0d0d1a;
  }
  .tic-tac-toe button:disabled {
      cursor: not-allowed;
      opacity: 0.8;
      box-shadow: none;
  }

  /* --- Memory Card Grid --- */
  .memory-grid {
    display: grid;
    grid-template-columns: repeat(4, 80px); /* Larger cards */
    grid-template-rows: repeat(4, 80px);
    gap: 12px; /* Larger gap */
    justify-content: center;
    margin: 0 auto 1.5rem;
  }
  .memory-card {
    width: 80px;
    height: 80px;
    background: #1a1a33; /* Darker card background */
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2.5rem; /* Larger symbols */
    color: #00ffff;
    cursor: pointer;
    user-select: none;
    box-shadow: 0 0 10px rgba(0, 255, 255, 0.5) inset;
    transition: transform 0.4s ease, background 0.4s ease, color 0.4s ease;
    transform-style: preserve-3d;
  }
  .memory-card.flipped {
    background: #00ffff;
    color: #0d0d1a;
    cursor: default;
    transform: rotateY(180deg);
  }
  .memory-card.matched {
    background: #00ff00; /* Green for matched */
    color: #0d0d1a;
    cursor: default;
    opacity: 0.7;
    box-shadow: 0 0 15px rgba(0, 255, 0, 0.7) inset;
  }

  /* --- Snake Game Canvas --- */
  #snakeCanvas {
    background: #0a0a1a;
    display: block;
    margin: 0 auto 1.5rem;
    border: 3px solid #00ffff; /* Stronger cyan border */
    border-radius: 15px;
    box-shadow: 0 0 20px rgba(0, 255, 255, 0.5);
  }

  /* --- Quiz Styles --- */
  .quiz-question {
    font-size: 1.3rem;
    margin-bottom: 1.5rem;
    color: #fff;
    text-shadow: 0 0 5px rgba(255, 255, 255, 0.5);
  }
  .quiz-options button {
    display: block;
    width: 100%;
    margin: 0.5rem 0;
    font-size: 1rem;
    border-radius: 10px;
    background: #1a1a33;
    color: #00ffff;
    border: 2px solid #00ffff;
    cursor: pointer;
    transition: background 0.3s ease, color 0.3s ease, transform 0.2s ease;
  }
  .quiz-options button:hover:not(:disabled) {
    background: #00ffff;
    color: #0d0d1a;
    transform: translateX(5px); /* Slide effect on hover */
  }
  .quiz-options button:disabled {
    cursor: not-allowed;
    opacity: 0.7;
  }
  .quiz-feedback {
    margin-top: 1.5rem;
    font-weight: 700;
    color: #00ff00; /* Green for correct */
    font-size: 1.2rem;
    text-shadow: 0 0 8px #00ff00;
  }
  .correct-answer {
    background: #00ff00 !important;
    color: #0d0d1a !important;
    box-shadow: 0 0 15px rgba(0, 255, 0, 0.7);
  }
  .wrong-answer {
    background: #ff0000 !important;
    color: #fff !important;
    box-shadow: 0 0 15px rgba(255, 0, 0, 0.7);
  }

  /* --- Footer --- */
  footer {
    margin-top: 4rem;
    padding: 1.5rem;
    text-align: center;
    color: #808080;
    font-size: 0.9rem;
    background: #0a0a1a;
    width: 100%;
    position: relative;
    z-index: 10;
    border-top: 3px solid #6a05ad; /* Matching purple border */
    box-shadow: 0 -5px 20px rgba(106, 5, 173, 0.5);
  }

  /* --- Efek Hujan Lucu (CSS) --- */
  .rain {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    pointer-events: none;
    z-index: 0;
  }

  .drop {
    position: absolute;
    background: radial-gradient(circle at 30% 30%, rgba(135, 206, 235, 0.8), rgba(0, 191, 255, 0.6)); /* Gradient for more depth */
    border-radius: 50%;
    animation: fall linear infinite;
    box-shadow: 0 0 5px rgba(0, 191, 255, 0.7); /* Subtle glow for drops */
  }

  @keyframes fall {
    0% {
      transform: translateY(-100px) translateX(0);
      opacity: 0;
    }
    10% {
        opacity: 0.7; /* Muncul penuh lebih cepat */
    }
    100% {
      transform: translateY(calc(100vh + 100px)) translateX(70px) scale(0.8); /* Jatuh lebih jauh dan sedikit mengecil */
      opacity: 0;
    }
  }

  /* --- Kontrol Suara (Opsional, untuk toggle suara) --- */
  #audioControls {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 100;
      background: rgba(0, 0, 0, 0.8);
      padding: 12px;
      border-radius: 10px;
      display: flex;
      gap: 12px;
      align-items: center;
      border: 2px solid #ff00ff; /* Magenta border */
      box-shadow: 0 0 15px rgba(255, 0, 255, 0.6);
  }
  #audioControls button {
      background: #ff00ff; /* Magenta button */
      color: #0d0d1a;
      padding: 10px 15px;
      font-size: 0.9rem;
      border-radius: 8px;
      box-shadow: none;
      margin: 0;
      font-family: 'Press Start 2P', cursive;
  }
  #audioControls button:hover {
      background: #e000e0; /* Darker magenta on hover */
      color: #fff;
  }

  /* --- Font Imports (opsional, tambahkan ini di <head> jika ingin font custom) --- */
  @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
</style>
</head>
<body>

<div id="audioControls">
    <button id="toggleMusicBtn">Music ON</button>
    <button id="toggleSFXBtn">SFX ON</button>
    <button id="testSoundBtn">Test Sound</button> </div>

<div class="rain" id="rainEffect"></div>

<header>
  ARCADE MANIA
</header>

<main>

<div class="marquee">🕹️ Selamat datang di Arcade Mania! Tantang dirimu di berbagai game seru dan raih skor tertinggi! Dukung kami di Saweria! 👾</div>

<section class="game-section" id="game-tebak-angka">
  <h2>Tebak Angka</h2>
  <div class="rules">
    Tebak angka rahasia antara 1 hingga 100. Kamu punya 10 kesempatan. Petunjuk akan muncul setelah setiap tebakan!
  </div>
  <div class="game-container">
    <input type="number" id="taInput" placeholder="Masukkan angka" min="1" max="100" />
    <button onclick="tebakAngkaCek()">Tebak!</button>
    <button onclick="tebakAngkaMulai()">Mulai Ulang</button>
    <div class="game-output" id="taOutput">Ayo mulai tebak angkanya!</div>
  </div>
</section>

<section class="game-section" id="game-tictactoe">
  <h2>Tic Tac Toe</h2>
  <div class="rules">
    Mainkan Tic Tac Toe melawan AI! Kamu 'X', coba buat 3 simbol berturut-turut secara horizontal, vertikal, atau diagonal.
  </div>
  <div class="game-container">
    <div class="tic-tac-toe" id="tttBoard">
      <button data-cell="0"></button><button data-cell="1"></button><button data-cell="2"></button>
      <button data-cell="3"></button><button data-cell="4"></button><button data-cell="5"></button>
      <button data-cell="6"></button><button data-cell="7"></button><button data-cell="8"></button>
    </div>
    <button onclick="tttReset()">Mulai Uulang</button>
    <div class="game-output" id="tttOutput">Giliran Kamu (X)</div>
  </div>
</section>

<section class="game-section" id="game-memory">
  <h2>Memory Card</h2>
  <div class="rules">
    Uji daya ingatmu! Klik dua kartu untuk menemukan pasangan simbol yang sama. Cocokkan semua kartu untuk menang.
  </div>
  <div class="game-container">
    <div class="memory-grid" id="memoryGrid"></div>
    <button onclick="memoryReset()">Mulai Ulang</button>
    <div class="game-output" id="memoryOutput">Klik kartu untuk mulai.</div>
  </div>
</section>

<section class="game-section" id="game-snake">
  <h2>Snake Game</h2>
  <div class="rules">
    Kendalikan ular dengan tombol panah keyboard. Makan makanan merah untuk tumbuh lebih panjang. Hindari tabrakan!
  </div>
  <div class="game-container">
    <canvas id="snakeCanvas" width="320" height="320"></canvas>
    <br />
    <button onclick="snakeStart()">Mulai Game</button>
    <button onclick="snakeReset()">Reset</button>
    <div class="game-output" id="snakeOutput">Tekan 'Mulai Game' untuk mulai.</div>
  </div>
</section>

<section class="game-section" id="game-quiz">
  <h2>Quiz Cepat</h2>
  <div class="rules">
    Jawab pertanyaan pilihan ganda secepat mungkin! Semakin cepat Anda menjawab dengan benar, semakin tinggi skor Anda.
  </div>
  <div class="game-container">
    <div class="quiz-question" id="quizQuestion"></div>
    <div class="quiz-options" id="quizOptions"></div>
    <button onclick="quizReset()">Mulai Ulang</button>
    <div class="game-output" id="quizOutput"></div>
  </div>
</section>

<div id="saweria">
  <a href="https://saweria.co/yourlink" target="_blank" rel="noopener noreferrer">💖 Dukung Kami di Saweria</a>
</div>

</main>

<footer>
    <p>&copy; 2025 Arcade Mania. All rights reserved. Game on!</p>
</footer>

<script>
// ===== Pengaturan Audio Global =====
const audioPaths = {
    // Ganti dengan path file audio Anda. Pastikan ada folder 'audio/' di root project
    // Disarankan menyediakan format .mp3 dan .ogg untuk kompatibilitas browser yang lebih baik.
    // Contoh: click: ['audio/button-click.mp3', 'audio/button-click.ogg']
    click: ['audio/button-click.mp3'],     // Suara klik tombol umum
    win: ['audio/game-win-fanfare.mp3'],   // Suara kemenangan game
    lose: ['audio/game-over-sad.mp3'],     // Suara kekalahan/game over
    match: ['audio/match-bling.mp3'],      // Suara untuk Memory Card match
    nomatch: ['audio/nomatch-buzz.mp3'],   // Suara untuk Memory Card no match
    eat: ['audio/snake-eat.mp3'],          // Suara saat ular makan
    correct: ['audio/quiz-correct.mp3'],   // Suara jawaban quiz benar
    wrong: ['audio/quiz-wrong.mp3'],       // Suara jawaban quiz salah
    music: ['audio/arcade-music-loop.mp3'], // Musik latar yang seru dan berulang
    rain: ['audio/rain-loop-funny.mp3']    // Efek suara hujan lucu
};

const sounds = {};
let isMusicOn = true;
let isSfxOn = true;

// Inisialisasi Audio
function initAudio() {
    for (const key in audioPaths) {
        const paths = audioPaths[key];
        let loadedSuccessfully = false; // Flag untuk melacak apakah suara berhasil dimuat

        for (let i = 0; i < paths.length; i++) {
            const currentPath = paths[i];
            const audio = new Audio();
            audio.src = currentPath; // Set src
            audio.preload = 'auto'; // Coba preload

            // Event listener untuk error pemuatan
            audio.addEventListener('error', (e) => {
                console.error(`[AUDIO ERROR] Gagal memuat audio: '${currentPath}'. Event:`, e);
                if (audio.error) {
                    console.error(`[AUDIO ERROR DETAILS] Code: ${audio.error.code}, Message: ${audio.error.message}`);
                    switch(audio.error.code) {
                        case MediaError.MEDIA_ERR_ABORTED:
                            console.error("[AUDIO HINT] Pemuatan audio dihentikan (misalnya, oleh pengguna).");
                            break;
                        case MediaError.MEDIA_ERR_NETWORK:
                            console.error("[AUDIO HINT] Terjadi masalah jaringan saat memuat audio. Periksa koneksi atau path.");
                            break;
                        case MediaError.MEDIA_ERR_DECODE:
                            console.error("[AUDIO HINT] Format audio tidak didukung atau file rusak. Coba format lain (misal .ogg) atau file lain.");
                            break;
                        case MediaError.MEDIA_ERR_SRC_NOT_SUPPORTED:
                            console.error("[AUDIO HINT] Sumber audio tidak didukung oleh browser ini. Pastikan path file benar dan formatnya didukung.");
                            break;
                        default:
                            console.error("[AUDIO HINT] Error pemuatan audio tidak diketahui.");
                    }
                }
                // Jika ini adalah path terakhir dan belum berhasil dimuat, beri peringatan
                if (i === paths.length - 1 && !loadedSuccessfully) {
                    console.warn(`[AUDIO WARNING] Tidak ada sumber yang didukung ditemukan untuk suara '${key}'. Pastikan file ada, path benar, dan formatnya didukung.`);
                }
            });

            // Event listener saat audio siap diputar
            audio.addEventListener('canplaythrough', () => {
                if (!loadedSuccessfully) { // Pastikan hanya memuat sekali per kunci
                    sounds[key] = audio;
                    if (key === 'music' || key === 'rain') {
                        sounds[key].loop = true;
                        sounds[key].volume = 0.3;
                    } else {
                        sounds[key].volume = 0.5;
                    }
                    console.log(`[AUDIO SUCCESS] Audio dimuat: '${currentPath}' untuk kunci '${key}'.`);
                    loadedSuccessfully = true;
                }
            }, { once: true }); // Hanya jalankan sekali setelah berhasil dimuat

            audio.load(); // Mulai memuat audio
        }
    }

    const toggleMusicBtn = document.getElementById('toggleMusicBtn');
    const toggleSFXBtn = document.getElementById('toggleSFXBtn');
    const testSoundBtn = document.getElementById('testSoundBtn');

    toggleMusicBtn.addEventListener('click', () => {
        isMusicOn = !isMusicOn;
        if (isMusicOn) {
            if (sounds.music) {
                sounds.music.play().catch(e => console.error("[AUDIO ERROR] Gagal memutar musik latar:", e));
            } else {
                console.warn("[AUDIO WARNING] Musik latar belum dimuat atau tidak ditemukan.");
            }
            toggleMusicBtn.textContent = 'Music ON';
        } else {
            if (sounds.music) {
                sounds.music.pause();
            }
            toggleMusicBtn.textContent = 'Music OFF';
        }
    });

    toggleSFXBtn.addEventListener('click', () => {
        isSfxOn = !isSfxOn;
        toggleSFXBtn.textContent = `SFX ${isSfxOn ? 'ON' : 'OFF'}`;
    });

    testSoundBtn.addEventListener('click', () => {
        playSound('click');
        console.log("[AUDIO TEST] Mencoba memutar suara 'click'.");
    });

    // Panggil musik dan hujan setelah interaksi pertama pengguna untuk mengatasi kebijakan autoplay browser
    document.body.addEventListener('click', () => {
        if (isMusicOn && sounds.music && sounds.music.paused) {
            sounds.music.play().catch(e => console.error("[AUDIO ERROR] Autoplay musik latar gagal:", e));
        }
        if (sounds.rain && sounds.rain.paused) {
            sounds.rain.play().catch(e => console.error("[AUDIO ERROR] Autoplay efek hujan gagal:", e));
        }
    }, { once: true });
}

function playSound(soundName) {
    if (isSfxOn && sounds[soundName]) {
        const clonedSound = sounds[soundName].cloneNode();
        clonedSound.volume = sounds[soundName].volume;
        clonedSound.currentTime = 0;
        clonedSound.play().catch(e => console.error(`[AUDIO ERROR] Gagal memutar '${soundName}':`, e));
    } else if (!sounds[soundName]) {
        console.warn(`[AUDIO WARNING] Suara '${soundName}' belum dimuat atau tidak ditemukan.`);
    }
}

// ===== Efek Hujan Lucu (JavaScript) =====
const rainContainer = document.getElementById('rainEffect');

function createRaindrop() {
    const drop = document.createElement('div');
    drop.classList.add('drop');
    const size = Math.random() * 8 + 4;
    const duration = Math.random() * 2 + 1;
    const delay = Math.random() * 2;
    const left = Math.random() * 100;

    drop.style.width = `${size}px`;
    drop.style.height = `${size}px`;
    drop.style.left = `${left}vw`;
    drop.style.animationDuration = `${duration}s`;
    drop.style.animationDelay = `${delay}s`;

    rainContainer.appendChild(drop);

    drop.addEventListener('animationend', () => {
        drop.remove();
    });
}

function startRainEffect() {
    setInterval(createRaindrop, 100);
}

document.addEventListener('DOMContentLoaded', () => {
    initAudio();
    startRainEffect();
});


// ===== Tebak Angka =====
let taTarget, taAttempts;
function tebakAngkaMulai() {
  playSound('click');
  taTarget = Math.floor(Math.random() * 100) + 1;
  taAttempts = 10;
  document.getElementById('taOutput').textContent = 'Tebak angka antara 1 - 100. Kamu punya 10 kesempatan.';
  document.getElementById('taInput').value = '';
  document.getElementById('taInput').disabled = false;
}
function tebakAngkaCek() {
  playSound('click');
  const input = parseInt(document.getElementById('taInput').value);
  if (isNaN(input) || input < 1 || input > 100) {
    document.getElementById('taOutput').textContent = 'Masukkan angka valid antara 1 sampai 100!';
    return;
  }
  if (taAttempts <= 0) {
    document.getElementById('taOutput').textContent = 'Game selesai! Kamu sudah kehabisan kesempatan. Tekan "Mulai Ulang" untuk bermain lagi.';
    document.getElementById('taInput').disabled = true;
    playSound('lose');
    return;
  }
  taAttempts--;
  if (input === taTarget) {
    document.getElementById('taOutput').textContent = `Selamat! Kamu benar, angka nya ${taTarget}.`;
    document.getElementById('taInput').disabled = true;
    playSound('win');
  } else if (input > taTarget) {
    document.getElementById('taOutput').textContent = `Terlalu tinggi! Kesempatan tersisa: ${taAttempts}`;
  } else {
    document.getElementById('taOutput').textContent = `Terlalu rendah! Kesempatan tersisa: ${taAttempts}`;
  }
  if (taAttempts === 0 && input !== taTarget) {
    document.getElementById('taOutput').textContent = `Game selesai! Angka yang benar adalah ${taTarget}. Tekan "Mulai Ulang" untuk bermain lagi.`;
    document.getElementById('taInput').disabled = true;
    playSound('lose');
  }
}
tebakAngkaMulai();

// ===== Tic Tac Toe =====
const tttBoardState = Array(9).fill(null);
let tttTurn = 'X';
let tttGameOver = false;
const tttButtons = document.querySelectorAll('#tttBoard button');
const tttOutput = document.getElementById('tttOutput');

tttButtons.forEach(button => {
  button.addEventListener('click', tttHandleClick);
});

function tttCheckWin(board, player) {
  const winPatterns = [
    [0,1,2],[3,4,5],[6,7,8], // rows
    [0,3,6],[1,4,7],[2,5,8], // columns
    [0,4,8],[2,4,6]        // diagonals
  ];
  return winPatterns.some(pattern => pattern.every(i => board[i] === player));
}

function tttCheckDraw(board) {
  return board.every(cell => cell !== null);
}

function tttHandleClick(event) {
  playSound('click');
  const cellIndex = parseInt(event.target.dataset.cell);

  if (tttBoardState[cellIndex] !== null || tttGameOver) {
    return;
  }

  tttBoardState[cellIndex] = tttTurn;
  event.target.textContent = tttTurn;
  event.target.disabled = true;

  if (tttCheckWin(tttBoardState, tttTurn)) {
    tttOutput.textContent = `Pemain ${tttTurn} Menang!`;
    tttGameOver = true;
    tttDisableButtons();
    playSound('win');
    return;
  }

  if (tttCheckDraw(tttBoardState)) {
    tttOutput.textContent = 'Seri!';
    tttGameOver = true;
    playSound('lose'); // Using lose sound for draw
    return;
  }

  tttTurn = tttTurn === 'X' ? 'O' : 'X';
  tttOutput.textContent = `Giliran ${tttTurn}`;

  if (tttTurn === 'O' && !tttGameOver) {
    setTimeout(tttAiMove, 500);
  }
}

function tttAiMove() {
  if (tttGameOver) return;

  const availableCells = tttBoardState.map((val, idx) => val === null ? idx : null).filter(idx => idx !== null);
  let bestMove = -1;

  for (let i = 0; i < availableCells.length; i++) {
    const tempBoard = [...tttBoardState];
    tempBoard[availableCells[i]] = 'O';
    if (tttCheckWin(tempBoard, 'O')) {
      bestMove = availableCells[i];
      break;
    }
  }

  if (bestMove === -1) {
    for (let i = 0; i < availableCells.length; i++) {
      const tempBoard = [...tttBoardState];
      tempBoard[availableCells[i]] = 'X';
      if (tttCheckWin(tempBoard, 'X')) {
        bestMove = availableCells[i];
        break;
      }
    }
  }

  if (bestMove === -1 && tttBoardState[4] === null) {
    bestMove = 4;
  }

  if (bestMove === -1) {
    const corners = [0, 2, 6, 8].filter(idx => tttBoardState[idx] === null);
    if (corners.length > 0) {
      bestMove = corners[Math.floor(Math.random() * corners.length)];
    }
  }

  if (bestMove === -1) {
    const sides = [1, 3, 5, 7].filter(idx => tttBoardState[idx] === null);
    if (sides.length > 0) {
      bestMove = sides[Math.floor(Math.random() * sides.length)];
    }
  }

  if (bestMove !== -1) {
    tttBoardState[bestMove] = 'O';
    tttButtons[bestMove].textContent = 'O';
    tttButtons[bestMove].disabled = true;

    if (tttCheckWin(tttBoardState, 'O')) {
      tttOutput.textContent = 'Komputer (O) Menang!';
      tttGameOver = true;
      tttDisableButtons();
      playSound('lose'); // AI wins, so player loses
      return;
    }
    if (tttCheckDraw(tttBoardState)) {
      tttOutput.textContent = 'Seri!';
      tttGameOver = true;
      playSound('lose'); // Using lose sound for draw
      return;
    }
  }
  tttTurn = 'X';
  tttOutput.textContent = 'Giliran Kamu (X)';
}

function tttDisableButtons() {
  tttButtons.forEach(button => button.disabled = true);
}

function tttReset() {
  playSound('click');
  for(let i=0; i<9; i++) {
    tttBoardState[i] = null;
    tttButtons[i].textContent = '';
    tttButtons[i].disabled = false;
  }
  tttTurn = 'X';
  tttGameOver = false;
  tttOutput.textContent = 'Giliran Kamu (X)';
}

tttReset();


// ===== Memory Card =====
const memorySymbols = ['⭐', '💖', '💡', '🌈', '🔥', '💧', '⚡', '🌸'];
let memoryCards = [];
let flippedCards = [];
let matchedPairs = 0;
let lockBoard = false;

const memoryGrid = document.getElementById('memoryGrid');
const memoryOutput = document.getElementById('memoryOutput');

function memoryShuffle(array) {
  for (let i = array.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [array[i], array[j]] = [array[j], array[i]];
  }
  return array;
}

function memoryGenerateCards() {
  memoryCards = [...memorySymbols, ...memorySymbols];
  memoryShuffle(memoryCards);

  memoryGrid.innerHTML = '';
  memoryCards.forEach((symbol, index) => {
    const card = document.createElement('div');
    card.classList.add('memory-card');
    card.dataset.symbol = symbol;
    card.dataset.index = index;
    card.addEventListener('click', memoryFlipCard);
    memoryGrid.appendChild(card);
  });
  memoryOutput.textContent = 'Klik kartu untuk mulai.';
}

function memoryFlipCard() {
  playSound('click');
  if (lockBoard) return;
  if (this === flippedCards[0]) return;

  this.classList.add('flipped');
  this.textContent = this.dataset.symbol;

  flippedCards.push(this);

  if (flippedCards.length === 2) {
    lockBoard = true;
    memoryCheckMatch();
  }
}

function memoryCheckMatch() {
  const [card1, card2] = flippedCards;
  const isMatch = card1.dataset.symbol === card2.dataset.symbol;

  if (isMatch) {
    card1.classList.add('matched');
    card2.classList.add('matched');
    card1.removeEventListener('click', memoryFlipCard);
    card2.removeEventListener('click', memoryFlipCard);
    matchedPairs++;
    memoryOutput.textContent = `Berhasil cocok! Pasangan: ${matchedPairs}/${memorySymbols.length}`;
    playSound('match'); // Play match sound

    if (matchedPairs === memorySymbols.length) {
      memoryOutput.textContent = 'Selamat! Kamu memenangkan game Memory Card!';
      playSound('win');
    }
    memoryResetFlippedCards();
  } else {
    memoryOutput.textContent = 'Tidak cocok! Coba lagi.';
    playSound('nomatch'); // Play no match sound
    setTimeout(() => {
      card1.classList.remove('flipped');
      card2.classList.remove('flipped');
      card1.textContent = '';
      card2.textContent = '';
      memoryResetFlippedCards();
    }, 1000);
  }
}

function memoryResetFlippedCards() {
  flippedCards = [];
  lockBoard = false;
}

function memoryReset() {
  playSound('click');
  flippedCards = [];
  matchedPairs = 0;
  lockBoard = false;
  memoryGenerateCards();
}

memoryGenerateCards();


// ===== Snake Game =====
const snakeCanvas = document.getElementById('snakeCanvas');
const ctx = snakeCanvas.getContext('2d');
const snakeOutput = document.getElementById('snakeOutput');

const gridSize = 20;
let snake = [{x: 10, y: 10}];
let food = {};
let dx = 0;
let dy = 0;
let score = 0;
let changingDirection = false;
let gameInterval;
let gameStarted = false;

function drawSnakePart(snakePart) {
  ctx.fillStyle = '#00ff00'; /* Brighter green snake */
  ctx.strokeStyle = '#0a0a1a';
  ctx.fillRect(snakePart.x * gridSize, snakePart.y * gridSize, gridSize, gridSize);
  ctx.strokeRect(snakePart.x * gridSize, snakePart.y * gridSize, gridSize, gridSize);
}

function drawFood() {
  ctx.fillStyle = '#ff0000'; /* Bright red food */
  ctx.strokeStyle = '#0a0a1a';
  ctx.fillRect(food.x * gridSize, food.y * gridSize, gridSize, gridSize);
  ctx.strokeRect(food.x * gridSize, food.y * gridSize, gridSize, gridSize);
}

function clearCanvas() {
  ctx.clearRect(0, 0, snakeCanvas.width, snakeCanvas.height);
}

function generateFood() {
  food.x = Math.floor(Math.random() * (snakeCanvas.width / gridSize));
  food.y = Math.floor(Math.random() * (snakeCanvas.height / gridSize));

  snake.forEach(part => {
    const foodIsOnSnake = (part.x === food.x && part.y === food.y);
    if (foodIsOnSnake) {
      generateFood();
    }
  });
}

function moveSnake() {
  if (!gameStarted) return;

  const head = {x: snake[0].x + dx, y: snake[0].y + dy};

  const hitLeftWall = head.x < 0;
  const hitRightWall = head.x * gridSize >= snakeCanvas.width;
  const hitTopWall = head.y < 0;
  const hitBottomWall = head.y * gridSize >= snakeCanvas.height;

  const hitSelf = snake.some((part, index) =>
    index > 0 && part.x === head.x && part.y === head.y
  );

  if (hitLeftWall || hitRightWall || hitTopWall || hitBottomWall || hitSelf) {
    snakeOutput.textContent = `Game Over! Skor: ${score}`;
    clearInterval(gameInterval);
    gameStarted = false;
    playSound('lose');
    return;
  }

  snake.unshift(head);

  const didEatFood = head.x === food.x && head.y === food.y;
  if (didEatFood) {
    score += 10;
    snakeOutput.textContent = `Skor: ${score}`;
    generateFood();
    playSound('eat'); // Play eat sound
  } else {
    snake.pop();
  }

  clearCanvas();
  snake.forEach(drawSnakePart);
  drawFood();
  changingDirection = false;
}

function changeDirection(event) {
  // playSound('click'); // Optional: sound for direction change on key press
  if (changingDirection) return;
  changingDirection = true;

  const keyPressed = event.keyCode;
  const LEFT_KEY = 37;
    const RIGHT_KEY = 39;
    const UP_KEY = 38;
    const DOWN_KEY = 40;

    const movingUp = dy === -1;
    const movingDown = dy === 1;
    const movingLeft = dx === -1;
    const movingRight = dx === 1;

    if (keyPressed === LEFT_KEY && !movingRight) {
    dx = -1;
    dy = 0;
  }
    if (keyPressed === UP_KEY && !movingDown) {
    dx = 0;
    dy = -1;
  }
    if (keyPressed === RIGHT_KEY && !movingLeft) {
    dx = 1;
    dy = 0;
  }
    if (keyPressed === DOWN_KEY && !movingUp) {
    dx = 0;
    dy = 1;
  }
}

function snakeStart() {
  playSound('click');
  if (gameStarted) return;
  snakeReset(); // Reset before starting to ensure clean state
  gameStarted = true;
  snakeOutput.textContent = 'Skor: 0';
  gameInterval = setInterval(moveSnake, 100);
  document.addEventListener('keydown', changeDirection);
}

function snakeReset() {
  playSound('click');
  clearInterval(gameInterval);
  snake = [{x: 10, y: 10}];
  dx = 0;
  dy = 0;
  score = 0;
  changingDirection = false;
  gameStarted = false;
  snakeOutput.textContent = 'Tekan \'Mulai Game\' untuk mulai.';
  clearCanvas();
  generateFood();
  drawFood();
  drawSnakePart(snake[0]);
  document.removeEventListener('keydown', changeDirection);
}

snakeReset();


// ===== Quiz Cepat =====
const quizQuestions = [
  {
    question: "Siapakah pencipta JavaScript?",
    options: ["Brendan Eich", "Guido van Rossum", "James Gosling", "Bjarne Stroustrup"],
    answer: "Brendan Eich"
  },
  {
    question: "Apa itu HTML?",
    options: ["Bahasa Pemrograman", "Bahasa Markup", "Kerangka Kerja CSS", "Sistem Database"],
    answer: "Bahasa Markup"
  },
  {
    question: "Apa singkatan dari CSS?",
    options: ["Cascading Style Sheets", "Creative Style System", "Computer Style Syntax", "Colorful Style Samples"],
    answer: "Cascading Style Sheets"
  },
  {
    question: "Framework JavaScript populer untuk membangun antarmuka pengguna adalah...",
    options: ["Angular", "React", "Vue", "Semua di atas"],
    answer: "Semua di atas"
  },
  {
    question: "Mana yang bukan bahasa pemrograman?",
    options: ["Python", "Java", "Markdown", "C#"],
    answer: "Markdown"
  }
];

let currentQuizIndex = 0;
let quizScore = 0;
let quizAttempts = 0;
let quizStartTime;
let quizTimeout;

const quizQuestionEl = document.getElementById('quizQuestion');
const quizOptionsEl = document.getElementById('quizOptions');
const quizOutputEl = document.getElementById('quizOutput');

function quizLoadQuestion() {
  if (currentQuizIndex >= quizQuestions.length) {
    quizEndGame();
    return;
  }

  const q = quizQuestions[currentQuizIndex];
  quizQuestionEl.textContent = q.question;
  quizOptionsEl.innerHTML = '';

  q.options.forEach(option => {
    const button = document.createElement('button');
    button.textContent = option;
    button.onclick = () => quizCheckAnswer(option, q.answer, button);
    quizOptionsEl.appendChild(button);
  });
  quizOutputEl.textContent = '';
  quizStartTime = Date.now();
  quizTimeout = setTimeout(() => quizCheckAnswer(null, q.answer, null), 10000); // Batas waktu 10 detik
}

function quizCheckAnswer(selectedOption, correctAnswer, buttonClicked) {
  playSound('click'); // Play click sound when option is chosen
  clearTimeout(quizTimeout);

  const allButtons = quizOptionsEl.querySelectorAll('button');
  allButtons.forEach(button => {
    button.disabled = true;
    if (button.textContent === correctAnswer) {
      button.classList.add('correct-answer');
    }
    if (buttonClicked && buttonClicked.textContent === selectedOption && selectedOption !== correctAnswer) {
      buttonClicked.classList.add('wrong-answer');
    }
  });

  if (selectedOption === correctAnswer) {
    const timeTaken = (Date.now() - quizStartTime) / 1000;
    quizScore += Math.max(0, 10 - Math.floor(timeTaken));
    quizOutputEl.textContent = `Benar! Skor sementara: ${quizScore}`;
    playSound('correct'); // Play correct sound
  } else {
    quizOutputEl.textContent = `Salah. Jawaban benar adalah: ${correctAnswer}. Skor sementara: ${quizScore}`;
    playSound('wrong'); // Play wrong sound
  }

  currentQuizIndex++;
  quizAttempts++;
  setTimeout(quizLoadQuestion, 2000);
}

function quizEndGame() {
  quizQuestionEl.textContent = 'Quiz Selesai!';
  quizOptionsEl.innerHTML = '';
  quizOutputEl.textContent = `Skor akhir Anda: ${quizScore} dari ${quizQuestions.length * 10} poin maksimal.`;
  playSound('win'); // Play win sound for finishing quiz
}

function quizReset() {
  playSound('click');
  currentQuizIndex = 0;
  quizScore = 0;
  quizAttempts = 0;
  clearTimeout(quizTimeout);
  quizLoadQuestion();
}

quizLoadQuestion();
</script>

</body>
</html>
