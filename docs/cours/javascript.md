# Initiation au Javascript


**Prérequis**

Avant d'entamer ce module, vous n'avez besoin d'aucune connaissance préalable en JavaScript, mais vous devriez être familier avec HTML et CSS. Nous vous conseillons de lire les modules concernant HTML et CSS avant d'aller plus loin.

# Une définition générale de JavaScript

JavaScript (« JS » en abrégé) est un langage de programmation dynamique complet qui, appliqué à un document HTML, peut fournir une interactivité dynamique sur les sites Web.

# Rôles du HTML / CSS / JavaScript
![Rôles du HTML / CSS / JavaScript](http://vdoit.in/wp-content/uploads/2016/09/vDoIT_html-css-logo1.jpg)
Rôles du HTML / CSS / JavaScript, source [http://vdoit.in/](http://vdoit.in/)

- HTML est un langage de balisage utilisé pour structurer et donner sens au contenu web. Par exemple : définir des paragraphes, en-têtes et tables de données ou encore intégrer des images ou des vidéos dans une page.
- CSS est un langage de règles de style utilisé pour appliquer un style au contenu HTML. Par exemple : en modifiant la couleur d’arrière-plan ou les polices, ou en disposant le contenu en plusieurs colonnes.
- JavaScript est un langage de programmation qui permet de créer du contenu mis à jour de façon dynamique, de contrôler le contenu multimédia, d’animer des images, à peu près tout. Bon, peut-être pas tout, mais vous pouvez faire bien des choses avec quelques lignes de JavaScript.
- Attention: Le JavaScript est exécuté par le moteur JavaScript du navigateur, après que le HTML et le CSS aient été assemblés et combinés en une page web. Cet enchaînement est nécessaire pour être sûr que la structure et le style de la page seront déjà en place quand le JavaScript commencera son exécution.

# Notion de DOM
## Présentation du DOM

Le Document Object Model (DOM) est une interface de programmation pour les documents HTML et XML. Il fournit une page dont des programmes peuvent modifier la structure, son style et son contenu. Cette représentation du document permet de le voir comme un groupe structuré de nœuds et d'objets possédant différentes propriétés et méthodes. Fondamentalement, il relie les pages Web aux scripts ou langages de programmation.

Une page Web est un document. Celui-ci peut être affiché soit dans la fenêtre du navigateur, soit sous la forme de son code source HTML. Mais il s'agit du même document dans les deux cas. Le modèle objet de document proposé par le DOM fournit une autre manière de représenter, stocker et manipuler ce même document. Le DOM est une représentation entièrement orientée objet de la page Web, et peut être manipulé à l'aide d'un langage de script comme JavaScript.

## DOM et JavaScript

Les codes qui sont écrit en JavaScript peuvent utiliser le DOM pour accéder au document et à ses éléments. Le DOM n'est pas un langage de programmation, mais sans lui le langage JavaScript n'aurait aucun modèle ni aucune notion des pages Web, des documents XML, et des éléments pour lesquels il est généralement utilisé. Chaque élément d'un document, que ce soit le document lui-même, ses en-têtes, les tableaux internes au document, les en-têtes de colonnes et le texte contenu dans les cellules de ces tableaux, fait partie du modèle objet de document (DOM) de ce document. Tous ces éléments sont donc accessibles et peuvent être manipulés à l'aide du DOM et d'un langage de script comme JavaScript.

À l'origine, JavaScript et le DOM étaient fortement liés, mais ils ont fini par évoluer en deux entités distinctes. Le contenu de la page est stocké dans le DOM et on peut y accéder et le manipuler via JavaScript, de la sorte qu'on pourrait écrire cette équation approximative :

API (page Web ou XML) = DOM + JS (langage de script)

Le DOM a été conçu pour être indépendant de tout langage de programmation, ce qui rend la représentation structurelle du document disponible à l'aide d'une API simple et cohérente.

# Premiers pas en JavaScript

## Ajouter des variables pour stocker les données

Une variable est un conteneur pour une valeur, tel un nombre à utiliser pour une addition, ou une chaîne devant faire partie d'une phrase. Mais un aspect spécial des variables est que les valeurs contenues peuvent changer. Voyons un exemple simple :

```html
<button>Pressez moi</button>
```

```javascript
var button = document.querySelector('button');

button.onclick = function() {
  var name = prompt('Quel est votre nom ?');
  alert('Salut ' + name + ', sympa de vous voir !');
}
```
Dans cet exemple, presser le bouton déclenche l'exécution de quelques lignes de code. La première ligne affiche à l'écran une boîte priant le lecteur de saisir son nom et stocke la valeur entrée dans une variable. La deuxième affiche un message de bienvenue qui contient le nom, pris dans la valeur de la variable.

## Les Fonctions

- Fonctions personnalisées
```javascript
function draw() {
  ctx.clearRect(0,0,WIDTH,HEIGHT);
  for (var i = 0; i < 100; i++) {
    ctx.beginPath();
    ctx.fillStyle = 'rgba(255,0,0,0.5)';
    ctx.arc(random(WIDTH), random(HEIGHT), random(50), 0, 2 * Math.PI);
    ctx.fill();
  }
}
```
Cette fonction dessine 100 cercles aléatoires dans un élément canvas. À chaque fois que nous voulons faire cela, il suffit d'invoquer la fonction comme suit :

```javascript
draw();
```
- Fonctions anonymes : vous pouvez également créer une fonction qui n'a pas de nom :
```javascript
function() {
  alert('hello');
}
```
Ceci est une fonction anonyme— elle n'a pas de nom ! De plus, elle ne produira pas d'effet par elle-même. Les fonctions anonymes sont généralement utilisées en association avec un gestionnaire d'évènement, comme dans l'exemple suivant qui lance le code inscrit dans la fonction lorsque le bouton associé est cliqué :
```javascript
var myButton = document.querySelector('button');

myButton.onclick = function() {
  alert('hello');
}
```
## Objet et héritage

### Les bases de l'objet

Un objet est une collection de données relatives entre elles et/ou de fonctionnalités (qui, souvent, se composent de plusieurs variables et fonctions, appelées propriétés et méthodes quand elles sont dans des objets). Prenons un exemple pour voir à quoi elles ressemblent.

Comme souvent dans JavaScript, pour créer un objet, on commence avec la définition et l'initialisation d'une variable. Essayez de mettre le code ci-dessous sous le code déjà écrit de votre fichier JavaScript, puis sauvegardez et rafraichissez la page :

```javascript
var personne = {};
```

Félicitations, vous avez créé votre premier objet ! Mais c'est un objet vide, on ne peut pas faire grand-chose avec. Modifions notre objet pour qu'il ressemble à ceci :

```javascript
var personne = {
  nom: ['Jean', 'Martin'],
  age: 32,
  sexe: 'masculin',
  interets: ['musique', 'skier'],
  bio: function() {
    alert(this.nom[0] + ' ' + this.nom[1] + ' a ' + this.age + ' ans. Il aime ' + this.interets[0] + ' et ' + this.interets[1] + '.');
  },
  salutation: function() {
    alert('Bonjour ! Je suis ' + this.nom[0] + '.');
  }
};
```
Vous avez désormais des données et des fonctionnalités dans votre objet, et vous pouvez y accéder avec une une syntaxe simple et claire !

```javascript
personne.nom[0]
personne.age
personne.interets[1]
personne.bio()
personne.salutation()
```

### Héritage

Ci-dessus vous trouverez le constructeur Personne ():
```javascript
function Personne(prenom, nom, age, genre, interets) {
  this.nom = {
    prenom,
    nom
  };
  this.age = age;
  this.genre = genre;
  this.interets = interets;
};
```
L'ensemble des méthodes est défini dans le prototype :
```javascript
Personne.prototype.saluer = function() {
  alert('Salut! Je suis ' + this.nom.prenom + '.');
};
```
Essayons de créer une classe Professeur similaire à celle que nous avons utilisée jusqu'ici dans les autres modules d'initiations à l'approche objet. Ainsi, cette classe hérite de Personne mais possède aussi :

Un nouvel attribut matière — qui contiendra la matière que le professeur enseigne.
Une méthode saluer un peu plus élaborée, qui sera un peu plus formelle que la méthode de base, cela sera plus approprié, lorsque le professeur s'adrressera à des étudiants, par exemple.

La première chose à faire est de créer le constructeur Professeur() via l'ajout du code suivant :

```javascript
function Professeur(prenom, nom, age, genre, interets, matiere) {
  Personne.call(this, prenom, nom, age, genre, interets);

  this.matiere = matiere;
}
```
Cela ressemble beaucoup au constructeur Personne mais il y a quelque chose que nous n'avons pas encore vu : la fonction call(). Cette fonction permet d'appeler une fonction définie ailleurs dans le contexte actuel. Le premier paramètre spécifie la valeur de this que l'on souhaite utiliser lors que l'on utilisera la fonction, les paramètres suivants seront les paramètres qui pourront être passés en arguments lorsqu'elle sera appelée.

Nous voulons que le constructeur Professeur() aie les mêmes attributs que Personne(), nous les spécifions donc dans l'appel fait via la fonction call().

La dernière ligne au sein du constructeur sert simplement à définir l'attribut matière que les professeurs enseignent, ce qui n'est pas valable pour les personnes génériques.

# Utilisation du DOM

La variable la plus important quand on veut utiliser le DOM,  c'est `document`. Elle designe la balise `<html>` qui est la racine du document. Voyons dans un premier temps des méthodes utiles, puis ensuite leur utilisation.

L'accès aux balises `<head>`et `<body>` depuis le DOM est un peu à part. Il suffit simplement de taper `document.head` et `document.body`.

Prenons comme exmple le code HTML suivant :
```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Ma page web</title>
    </head>
    <body>
        <h1>Ma page web</h1>
        <p>Bonjour, je m'appelle Baptiste.</p>
        <p>J'habite dans la belle ville de <a href="http://www.lyon.fr">Lyon</a>.</p>
    </body>
</html>
```
Source [openclassrooms.com](openclassrooms.com)
    
Le DOM de ce code peut être représenté de façon hiérarchisé sous la forme d'un arbre.

![Représentation sous forme d'arbre de la page WEB d'exemple](https://s3-eu-west-1.amazonaws.com/sdz-upload/prod/upload/DOM1.DOM "Représentation sous forme d'arbre de la page WEB d'exemple")
Représentation sous forme d'arbre de la page WEB d'exemple, source [openclassrooms.com](openclassrooms.com)

## Parcours initial

Il est possible d'accéder à tous les noeuds avec les méthodes `childNodes` et `parentNode` qui renvoient, respectivement, un tableau contenant les noeuds fils et le noeud parent d'un noeud choisi. Il est donc théoriquement possible d'accèder à n'importe quel élément de la page depuis la racine avec ces deux méthodes.

Ainsi, si on reprends l'exemple vu plus haut, pour accèder à la balise `<a>`contenue dans le dernier noeud `<p>`, il faudrait écrire `document.body.childNodes[5].childNodes[1]`. Il y a cependant quelque chose à bien noter. Pour accéder au noeud `<p>`, on a accedé au 6ème élement de la liste des enfants de `body` (`document.body.childNodes[5]`, la numérotation commencant à 0) et non le troisième comme on aurait pu le supposer avec la vue du document sous forme d'arbre. Ceci est dû aux retours à la ligne présent dans le document HTML. En effet ils sont considérés par le DOM comme des noeuds textuels, et donc rentrent en compte dans la liste des noeuds fils.

Cette méthode d'accès a cependant des gros défauts. En effet elle est sensible à la structure de la page HTML, ce qui veut dire que si on rajoute un élément, on va devoir modifier les index utilisés pour récupérer tel ou tel élément. Ensuite elle manque de lisibilité. En effet, avec `document.body.childNodes[5]` on a accédé à une balise `<p>`, mais ce n'est pas forcément évident de savoir ce qu'on récupère. Et puis supposons que l'on souhaite récupérer toutes les balises `<p>`, c'est pas très évident à faire avec cette méthode.

Pour ce faire, d'autres méthodes de sélection d'élements existent.

## Parcours plus précis

Plusieurs méthodes existent pour permettre de sélectionner de manière plus fine et plus précise :
- `getElementsByTagName` permet de selectionner tous les éléments d'un même tag, par exemple tous les titres de niveau 2 avec `document.getElementsByTagName("h2")`,
- `getElementsByClassName` permet de selectionner tous les éléments d'un possèdant la même classe CSS, par exemple tous les éléments possédant la classe `gras` avec `document.getElementsByClassName("gras")`,
- `getElementById` permet de selectionner le premier élément qui possède l'identifiant CSS, par exemple l'élément identifié par `photoProfil` avec `document.getElementById("photoProfil")`,
- `querySelectorAll` permet de sélectionner tous les éléments qui suivent un sélecteur CSS, par exemple tous les éléments de paragraphe qui ont la classe italique avec `document.querySelectorAll("p.italique")`,
- `querySelector` fonctionne de la même manière que `querySelectorAll` à ceci près qu'il renvoie uniquement le premier élément correspondant au selecteur CSS

Considérons maintenant un exemple un peu plus complet.

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Les sept merveilles du monde</title>
    </head>
    <body>
        <h1>Les sept merveilles du monde</h1>
        <p>Connaissez-vous les merveilles du monde ?</p>
        <div id="contenu">
            <h2>Merveilles du monde antique</h2>
            <p>Cette liste nous vient de l'Antiquité.</p>
            <ul class="merveilles" id="antiques">
                <li class="existe">La pyramide de Khéops</li>
                <li>Les jardins suspendus de Babylone</li>
                <li>La statue de Zeus</li>
                <li>Le temple d'Artémis</li>
                <li>Le mausolée d'Halicarnasse</li>
                <li>Le Colosse de Rhodes</li>
                <li>Le phare d'Alexandrie</li>
            </ul>
            <h2>Nouvelles merveilles du monde</h2>
            <p>Cette liste a été établie en 2009 à la suite d'un vote par Internet.</p>
            <ul class="merveilles" id="nouvelles">
                <li class="existe">La Grande Muraille de Chine</li>
                <li class="existe">Pétra</li>
                <li class="existe">Le Christ du Corcovado</li>
                <li class="existe">Machu Picchu</li>
                <li class="existe">Chichén Itzá</li>
                <li class="existe">Le Colisée</li>
                <li class="existe">Le Taj Mahal</li>
            </ul>
            <h2>Références</h2>
            <ul>
                <li><a href="https://fr.wikipedia.org/wiki/Sept_merveilles_du_monde">Merveilles antiques</a></li>
                <li><a href="https://fr.wikipedia.org/wiki/Sept_nouvelles_merveilles_du_monde">Nouvelles merveilles</a></li>
            </ul>
        </div>
        <script src="../js/cours.js"></script>
    </body>
</html>
```
Source [openclassrooms.com](openclassrooms.com)

Supposons que nous voulons sélectionner toutes les nouvelles merveilles du monde. Nous souhaitons donc avoir plusieurs lignes. Plusieurs méthode sont possibles, nous allons en présenter deux : la première utilise `getElementsByTagName`, la seconde `querySelectorAll`.

Pour la première méthode, il faut tout d'abord analyser la structure du document. Les éléments que nous souhaitons récupérer sont tous des éléments de type `<li>` situés dans un élément de type `<ul>`. Cet élément est le deuxième de ce type dans l'élément `<div>` parent. La commande a utilisé serait donc : `document.body.getElementsByTagName("div")[0].getElementsByTagName("ul")[1].getElementsByTagName("li")`. Cette commande, bien que fonctionnelle, a deux inconvénients :
1. Elle est sensible à la structure de la page. Si on rajoute un élément `<div>` avant celui que nous visons ou bien un autre élément de type `<ul>`, la commande devra changer.
2. Elle est très longue, et donc augmente le risque d'erreurs dans sa conception.

À noter que la sélection peut être un peu simplifiée en remarquant que la liste visée possède un identifiant noté `nouvelles`.

La seconde methode utilise la puissance des sélecteurs CSS avant `querySelectorAll`. On reprends la même sélection qu'à la méthode précédente, mais traduite avec des sélecteurs CSS. Il faut seulement remarquer que l'élément `<ul>` que nous visons possède l'identifiant `nouvelles`. La commande devient `document.querySelectorAll("div > ul#nouvelles > li")`.

# Manipulation du CSS en Javascript

Le CSS se manipule assez simplement en Javascript. Pour accéder au style de l'élément `element`, il suffit d'écrire `element.style`. Ainsi on pourra accéder à ses attributs de style très simplement en ecrivant `element.style.property`. La modification du style est effectué de la même manière : `element.style.property = value`. Attention à ne pas oublier l'unité de `value` (px, cm, in,...).

Prenons quelques exemple. Pour accéder à la couleur du texte d'un element (en supposant qu'on ait récupéré au préalable l'élément), il suffit d'écrire `element.style.color`. De même pour définir cette couleur à bleu, il faut écrire : `element.style.color = blue`. Pour récupérer la couleur de fond, il faut écrire `element.style.backgroundColor`. Attention, la propriété CSS correspondant à la couleur de fond est `background-color`, mais Javascript n'accepte pas les tirets, il faut donc l'ommettre et remplacer la première lettre du deuxième mot par une majuscule.

Cette méthode est très pratique, mais elle ne permet pas de récupérer les styles définis dans des fichiers CSS. Pour ce faire, il faut utiliser la fonction `getComputedStyle`. Par exemple, si on veut récupérer la couleur de fond d'un élément, sachant que cette couleur a été définie dans un fichier CSS, il faut écrire `getComputedStyle(element).backgroundColor`.

# TP : Alternance de deux images 

- Créer une page HTML contenant une image.
- Programmer en JavaScript une alternance entre cette image et une autre, toutes les deux secondes.
- Ajouter un bouton et le code JavaScript associé pour arrêter ce défilement.
- Ajouter un bouton et le code JavaScript associé pour le reprendre

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <title>Actions utilisateur et JavaScript</title>
  <meta charset="utf-8" />
  <link rel="stylesheet" href="idemm.css" />
  <script>
    var alecran = 'unchat';
    function diaporama () {
      if (alecran == 'unchat') {
        document.getElementById('diapo').setAttribute('src','images/chien.jpg');
        alecran = 'unchien';
      } else {
        document.getElementById('diapo').setAttribute('src','images/chat.jpg');
        alecran = 'unchat';
      }
    }
  </script>
</head>

<body onload="chienchat = setInterval('diaporama();',2000);">

  <h1>Actions utilisateur et JavaScript</h1>

  <h2>Diaporama automatique</h2>

  <div class="illustration">
  <img id="diapo" src="images/chat.jpg" alt="un chat" height="200" />
  </div>

  <button onclick="clearInterval(chienchat);">stop!</button>

  <button onclick="chienchat = setInterval('diaporama();',2000);">on y retourne!</button>

</body>
</html>
```
Vous y trouverez la démonstration au lien suivant: [[Démo]](http://www.grappa.univ-lille3.fr/~torre/Enseignement/tp/JavaScript/seances/tp4.html).
Seul le code JavaScript sera commenté. Pour le code HTML voir le cours sur HTML et CSS.
```html
<script>
  var alecran = 'unchat';
  ...

</script>
```
Nous commençons par la déclaration d'une variable qui pour nom `alecran` et pour valeur la chaine de caractère `unchat`.  
```html
<script>
  ...
  function diaporama () {
    if (alecran == 'unchat') {
      document.getElementById('diapo').setAttribute('src','images/chien.jpg');
      alecran = 'unchien';
    } else {
      document.getElementById('diapo').setAttribute('src','images/chat.jpg');
      alecran = 'unchat';
    }
  }
</script>
```
Il s'agit d'une fonction `diaporama()` comme vous pouvez le constater. si l'objet `alecran` prend la valeur `unchat` alors on récupère l'élément identifié par `diapo` et l'aide de `setAttribute('src','images/chien.jpg')` nous pourrions afficher l'image du chien qui est sur le lien `images/chien.jpg`. Nous avons le processus inverse lorsque `alecran` prend la valeur `unchien`.

# TP : Diaporama
- Placer des noms d'images dans un tableau JavaScript.
- Programmer l'affichage une par une de ces images dirigés par deux boutons, un précédent, un suivant
```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <title>Actions utilisateur et JavaScript</title>
  <meta charset="utf-8" />
  <link rel="stylesheet" href="idemm.css" />
  <script>
    var mesphotos = ['chat.jpg','chien.jpg','sanglier.jpg','lapin.jpg'];
    var image_en_cours = 0;
    function suivante () {
      image_en_cours = image_en_cours + 1;
      if (image_en_cours == mesphotos.length) {
        image_en_cours = 0;
      }
      document.getElementById('ecran').src = 'images/'+mesphotos[image_en_cours];
    }
    function precedente () {
      image_en_cours = image_en_cours - 1;
      if (image_en_cours < 0) {
        image_en_cours = mesphotos.length-1;
      }
      document.getElementById('ecran').src = 'images/'+mesphotos[image_en_cours];
    }
  </script>
</head>

<body>

  <h1>Actions utilisateur et JavaScript</h1>

  <h2>Diaporama manuel</h2>

  <div class="illustration">
  <img id="ecran" src="images/chat.jpg" alt="un chat" height="200" />
  </div>

  <button onclick="precedente();">image précédente</button>
  <button onclick="suivante();">image suivante</button>

  </body>
</html>

```
Vous y trouverez la démonstration au lien suivant: [Démo](http://www.grappa.univ-lille3.fr/~torre/Enseignement/tp/JavaScript/seances/tp4bis.html)

NB: il y aucune différence entre `document.getElementById('ecran').src=""` et `document.getElementById('diapo').setAttribute('src','images/chat.jpg');`, ils ont tous les deux le même rôle. Le `.src=` est une mannière plus simple d'écrire le `.setAttribute("","")`.

# À VOUS DE JOUER

Dans cette partie il sera question de faire un script en JavaScript qui permettra de défiler chaque 5 secondes des images(au moins 5 images contenues dans un tableau). 

- Placer des noms d’images dans un tableau JavaScript
- Programmer l’affichage une par une de ces images qui apparaîtront les unes à suite des autres chaque 5 secondes.