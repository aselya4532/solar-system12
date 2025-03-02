<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Юпитер в WebAR</title>
    
    <!-- Подключаем A-Frame и AR.js -->
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/jeromeetienne/AR.js/aframe/build/aframe-ar.min.js"></script>
</head>
<body style="margin: 0; overflow: hidden;">

    <a-scene embedded arjs>
        <!-- Загружаем модель Юпитера -->
        <a-assets>
            <a-asset-item id="jupiter" 
                src="https://raw.githubusercontent.com/aselya4532/solarsystem/main/solar-system12.git>
            </a-asset-item>
        </a-assets>

        <!-- Юпитер -->
        <a-entity gltf-model="#jupiter" position="0 0 -3" scale="0.5 0.5 0.5"
            animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        </a-entity>

        <!-- Камера -->
        <a-camera position="0 1.6 0"></a-camera>
    </a-scene>

</body>
</html>
