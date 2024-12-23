# Cuento-David-y-Daniel
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cuento de David y Daniel</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Fredoka+One&family=Montserrat:wght@300;400&display=swap');

        body {
            font-family: 'Montserrat', sans-serif;
        }

        .page {
            display: none;
            opacity: 0;
            transition: opacity 0.5s;
            position: relative;
        }

        .page-active {
            display: block;
            opacity: 1;
        }

        .page-img {
            width: 100%;
            height: auto;
        }

        .page-text {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(255, 255, 255, 0.8);
            padding: 10px;
            border-radius: 5px;
            font-family: 'Fredoka One', cursive;
            font-size: 1.5rem;
            text-align: center;
            width: 90%;
        }

        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            background-color: #f0f4f8;
            position: relative;
        }

        .nav-btn {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background-color: #ff6f61;
            color: white;
            padding: 0.5rem 1rem;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s;
            z-index: 10;
        }

        .nav-btn:hover {
            background-color: #ff4f41;
        }

        .nav-left {
            left: 10px;
        }

        .nav-right {
            right: 10px;
        }
    </style>
</head>
<body>
    <div id="app" class="container">
        <div id="page1" class="page page-active">
            <img src="1.jpeg" class="page-img" alt="Imagen 1">
            <p class="page-text">David y Daniel son dos hermanos que aman la aventura. David, con sus 8 años, siempre lleva puesta su camiseta del Atleti, y Daniel, de 4 años, no se separa de su jirafa de peluche. A los dos les encanta montar en bicicleta y jugar en el parque, siempre acompañados por su perro fiel.</p>
        </div>
        <div id="page2" class="page">
            <img src="2.jpeg" class="page-img" alt="Imagen 2">
            <p class="page-text">Una tarde soleada, David y Daniel salieron a dar un paseo en bicicleta junto con su perro y la jirafa de peluche de Daniel. Mientras recorrían el parque, de repente, la bicicleta de David desapareció en un abrir y cerrar de ojos.</p>
        </div>
        <div id="page3" class="page">
            <img src="3.jpeg" class="page-img" alt="Imagen 3">
            <p class="page-text">“¡No te preocupes, David! La encontraremos”, dijo Daniel con determinación. Con la ayuda del perro y la jirafa, comenzaron a seguir las huellas que los llevaban a través de un sendero misterioso lleno de aventuras.</p>
        </div>
        <div id="page4" class="page">
            <img src="4.jpeg" class="page-img" alt="Imagen 4">
            <p class="page-text">En su búsqueda, los hermanos encontraron a varios animales del bosque. Un conejo curioso, un zorro astuto y un búho sabio se unieron a la misión. Cada uno aportó algo útil: el conejo encontró más huellas, el zorro sugirió caminos alternativos, y el búho vigilaba desde las alturas.</p>
        </div>
        <div id="page5" class="page">
            <img src="5.jpeg" class="page-img" alt="Imagen 5">
            <p class="page-text">Finalmente, descubrieron que la bicicleta había sido tomada por una ardilla juguetona que la había llevado a su casa en un árbol. Con la ayuda de sus nuevos amigos del bosque, lograron recuperar la bicicleta de David.</p>
        </div>
        <div id="page6" class="page">
            <img src="6.jpeg" class="page-img" alt="Imagen 6">
            <p class="page-text">Contentos y agradecidos, David y Daniel regresaron a casa con su bicicleta recuperada. Para celebrar, organizaron una gran comida con su familia y los nuevos amigos del bosque, disfrutando de un festín de deliciosos platos.</p>
        </div>
        <button id="prevButton" class="nav-btn nav-left">Anterior</button>
        <button id="nextButton" class="nav-btn nav-right">Siguiente</button>
    </div>

    <script>
        const pages = document.querySelectorAll('.page');
        let currentPage = 0;

        document.getElementById('nextButton').addEventListener('click', () => {
            pages[currentPage].classList.remove('page-active');
            currentPage = (currentPage + 1) % pages.length;
            pages[currentPage].classList.add('page-active');
        });

        document.getElementById('prevButton').addEventListener('click', () => {
            pages[currentPage].classList.remove('page-active');
            currentPage = (currentPage - 1 + pages.length) % pages.length;
            pages[currentPage].classList.add('page-active');
        });
    </script>
</body>
</html>
