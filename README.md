<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Biodata | Tasya Alika ✨</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            background: linear-gradient(135deg, #fbc2eb 0%, #a6c1ee 100%);
            font-family: 'Poppins', 'Segoe UI', system-ui, -apple-system, 'Quicksand', sans-serif;
            padding: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }

        /* efek bintang animasi */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }

        .star {
            position: absolute;
            background-color: white;
            border-radius: 50%;
            opacity: 0.6;
            animation: twinkle 3s infinite alternate;
        }

        @keyframes twinkle {
            0% { opacity: 0.2; transform: scale(1);}
            100% { opacity: 0.9; transform: scale(1.2);}
        }

        /* kartu biodata utama */
        .card {
            max-width: 700px;
            width: 100%;
            background: rgba(255, 255, 255, 0.96);
            backdrop-filter: blur(2px);
            border-radius: 64px 48px 64px 48px;
            box-shadow: 0 25px 45px rgba(0, 0, 0, 0.2), 0 0 0 1px rgba(255, 255, 255, 0.5);
            overflow: hidden;
            transition: transform 0.3s ease;
            z-index: 2;
            position: relative;
        }

        .card:hover {
            transform: scale(1.01);
        }

        /* header dengan aksen */
        .header-bg {
            background: linear-gradient(120deg, #ff9a9e, #fad0c4, #fad0c4);
            padding: 32px 28px 28px;
            text-align: center;
            border-bottom: 5px solid #fbc2eb;
        }

        .avatar {
            width: 120px;
            height: 120px;
            background: #fff0e0;
            border-radius: 50%;
            margin: 0 auto 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 12px 18px rgba(0, 0, 0, 0.1);
            border: 4px solid #ffffff;
            background: linear-gradient(145deg, #ffe6f0, #ffe0c0);
        }

        .avatar span {
            font-size: 4rem;
        }

        h1 {
            font-size: 1.9rem;
            font-weight: 700;
            background: linear-gradient(135deg, #2d1b4e, #a13e6f);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            letter-spacing: -0.3px;
            margin-bottom: 8px;
        }

        .badge {
            background: #ffffffcc;
            backdrop-filter: blur(4px);
            display: inline-block;
            padding: 6px 18px;
            border-radius: 60px;
            font-size: 0.85rem;
            font-weight: 600;
            color: #aa2e6b;
            margin-top: 8px;
            box-shadow: inset 0 1px 2px #0001, 0 4px 8px rgba(0,0,0,0.05);
        }

        /* isi biodata */
        .info-container {
            padding: 28px 30px;
            background: #fefaf5;
        }

        .info-grid {
            display: flex;
            flex-direction: column;
            gap: 18px;
            margin-bottom: 32px;
        }

        .info-item {
            display: flex;
            align-items: baseline;
            flex-wrap: wrap;
            border-bottom: 1px dashed #ffcdb0;
            padding-bottom: 10px;
        }

        .info-label {
            font-weight: 700;
            width: 110px;
            color: #b24c7c;
            font-size: 1rem;
            letter-spacing: 0.3px;
        }

        .info-value {
            flex: 1;
            color: #2d2f36;
            font-weight: 500;
            font-size: 1.05rem;
            word-break: break-word;
        }

        .motivation-box {
            background: #fff1e6;
            border-radius: 48px;
            padding: 18px 24px;
            margin: 20px 0 30px;
            border-left: 12px solid #ffb347;
            box-shadow: 0 5px 12px rgba(0, 0, 0, 0.05);
        }

        .motivation-box p:first-child {
            font-weight: 700;
            font-size: 1.2rem;
            color: #d46b2e;
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 8px;
        }

        .motivation-box p:last-child {
            font-size: 1.1rem;
            font-weight: 500;
            color: #2c3e2f;
            font-style: italic;
        }

        /* tombol menuju proyek game kucing */
        .project-btn {
            display: flex;
            justify-content: center;
            margin: 16px 0 10px;
        }

        .btn-cat {
            background: linear-gradient(95deg, #ffb347, #ff8c42);
            border: none;
            padding: 14px 28px;
            border-radius: 60px;
            font-size: 1.1rem;
            font-weight: bold;
            font-family: inherit;
            color: white;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            cursor: pointer;
            transition: all 0.25s ease;
            box-shadow: 0 8px 18px rgba(0, 0, 0, 0.15);
            text-decoration: none;
            width: auto;
            border: 1px solid rgba(255,255,200,0.6);
        }

        .btn-cat:hover {
            transform: translateY(-3px);
            background: linear-gradient(95deg, #ffa032, #ff6e1f);
            box-shadow: 0 15px 25px rgba(0,0,0,0.2);
        }

        .btn-cat:active {
            transform: translateY(2px);
        }

        .btn-cat span {
            font-size: 1.5rem;
        }

        footer {
            text-align: center;
            font-size: 0.7rem;
            color: #b47c58;
            background: #f9eddf;
            padding: 16px;
            border-top: 1px solid #ffe0c0;
            font-weight: 500;
        }

        /* efek tambahan */
        .glow-text {
            text-shadow: 0 1px 2px rgba(255,255,200,0.6);
        }

        @media (max-width: 500px) {
            .info-label {
                width: 90px;
                font-size: 0.9rem;
            }
            .info-value {
                font-size: 0.95rem;
            }
            h1 {
                font-size: 1.5rem;
            }
            .card {
                border-radius: 44px;
            }
        }
    </style>
</head>
<body>

<!-- Background bintang dinamis -->
<div class="stars" id="starsContainer"></div>

<div class="card">
    <div class="header-bg">
        <div class="avatar">
            <span>🐱✨</span>
        </div>
        <h1>Tasya Alika Shabrina Nayasza</h1>
        <div class="badge">🌟 “Dream Big, Shine Bright” 🌟</div>
    </div>

    <div class="info-container">
        <div class="info-grid">
            <div class="info-item">
                <div class="info-label">📅 Usia</div>
                <div class="info-value">17 tahun (Generasi Z yang ambisius)</div>
            </div>
            <div class="info-item">
                <div class="info-label">🎓 Sekolah</div>
                <div class="info-value">SMAN 15 Jakarta</div>
            </div>
            <div class="info-item">
                <div class="info-label">📏 Tinggi Badan</div>
                <div class="info-value">154.5 cm <span style="font-size:0.8rem;">(tetap kece!)</span></div>
            </div>
            <div class="info-item">
                <div class="info-label">💪 Motivasi Hidup</div>
                <div class="info-value">“Ingin menjadi orang tajir dan sukses”</div>
            </div>
        </div>

        <div class="motivation-box">
            <p>🚀✨ MOTTO HIDUP ✨🚀</p>
            <p>“Jangan hanya jadi penonton kesuksesan, wujudkan mimpimu menjadi tajir dan sukses dengan kerja cerdas, doa, dan konsistensi. Masa depan gemilang menanti!”</p>
        </div>

        <!-- TOMBOL LINK PROYEK GAME KUCING TALKING ANGELA STYLE -->
        <div class="project-btn">
            <a href="https://tasyaalika.github.io/talking-catcute/" target="_blank" rel="noopener noreferrer" class="btn-cat">
                <span>🐈⬛</span> Mainkan Game Kucing Pintarku <span>🎮➡️</span>
            </a>
        </div>
        <p style="text-align: center; margin-top: 14px; font-size: 0.75rem; color: #aa7a5c;">
            ✨ Klik tombol di atas untuk bermain dengan kucing virtual yang bisa bicara, makan, dan hidup sehari-hari ✨
        </p>
    </div>

    <footer>
        © 2026 - Biodata Tasya Alika | Jangan lupa semangat jadi sukses dan kaya raya 💎
    </footer>
</div>

<script>
    // Animasi background bintang-bintang kecil yang manis
    function createStars() {
        const starsContainer = document.getElementById('starsContainer');
        const starCount = 110;
        for (let i = 0; i < starCount; i++) {
            const star = document.createElement('div');
            star.classList.add('star');
            const size = Math.random() * 4 + 1.5; // 1.5px - 5.5px
            star.style.width = size + 'px';
            star.style.height = size + 'px';
            star.style.left = Math.random() * 100 + '%';
            star.style.top = Math.random() * 100 + '%';
            star.style.animationDelay = Math.random() * 5 + 's';
            star.style.animationDuration = Math.random() * 2 + 1.5 + 's';
            star.style.opacity = Math.random() * 0.5 + 0.3;
            starsContainer.appendChild(star);
        }
    }

    // efek tambahan untuk membuat biodata terasa hidup (cursor sparkle opsional)
    function addSoftGlow() {
        const card = document.querySelector('.card');
        if(card) {
            card.addEventListener('mousemove', (e) => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                card.style.boxShadow = `0 25px 45px rgba(0, 0, 0, 0.2), 0 0 0 1px rgba(255,235,200,0.8), inset 0 0 20px rgba(255,180,80,0.1)`;
            });
            card.addEventListener('mouseleave', () => {
                card.style.boxShadow = '0 25px 45px rgba(0, 0, 0, 0.2), 0 0 0 1px rgba(255, 255, 255, 0.5)';
            });
        }
    }

    // Konfirmasi bahwa tombol mengarah ke proyek game Talking Cat (bisa ditambahkan popup manis)
    function setupButtonHint() {
        const btn = document.querySelector('.btn-cat');
        if(btn) {
            btn.addEventListener('click', (e) => {
                // hanya efek notifikasi kecil supaya user tahu diarahkan ke proyek game kucing
                console.log('Menuju ke proyek game kucing interaktif: https://tasyaalika.github.io/talking-catcute/');
                // (tidak ada preventDefault, link akan berjalan normal)
                // sedikit animasi semangat
                btn.style.transform = 'scale(0.98)';
                setTimeout(() => { btn.style.transform = ''; }, 150);
            });
        }
    }

    // update tahun dinamis di footer (opsional)
    function updateFooterYear() {
        const footer = document.querySelector('footer');
        if(footer) {
            const year = new Date().getFullYear();
            footer.innerHTML = footer.innerHTML.replace('2026', year);
        }
    }

    createStars();
    addSoftGlow();
    setupButtonHint();
    updateFooterYear();
</script>
</body>
</html>
