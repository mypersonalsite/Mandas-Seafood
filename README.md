<!DOCTYPE html>
<html lang="el">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Mantas Restaurant | Fish & Seafood</title>
<meta name="description" content="Mantas Restaurant - Φρέσκα ψάρια, θαλασσινά, ορεκτικά και διεθνείς γεύσεις σε premium μενού.">
<meta name="keywords" content="Mantas, ψαροταβέρνα, ψάρια, θαλασσινά, Ευόσμος, εστιατόριο, seafood, fish, restaurant">
<meta name="author" content="Mantas Restaurant">
<meta property="og:title" content="Mantas Restaurant">
<meta property="og:description" content="Φρέσκα ψάρια & θαλασσινά σε premium περιβάλλον.">
<meta property="og:type" content="website">

<link rel="manifest" href="manifest.json">

<style>
/* ---------------------------------------------------
   GLOBAL
--------------------------------------------------- */
* {
    transition: background 0.3s, color 0.3s, border 0.3s;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #000814;
    background-image: url("waves.svg");
    background-size: cover;
    background-attachment: fixed;
    animation: waveMove 18s linear infinite;
    color: white;
    text-align: center;
}

@keyframes waveMove {
    from { background-position: 0 0; }
    to { background-position: 1000px 0; }
}

body.light {
    background: #f0f2f5;
    color: #111;
}

/* ---------------------------------------------------
   LOADING SCREEN
--------------------------------------------------- */
#loader {
    position: fixed;
    inset: 0;
    background: #000814;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 9999;
    animation: fadeOut 1.2s ease forwards;
    animation-delay: 1.2s;
}

.loader-logo {
    width: 140px;
    opacity: 0;
    animation: popIn 1s ease forwards;
}

@keyframes popIn {
    from { opacity: 0; transform: scale(0.7); }
    to { opacity: 1; transform: scale(1); }
}

@keyframes fadeOut {
    to { opacity: 0; visibility: hidden; }
}

/* ---------------------------------------------------
   HEADER
--------------------------------------------------- */
header {
    padding: 40px 20px;
    animation: fadeDown 0.8s ease-out;
    position: relative;
}

@keyframes fadeDown {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
}

.logo {
    width: 160px;
    margin-bottom: 10px;
    filter: drop-shadow(0px 4px 10px rgba(0,0,0,0.4));
    transition: transform 0.2s ease-out;
}

.tagline {
    margin-top: -5px;
    font-size: 15px;
    opacity: 0.75;
    letter-spacing: 1px;
}

/* ---------------------------------------------------
   LANGUAGE BUTTON
--------------------------------------------------- */
.lang-btn {
    position: absolute;
    top: 20px;
    left: 20px;
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.3);
    padding: 8px 14px;
    border-radius: 8px;
    color: white;
    cursor: pointer;
    backdrop-filter: blur(6px);
}

/* ---------------------------------------------------
   CATEGORY BUTTONS
--------------------------------------------------- */
.category-buttons {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 12px;
    margin: 30px auto;
    max-width: 900px;
    position: sticky;
    top: 0;
    padding: 15px 0;
    background: rgba(0,0,0,0.35);
    backdrop-filter: blur(10px);
    z-index: 50;
}

.category-buttons button {
    background: rgba(255,255,255,0.12);
    border: 1px solid rgba(255,255,255,0.25);
    padding: 12px 24px;
    border-radius: 10px;
    color: white;
    font-size: 16px;
    cursor: pointer;
    transition: 0.25s;
    backdrop-filter: blur(8px);
}

.category-buttons button:hover {
    background: rgba(255,255,255,0.25);
    transform: translateY(-3px) scale(1.03);
}

/* ---------------------------------------------------
   MENU ITEMS
--------------------------------------------------- */
.menu-container {
    max-width: 900px;
    margin: 40px auto;
    padding: 20px;
    animation: fadeIn 0.4s ease;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(6px); }
    to { opacity: 1; transform: translateY(0); }
}

.menu-item {
    background: rgba(255,255,255,0.10);
    border: 1px solid rgba(255,255,255,0.18);
    padding: 18px;
    border-radius: 14px;
    margin-bottom: 20px;
    display: flex;
    gap: 18px;
    align-items: center;
    transition: 0.25s;
}

