<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Koranübersetzung von Frank Bubenheim</title>
  <link rel="stylesheet" href="styles.css">
</head>
<style>body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
  }
  
  header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1rem 0;
  }
  
  nav {
    background-color: #555;
    color: white;
    padding: 1rem;
  }
  
  nav ul {
    list-style: none;
    padding: 0;
  }
  
  nav ul li {
    padding: 0.5rem;
    cursor: pointer;
  }
  
  nav ul li:hover {
    background-color: ;
  }
  
  main {
    padding: 1rem;
  }
  
  #sura-title {
    color: #b99696;
  }
  
  #sura-content {
    margin-top: 1rem;
    padding: 1rem;
    background-color: #fff;
    border: 1px solid #ccc;
  }
  </style>
<script>// Beispiel: Liste der Suren
    const suren = [
      {
        nummer: 1,
        name: "Al-Fatiha",
        inhalt: [
          "1. Im Namen Allahs, des Allerbarmers, des Barmherzigen.",
          "2. Alles Lob gebührt Allah, dem Herrn der Welten.",
          "3. Dem Allerbarmer, dem Barmherzigen,",
          "4. Dem Herrscher am Tage des Gerichts.",
          "5. Dir allein dienen wir, und Dich allein bitten wir um Hilfe.",
          "6. Leite uns den geraden Weg,",
          "7. Den Weg derer, denen Du Gnade erwiesen hast, nicht derer, die (Deinen) Zorn erregt haben und nicht der Irregehenden."
        ]
      },
      {
        nummer: 2,
        name: "Al-Baqara",
        inhalt: [
          "1. Alif-Lam-Mim.",
          "2. Dies ist das Buch, an dem es keinen Zweifel gibt, eine Rechtleitung für die Gottesfürchtigen.",
          "3. Die an das Verborgene glauben und das Gebet verrichten und von dem, was Wir ihnen gegeben haben, ausgeben."
          // Weitere Verse hinzufügen
        ]
      }
      // Weitere Suren können hier hinzugefügt werden
    ];
    
    // Elemente auswählen
    const suraList = document.getElementById("sura-list");
    const suraTitle = document.getElementById("sura-title");
    const suraContent = document.getElementById("sura-content");
    
    // Suren in die Navigation einfügen
    suren.forEach(sura => {
      const listItem = document.createElement("li");
      listItem.textContent = `Sure ${sura.nummer}: ${sura.name}`;
      listItem.addEventListener("click", () => loadSura(sura));
      suraList.appendChild(listItem);
    });
    
    // Funktion zum Laden der Sure
    function loadSura(sura) {
      suraTitle.textContent = `Sure ${sura.nummer}: ${sura.name}`;
      suraContent.innerHTML = "";
      sura.inhalt.forEach(vers => {
        const p = document.createElement("p");
        p.textContent = vers;
        suraContent.appendChild(p);
      });
    }
    </script>
<body>
  <header>
    <h1>Koranübersetzung von Frank Bubenheim</h1>
  </header>

  <nav>
    <ul id="sura-list">
      <!-- Die Suren werden hier dynamisch hinzugefügt -->
    </ul>
  </nav>

  <main>
    <h2 id="sura-title">Wähle eine Sure</h2>
    <div id="sura-content">
      <!-- Die Übersetzungen werden hier dynamisch angezeigt -->
    </div>
  </main>

  <script src="script.js"></script>
</body>
</html>
