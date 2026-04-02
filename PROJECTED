<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Wedding of Piter & ???</title>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    <style>
        :root { --gold: #b8860b; --dark: #2c3e50; --cream: #fffaf0; }
        * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
        body { font-family: 'Montserrat', sans-serif; background-color: var(--cream); color: var(--dark); }

        /* Navigation */
        nav { position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%); background: rgba(255,255,255,0.9); 
               padding: 10px 20px; border-radius: 30px; display: flex; gap: 20px; z-index: 1000; box-shadow: 0 4px 15px rgba(0,0,0,0.1); }
        nav a { text-decoration: none; color: var(--dark); font-size: 0.8rem; font-weight: 600; }

        /* Sections */
        section { padding: 80px 20px; text-align: center; min-height: 100vh; display: flex; flex-direction: column; justify-content: center; }
        .hero { background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1519741497674-611481863552?auto=format&fit=crop&w=1500&q=80') center/cover; color: white; }
        
        h1 { font-family: 'Great Vibes', cursive; font-size: 4rem; color: var(--gold); }
        h2 { font-family: 'Great Vibes', cursive; font-size: 3rem; margin-bottom: 20px; }

        /* Gallery */
        .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 10px; max-width: 800px; margin: 0 auto; }
        .gallery-grid img { width: 100%; border-radius: 8px; transition: 0.3s; cursor: pointer; }
        .gallery-grid img:hover { transform: scale(1.05); }

        /* Guestbook Form */
        form { max-width: 500px; margin: 0 auto; display: flex; flex-direction: column; gap: 10px; }
        input, textarea { padding: 12px; border: 1px solid #ccc; border-radius: 8px; font-family: inherit; }
        button { background: var(--gold); color: white; border: none; padding: 15px; border-radius: 8px; cursor: pointer; font-weight: bold; }

        /* Digital Gift */
        .bank-card { background: white; padding: 20px; border-radius: 15px; max-width: 400px; margin: 20px auto; border: 1px dashed var(--gold); }
        .btn-copy { font-size: 0.7rem; background: #eee; padding: 5px 10px; border-radius: 5px; cursor: pointer; }

        footer { padding: 50px; font-size: 0.8rem; opacity: 0.7; }
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
        <p>THE WEDDING OF</p>
        <h1 class="animate__animated animate__fadeIn">Piter & ???</h1>
        <p>16 Mei 2026</p>
    </section>

    <section id="gallery">
        <h2>Pre-Wedding Gallery</h2>
        <div class="gallery-grid">
            <img src="https://images.unsplash.com/photo-1583939003579-730e3918a45a?w=400" alt="Prewed 1">
            <img src="https://images.unsplash.com/photo-1511285560929-80b456fea0bc?w=400" alt="Prewed 2">
            <img src="https://images.unsplash.com/photo-1494774157365-9e04c6720e47?w=400" alt="Prewed 3">
            <img src="https://images.unsplash.com/photo-1522673607200-1648832cee98?w=400" alt="Prewed 4">
        </div>
    </section>

    <section id="wish" style="background: white;">
        <h2>Kirim Ucapan</h2>
        <form id="guestbook">
            <input type="text" placeholder="Nama Anda" required>
            <textarea placeholder="Tulis doa dan ucapan..." rows="4" required></textarea>
            <button type="submit">Kirim Ucapan</button>
        </form>
        <div id="display-wish" style="margin-top: 30px; font-style: italic; color: #666;">
            </div>
    </section>

    <section id="gift">
        <h2>Digital Gift</h2>
        <p>Doa restu Anda sudah cukup bagi kami, namun jika ingin memberi tanda kasih, silakan melalui:</p>
        <div class="bank-card">
            <p><strong>BANK CENTRAL ASIA (BCA)</strong></p>
            <p id="rekening">1234567890</p>
            <p>a.n Piter Andreas Sinaga</p>
            <span class="btn-copy" onclick="copyRek()">Salin No. Rekening</span>
        </div>
    </section>

    <footer>
        <p>Created by Alvin Phanestu | 2026</p>
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
