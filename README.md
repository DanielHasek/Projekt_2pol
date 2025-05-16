
<body>
    <body>   
<h1>Projekt</h1>                         
<h2>Úvod do projektu</h2>
<p>
Hlavním cílem projetku bylo a stále je, se donutit a zkusit něco nového v oblasti kódování webových stránek. Hlavní nástroj pro stavbu stránky slouží jazyk HTML, společně se stylizací v CSS, povedlo se lehce začlenit i JavaScript. Do repozitáře přikládám všechny potřebné materiály.
</p>
  
<h2>Poděkování</h2>
<p>Chci poděkovat dlouholetému příteli Robinu Řepkovi za celkovou výpomoc, zodpovězení mých dotazů a případnou korekturu.</p>


<h2>Status</h2>
<p>Z prvotního nápadu "Portfolio", by se dalo říci sešlo, nyní je to spíš takový můj volnočasový projekt. Když vidím pěkně vypadajicí scenérii, tak ji vyfotím, proto je web spíše orientován hlavně na mé fotky. Jestli někdy vymyslím pár věcí o mně samotném, tak je do sekce "About" doplním, zatím si vystačím s Lorem impsum. Na stránce jsou funkční karty: About, Gallery, po rozkliknutí loga se dá přesměrovat na homepage. (karta "Other" funkční není, zatím mě nenapadlo žádně využití, krom estetické stránky).
</p> <br>
<p>Web je dostupný přes odkaz <a href ="https://hasekdaniel.netlify.app/">hasekdaniel.netlify.app<a/>, jedná se pouze o malou zkoušku, jak fungují neplacené web hostingy. Popřípadě je to jedna z možností, jak se na projekt dostat.
<p/>

<h1>Popis projektu</h1>
<p>Web je celkem postaven z 8 souborů (pro plnou funkčnost je potřeba stáhnout dodatky k Lightboxu a přiložené fotografie). Většina z nich má identický začátek, poté úpravy podle obsahu. Budu tedy popisovat hlavně částí které jsou: klíčové, neopakují se a jsou něčím zajímavé.</p>
<ol>
    <h2><li>index</li></h2>
    <p>Prvotně vytvořená stránka. Slouží jako takový homepage. Je úvodní. Níže je stručný popis částí kódu</p>
    <ul>
        <h3><li>HTML</li></h3>
        
 ```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel="stylesheet" href="styles.css">
<script src="https://kit.fontawesome.com/864f740a28.js" crossorigin="anonymous"></script>
 <title>web</title>
 </head>
```
   <p>Jedná se o část kódu předem vygenerovanou VS Studiem.
   Popisuje: o jaký typ dokumentu se jedná, jaký je používám encoding, zároveň generuje části: "head" a "body", <br>
             dále je přídána část "link", ta sváže html soubor se souborem css, <br>
            Je zde obsažen "script", který přidává možnost vložení ikon.
    </p>
    
 ```html


<header>
        <a class="logo"  href="index.html">
        <img src="https://lh3.googleusercontent.com/pw/AP1GczPc8bhBbcwgzBQzJtmKdNj7ZN3mzF4SjgJf2S1lU9T5JhU5kDTVVXppfQ7LRaX6nKahlNVx266vEfWPcEVmU9xIgKl089O0Z7yISYsEnM7eiwt90vc=w2400">     
        </a>
        <nav>
            <ul class="nav_links">
                <li><a href="about.html">About</a></li> 
                <li><a href="gallery.html">Gallery</a></li>
                <li><a href="#">Other</a></li>
            </ul>
         </nav>
        <a class="button_ig" href="https://www.instagram.com/daniel_hasek_/"><i class="fa-brands fa-instagram"></i></a>
    </header>
  ```
