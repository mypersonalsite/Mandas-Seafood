<html lang="el">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Taverna O Mantas</title>

<style>
    body {
        margin: 0;
        font-family: Arial, sans-serif;
        background: radial-gradient(circle, #003a66 0%, #001a33 100%);
        color: white;
        text-align: center;
    }

    /* Logo */
    .logo-container {
        margin-top: 35px;
        margin-bottom: 10px;
    }
    .logo-title {
        font-size: 26px;
        font-weight: bold;
        letter-spacing: 1px;
    }
    .logo-sub {
        font-size: 18px;
        margin-top: 4px;
    }
    .logo-line {
        width: 140px;
        height: 2px;
        background-color: #ffffff;
        margin: 12px auto 25px auto;
        opacity: 0.85;
    }

    /* Buttons */
    .menu-button {
        width: 85%;
        background: #f2f8ff;
        color: #001a33;
        padding: 18px;
        margin: 12px auto;
        border-radius: 14px;
        border: 1px solid #bcd4e8;
        font-size: 20px;
        font-weight: bold;
        box-shadow: 0 4px 10px rgba(0,0,0,0.25);
        transition: transform 0.12s ease;
    }

    .menu-button:active {
        transform: scale(0.97);
    }

    /* Accordion */
    details {
        width: 85%;
        margin: 12px auto;
        background: #f2f8ff;
        color: #001a33;
        border-radius: 14px;
        border: 1px solid #bcd4e8;
        box-shadow: 0 4px 10px rgba(0,0,0,0.25);
        padding: 10px 16px;
    }

    summary {
        font-size: 20px;
        font-weight: bold;
        cursor: pointer;
        padding: 10px 0;
    }

    .item {
        text-align: left;
        padding: 6px 0;
        font-size: 17px;
        border-bottom: 1px solid #d0d0d0;
    }

    .item:last-child {
        border-bottom: none;
    }

    /* Language buttons */
    .lang-container {
        margin-top: 10px;
        margin-bottom: 25px;
    }

    .lang-btn {
        display: inline-block;
        background: #f2f8ff;
        color: #001a33;
        padding: 10px 18px;
        margin: 0 6px;
        border-radius: 14px;
        border: 1px solid #bcd4e8;
        font-weight: bold;
        box-shadow: 0 4px 10px rgba(0,0,0,0.25);
        transition: transform 0.12s ease;
    }

    .lang-btn:active {
        transform: scale(0.97);
    }

</style>
</head>

<body>

    <!-- LOGO -->
    <div class="logo-container">
        <div class="logo-title">TAVERNA O MANTAS</div>
        <div class="logo-sub">ΤΑΒΕΡΝΑ Ο ΜΑΝΤΑΣ</div>
        <div class="logo-line"></div>
    </div>

    <!-- LANG -->
    <div class="lang-container">
        <div class="lang-btn">GR</div>
        <div class="lang-btn">EN</div>
    </div>

    <!-- MAIN BUTTONS -->
    <button class="menu-button">Google Review ⭐</button>
    <button class="menu-button">Navigation 📍</button>

    <!-- ACCORDION EXAMPLE -->
    <details>
        <summary>Ορεκτικά</summary>
        <div class="item">Τζατζίκι</div>
        <div class="item">Φέτα ψητή</div>
        <div class="item">Πατάτες τηγανητές</div>
    </details>

    <details>
        <summary>Θαλασσινά</summary>
        <div class="item">Γαρίδες σαγανάκι</div>
        <div class="item">Καλαμάρι τηγανητό</div>
        <div class="item">Χταπόδι ψητό</div>
    </details>

</body>
</html>
