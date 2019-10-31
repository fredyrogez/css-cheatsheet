# CSS Cheat Sheet

### Unités
    <length> : taille (px | em)
    <length%> : taille (px | em | %)
    <color> : couleur ( color-name | #rrvvbb | rvb(r,v,b) | rvba (r,v,b,a) | hsl(h,s,l) | hsla(h,s,l,a) )
    <line-style> : none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset

### Selecteurs
    p {}             // tous les éléments p
    .maClasse {}     // class="maClasse"
    p.maClasse {}    // sélectionne les éléments p qui ont class="maClasse"
    p.cla1.cla2 {}   // sélectionne les éléments p qui ont class="... cla1 cla2 ..."
    #monID {}        // id="monID"
    [title] {}       // sélection les éléments qui ont un attribut title
    p[title] {}      // sélectionne les éléments p qui ont un attribut title    

### Combinateurs
    div p {}            // cible les p dans un div
    div > p {}          // cible les p enfants-uniquement des div sur un seul niveau
    div + ul {}         // cible un seul ul qui suit directement un div
    div ~ ul {}         // cible tous les ul qui suivent un div
    
### Pseudo-classes
    a:hover {}      // élément survolé avec le pointeur
    a:link {}       // lien non visité
    a:active {}     // lien en train d'être cliqué, avant relâchement du pointeur
    a:visited {}    // lien déjà visité
    
    p:first-child {}    // premier élément fils par rapport au parent
    p:last-child {}     // dernier élément fils par rapport au parent
    p:nth-child(3) {}   // 3ème élément fils...
    
    p:first-of-type {}  // premier élément d'un type donnée dans le parent
    p:nth-of-type(3) {} //  ...
    
    input:checked {}      // élément coché (radio, case à cocher..)
    input:focus {}        // élément qui a le focus (input...)
    input:in-range {}     // ex : <input id="valeur1" name="valeur1" type="number" placeholder="de 1 à 10" min="1" max="10" value="12">
    input:out-of-range {} // ...
    input:enabled {}      // éléments non-désactivés
    input:disabled {}     // éléments désactivés
    input:default {}      // élément coché par défaut (ex: <input type="radio" name="radios" id="r1" checked>)
    :target               // élément cible d'un lien interne (href="#cible")
    :empty                // élément sans contenu
    
### Pseudos-éléments
    p::before { content: "xxx"; } // ajoute du contenu au début d'un élément
    p::after { content: "xxx"; }  // ajoute du contenu à la fin d'un élément
    p::first-letter { }           // sélectionne la première lettre d'un élément    
    
### Typographie
    font: bold 20px Verdana;
    font: font-style font-variant font-weight font-size/line-height font-family;
       
    color: red;
    color: #ff0000;
    color: rgb(255, 0, 0);        // r, g, b (0-255)
    color: rgba(255, 0, 0, 0.5);  // r, g, b, alpha(0-1)
    color: hsl(50, 50%, 80%); // hue:0-359, sat:0-100%, lum:0-100%
    color: hsla(50, 50%, 80%, 0.5); // + alpha 0-1
    
    font-family: "Arial", sans-serif; // serif, sans-serif, monospace, cursive, fantasy
    
    font-size: <length>;       // taille en pixels (16=taille par défaut)
    font-size: <percentage>;   // idem em
    font-size: <keyword>;      // taille absolue : xx-small | x-small | small | medium | large | x-large | xx-large
    font-size: <keyword>;      // taille relative : larger | smaller

    font-weight: <keyword>;    // valeur absolue : normal | bold
    font-weight: bolder;       // valeur relative : lighter | bolder
    font-weight: <number>;     // 100 | 200 | 300 | 400=Normal | 500 | 600 | 700=Bold | 800 | 900
    
    text-decoration: <keyword>;     // none | underline
    font-style: <keyword>;          // normal | italic | oblique
    font-variant: <keyword>;        // normal | small-cap
    text-transform: <keyword>;      // uppercase | lowercase | capitalize | none
        
    text-overflow: clip;        // clip=couper si trop grand, ellipsis=... si trop grand
    white-space: nowrap;        // normal, nowrap, pre, pre-warp, pre-line
    word-break: break-all;      // normal, break-all
    letter-spacing: 1px;        // normal, 1px, 0.1em
    line-height: normal;        // normal, 10px, 1.5, 1.5em, 
    word-spacing: 5px;          // normal, 1px, 2em
    text-indent: 10px;          // -10px, 3em, 0    
    text-align: left;           // left, right, center, justify    
        
    text-shadow: 2px 2px 4px red; // offest horizontal, offset vertical, flou, couleur

### Box
    margin:       raccourci // top, right, bottom, left / top, right+left, bottom / top+bottom, right,left / top+bottom+right+left
                  (margin-top, margin-right, margin-bottom, margin-left)
    paddind:      raccourci // top, right, bottom, left / top, right+left, bottom / top+bottom, right,left / top+bottom+right+left
                  (padding-top, padding-right, padding-bottom, padding-left)
                  
    border-with: <T> <T> <T> <T>
    border-with: <T> <T> <T>
    border-with: <T> <T>
    border-with: <T>    
    border-top-width: <T>        
    border-right-width: <T>        
    border-bottom-width: <T>        
    border-left-width: <T>
   
    border-color: <color>
    border-top-color: <color>
    border-right-color: <color>
    border-bottom-color: <color>
    border-left-color: <color>

    border-style: <line-style>         // none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset
    border-top-style: <line-style>
    border-right-style: <line-style>
    border-bottom-style: <line-style>
    border-left-style: <line-style>
   
    border:                 // border-with border-style border-color
   
   
### Grid [[MDN](https://developer.mozilla.org/fr/docs/Web/CSS/grid)]
    display: grid;                          // conteneur principal en "grid"
    grid-template-columns: 1fr, 1fr, 1fr;   // 3 colonnes égales
    grid-template-rows: 1fr, 1fr, 1fr;
    grid-auto-columns: 100px;
    grid-auto-rows: 100px;
    
    grid-column-start: 1; 
    grid-column-end: 4; 
    grid-row-start: 1; 
    grid-row-end: 3;
    
    grid-column: 1 / 3;         // raccourci : grid-column-start / grid-column-end
    grid-row: 1 / 3;            // raccourci : grid-row-start / grid-row-end    
    grid-area: 1 / 3 / 1 / 3    // raccourci : grid-row-start, grid-column-start, grid-row-end, grid-column-end
    grid-area: hd;              // donne un nom à une zone pour utilisation avec grid-template-areas
    grid-template-areas: "hd hd hd" "sd mn mn" ". ft ."; // . = cellule vide
        
    grid-column-gap: 5px;       // espace entre les colonnes
    grid-row-gap: 5m;           // espace entre les lignes
    
### Flexbox [[MDN](https://developer.mozilla.org/fr/docs/Web/CSS/flex)]
    display: flex;              // conteneur principal en "mode flexbox"
    flex-direction: row;        // row, row-reverse, column, column-reverse 
    flex-wrap: wrap;            // wrap, nowrap, wrap-reverse 
    flex-flow: row wrap         // raccourcis pour : flex-direction flex-wrap
    justify-content: center;    // flex-start, flex-end, center, space-between, space-around
    align-items: center;        // axe perpendiculaire : flex-start, flex-end, center, baseline, stretch
    align-content: stretch;     // si flex-wrap : stretch, flex-start, flex-end, center, space-between, space-around
    flex-grow: 0;               // agrandissement si espace dispo : 0 = par défaut, 1 = reste de la place, 2 = double
    flex-shrink: 1;             // réduction si pas assez d'espace : 1 = par défaut, 0 = no shrink (overflow possible)
    order: 1;                   // 0 = par défaut, permet de modifier l'ordre de l'élément dans le flux
    align-self:                 // comme align-items, mais sur un seul élément.
    flex-basis: 100px;          // auto = défaut. Taille d'origine d'un élément
    
### Réfs
[MDN / Couleurs](https://developer.mozilla.org/fr/docs/Web/CSS/Type_color)    