.menu-item:hover {
    background: rgba(255,255,255,0.18);
    transform: translateY(-2px);
}

.menu-item img {
    width: 115px;
    height: 95px;
    object-fit: cover;
    border-radius: 10px;
    box-shadow: 0px 4px 10px rgba(0,0,0,0.35);
}

.menu-text h3 {
    margin: 0;
    font-size: 18px;
    font-weight: bold;
}

.menu-text p {
    margin: 5px 0;
    font-size: 14px;
    opacity: 0.9;
}

.price {
    font-size: 17px;
    font-weight: bold;
    color: #7df9ff;
    margin-top: 6px;
}

/* ---------------------------------------------------
   FLOATING NAV
--------------------------------------------------- */
.bottom-nav {
    position: fixed;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    background: rgba(255,255,255,0.15);
    backdrop-filter: blur(10px);
    padding: 10px 20px;
    border-radius: 40px;
    display: flex;
    gap: 20px;
    border: 1px solid rgba(255,255,255,0.25);
}

.bottom-nav button {
    background: none;
    border: none;
    font-size: 22px;
    cursor: pointer;
    color: white;
}

/* ---------------------------------------------------
   FISH ANIMATION
--------------------------------------------------- */
.fish, .fish2 {
    position: fixed;
    width: 60px;
    height: 30px;
    background: url("fish-icon.png") no-repeat center/contain;
    top: 40%;
    animation: swim 12s linear infinite;
    opacity: 0.25;
}

.fish2 {
    top: 70%;
    animation-duration: 18s;
    opacity: 0.18;
}

@keyframes swim {
    from { left: -100px; }
    to { left: 110%; }
}
</style>
</head>

<body>

<!-- LOADING SCREEN -->
<div id="loader">
    <img src="logo.png" class="loader-logo">
</div>

<!-- FISH -->
<div class="fish"></div>
<div class="fish fish2"></div>

<header>
    <button id="langToggle" class="lang-btn">GR / EN</button>
    <img src="logo.png" class="logo" alt="Mantas Logo">
    <h1>Mantas Restaurant</h1>
    <p class="tagline">Fresh Fish • Seafood • International Cuisine</p>
</header>

<div class="category-buttons" id="categoryButtons"></div>

<div class="menu-container" id="menuContainer"></div>

<!-- FLOATING NAV -->
<div class="bottom-nav">
    <button onclick="scrollToTop()">⬆️</button>
    <button onclick="renderCategoryButtons()">📂</button>
    <button onclick="document.body.classList.toggle('light')">🌗</button>
</div>

<audio id="tapSound" src="tap.mp3" preload="auto"></audio>

