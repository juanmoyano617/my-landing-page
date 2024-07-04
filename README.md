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
            background-color: #FFD700; /* Color amarillo del encabezado */
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
            overflow-x: auto;
            scroll-snap-type: x mandatory;
        }
        .slide {
            min-width: 100%;
            height: 100vh;
            flex: 1 0 100%;
            scroll-snap-align: start;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
            box-sizing: border-box;
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
            color: #FFD700; /* Color amarillo */
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
    </style>
</head>
<body>
    <div class="header">
        <img src="logo-combee.png" alt="COMBEE Logo"> <!-- Asegúrate de tener el logo guardado como logo-combee.png -->
    </div>
    <div class="slide-container">
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
</body>
</html>
