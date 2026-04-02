<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Favorite Person</title>
    <style>
        :root {
            --primary-pink: #ff4d6d;
            --soft-white: #fff5f5;
        }

        body {
            margin: 0;
            font-family: 'Georgia', serif;
            background-color: var(--soft-white);
            color: #333;
            overflow-x: hidden;
        }

        /* Floating Hearts Animation */
        .hearts-bg {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            background: linear-gradient(rgba(255, 255, 255, 0.6), rgba(255, 255, 255, 0.6)), 
                        url('https://images.unsplash.com/photo-1516589174184-c68526516282?auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
        }

        h1 { font-size: 4rem; color: var(--primary-pink); margin: 0; text-shadow: 2px 2px 4px rgba(0,0,0,0.1); }
        
        .music-section {
            padding: 50px 20px;
            background: white;
            border-radius: 20px;
            margin: -50px 20px 50px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        .photo-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 15px;
            padding: 20px;
            max-width: 1200px;
            margin: auto;
        }

        .photo-grid img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .photo-grid img:hover { transform: scale(1.03); }

        footer { padding: 40px; text-align: center; color: #999; }
    </style>
</head>
<body>

    <div class="hearts-bg" id="hearts"></div>

    <section class="hero">
        <h1>Forever & Always</h1>
        <p style="font-size: 1.5rem; font-style: italic;">"You are my greatest adventure."</p>
    </section>

    <section class="music-section">
        <h2>Our Soundtrack</h2>
        <p>Press play to set the mood:</p>
        <iframe width="100%" height="150" src="https://www.youtube.com/embed/jfKfPfyJRdk" frameborder="0" allow="autoplay; encrypted-media" style="border-radius:12px;"></iframe>
    </section>

    <h2 style="text-align: center; color: var(--primary-pink);">Our Memories</h2>
    <div class="photo-grid">
        <img src="https://images.unsplash.com/photo-1522673607200-16488352435b?auto=format&fit=crop&w=500&q=80" alt="Memory 1">
        <img src="https://images.unsplash.com/photo-1494774157365-9e04c6720e47?auto=format&fit=crop&w=500&q=80" alt="Memory 2">
        <img src="https://images.unsplash.com/photo-1529333166437-7750a6dd5a70?auto=format&fit=crop&w=500&q=80" alt="Memory 3">
    </div>

    <footer>
        <p>Made with ❤️ &mdash; 2026</p>
    </footer>

    <script>
        // Simple script to add floating emojis
        const heartContainer = document.getElementById('hearts');
        function createHeart() {
            const heart = document.createElement('div');
            heart.innerHTML = '🌸';
            heart.style.position = 'absolute';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.top = '100vh';
            heart.style.fontSize = Math.random() * 20 + 10 + 'px';
            heart.style.opacity = Math.random();
            heart.style.transition = 'transform 5s linear, opacity 5s linear';
            
            heartContainer.appendChild(heart);

            setTimeout(() => {
                heart.style.transform = 'translateY(-110vh)';
                heart.style.opacity = '0';
            }, 100);

            setTimeout(() => { heart.remove(); }, 6000);
        }
        setInterval(createHeart, 500);
    </script>
</body>
</html>
<img width="896" height="1195" alt="1000101897" src="https://github.com/user-attachments/assets/dbfbf767-a012-4642-9f56-4973a250ec4a" />