<script>
const MENU_DATA = {

  /* -----------------------------------------
     ΟΡΕΚΤΙΚΑ | APPETIZERS
  ----------------------------------------- */
  appetizers: {
    title: "Ορεκτικά | Appetizers",
    subtitle: "Ζεστά και κρύα ορεκτικά από Ελλάδα και διεθνή κουζίνα.",
    items: [
      { name: "Πατάτες Τηγανητές", desc: "Φρέσκες, χειροποίητες, τραγανές.", price: "3.00€", img: "french-fries.jpg" },
      { name: "Σκορδαλιά", desc: "Παραδοσιακή ελληνική σκορδαλιά με πατάτα.", price: "3.50€", img: "skordalia.jpg" },
      { name: "Παντζάρια", desc: "Βραστά παντζάρια με ξύδι και λάδι.", price: "3.50€", img: "beetroot-salad.jpg" },
      { name: "Stamnagathi", desc: "Άγρια χόρτα εποχής.", price: "4.00€", img: "stamnagathi.jpg" },
      { name: "Sausages", desc: "Ψητά λουκάνικα.", price: "5.00€", img: "sausages.jpg" },
      { name: "Marinated Anchovies", desc: "Γαύρος μαρινάτος.", price: "5.00€", img: "marinated-anchovies.jpg" },
      { name: "Edamame", desc: "Ιαπωνικό ορεκτικό με αλάτι.", price: "260₹", img: "" },
      { name: "Spicy Edamame", desc: "Πικάντικο edamame.", price: "280₹", img: "" },
      { name: "Gyoza", desc: "Ιαπωνικά dumplings.", price: "320₹", img: "" },
      { name: "Spicy Gyoza", desc: "Πικάντικα dumplings.", price: "340₹", img: "" },
      { name: "Chicken Karaage", desc: "Ιαπωνικό τηγανητό κοτόπουλο.", price: "360₹", img: "" },
      { name: "Spicy Chicken Karaage", desc: "Πικάντικο τηγανητό κοτόπουλο.", price: "380₹", img: "" }
    ]
  },

  /* -----------------------------------------
     ΣΑΛΑΤΕΣ | SALADS
  ----------------------------------------- */
  salads: {
    title: "Σαλάτες | Salads",
    subtitle: "Φρέσκες σαλάτες από Ελλάδα και διεθνή κουζίνα.",
    items: [
      { name: "Greek Salad", desc: "Ντομάτα, αγγούρι, φέτα, ελιές.", price: "7.00€", img: "greek-salad.jpg" },
      { name: "Wakame", desc: "Ιαπωνική σαλάτα με φύκια.", price: "6,000₩", img: "" },
      { name: "Seafood Salad", desc: "Ανάμεικτα θαλασσινά με λαχανικά.", price: "9,000₩", img: "" },
      { name: "Noodle Salad", desc: "Δροσερή σαλάτα με noodles.", price: "6,000₩", img: "" },
      { name: "Greens with Olive Oil", desc: "Φρέσκα χόρτα με ελαιόλαδο.", price: "6,000₩", img: "" },
      { name: "Caesar Salad", desc: "Κλασική Caesar με dressing.", price: "6,000₩", img: "" }
    ]
  },

  /* -----------------------------------------
     ΤΗΓΑΝΗΤΑ | FRIED
  ----------------------------------------- */
  fried: {
    title: "Τηγανητά | Fried",
    subtitle: "Τραγανά πιάτα τηγανητής κουζίνας.",
    items: [
      { name: "Καλαμάρι Τηγανητό", desc: "Φρέσκο καλαμάρι, τραγανό.", price: "11.50€", img: "fried-calamari.jpg" },
      { name: "Fried Fish Platter", desc: "Ποικιλία τηγανητών ψαριών.", price: "12.00€", img: "fried-fish-1.jpg" },
      { name: "Fried Fish Platter 2", desc: "Τηγανητά ψάρια ημέρας.", price: "12.00€", img: "fried-fish-2.jpg" },
      { name: "Chicken Pakoda", desc: "Ινδικό τηγανητό κοτόπουλο.", price: "80.00", img: "" },
      { name: "Chicken 65", desc: "Πικάντικο τηγανητό κοτόπουλο.", price: "80.00", img: "" },
      { name: "Chicken Manchurian", desc: "Ινδοκινέζικο τηγανητό πιάτο.", price: "80.00", img: "" }
    ]
  },

  /* -----------------------------------------
     ΘΑΛΑΣΣΙΝΑ | SEAFOOD
  ----------------------------------------- */
  seafood: {
    title: "Θαλασσινά | Seafood",
    subtitle: "Φρέσκα θαλασσινά από Ελλάδα και διεθνή κουζίνα.",
    items: [
      { name: "Χταπόδι Κρασάτο", desc: "Μαλακό χταπόδι σε κόκκινη σάλτσα.", price: "13.00€", img: "octopus-stew.jpg" },
      { name: "Cuttlefish Stew", desc: "Σουπιά μαγειρεμένη με μυρωδικά.", price: "12.00€", img: "cuttlefish-stew.jpg" },
      { name: "Traditional Squid with Fennel", desc: "Καλαμάρι με μάραθο.", price: "11.00€", img: "" },
      { name: "Octopus in Wine Sauce", desc: "Χταπόδι σε σάλτσα κρασιού.", price: "12.50€", img: "" },
      { name: "Marinated Anchovies", desc: "Γαύρος μαρινάτος.", price: "5.00€", img: "marinated-anchovies.jpg" }
    ]
  },

  /* -----------------------------------------
     ΨΑΡΙΑ | FISH
  ----------------------------------------- */
  fish: {
    title: "Ψάρια | Fish",
    subtitle: "Φρέσκα ψάρια ημέρας.",
    items: [
      { name: "Τσιπούρα Ψητή", desc: "Φρέσκια τσιπούρα στη σχάρα.", price: "12.00€", img: "grilled-fish-1.jpg" },
      { name: "Λαβράκι Ψητό", desc: "Λαβράκι στη σχάρα.", price: "13.00€", img: "grilled-fish-2.jpg" },
      { name: "Σαρδέλες Ψητές", desc: "Φρέσκες σαρδέλες στη σχάρα.", price: "9.00€", img: "sardines-grilled.jpg" },
      { name: "Κουτσομούρα", desc: "Φρέσκια κουτσομούρα τηγανητή.", price: "14.00€", img: "koutsomoura.jpg" },
      { name: "Fish Steaks", desc: "Μπριζόλες ψαριού στη σχάρα.", price: "14.00€", img: "fish-steaks-grilled.jpg" }
    ]
  },

  /* -----------------------------------------
     ΨΗΤΑ | GRILLED
  ----------------------------------------- */
  grilled: {
    title: "Ψητά | Grilled",
    subtitle: "Ψητά πιάτα από θάλασσα και στεριά.",
    items: [
      { name: "Grilled Fish Platter", desc: "Ποικιλία ψητών ψαριών.", price: "15.00€", img: "grilled-fish-3.jpg" },
      { name: "Grilled Fish Platter 2", desc: "Φρέσκα ψάρια στη σχάρα.", price: "15.00€", img: "grilled-fish-4.jpg" },
      { name: "Grilled Shrimp", desc: "Γαρίδες στη σχάρα.", price: "12.00€", img: "grilled-shrimp.jpg" },
      { name: "Chicken Tikka", desc: "Ινδικό κοτόπουλο στη σχάρα.", price: "100.00", img: "" },
      { name: "Chicken Tandoori", desc: "Κοτόπουλο με μπαχαρικά.", price: "100.00", img: "" }
    ]
  },

  /* -----------------------------------------
     ΖΥΜΑΡΙΚΑ | PASTA
  ----------------------------------------- */
  pasta: {
    title: "Ζυμαρικά | Pasta",
    subtitle: "Ζυμαρικά με θαλασσινά και διεθνείς γεύσεις.",
    items: [
      { name: "Μακαρονάδα με Γαρίδες", desc: "Σπαγγέτι με γαρίδες και λαχανικά.", price: "12.00€", img: "shrimp-pasta.jpg" },
      { name: "Seafood Pasta", desc: "Ζυμαρικά με ανάμεικτα θαλασσινά.", price: "11.00€", img: "" },
      { name: "Noodles with Vegetables", desc: "Νουντλς με λαχανικά.", price: "6,000₩", img: "" }
    ]
  },

  /* -----------------------------------------
     ΜΑΓΕΙΡΕΥΤΑ | COOKED DISHES
  ----------------------------------------- */
  cooked: {
    title: "Μαγειρευτά | Cooked Dishes",
    subtitle: "Παραδοσιακά και διεθνή μαγειρευτά πιάτα.",
    items: [
      { name: "Octopus in Wine Sauce", desc: "Χταπόδι μαγειρεμένο σε κόκκινη σάλτσα κρασιού.", price: "12.50€", img: "octopus-stew.jpg" },
      { name: "Cuttlefish Stew", desc: "Σουπιά μαγειρεμένη με μυρωδικά.", price: "12.00€", img: "cuttlefish-stew.jpg" },
      { name: "Traditional Squid with Fennel", desc: "Καλαμάρι με μάραθο.", price: "11.00€", img: "" },
      { name: "Chicken Curry", desc: "Ινδικό κοτόπουλο με κάρυ.", price: "120.00", img: "" },
      { name: "Chicken Masala", desc: "Κοτόπουλο με ινδικά μπαχαρικά.", price: "120.00", img: "" }
    ]
  },

  /* -----------------------------------------
     ΠΟΤΑ | DRINKS
  ----------------------------------------- */
  drinks: {
    title: "Ποτά | Drinks",
    subtitle: "Αναψυκτικά, μπύρες, κρασιά και διεθνή ροφήματα.",
    items: [
      { name: "Coca Cola", desc: "330ml", price: "2.00€", img: "" },
      { name: "Sprite", desc: "330ml", price: "2.00€", img: "" },
      { name: "Fanta", desc: "330ml", price: "2.00€", img: "" },
      { name: "Beer", desc: "Μπύρα ελληνική.", price: "3.50€", img: "" },
      { name: "Soju", desc: "Κορεάτικο ποτό.", price: "4,000₩", img: "" },
      { name: "Makgeolli", desc: "Παραδοσιακό κορεάτικο ποτό.", price: "4,000₩", img: "" }
    ]
  },

  /* -----------------------------------------
     ΓΛΥΚΑ | DESSERTS
  ----------------------------------------- */
  desserts: {
    title: "Γλυκά | Desserts",
    subtitle: "Ελληνικά και διεθνή γλυκά.",
    items: [
      { name: "Ice Cream", desc: "Διάφορες γεύσεις.", price: "3.00€", img: "" },
      { name: "Apple Crumble", desc: "Αγγλικό γλυκό με μήλο.", price: "4.00€", img: "" },
      { name: "Chocolate Cake", desc: "Σοκολατένιο κέικ.", price: "4.50€", img: "" }
    ]
  }

};
/* ---------------------------------------------------
   LANGUAGE SWITCHER
--------------------------------------------------- */
let lang = "GR";