<p> "Header" je vlastně takový naváděcí panel. Zde je vložen přechod mezi stránkami About a Gallery, logo a Instagramová ikona. <br>
    "class" je upřesnění části kódu pro pozdější úpravu v CSS. <br>
    V elementu s class "nav_links" jsou právě zmiňováné přechodní body mezi ostatním obsahem webu, ("ul") je označení pro body, zde by mohly místo toho být elementy "button", avšak účel to plní stejný.).<br>
    Element s class "button_ig" se stará o hypertextování ikony Instagramu, aby po rozkliknutí přesměrovala na Instagramový profil.
<p/>
    
 ```html
    <main>
         <div class="uvod">
            <h2>Gallery</h2>
            <h1>Daniel Hašek</h1>
            <h4>Projekt</h4>
         </div>
    </main>    
```
<p>Sekce "main" slouží pro úvodní text. Zde již byl poprvé použit "div", používá se k seskupení části obsahu, pro snažší úpravu v CSS.</p>    

 <h3><li>CSS</li></h3>
 <p>CSS určuje strukturu stránky a jak bude vypadat.</p>

 ```css
   {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}
```

 <p>
     Tato část nemá definováno, ke které skupině v kódu patří, tudíž se vztahuje na celou stránku. <br>
    "box-sizing. border-box;" slučuje padding (vnitřní okraj, část mezi obsahem a rámečkem) a border (rámeček) do jednoho prvku, zjednodušuje práci s rozměry. <br>
     "Margin 0" nastaví odsazení stránky na 0.
 </p>

```css
.nav_links li {
    display: inline-block;
    padding: 0px 15px;
}

.nav_links li a {
    transition: all 0.3s ease 0s;
    color: black;
    border: 10px solid transparent;
    letter-spacing: 1px;
    border-radius: 50%;
}

.nav_links li a:hover {
border-radius: 50%;
background-color: #ec9b43;
color: aliceblue;
```
<p>Zde je stylizace přechodních bodů mezi stránkami. Jsou mezi sebou odsazeny "paddingem". Dále je zde funkce hover, ta zabarví celou buňku při najetí kurzorem.
</p>



</ul>
    <h2><li>gallery</li></h2>
    <p>Popis funkčnosti vybraných prvků na stránce s galerií.</p>
    <ul>
        <h3><li>HTML</li></h3>
        
```html
   <main>
        <div class="container"> 
            <div class="gallery"> 
                <a href="images/image_1.jpg" data-lightbox="models" data-title="Trafalgar square">
                    <img src="images/image_1.jpg">
                    </a>
                <a href="images/image_2.jpg" data-lightbox="models" data-title="Sveti Petar na Moru">
                    <img src="images/image_2.jpg">
                    </a>
                <a href="images/image_3.jpg" data-lightbox="models" data-title="Nin">
                    <img src="images/image_3.jpg">
                    </a>
                <a href="images/image_4.jpg" data-lightbox="models" data-title="London">
                    <img src="images/image_4.jpg">
                    </a>            
            </div>
        </div>
        <script src="lightbox-plus-jquery.js"></script>
    </main>
```
<p> Celá část "main" je uzavřena do classy "container" pro snazší editaci. Dále je vymezená část pro galerii další classou. Díky tomu mohu přidat kdykoliv jinou tématiku pomocí další classy, a tak galerie zůstane nezměněná. <br>
Fotografie jsou zde přidáný standardním způsobem "img src", ten je na stránce zobrazen jako menší náhled <br>
Vužívám zde script "lightbox", jelikož je daný v elementu "a href" (hypertext), tak se spustí až po kliknutí na daný obrázek. Ve skriptu je obsaženo ztmavení pozadí, popis obrázku a možnost přepínat mezi sousedními obrázky.</p>

 <h3><li>CSS</li></h3>
 
