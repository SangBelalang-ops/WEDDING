<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Wedding of Piter & ???</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Playfair+Display:ital,wght@0,400;1,400&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    <style>
        :root { --gold: #b8860b; --dark: #2c3e50; --cream: #fffaf0; --pink: #ffb6c1; }
        * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
        
        /* Pointer Mouse Love */
        body { 
            font-family: 'Poppins', sans-serif; 
            background-color: var(--cream); 
            color: var(--dark); 
            overflow-x: hidden; 
            cursor: url('https://cdn.pixabay.com/photo/2012/04/18/13/21/heart-37009_1280.png'), auto; /* Fallback jika link mati, gunakan 'auto' */
            cursor: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="%23b8860b" d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>'), auto; /* Link SVG Love Gold */
        }

        /* Navigation */
        nav { position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%); background: rgba(255,255,255,0.95); 
               padding: 10px 20px; border-radius: 30px; display: flex; gap: 20px; z-index: 1000; box-shadow: 0 4px 15px rgba(0,0,0,0.1); border: 1px solid var(--gold); }
        nav a { text-decoration: none; color: var(--dark); font-size: 0.85rem; font-weight: 600; font-family: 'Poppins', sans-serif; transition: 0.3s; }
        nav a:hover { color: var(--gold); }

        /* Sections */
        section { padding: 100px 20px; text-align: center; min-height: 100vh; display: flex; flex-direction: column; justify-content: center; }
        
        /* Font Bagus */
        .hero { background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1519741497674-611481863552?auto=format&fit=crop&w=1500&q=80') center/cover; color: white; }
        .hero p { font-family: 'Playfair Display', serif; letter-spacing: 5px; font-size: 1rem; text-transform: uppercase; }
        h1 { font-family: 'Dancing Script', cursive; font-size: 5.5rem; color: var(--gold); text-shadow: 2px 2px 4px rgba(0,0,0,0.3); }
        .hero .date { font-family: 'Playfair Display', serif; font-size: 1.5rem; margin-top: 20px; border-top: 1px solid white; border-bottom: 1px solid white; display: inline-block; padding: 10px 20px; }
        
        h2 { font-family: 'Dancing Script', cursive; font-size: 3.5rem; margin-bottom: 30px; color: var(--dark); }

        /* Gallery */
        .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; max-width: 900px; margin: 0 auto; padding: 20px; }
        .gallery-grid img { width: 100%; border-radius: 12px; transition: 0.5s; cursor: pointer; border: 4px solid white; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }
        .gallery-grid img:hover { transform: scale(1.08) rotate(2deg); box-shadow: 0 10px 20px rgba(0,0,0,0.2); border-color: var(--pink); }

        /* Guestbook Form */
        form { max-width: 500px; margin: 0 auto; display: flex; flex-direction: column; gap: 15px; background: white; padding: 30px; border-radius: 15px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); }
        input, textarea { padding: 15px; border: 1px solid #ddd; border-radius: 8px; font-family: 'Poppins', sans-serif; font-size: 0.9rem; transition: 0.3s; }
        input:focus, textarea:focus { border-color: var(--pink); outline: none; box-shadow: 0 0 5px rgba(255,182,193,0.5); }
        button { background: var(--gold); color: white; border: none; padding: 15px; border-radius: 8px; cursor: pointer; font-weight: bold; font-family: 'Poppins', sans-serif; transition: 0.3s; }
        button:hover { background: #966d09; transform: translateY(-2px); }

        /* Digital Gift */
        .bank-card { background: white; padding: 30px; border-radius: 15px; max-width: 450px; margin: 30px auto; border: 2px dashed var(--pink); box-shadow: 0 4px 15px rgba(0,0,0,0.05); }
        .bank-card p { font-family: 'Playfair Display', serif; margin-bottom: 5px; }
        .bank-card #rekening { font-family: 'Poppins', sans-serif; font-weight: 600; font-size: 1.3rem; color: var(--dark); }
        .btn-copy { font-size: 0.8rem; background: #fdf2f2; color: #e74c3c; padding: 8px 15px; border-radius: 20px; cursor: pointer; display: inline-block; margin-top: 10px; font-weight: 600; transition: 0.3s; }
        .btn-copy:hover { background: #fde2e2; }

        footer { padding: 50px; font-size: 0.8rem; opacity: 0.7; font-family: 'Poppins', sans-serif; }

        /* Animasi Sakura Berguguran */
        .sakura { position: absolute; background-color: var(--pink); border-radius: 100% 0 100% 0; opacity: 0.6; animation: fall 10s infinite linear; pointer-events: none; z-index: 100; }
        @keyframes fall {
            0% { transform: translate(0, -10px) rotate(0deg); opacity: 0.8; }
            100% { transform: translate(100px, 100vh) rotate(360deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <script>
        function createSakura() {
            const sakura = document.createElement('div');
            sakura.classList.add('sakura');
            sakura.style.left = Math.random() * 100 + 'vw';
            sakura.style.animationDuration = Math.random() * 5 + 5 + 's'; // 5-10s
            sakura.style.width = Math.random() * 10 + 10 + 'px'; // 10-20px
            sakura.style.height = sakura.style.width;
            document.body.appendChild(sakura);
            setTimeout(() => { sakura.remove(); }, 10000); // Hapus setelah 10s
        }
        setInterval(createSakura, 200); // Buat setiap 0.2s
    </script>

    <nav>
        <a href="#home">Home</a>
        <a href="#gallery">Gallery</a>
        <a href="#wish">Wish</a>
        <a href="#gift">Gift</a>
    </nav>

    <section id="home" class="hero">
        <p class="animate__animated animate__fadeInDown">THE WEDDING OF</p>
        <h1 class="animate__animated animate__zoomIn">Piter & ???</h1>
        <div class="date animate__animated animate__fadeInUp">16 Mei 2026</div>
    </section>

    <section id="gallery">
        <h2>Pre-Wedding Gallery</h2>
        <div class="gallery-grid">
            <img src="https://images.unsplash.com/photo-1583939003579-730e3918a45a?w=600" alt="Prewed 1">
            <img src="https://images.unsplash.com/photo-1511285560929-80b456fea0bc?w=600" alt="Prewed 2">
            <img src="https://images.unsplash.com/photo-1494774157365-9e04c6720e47?w=600" alt="Prewed 3">
            <img src="https://images.unsplash.com/photo-1522673607200-1648832cee98?w=600" alt="Prewed 4">
        </div>
    </section>

    <section id="wish" style="background: white;">
        <h2>Kirim Ucapan & Doa</h2>
        <form id="guestbook">
            <input type="text" placeholder="Nama Anda" required>
            <textarea placeholder="Tulis doa dan ucapan manis untuk Piter & pasangan..." rows="4" required></textarea>
            <button type="submit">Kirim Ucapan</button>
        </form>
        <div id="display-wish" style="margin-top: 30px; font-style: italic; color: #666;">
            </div>
    </section>

    <section id="gift">
        <h2>Digital Gift</h2>
        <p style="max-width: 500px; margin: 0 auto; color: #666;">Doa restu Anda sudah cukup bagi kami, namun jika ingin memberi tanda kasih, silakan melalui:</p>
        <div class="bank-card">
            <p><strong>BANK CENTRAL ASIA (BCA)</strong></p>
            <p id="rekening">1234567890</p>
            <p>a.n Piter Andreas Sinaga</p>
            <span class="btn-copy" onclick="copyRek()">Salin No. Rekening</span>
        </div>
    </section>

    <footer>
        <p>Created with Love & Code by Alvin Phanestu | 2026</p>
    </footer>

    <script>
        // Fungsi Salin Rekening
        function copyRek() {
            const rek = document.getElementById('rekening').innerText;
            navigator.clipboard.writeText(rek);
            alert("Nomor Rekening Berhasil Disalin!");
        }

        // Simulasi Form Ucapan
        document.getElementById('guestbook').addEventListener('submit', function(e) {
            e.preventDefault();
            alert("Terima kasih atas ucapannya! (Data tersimpan di simulasi)");
            this.reset();
        });
    </script>
</body>
</html>