document.getElementById("langToggle").onclick = () => {
    lang = lang === "GR" ? "EN" : "GR";
    renderCategoryButtons();
    renderMenu(Object.keys(MENU_DATA)[0]);
};

function getTitle(title) {
    if (lang === "GR") return title.split("|")[0].trim();
    return title.split("|")[1].trim();
}

/* ---------------------------------------------------
   CATEGORY BUTTONS
--------------------------------------------------- */
const categoryButtons = document.getElementById("categoryButtons");
const menuContainer = document.getElementById("menuContainer");
const tapSound = document.getElementById("tapSound");

function playTap() {
    tapSound.currentTime = 0;
    tapSound.play();
}

function renderCategoryButtons() {
    categoryButtons.innerHTML = "";

    Object.keys(MENU_DATA).forEach(categoryKey => {
        const btn = document.createElement("button");
        btn.textContent = getTitle(MENU_DATA[categoryKey].title);
        btn.onclick = () => { playTap(); renderMenu(categoryKey); };
        categoryButtons.appendChild(btn);
    });
}

/* ---------------------------------------------------
   RENDER MENU
--------------------------------------------------- */
function renderMenu(categoryKey) {
    const category = MENU_DATA[categoryKey];
    menuContainer.innerHTML = "";

    const title = document.createElement("h2");
    title.textContent = getTitle(category.title);
    menuContainer.appendChild(title);

    const subtitle = document.createElement("p");
    subtitle.textContent = category.subtitle;
    subtitle.style.opacity = "0.8";
    subtitle.style.marginBottom = "25px";
    menuContainer.appendChild(subtitle);

    category.items.forEach(item => {
        const div = document.createElement("div");
        div.className = "menu-item";

        const img = document.createElement("img");
        img.src = item.img && item.img !== "" ? item.img : "placeholder.jpg";
        img.alt = item.name;

        const textDiv = document.createElement("div");
        textDiv.className = "menu-text";

        const name = document.createElement("h3");
        name.textContent = item.name;

        const desc = document.createElement("p");
        desc.textContent = item.desc;

        const price = document.createElement("div");
        price.className = "price";
        price.textContent = item.price;

        textDiv.appendChild(name);
        textDiv.appendChild(desc);
        textDiv.appendChild(price);

        div.appendChild(img);
        div.appendChild(textDiv);

        menuContainer.appendChild(div);
    });
}

/* ---------------------------------------------------
   SCROLL TO TOP
--------------------------------------------------- */
function scrollToTop() {
    window.scrollTo({ top: 0, behavior: "smooth" });
}

/* ---------------------------------------------------
   AUTO DARK MODE
--------------------------------------------------- */
if (window.matchMedia("(prefers-color-scheme: light)").matches) {
    document.body.classList.add("light");
}

/* ---------------------------------------------------
   SERVICE WORKER
--------------------------------------------------- */
if ("serviceWorker" in navigator) {
    navigator.serviceWorker.register("sw.js");
}

/* ---------------------------------------------------
   INITIAL LOAD
--------------------------------------------------- */
renderCategoryButtons();
renderMenu(Object.keys(MENU_DATA)[0]);

</script>
</body>
</html>
