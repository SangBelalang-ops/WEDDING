<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Wedding of Piter & ???</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Playfair+Display:ital,wght@0,400;1,400&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    
    <style>
        :root { --gold: #b8860b; --dark: #2c3e50; --cream: #fffaf0; --pink: #ffb6c1; --soft-pink: #fff0f3; }
        * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
        
        body { 
            font-family: 'Poppins', sans-serif; 
            color: var(--dark); 
            overflow-x: hidden; 
            /* Pointer Love */
            cursor: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="%23b8860b" d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>'), auto;
        }

        /* Navigasi */
        nav { position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%); background: rgba(255,255,255,0.95); padding: 10px 20px; border-radius: 30px; display: flex; gap: 20px; z-index: 1000; box-shadow: 0 4px 15px rgba(0,0,0,0.1); border: 1px solid var(--gold); }
        nav a { text-decoration: none; color: var(--dark); font-size: 0.85rem; font-weight: 600; }

        /* Sections & Backgrounds */
        section { padding: 80px 20px; text-align: center; min-height: 100vh; display: flex; flex-direction: column; justify-content: center; position: relative; background-size: cover; background-position: center; background-attachment: fixed; }
        
        /* 1. HERO (TEMA: FOTO UTAMA FULLSCREEN) */
        /* GANTI URL DI BAWAH INI DENGAN LINK FOTO UTAMA PREWED PITER */
        .hero { background-image: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1519741497674-611481863552?auto=format&fit=crop&w=1500&q=80'); color: white; }
        h1 { font-family: 'Dancing Script', cursive; font-size: 5rem; color: var(--gold); margin: 20px 0; }
        .hero p { letter-spacing: 3px; font-family: 'Playfair Display', serif; }

        /* 2. GALLERY (TEMA: FLOWER PATTERN) */
        /* GANTI URL DI BAWAH INI DENGAN LINK PATTERN BUNGA LEMBUT */
        #gallery { background-color: var(--cream); background-image: url('https://www.transparenttextures.com/patterns/cream-pixels.png'); } /* Pattern Halus Krem */
        .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; max-width: 1200px; margin: 0 auto; padding: 20px; }
        .gallery-item { position: relative; overflow: hidden; border-radius: 15px; border: 5px solid white; box-shadow: 0 5px 15px rgba(0,0,0,0.1); transition: 0.3s; }
        .gallery-item img { width: 100%; height: 350px; object-fit: cover; transition: 0.5s; }
        .gallery-item:hover { transform: translateY(-5px); border-color: var(--gold); }
        .gallery-item:hover img { transform: scale(1.1); }

        /* 3. WISHES (TEMA: SOFT PINK FADE) */
        #wish { background-color: var(--soft-pink); background-image: url('https://www.transparenttextures.com/patterns/soft-wallpaper.png'); } /* Pattern Kain Lembut */
        form { max-width: 550px; margin: 0 auto 40px; display: flex; flex-direction: column; gap: 15px; text-align: left; background: white; padding: 40px; border-radius: 20px; box-shadow: 0 15px 35px rgba(0,0,0,0.05); }
        input, textarea { padding: 15px; border: 1px solid #ddd; border-radius: 10px; font-family: 'Poppins', sans-serif; outline: none; }
        input:focus, textarea:focus { border-color: var(--gold); }
        button { background: var(--gold); color: white; border: none; padding: 15px; border-radius: 10px; cursor: pointer; font-weight: bold; transition: 0.3s; font-size: 1rem; }
        button:hover { background: #966d09; transform: translateY(-2px); }

        .wish-container { max-height: 400px; overflow-y: auto; padding-right: 10px; }
        .wish-card { background: white; margin: 15px auto; padding: 25px; border-radius: 15px; border-left: 6px solid var(--gold); text-align: left; max-width: 500px; box-shadow: 0 4px 10px rgba(0,0,0,0.03); animation: fadeInUp 0.8s; }

        /* 4. GIFT (TEMA: ELEGANT DARK/GOLD) */
        /* GANTI URL DI BAWAH INI DENGAN GAMBAR BACKGROUND MEWAH GELAP (Misal Marmer Hitam/Tekstur Emas) */
        #gift { background-color: var(--dark); background-image: linear-gradient(rgba(44,62,80,0.9), rgba(44,62,80,0.95)), url('https://images.unsplash.com/photo-1581012771300-224937651c42?q=80&w=1470&auto=format&fit=crop'); color: white; }
        .bank-card { background: rgba(255,255,255,0.05); padding: 40px; border-radius: 20px; max-width: 450px; margin: 30px auto; border: 2px dashed var(--gold); box-shadow: 0 10px 30px rgba(0,0,0,0.2); backdrop-filter: blur(5px); }
        .btn-copy { font-size: 0.8rem; background: var(--gold); color: var(--dark); padding: 8px 15px; border-radius: 20px; cursor: pointer; display: inline-block; margin-top: 15px; font-weight: 600; }
        .btn-copy:hover { background: white; }

        /* Sakura Animation */
        .sakura { position: fixed; background-color: var(--pink); border-radius: 100% 0 100% 0; opacity: 0.7; pointer-events: none; z-index: 9999; animation: fall linear infinite; }
        @keyframes fall { 0% { transform: translateY(-10vh) rotate(0deg); } 100% { transform: translateY(110vh) rotate(360deg); } }
    </style>
</head>
<body>

    <nav>
        <a href="#home">Home</a>
        <a href="#gallery">Gallery</a>
        <a href="#wish">Wish</a>
        <a href="#gift">Gift</a>
    </nav>

    <section id="home" class="hero">
        <p class="animate__animated animate__fadeInDown">THE WEDDING OF</p>
        <h1 class="animate__animated animate__zoomIn">Piter & ???</h1>
        <div style="font-family: 'Playfair Display', serif; font-size: 1.5rem;" class="animate__animated animate__fadeInUp">16 Mei 2026</div>
    </section>

    <section id="gallery">
        <h2 style="font-family: 'Dancing Script', cursive; font-size: 3.5rem; margin-bottom: 40px; color: var(--gold);">Our Pre-Wedding Gallery</h2>
        <div class="gallery-grid">
            
            <div class="gallery-item animate__animated animate__fadeInLeft">
                <img src="https://images.unsplash.com/photo-1583939003579-730e3918a45a?w=600" alt="Foto Prewed Piter 1">
            </div>
            
            <div class="gallery-item animate__animated animate__fadeInUp">
                <img src="https://images.unsplash.com/photo-1511285560929-80b456fea0bc?w=600" alt="Foto Prewed Piter 2">
            </div>
            
            <div class="gallery-item animate__animated animate__fadeInRight">
                <img src="https://images.unsplash.com/photo-1494774157365-9e04c6720e47?w=600" alt="Foto Prewed Piter 3">
            </div>

             <div class="gallery-item animate__animated animate__fadeInLeft">
                <img src="https://images.unsplash.com/photo-1522673607200-1648832cee98?w=600" alt="Foto Prewed Piter 4">
            </div>

        </div>
    </section>

    <section id="wish">
        <h2 style="font-family: 'Dancing Script', cursive; font-size: 3.5rem; margin-bottom: 30px; color: var(--gold);">Doa & Ucapan Manis</h2>
        <form id="guestbook">
            <input type="text" id="nama" placeholder="Nama Anda" required>
            <textarea id="pesan" placeholder="Tulis doa dan ucapan terbaik untuk Piter & pasangan..." rows="4" required></textarea>
            <button type="submit" id="btnKirim">Kirim Ucapan</button>
        </form>
        
        <div id="display-wish" class="wish-container">
            </div>
    </section>

    <section id="gift">
        <h2 style="font-family: 'Dancing Script', cursive; font-size: 3.5rem; margin-bottom: 30px; color: var(--gold);">Digital Gift</h2>
        <p style="color: white; opacity: 0.8; max-width: 500px; margin: 0 auto;">Doa restu Anda sudah cukup bagi kami, namun jika ingin memberi tanda kasih:</p>
        <div class="bank-card">
            <p style="color: white;"><strong>BANK CENTRAL ASIA (BCA)</strong></p>
            <p id="rekening" style="font-size: 1.8rem; font-weight: 600; margin: 15px 0; color: var(--gold);">1234567890</p>
            <p style="color: white;">a.n Piter Andreas Sinaga</p>
            <div class="btn-copy" onclick="copyRek()">Salin Nomor Rekening</div>
        </div>
    </section>

    <footer style="padding: 40px; font-size: 0.8rem; opacity: 0.6; background: var(--dark); color: white;">
        <p>Created with Love by Alvin Phanestu &copy; 2026</p>
    </footer>

    <script src="https://www.gstatic.com/firebasejs/8.10.1/firebase-app.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.10.1/firebase-database.js"></script>

    <script>
        // 1. KONFIGURASI FIREBASE KAMU
        const firebaseConfig = {
            apiKey: "AIzaSyCtmSRH_Y1NtGaN1VNLb-1jfQaMum5lOPk",
            authDomain: "wedding-f13d8.firebaseapp.com",
            projectId: "wedding-f13d8",
            storageBucket: "wedding-f13d8.firebasestorage.app",
            messagingSenderId: "933008597878",
            appId: "1:933008597878:web:77d64d919b3bad44ded057",
            measurementId: "G-RYTS4YDPEH",
            databaseURL: "https://wedding-f13d8-default-rtdb.firebaseio.com/" 
        };

        firebase.initializeApp(firebaseConfig);
        const database = firebase.database();

        // 2. KIRIM UCAPAN
        const form = document.getElementById('guestbook');
        form.addEventListener('submit', function(e) {
            e.preventDefault();
            const nama = document.getElementById('nama').value;
            const pesan = document.getElementById('pesan').value;
            const btn = document.getElementById('btnKirim');

            btn.disabled = true;
            btn.innerText = "Mengirim...";

            database.ref('wishes').push({
                nama: nama,
                pesan: pesan,
                timestamp: Date.now()
            }).then(() => {
                form.reset();
                btn.disabled = false;
                btn.innerText = "Kirim Ucapan";
            });
        });

        // 3. TAMPILKAN UCAPAN (REAL-TIME)
        database.ref('wishes').on('value', (snapshot) => {
            const data = snapshot.val();
            const container = document.getElementById('display-wish');
            container.innerHTML = '';
            
            if (data) {
                const list = Object.values(data).reverse();
                list.forEach(item => {
                    const card = document.createElement('div');
                    card.className = "wish-card";
                    card.innerHTML = `<strong>${item.nama}</strong><br><p style="margin-top:5px; color:#555;">${item.pesan}</p>`;
                    container.appendChild(card);
                });
            }
        });

        // 4. SALIN REKENING
        function copyRek() {
            const text = document.getElementById('rekening').innerText;
            navigator.clipboard.writeText(text).then(() => {
                alert("Nomor Rekening Berhasil Disalin!");
            });
        }

        // 5. ANIMASI SAKURA
        function createSakura() {
            const sakura = document.createElement('div');
            sakura.classList.add('sakura');
            sakura.style.left = Math.random() * 100 + 'vw';
            sakura.style.animationDuration = Math.random() * 3 + 4 + 's';
            sakura.style.width = Math.random() * 10 + 10 + 'px';
            sakura.style.height = sakura.style.width;
            document.body.appendChild(sakura);
            setTimeout(() => { sakura.remove(); }, 7000);
        }
        setInterval(createSakura, 200);
    </script>
</body>
</html>
