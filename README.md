# Testing_browser
Para masubukan sa android phone na may maliit na screen at sa malaking screen gaya ng computer at iba pa
LINK NG AKING PAHINA  https://espedidorobin372-cmyk.github.io/Testing_browser/
Ito ay pagsasanay lang kaya makikita na iba iba ang laman ng Reposetory
            ito para subukan sa windows at mobile at sa ibang device na may ibat ibang laki ng screen,
            at iba pa, maraming salamat!
<!DOCTYPE html>
<html lang="tl-PH">
    <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pagsasanay Reposetory</title>
        <link rel="icon" href="robin.ico" type="image/x-icon">
    <style>
        body {
            background-color: antiquewhite;
        }

         /* 1. Dito ang istilo — itago ang lahat ng pahina maliban sa nakabukas */
    .pahina { display: none; }
    .aktibo { display: block; }
    button { margin: 5px; padding: 8px 12px; cursor: pointer; }
        pre {
            color: brown;
            font-size: 20px;
        }
    </style>

    </head>
    <body>
        <pre>
            Ito ay pagsasanay lang kaya makikita na iba iba ang laman ng Reposetory
            ito para subukan sa windows at mobile at sa ibang device na may ibat ibang laki ng screen,
            at iba pa, maraming salamat!
        </pre>
        
<!--        <h2>TORTA</h2>
    <img src="Torta.jpg" alt="Kababayan" class="litrato">

    <br><br>
    <a href="larawan_ng_tinapay_menu.html" class="balik">⬅ BALIK SA LISTAHAN</a>
    <br>
    <a href="timpla_tinapay2.html" class="balik">🏠 BALIK SA PANGUNAHING MENU</a>   --> 

    <!--============================================================================-->
    <div id="menu" class="pahina aktibo">
    <h1>🥯 Menu ng Tinapay</h1>
    <button onclick="buksan('tinapayA')">Tinapay A</button>
  </div>

  <div id="tinapayA" class="pahina">
    <h2>Tinapay A</h2>
    <button onclick="buksan('menu')">⬅️ Balik sa Menu</button>
    <button onclick="buksan('tinapayA_sangkap')">📋 Mga Sangkap</button>
  </div>

  <div id="tinapayA_sangkap" class="pahina">
    <h2>Sangkap ng Tinapay A</h2>
    <button onclick="buksan('tinapayA')">⬅️ Balik sa Tinapay</button>
    <button onclick="buksan('menu')">🏠 Diretso sa Menu</button>
  </div>
  <!--=================================================================================-->
  <script>
    alert("KUMUSTA PO"); // java script pwedi sa loob ng head o sa loob ng body

    function buksan(pangalan) {
  aydaanLahat(); // Itago lahat muna
  ipakita(pangalan); // Ipakita ang napiling pahina

  // ↓ ITO ANG UNA — ILAGAY SA KASAYSAYAN ↓
  history.pushState({pahina: pangalan}, '', '#' + pangalan);
}

// ↓ ITO ANG PANGALAWA — KAPAG PININDOT ANG BACK BUTTON ↓
window.onpopstate = function(e) {
  if (e.state && e.state.pahina) {
    aydaanLahat();
    ipakita(e.state.pahina);
  }
};

// ==============================================
// MGA TULONG NA GAWAIN — SA ILALIM NITO
// ==============================================
function aydaanLahat() {
  document.querySelectorAll('.pahina').forEach(p => p.classList.remove('aktibo'));
}

function ipakita(pangalan) {
  document.getElementById(pangalan).classList.add('aktibo');
}

// ✅ Para gumana kapag binuksan ang link na may #tandaan sa dulo
window.onload = function() {
  const kasunod = location.hash.replace('#', '');
  if (kasunod) buksan(kasunod);
};
  </script>
    </body>
</html>

