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
         

