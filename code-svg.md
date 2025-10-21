![logo-web3.lu](https://github.com/mbarnig/qubit-lu-project/blob/main/logos/logo-web3.svg)

Le code pour afficher mon logo web3.lu suivant se présente comme suit : 

```
<!-- web3.lu — Logo texte italique (Outfit) avec nuage tricolore et carrés équilibrés -->
<svg width="320" height="120" viewBox="0 0 320 120" xmlns="http://www.w3.org/2000/svg" role="img" aria-labelledby="title desc">
  <title id="title">web3.lu — logo texte final (Outfit italique, nuage tricolore corrigé)</title>
  <desc id="desc">Logo "web3.lu" en italique, police Outfit, fond noir arrondi.</desc>

  <defs>
    <!-- Dégradé luxembourgeois aligné sur le 3 -->
    <linearGradient id="lux-flag" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%"  stop-color="#EF3340"/>
      <stop offset="43%" stop-color="#EF3340"/>
      <stop offset="43%" stop-color="#FFFFFF"/>
      <stop offset="61%" stop-color="#FFFFFF"/>
      <stop offset="61%" stop-color="#00A3E0"/>
      <stop offset="100%" stop-color="#00A3E0"/>
    </linearGradient>

    <!-- Styles -->
    <style>
      .card { fill: #0B0C10; }
      .label {
        font-family: "Outfit", sans-serif;
        font-weight: 700;
        letter-spacing: 0.5px;
        transform: skewX(-10deg);
        transform-origin: left center;
      }
      .dot-red { fill: #EF3340; }
      .dot-white { fill: #FFFFFF; }
      .dot-blue { fill: #00A3E0; }
    </style>
  </defs>

  <!-- Fond noir arrondi -->
  <rect x="0" y="0" width="320" height="120" rx="20" class="card"/>

  <!-- Texte principal -->
  <g transform="translate(32, 78)">
    <text x="0" y="0" class="label" font-size="64" fill="url(#lux-flag)">web3.lu</text>
  </g>
</svg>

```
J'ai demandé à ChatGPT-5 comment réduire sa largeur. Voici sa réponse : 

Pour réduire la largeur totale du logo à 280 px, tu as deux possibilités selon ce que tu veux faire :

🟢 Option 1 — Affichage à 280 px (sans modifier les proportions internes)

C’est la méthode la plus propre et la plus sûre.
Tu gardes le viewBox tel quel (il définit le repère interne),
et tu changes seulement l’attribut width :
`<svg width="280" height="105" viewBox="0 0 320 120" xmlns="http://www.w3.org/2000/svg" role="img" aria-labelledby="title desc">`