<!--============================================================-->
<!DOCTYPE html>
<html lang="tl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mga Larawan — Aayon sa Screen</title>
    <style>
        /* Buong pahina */
        body {
            background-color: #f0f0f0;
            padding: 20px;
            font-family: sans-serif;
        }

        /* Lalagyan ng lahat ng larawan — dito nangyayari ang pag-aayos */
        .gallery {
            display: flex;          /* Magkakatabi mula kaliwa pakanan */
            flex-wrap: wrap;        /* ✅ Kapag puno na, bumababa sa susunod na linya */
            gap: 20px;              /* Espasyo sa pagitan ng bawat larawan */
            justify-content: flex-start; /* Magsisimula sa kaliwa */
        }

        /* Bawat kahon ng larawan */
        .gallery-item {
            flex: 0 0 auto;         /* Hindi magpipilit magpalit ng lapad */
        }

        /* Ang mismong larawan */
        .gallery-item img {
            width: 200px;           /* Lapad ng larawan sa computer */
            height: 150px;          /* Taas ng larawan */
            object-fit: cover;      /* Hindi magiging hiwa-hiwa ang itsura */
            border-radius: 8px;     /* Medyo bilog ang gilid — maganda tignan */
            box-shadow: 0 2px 5px rgba(0,0,0,0.2); /* May anino */
            border: 4px solid rgb(255, 0, 0); /* ITO YONG BOX SA PALIBOT NG LARAWAN */
        }

        /* ✅ Para sa CELLPHONE — kapag mas maliit sa 768px */
        @media (max-width: 768px) {
            .gallery-item img {
                width: 150px;       /* Mas maliit na larawan sa cellphone */
                height: 110px;
            }
            .gallery {
                gap: 15px;          /* Mas maliit na espasyo */
            }
        }

        /* ✅ Napakaliit na cellphone — mas maliit sa 480px */
        @media (max-width: 480px) {
            .gallery-item img {
                width: 130px;
                height: 100px;
            }
            .gallery {
                gap: 10px;
            }
        }
        H1 {font-weight: bold; color: blue}
        .gallery {
            border: 4px solid rgb(255, 153, 0);
            padding: 15px;
        }
        .gallery-item img {
            width: 180px; /*180px*/
            height: auto;
            border-radius: 6px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>
    <h1>Ang Aking Koleksyon ng Larawan 📷</h1>
    <div class="gallery">
        <div class="gallery-item"><img src="larawan1.jpg" alt="Larawan 1"></div>
        <div class="gallery-item"><img src="larawan2.jpg" alt="Larawan 2"></div>
        <div class="gallery-item"><img src="larawan3.jpg" alt="Larawan 3"></div>
        <div class="gallery-item"><img src="larawan4.jpg" alt="Larawan 4"></div>
        <div class="gallery-item"><img src="larawan5.jpg" alt="Larawan 5"></div>
        <div class="gallery-item"><img src="larawan6.jpg" alt="Larawan 6"></div>
        <div class="gallery-item"><img src="larawan7.jpg" alt="Larawan 7"></div>
        <div class="gallery-item"><img src="larawan8.jpg" alt="Larawan 8"></div>
        <div class="gallery-item"><img src="larawan9.jpg" alt="Larawan 9"></div>
        <div class="gallery-item"><img src="larawan10.jpg" alt="Larawan 10"></div>
        <div class="gallery-item"><img src="larawan11.jpg" alt="Larawan 11"></div>
        <div class="gallery-item"><img src="larawan12.jpg" alt="Larawan 12"></div>
        <div class="gallery-item"><img src="larawan13.jpg" alt="Larawan 13"></div>
        <div class="gallery-item"><img src="larawan14.jpg" alt="Larawan 14"></div>
        <div class="gallery-item"><img src="larawan15.jpg" alt="Larawan 15"></div>
        <div class="gallery-item"><img src="larawan16.jpg" alt="Larawan 16"></div>
    </div>
</body>
</html>
