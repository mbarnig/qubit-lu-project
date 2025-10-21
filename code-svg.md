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

## 🟢 Option 1 — Affichage à 280 px (sans modifier les proportions internes)

C’est la méthode la plus propre et la plus sûre.
Tu gardes le viewBox tel quel (il définit le repère interne),
et tu changes seulement l’attribut width :  

`<svg width="280" height="105" viewBox="0 0 320 120" xmlns="http://www.w3.org/2000/svg" role="img" aria-labelledby="title desc">`

Le résultat se présente comme suit : 


![logo-web3.lu-w280](https://github.com/mbarnig/qubit-lu-project/blob/main/logos/logo-web3-lu-w280.svg)

👉 Pourquoi ?

Tu divises la largeur par 320/280 = 0.875 → 87.5 % de la taille originale.

Si tu veux garder les mêmes proportions, tu peux aussi ajuster la height proportionnellement :
120 × 0.875 = 105.

Tout le contenu (texte, fond, dégradé, etc.) se mettra à l’échelle automatiquement grâce au viewBox.

💡 Résultat :
Le logo aura une largeur de 280 px à l’écran, tout en restant vectoriel et parfaitement proportionné.

## 🔵 Option 2 — poure garder la taille du texte web3.lu, mais en réduisant la largeur et la hauteur de la box !

Parfait — on garde la taille du texte (font-size="64") et on rétrécit seulement la “box” (le rectangle de fond) en largeur et en hauteur.
Voici une version où la box passe de 320×120 à 280×96, centrée dans le même canvas. Le texte ne change pas.

```

```
Notes rapides

Le canvas (320×120) reste identique → le texte garde exactement sa taille visuelle.

Seule la box (rectangle de fond) est plus étroite et moins haute.

Si tu veux la box encore plus serrée autour du texte, diminue encore width et height (ex. width="260" height="88") et ajuste x/y pour la centrer (par ex. x="30" y="16").

Si tu veux réduire aussi le canvas (pour que l’SVG entier soit plus petit) sans toucher la taille du texte, on peut changer uniquement l’attribut width/height du rectangle tout en gardant le viewBox et les tailles de texte comme ici — ou recadrer le viewBox autour du contenu si nécessaire.

