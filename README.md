<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rumah 3D dengan Teks AR</title>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
</head>
<body style="margin: 0; overflow: hidden;">
    <a-scene embedded arjs="sourceType: webcam; debugUIEnabled: false;">
        <!-- Objek 3D: Rumah -->
        <a-entity id="rumah" position="0 0 -5" scale="0.1 0.1 0.1">
            <!-- Atap Rumah (Limasan) -->
            <a-entity geometry="primitive: cone; radiusTop: 0; radiusBottom: 18; height: 15;" material="color: brown" position="0 17 0"></a-entity>
            
            <!-- Dinding Rumah Depan (Balok) -->
            <a-entity geometry="primitive: box; width: 30; height: 14; depth: 3" material="color: green" position="0 5.5 -15"></a-entity>
            
             
            <!-- Dinding Rumah Kiri (Balok) -->
            <a-entity geometry="primitive: box; width: 3; height: 14; depth: 30" material="color: green" position="-15 5.5 0"></a-entity>
            
            <!-- Dinding Rumah Kanan (Balok) -->
            <a-entity geometry="primitive: box; width: 3; height: 14; depth: 30" material="color: green" position="15 5.5 0"></a-entity>
            
            <!-- Lantai Rumah (Balok) -->
            <a-entity geometry="primitive: box; width: 31; height: 1.5; depth: 34.5" material="color: blue" position="0 -2 0"></a-entity>
            
            <!-- Pintu Rumah (Persegi Panjang) -->
            <a-entity geometry="primitive: box; width: 4; height: 8; depth: 0.5" material="color: white" position="0 2.5 15.5"></a-entity>
            <a-entity geometry="primitive: box; width: 1.5; height: 4; depth: 0.5" material="color: pink" position="0 2.5 15.5"></a-entity>
            <!-- Jendela Rumah Kiri (2 Lingkaran dalam Kotak) -->
            <a-entity geometry="primitive: box; width: 1.5; height: 4; depth: 0.5" material="color: white" position="-7.5 6.5 -15.5"></a-entity>
            <a-entity geometry="primitive: cylinder; radius: 1; height: 0.5" material="color: black" position="-7.5 6.5 -15.5"></a-entity>
            <a-entity geometry="primitive: cylinder; radius: 1; height: 0.5" material="color: black" position="-7.5 6.5 -15.5" rotation="0 90 0"></a-entity>
            
            <!-- Jendela Rumah Kanan (2 Lingkaran dalam Kotak) -->
            <a-entity geometry="primitive: box; width: 1.5; height: 4; depth: 0.5" material="color: white" position="7.5 6.5 -15.5"></a-entity>
            
            <a-entity geometry="primitive: cylinder; radius: 1; height: 0.5" material="color: black" position="7.5 6.5 -15.5"></a-entity>
            <a-entity geometry="primitive: cylinder; radius: 1; height: 0.5" material="color: black" position="7.5 6.5 -15.5" rotation="0 90 0"></a-entity>
            
            <!-- Teks AR untuk Setiap Objek -->
            <a-entity text="value: Pintu; align: center; wrapCount: 15; color: green; width: 4" position="0 2.5 18.5" scale="2 2 2"></a-entity>
            <a-entity text="value: Atap; align: center; wrapCount: 15; color: black; width: 4" position="0 20 0" scale="2 2 2"></a-entity>
            <a-entity text="value: Lantai; align: center; wrapCount: 15; color: white; width: 4" position="0 -2 0" scale="2 2 2"></a-entity>
            <a-entity text="value: Jendela; align: center; wrapCount: 15; color: brown; width: 4" position="-7.5 6.5 -14" scale="2 2 2"></a-entity>
            <a-entity text="value: Jendela; align: center; wrapCount: 15; color: brown; width: 4" position="7.5 6.5 -14" scale="2 2 2"></a-entity>
        </a-entity>

        <!-- Kamera AR -->
        <a-entity camera></a-entity>
    </a-scene>
</body>
</html>
