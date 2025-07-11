
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pagina de gatitos</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f5;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #ff8c00;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .tabs {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            background-color: #333;
        }

        .tabs a {
            padding: 14px 20px;
            color: white;
            text-decoration: none;
            text-align: center;
            background-color: #444;
            margin: 2px;
            flex: 1 1 auto;
        }

        .tabs a:hover,
        .tabs a.active {
            background-color: #ff8c00;
        }

        .content {
            padding: 20px;
            display: none;
        }

        .content.active {
            display: block;
        }

        .image-gallery img,
        .video-gallery video {
            width: 100%;
            max-width: 400px;
            display: block;
            margin: 20px auto;
            border-radius: 8px;
        }

        form {
            max-width: 600px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
        }

        form input[type="text"],
        form textarea {
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            margin-bottom: 15px;
            border-radius: 5px;
            border: 1px solid #ccc;
            font-size: 1em;
        }

        form input[type="submit"] {
            padding: 10px;
            background-color: #ff8c00;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1em;
            cursor: pointer;
        }

        form input[type="submit"]:hover {
            background-color: #e67e00;
        }

        img {
            max-width: 100%;
            height: auto;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.5em;
            }

            .tabs {
                flex-direction: column;
                align-items: stretch;
            }

            .tabs a {
                flex: none;
                width: 100%;
                text-align: center;
            }

            .image-gallery img,
            .video-gallery video {
                max-width: 100%;
            }

            form {
                padding: 10px;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>Gatitos Adorables</h1>
        <p>¡Bienvenidos al mundo de los gatitos!</p>
    </header>

    <div class="tabs">
        <a href="#" class="tab-link active" data-tab="home">Inicio</a>
        <a href="#" class="tab-link" data-tab="gallery">Galería</a>
        <a href="#" class="tab-link" data-tab="videos">Videos</a>
        <a href="#" class="tab-link" data-tab="contact">Contacto</a>
    </div>

    <div id="home" class="content active">
        <h2>¡Bienvenidos a la página de los Gatitos!</h2>
        <p>Aquí encontrarás imágenes, videos y todo sobre los gatitos más lindos del mundo.</p>
        <img src="gato4L.jpg" alt="Gatito uno">
        <h3>Descripción</h3>
        <p>Los gatos son animales curiosos, juguetones y excelentes compañeros.</p>
        <img src="gato5.png" alt="Gatito dos">
        <p>Son mamíferos cubiertos de pelo, con gran capacidad de adaptabilidad.</p>
        <img src="gato6.jpg" alt="Gatito tres">
        <p>Se comunican mediante maullidos y son muy populares como mascotas.</p>
    </div>

    <div id="gallery" class="content">
        <h2>Galería de Imágenes</h2>
        <div class="image-gallery">
            <img src="gatito1.jpg" alt="Gatito 1 de Brasil">
            <p>Gatitos brasileños en adopción. Nacieron el 15 de marzo de 2025.</p>
            <img src="gatito2.jpg" alt="Gatito 2 de México">
            <p>Gatito mexicano en adopción. Nació el 20 de marzo de 2025.</p>
            <img src="gatito3.jpg" alt="Gatito 3 de Argentina">
            <p>Gatitos argentinos buscando hogar.</p>
        </div>
    </div>

    <div id="videos" class="content">
        <h2>Videos de Gatitos</h2>
        <div class="video-gallery">
            <video controls>
                <source src="WhatsApp Video 2025-04-01 at 5.20.44 PM.mp4" type="video/mp4">
                Tu navegador no soporta el video.
            </video>
            <video controls>
                <source src="WhatsApp Video 2025-04-01 at 6.19.51 PM.mp4" type="video/mp4">
                Tu navegador no soporta el video.
            </video>
        </div>
    </div>

    <div id="contact" class="content">
        <h2>Contacto</h2>
        <p>¿Tienes alguna duda sobre gatitos? ¡Escríbenos!</p>
        <form>
            <label for="name">Nombre:</label>
            <input type="text" id="name" name="name" required>
            <label for="message">Mensaje:</label>
            <textarea id="message" name="message" rows="5" required></textarea>
            <input type="submit" value="Enviar">
        </form>
        <img src="gato7.jpg" alt="Gatito contacto">
    </div>

    <script>
        const tabs = document.querySelectorAll('.tab-link');
        const contents = document.querySelectorAll('.content');

        tabs.forEach(tab => {
            tab.addEventListener('click', (e) => {
                e.preventDefault();
                tabs.forEach(t => t.classList.remove('active'));
                contents.forEach(c => c.classList.remove('active'));
                tab.classList.add('active');
                document.getElementById(tab.getAttribute('data-tab')).classList.add('active');
            });
        });
    </script>

</body>
</html>
