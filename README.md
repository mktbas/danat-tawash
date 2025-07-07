<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>مركز دانه الطواش لخدمات العمالة المساعدة ش.ذ.م.م</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
    <style>
        body {
            font-family: 'Tahoma', sans-serif;
            background-color: #f8f9fa;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 800px;
            margin: auto;
            padding: 20px;
        }
        h1 {
            color: #007b8f;
            font-size: 26px;
        }
        .info {
            margin-bottom: 20px;
            line-height: 1.8;
        }
        #map {
            height: 400px;
            border: 2px solid #ccc;
            border-radius: 8px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>مركز دانه الطواش لخدمات العمالة المساعدة ش.ذ.م.م</h1>
        <div class="info">
            <strong>رقم الهاتف:</strong> 0529621350<br>
            <strong>الموقع على Google Maps:</strong>
            <a href="https://maps.app.goo.gl/Y5bwNmQDaSfduwEYA" target="_blank">
                عرض على الخريطة
            </a>
        </div>
        <div id="map"></div>
    </div>

    <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
    <script>
        // الإحداثيات المستخرجة من رابط Google Maps الخاص بك
        var map = L.map('map').setView([25.253174, 55.297888], 17);
        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            maxZoom: 19,
            attribution: '© OpenStreetMap'
        }).addTo(map);

        L.marker([25.253174, 55.297888]).addTo(map)
            .bindPopup('مركز دانه الطواش')
            .openPopup();
    </script>
</body>
</html>
