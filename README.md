# nxBene.github.io

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>How to Install Datapacks</title>
    <style>
        body {
            background-color: #202124;
            font-family: Arial, sans-serif;
            color: white;
            text-align: center;
            margin: 0;
        }
        h1 {
            font-size: 60px;
            margin-top: 20px;
        }
        p {
            font-size: 35px;
            margin-top: 10px;
        }
        .image-container {
            display: inline-block;
            margin: 10px;
            cursor: pointer;
            transition: transform 0.2s; /* Übergangseffekt für die Vergrößerung */
        }
        .image-container:hover {
            transform: scale(1.04); /* Vergrößerung bei Hover */
        }
        .thumbnail {
            max-width: 400px; /* Maximalgröße der Miniaturansicht */
            height: auto;
            border-radius: 10px; /* Abgerundete Ecken */
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3); /* Schatten */
        }
        .image-caption {
            font-size: 16px;
            font-style: italic;
        }
        /* Lightbox-Stil */
        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 9999;
        }
        .lightbox img {
            max-width: 80%;
            max-height: 80%;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        .header {
            background-color: #00000000;
            padding: 10px 0;
            position: fixed;
            top: -100px; /* Anfangsposition oben */
            width: 100%;
            z-index: 1000;
            display: flex;
            align-items: center;
            transition: top 0.5s; /* Übergangseffekt für die Erscheinung */
        }
        .start-link {
            font-size: 30px;
            font-weight: bold;
            cursor: pointer;
            text-decoration: none;
            color: white;
            margin-left: 20px;
        }
        .separator {
            background-color: #202124;
            height: 1px;
            width: 100%;
        }
        .line {
            background-color: #202124;
            height: 2px;
            width: 100%;
            margin: 0;
        }

        .instagram-icon {
            width: 39px; /* Kleinere Breite */
            height: 39px; /* Kleinere Höhe */
            margin-left: 10px;
        }
    </style>
</head>
<body>
    <div class="header">
        <a href="https://page.nxBene.repl.co" class="start-link">
            nxBene
            <a href="https://instagram.com/nxbene" target="_blank" class="start-link"><img src="instagram_icon.png" alt="Instagram" class="instagram-icon">
        </a>
    </div>
    

    <div class="line"></div>
    <div class="separator"></div>
    <h1>How to Install the NoGmSwitch Datapack</h1>


    <p><br><br>1. Click on your World and click on edit</p>
    <div class="image-container">
        <img src="1.png" alt="Step 1" class="thumbnail lightbox-trigger">
    </div>
    <p>2. Click on open folder</p>
    <div class="image-container">
        <img src="2.png" alt="Step 2" class="thumbnail lightbox-trigger">
    </div>
    <p>3. This leads you to this window. Go to the datapacks folder</p>
    <div class="image-container">
        <img src="3.png" alt="Step 3" class="thumbnail lightbox-trigger">
    </div>
    <p class="image-caption">it works the same way on windows</p>
    <p>4. Put the file from GitHub into this folder</p>
    <div class="image-container">
        <img src="4.png" alt="Step 4" class="thumbnail lightbox-trigger">
    </div>

    <!-- Lightbox-Inhalt -->
    <div class="lightbox">
        <img src="" alt="" class="lightbox-img">
    </div>

    <script>
        // JavaScript, um Lightbox zu aktivieren
        const lightboxTriggers = document.querySelectorAll('.lightbox-trigger');
        const lightbox = document.querySelector('.lightbox');
        const lightboxImg = document.querySelector('.lightbox-img');

        // Zeige den Balken, wenn der Benutzer scrollt
        window.addEventListener('scroll', function() {
            const header = document.querySelector('.header');
            if (window.scrollY > 0) {
                header.style.top = '0';
            } else {
                header.style.top = '-100px'; // Anfangsposition oben
            }
        });

        lightboxTriggers.forEach(trigger => {
            trigger.addEventListener('click', () => {
                lightboxImg.src = trigger.src;
                lightboxImg.alt = trigger.alt;
                lightbox.style.display = 'block';
            });
        });

        lightbox.addEventListener('click', () => {
            lightbox.style.display = 'none';
        });
    </script>
</body>
</html>
