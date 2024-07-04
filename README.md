<!DOCTYPE html>
<html>
<head>
    <title>COMBEE - Landing Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #FFF8DC; /* Fondo amarillo suave */
            margin: 0;
            padding: 0;
            overflow-x: hidden; /* Para evitar el desplazamiento horizontal */
        }
        .header {
            width: 100%;
            padding: 10px;
            background-color: #000; /* Color negro del encabezado */
            display: flex;
            justify-content: flex-start;
            align-items: center;
        }
        .header img {
            height: 50px;
            margin-left: 20px;
        }
        .slide-container {
            display: flex;
            flex-direction: row;
            overflow-x: hidden;
            scroll-snap-type: x mandatory;
            scroll-behavior: smooth;
            width: 100vw;
            height: 100vh;
            position: relative;
        }
        .slide {
            min-width: 100vw;
            height: 100vh;
            flex: 1 0 100%;
            scroll-snap-align: start;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
            box-sizing: border-box;
            transition: transform 1s ease;
        }
        .container {
            background-color: #ffffff;
            padding: 50px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 800px;
            text-align: center;
        }
        h1, h2 {
            color: #000; /* Color negro */
        }
        p {
            color: #333333;
            font-size: 18px;
        }
        .benefits ul {
            list-style-type: disc;
            margin: 10px 0;
            padding-left: 20px;
            text-align: left;
        }
        .map {
            width: 100%;
            height: 400px;
            background: url('mapa-placeholder.png') no-repeat center center;
            background-size: cover;
            position: relative;
        }
        .marker {
            position: absolute;
            background-color: #808080; /* Color gris */
            color: #fff;
            padding: 5px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 12px;
        }
        .marker:hover {
            background-color: #696969;
        }
        .marker1 { top: 20%; left: 30%; }
        .marker2 { top: 30%; left: 40%; }
        .marker3 { top: 40%; left: 50%; }
        .marker4 { top: 50%; left: 60%; }
        .marker5 { top: 60%; left: 70%; }
        .marker6 { top: 70%; left: 80%; }
        .marker7 { top: 80%; left: 90%; }
        .marker8 { top: 90%; left: 20%; }
        .marker9 { top: 20%; left: 80%; }
        .marker10 { top: 80%; left: 30%; }
        .pagination {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 10px;
        }
        .pagination div {
            width: 10px;
            height: 10px;
            background-color: #ccc;
            border-radius: 50%;
            cursor: pointer;
        }
        .pagination .active {
            background-color: #000;
        }
    </style>
</head>
<body>
    <div class="header">
        <img src="logo-combee.png" alt="COMBEE Logo"> <!-- Asegúrate de tener el logo guardado como logo-combee.png -->
    </div>
    <div class="slide-container" id="slide-container">
        <div class="slide">
            <div class="container">
                <h1>COMBEE</h1>
                <p>Bienvenido a la landing page de COMBEE. Estamos trabajando para ofrecerte la mejor experiencia de autos compartidos.</p>
            </div>
        </div>
        <div class="slide">
            <div class="container">
                <h2 class="section-title">Sobre COMBEE</h2>
                <p>En COMBEE, somos una plataforma de viajes compartidos que conecta personas que viajan a un mismo destino. Nos enfocamos en viajes de mediana y larga distancia, ofreciendo una alternativa de transporte más sostenible y colaborativa.</p>
                <p><strong>Disponibilidad en 2025:</strong> Nos complace anunciar que COMBEE estará disponible para todos los usuarios en 2025. ¡Prepárate para una nueva forma de moverte por la ciudad!</p>
            </div>
        </div>
        <div class="slide">
            <div class="container">
                <h2 class="section-title">Ventajas para los Usuarios</h2>
                <div class="benefits">
                    <ul>
                        <li>Acceso fácil a una variedad de autos.</li>
                        <li>Precios competitivos y opciones de pago flexibles.</li>
                        <li>Soporte al cliente 24/7 para una experiencia sin problemas.</li>
                        <li>Plataforma segura con tecnología avanzada de encriptación.</li>
                        <li>Opciones de alquiler por hora, día o semana según tus necesidades.</li>
                        <li>Contribución a la reducción de emisiones y a un futuro más verde.</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
    <div class="pagination" id="pagination"></div>
    <div class="map">
        <div class="marker marker1">Fácil acceso a autos</div>
        <div class="marker marker2">Precios competitivos</div>
        <div class="marker marker3">Soporte 24/7</div>
        <div class="marker marker4">Plataforma segura</div>
        <div class="marker marker5">Opciones flexibles</div>
        <div class="marker marker6">Reducción de emisiones</div>
        <div class="marker marker7">Economía sostenible</div>
        <div class="marker marker8">Transporte colaborativo</div>
        <div class="marker marker9">Tecnología avanzada</div>
        <div class="marker marker10">Beneficios personales</div>
    </div>
    <script>
        let slideIndex = 0;
        const slides = document.querySelectorAll('.slide');
        const totalSlides = slides.length;
        const slideContainer = document.getElementById('slide-container');
        const pagination = document.getElementById('pagination');

        for (let i = 0; i < totalSlides; i++) {
            const dot = document.createElement('div');
            dot.addEventListener('click', () => goToSlide(i));
            pagination.appendChild(dot);
        }

        const dots = document.querySelectorAll('.pagination div');

        function showSlides() {
            slideIndex++;
            if (slideIndex >= totalSlides) {
                slideIndex = 0;
            }
            slideContainer.style.transform = 'translateX(' + (-slideIndex * 100) + 'vw)';
            updatePagination();
        }

        function goToSlide(index) {
            slideIndex = index;
            slideContainer.style.transform = 'translateX(' + (-slideIndex * 100) + 'vw)';
            updatePagination();
        }

        function updatePagination() {
            dots.forEach(dot => dot.classList.remove('active'));
            dots[slideIndex].classList.add('active');
        }

        setInterval(showSlides, 5000); // Cambiar cada 5 segundos

        // Inicializar la paginación
        updatePagination();
    </script>
</body>
</html>