```css
 .gallery img {
    width: 100%;
    object-fit: cover;
    aspect-ratio: 1;
    display: block;
}

.container {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    min-height: 100vh;
    padding: 50px 8%;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 30px;
}

.gallery img {
    width: 100%;
    object-fit: cover;
    aspect-ratio: 1;
    display: block;
}

```
<p>Celý ".container" je posazen do "flex" (seskupení obsahu do jednoho celku). <br>
        ".gallery" používá navíc i "grid". Se spojení s "flex", nastane možnost upravit danou část jako celek, ale i měnit nezávisle grid (obsah ve flexboxu) zvlášť. <br>
        "grid-template-colums: repeat(auto-fit)" urovná opakovaně obsah do sloupců, dle rozměrů obsahu a dalších parametrů. </p>


</ul>
</ol>

<h1>Závěr</h1>
<p>Při první myšlence a vizi v psaní webovky, se všechno zdálo jako jednoduchá věc a zábava. Všiml jsem si jedné věci při vytváření webu. Je to zajímavé, ale asi nic pro mě. Zdá se mi, že pro to nemám vlohy, nebo se nedostatečně snažím, a nebo jsem se tomu málo věnoval. Je pravda, že jsem zkusil pouhý zlomek, co se těchto věcí týče. Ale mohu říct, že to nebylo na škodu. Poprvé jsem si zkusil zpracovat dokumentaci tohoto typu a seznámit se s Githubem.</p> 

<h2>Cíle</h2>
<p>jedná se o budoucí cíle, které bych chtěl za život doplnit.</p>
<ul>
    <li>Najít mnou ztracené Raspberry Pi 2 a zkusit ho využít na hosting webu.</li>
    <li>Dodělat pár nezrealizovaných nápadu, které jsem měl v hlavě.</li>
    <li>Zkusit něco nového.</li>
</ul>

<h2>Nástroje</h2>
<p>GITHUB. Github. Online. 2024. Dostupné z: <a href="https://github.com/">https://github.com/</a> [cit. 2024-12-19].<br></p>
<p>CITACE.COM, S.R.O. Citace.com. Online. © 2024. Dostupné z: <a href="https://www.citace.com/">https://www.citace.com/</a>. [cit. 2024-12-19].</p>
<p>MICROSOFT Corporation. Visual Studio Code. Online. 2015. Dostupné z: <a href="https://code.visualstudio.com/">https://code.visualstudio.com/</a>. [cit. 2024-12-19].</p>
<p>OPENAI. ChatGPT. Online. Dostupné z: <a href="https://chatgpt.com/"> https://chatgpt.com/</a>. [cit. 2025-05-15].</p>
<p>DHAKAR, Lokesh. Lightbox2. Online. Dostupné z:<a href="https://lokeshdhakar.com/projects/lightbox2/#license"> https://lokeshdhakar.com/projects/lightbox2/#license.</a> [cit. 2025-05-15].</p>
<p>FONTICONS, INC. Online. Dostupné z: <a href="https://fontawesome.com/"> https://fontawesome.com/.</a> [cit. 2025-05-15].</p>
<p>NETIFY. Online. Dostupné z: <a href="https://www.netlify.com"> https://www.netlify.com.</a> [cit. 2025-05-15].</p>

<h2>Literatura</h2>
<p>HTML & CSS Full Course for free 🌎. Online. 2023 31. 5. Dostupné z: <a href="https://www.youtube.com/watch?v=HGTJBPNC-Gw">https://www.youtube.com/watch?v=HGTJBPNC-Gw</a> . [cit. 2024-12-19].</p>
<p>HTML & CSS Full Course - Beginner to Pro. Online. 2022 5 2. Dostupné z: <a href="https://www.youtube.com/watch?v=G3e-cpL7ofc".>https://www.youtube.com/watch?v=G3e-cpL7ofc</a> [cit. 2024-12-19].</p>
<p>GITHUB. Lightbox2. Online. Dostupné z:<a href="https://github.com/lokesh/lightbox2"> https://github.com/lokesh/lightbox2.<a/> [cit. 2025-05-15].</p>
</body>
</body>
</html> 
