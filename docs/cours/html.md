# Les bases de HTML5 et CSS3 !

Les langages HTML et CSS sont à la base de tout projet de développement web. En effet, les navigateurs vont utiliser ces deux langages pour afficher des pages web. En bref, pour créer un site e-commerce, un blog ou encore une application mobile, il est nécessaire de passer par du code en HTML ou CSS.  

*   HTML est l’abréviation de HyperText Markup langage, soit en français “langage de balisage hypertexte”. Grâce à cela, on va pouvoir indiquer au navigateur si le texte fait partie d’un paragraphe, d’un titre, … Il va aussi permettre d’insérer différents types d’éléments dans les pages web: texte, liens, images, ...

*   CSS est l’abréviation de Cascading StyleSheets, ou feuilles de style en cascade. Ce langage va permettre de définir la taille, la couleur et l’alignement d’un texte.

Il est donc très clair que l’utilisation de l’un ne va pas sans l’autre. Pour le développement d’un site, on fera donc des liens entre ces deux langages. Par exemple, l’utilisation du CSS sur un code HTML servira à améliorer le résultat visuel final.

Pourquoi apprendre le HTML et le CSS ?

C’est avant tout pour se créer un socle indispensable pour comprendre comment fonctionne son site et ainsi pouvoir le modifier ou corriger si besoin.

Nous nous concentrerons sur les versions HTML5 et CSS3 qui sont les dernières versions stables en date de ces deux langages.

# Les bases en HTML5

## Quelques définitions et utilité des éléments, des balises et des attributs:

*   **Eléments:**  
    Les éléments HTML servent à structurer le contenu pour lui donner un sens. Par exemple, on utilise des éléments pour définir un paragraphe, un titre, insérer une image ou une vidéo dans un document.

*   **Balises:**  
    Un élément HTML est constitué dans la majorité des cas d’une paire de balise et d’un contenu. Mais il peut aussi être constitué d’une balise unique qu’on dit alors orpheline.  
    Exemple pour écrire un paragraphe: `<p> Je suis un paragraphe HTML </p>`. Pour faire un retour à la ligne, on utilise l’élément `<br />` qui est une balise orpheline.

*   **Attributs:**  
    La balise ouvrante d’un élément HTML peut contenir des attributs, parfois même obligatoire. Ils servent à définir ou compléter un élément. Un attribut contient toujours une valeur.  
    Exemple: l’élément a (pour “anchor”) servant à créer des liens vers d’autres pages a besoin d’un attribut href (“hypertexte reference”) qui va prendre comme valeur l’adresse de la page vers laquelle on souhaite faire un lien.  
    `<a href=”https://www.imt-atlantique.fr/fr”> Mon site </a>`

Attention: Les balises et les attributs ne seront jamais affichés par le navigateur. Ils servent à indiquer au navigateur comment il doit traiter chaque contenu.

## Structure d’une page HTML:

Voici le code minimum pour une telle page avec un titre, un en-tête et un corps.

![code minimum](images/img1.png)

Le doctype du document sert à préciser le type du document. Les balises `<html>` et `</html>` représentent la page html. L’élément head va contenir des méta-informations relatives à la page comme le type d’encodage et l’élément body va contenir tout le contenu visible de la page. Il y a deux renseignements à indiquer à l’intérieur de l’élément head: l’élément `<title>` qui va contenir le titre de la page et son attribut `<charset>` qui va permettre de définir l’encodage de la page.

Il faut bien veiller à ce que le premier élément déclaré soit le dernier refermé, tandis que le premier ouvert doit toujours être le premier fermé. Il est vivement conseillé de bien indenter son code et de mettre des commentaires comme suit: `<!-- mon commentaire -- >`.

## Les titres et paragraphes:

Il y a 6 niveaux d’organisation pour les titres définis par les éléments h1, h2, h3, h4, h5 et h6\. h1 étant le titre principal et h6 le titre le plus petit.  
Pour ajouter un titre dans une page html, c’est très simple il suffit d’utiliser les balises comme par exemple:

`<h3> Mon titre </h3>`

Attention: Ne pas confondre les éléments h1, h2, etc. et l'élément title, qui sont complètement différents. Les éléments h1, h2, etc servent à définir des titres à l’intérieur de la page, tandis que l’élément title sert à définir le titre de la page, qui va s’afficher dans la barre haute de votre navigateur.

Pour créer des paragraphes, il faut utiliser l’élément p. On peut créer autant de paragraphes que l’on souhaite dans une page. A chaque paragraphe, il faut utiliser un nouvel élément p.

`<p> 1er paragraphe </p>`  
`<p> 2nd paragraphe </p>`

Voici un exemple utilisant des titres et paragraphes:

![titres et paragraphes](images/img2tri.png)

## Les espaces et retours à la ligne en html:

Les espaces “en trop” au sein d’un paragraphe ne seront jamais affichés visuellement. Pour effectuer des retours à la ligne ou marquer des espaces en HTML, il faudra utiliser des éléments. Retour à la ligne: élément br balise orpheline qui est à placer avant ce qu’on souhaite mettre à la ligne suivante. Remarque: On peut aussi utiliser l’élément hr qui est un retour ligne avec changement de thématique, c’est à dire qu’un “trait” sera tracée entre les deux lignes.

Gestion des espaces:  
L’élément pre sert à préformater un texte. C’est à dire qu’il va garder la même mise en forme que celui écrit à l’intérieur de la balise.  
`<pre> Le texte ici sera affiché tel qu’il a été écrit </pre>`

## Définir l’importance des textes:

L’élément strong sert à signifier qu’un contenu est très important (il va alors être affiché en gras) nous utiliserons ensuite CSS pour gérer le poids d’un texte.  
L’élément em sert à signifier que le contenu est “relativement” important (il va être affiché en italique).

![exemple em](images/img3tri.png)

## Les listes en HTML:

Les listes sont très utiles pour donner de la clarté et de l’ordre aux documents. Il existe plusieurs types de listes: les listes non-ordonnées, les listes ordonnées et les listes de définitions.

**Les listes non-ordonnées:**  
Elles servent à lister des éléments sans hiérarchie ni ordre logique. Pour créer un telle liste, nous avons besoin d’un élément u1 qui va représenter la liste en soi ainsi que d’éléments li représentant chaque élément de la liste. Visuellement des puces apparaissent automatiquement devant chaque élément d’une liste non-ordonnée.

Par exemple:

```html
<ul>  
    <li>Pomme</li>
    <li>Vélo</li>
    <li>Guitare</li>
</ul>
```


**Les listes ordonnées:**  
Lorsqu’on souhaite une notion d’ordre ou de progression logique entre les éléments d’une liste. On va utiliser l’élément ol pour définir la liste en soi et à nouveau des éléments li pour les différents éléments de la liste.

Par exemple:

```html
<ol>  
    <li>Partie 1</li>
    <li>Partie 2</li>  
    <li>Partie 3</li>   
</ol>
```

_Nous pouvons faire le choix d’ajouter un attribut type dans l’élément ol.  
“I” correspond à des chiffres romain majuscule devant chaque éléments, “i” à des chiffres romain minuscules, “A” signifie que des lettres majuscules apparaîtront devant chaque élément de la liste et “a” des lettres minuscules._

![lites html](images/img4tri.png)

**Les listes de définition:**  
Ces listes vont permettre de lister des termes et d’ajouter des définitions ou descriptions pour chacun de ces termes. Nous allons utiliser l’élément dl pour chaque élément à décrire puis l’élément dt pour chaque élément à décrire et enfin l’élément dd pour la définition/ description en soi.

Par exemple:

```html
<dl>  
    <dt>HTML</dt>  
    <dd>HTML signifie HyperText Markup Language.</dd>
</dl>
```

Remarque: Il est tout à fait possible d’imbriquer plusieurs listes.

## Liens internes et externes en HTML:

Pour créer des liens en HTML, on va utiliser l’élément a accompagné de son attribut href qui va prendre comme valeur la cible du lien. Il y a deux types de liens: les liens permettant de se déplacer d’une page à une autre à travers un même site (liens internes) et les liens permettant de se rendre sur un autre site (lien externe). Dans les deux cas, c’est la valeur de l’attribut href qui va changer.

_Liens externes:_

On place tout d’abord le lien hypertexte entre deux balises de l’élément a. Pour la balise entrante, on place l’attribut href avec l’adresse du lien.

Par exemple:  
`<p> Cliquer sur <a href=”facebook.com”> ce lien </a> pour aller sur facebook. </p>` Ici le texte “ce lien” sera affiché en hypertexte et l’utilisateur pourra consulter facebook en cliquant dessus.

Attention: Il faut que l’attribut href prenne une URL complète en valeur (adresse absolue).

_Liens internes:_

Ici même principe, mais l’attribut va prendre comme valeur, une adresse relative à l’adresse de départ. C’est à dire celle à partir de laquelle on fait notre lien.  
Un site n’est qu’un ensemble de fichiers liés entre eux. Il faut alors distinguer trois cas: la cas où la page de départ et celle d’arrivée sont dans le même dossier; le cas où la page destination est dans un sous-dossier par rapport à la page de départ et le cas où la page de destination est un dossier parent par rapport à la page de départ.

Exemple pour chacun des cas:  
Fichier dans un même dossier:
`<p> Cliquer <a href=”fichier_meme_dossier.html”> ici</a> </p>`
Fichier dans un dossier parent:
`<p> Cliquer <a href=”../fichier-parent.html”> ici </a> </p>`
Fichier dans un sous-dossier de nom “sous”:
`<p> Cliquer <a href=”sous/fichier-sous.html”> ici </a> </p>`

L’attribut target: Cet attribut va permettre de choisir où doit s’ouvrir notre page de destination. En pratique, nous utiliserons souvent la valeur “_blank” qui spécifie qui spécifie que la nouvelle page doit s’ouvrir dans un nouvel onglet.

Par exemple: `<p> Vers <a href=”http://wikipedia.org” target=”_blank”> Wikipédia </a> </p>`

_Remarque:_  
-On peut aussi permettre l’envoi d’un mail, lorsqu’un visiteur va cliquer sur le lien, sa messagerie par défaut va automatiquement s’ouvrir:
`<p> M’envoyer <a href=”mailto: louis.somme@imt-atlantique.net”> un mail </a> </p>`

## Insérer des images en HTML:

Chaque format d’image (JPG, PNG, GIF ou BITMAP) possède ses propres spécificités. Il faut donc bien faire attention au format lorsqu’on enregistre une image. Généralement on utilisera le format JPG.  
L’insertion d’image dans une page HTML va se faire au moyen de l’élément img. Cet élément est représenté par une balise orpheline. De plus, on va utiliser les attributs src et alt. L’attribut src va prendre comme valeur l’adresse de l’image tandis que l’attribut alt va contenir un texte décrivant l’image. Ce texte ne va être affiché QUE si l’image n’a pas pu l’être pour une raison ou pour une autre.  
L’image sera affichée en taille originale.

Exemple:  

`<img src=”image_de_chat.png” alt=”Mon chat felix”>`

Il est également possible d’afficher une image provenant d’un autre site en entrant l’adresse absolue du site en question dans le src.

_Evaluation sur les bases en HTML_:

1- Dans le tableau suivant , relier les différents éléments à ce qu’ils servent à faire

![tableau évaluation html](images/evaluation_html.png)

2- Combien de niveaux d’organisation sont définis pour les titres en HTML ?

3- Nous souhaitons écrire un sommaire avec le titre des grandes partie

    a) Est-il plus pertinent d’utiliser une liste ordonnée ou non ordonnée?

    b) Quel attribut permet de placer des chiffres romain en majuscule devant le titre de chaque partie

    c) Utiliser un code HTML pour écrire le sommaire de ce cours (les grandes partie du Chapitre “Les bases en HTML”)

4- Quels attributs utilise-t-on pour ajouter une image à une page web?

5- On souhaite ajouter une image d’un coucher de soleil ayant le nom coucher_soleil.png. Proposer un code HTML pour ajouter cette image à une page web.

_Correction_:

1-

Element p       Créer un paragraphe

Element a       Créer des liens vers d'autres pages

Element img     Insérer une image

Element br      Retour à la ligne


2- Il existe 6 niveaux d'organisation pour les titres HTML.


3- a) Il est dans ce cas plus pertinent d'utiliser une liste ordonnée

b) L'attribut I permet de placer des chiffres romains devant le titre des parties

c) ```html
	<p> Sommaire: </p>

           <ol type="I">

               <li> Quelques définitions et utilité des éléments, des balises et des attributs: </li>
               <li> Structure d'une page HTML: </li>
               <li> Les titres et paragraphes: </li>
               <li> Les espaces et retours à la ligne en HTML: </li>
               <li> Définir l'importance des textes: </li>
               <li> Les listes en HMTL: </li>
               <li> Liens internes et externes en HTML: </li>
               <li> Insérer des images en HTML </li>

           </ol>
	```

4- Pour ajouter une image à une page web, on utilise les attributs src et alt.

5- `<img src="coucher_soleil.png" alt=" Coucher de soleil" >`

# Les bases en CSS:

## Sélecteurs, propriétés:

CSS va permettre de mettre en page un contenu et de changer son apparence en lui appliquant des styles. Pour appliquer un style à un élément HTML, il faut tout d’abord le sélectionner, c’est le rôle du sélecteur. Il existe différents types de sélecteurs appelés “sélecteurs simples” (ce sont des sélecteurs d’éléments) ou “sélecteurs complexes”.

Les propriétés CSS vont permettre de choisir quels aspects d’un élément HTML on souhaite modifier. La propriété color peut prendre le nom d’une couleur.

Exemple:

```
p{
    color: blue;
    font-size: 14px;
}
```

Ici nous utilisons un sélecteur CSS simple p qui va cibler tous les paragraphes de la page HTML. Ensuite deux propriétés sont utilisées: color pour modifier la couleur et font-size pour modifier la police d’écriture.

Le couple “propriété: valeur” est appelé déclaration CSS et chaque déclaration doit être séparé d’une autre par un point virgule.

Où écrire le code CSS ?

1. On peut l’écrire dans un élément HTML style. Ainsi le code CSS ne s’appliquera qu’à la page HTML dans laquelle il a été écrit. L’élément style sera en général placé en haut d’une page HTML, à l’intérieur de l’élément head.
Cette méthode n’est pas recommandée (soucis d’organisation).
2. On peut écrire le CSS dans la balise ouvrante des éléments HTML en utilisant un attribut style. Par exemple: pour appliquer le style à tout un paragraphe:
<p style=”color: blue;font-size: 16px;”>Un paragraphe</p>

Non recommandé non plus car pas très lisible.

3. La meilleure méthode est d’écrire le CSS dans un fichier séparé portant l’extension “.css” et enregistré dans le même dossier que le fichier HTML. Un avantage est qu’on va pouvoir appliquer des styles à plusieurs page HTML en même temps.
Il reste ensuite à lier le fichier CSS avec le fichier HTML avec l’élément link qui va avoir besoin de deux attributs: rel, qui va préciser le type de fichier et href qui va indiquer l’adresse relative du fichier CSS. On place l’élément link (balise orpheline) dans l’élément head de notre fichier HTML.

Exemple: <link rel=”stylesheet” href=”styles.css”>     (dans le head)

## Commentaires et indentation:

On utilise la syntaxe suivante pour commenter à l’intérieur d’un code: /*Je suis un commentaire*/.
L’indentation est importante en CSS, après chaque déclaration, il vaut mieux retourner à la ligne.

## Sélecteurs CSS simples:

Des exemples de sélecteurs: le sélecteur p va cibler tous les éléments d’un paragraphe, le sélecteur h1 va permettre d’appliquer des styles au titre h1, le sélecteur a va permettre de mettre en forme les liens, etc

![exemple sélecteurs css simples](images/img5.png)

Remarque: On peut appliquer les styles à plusieurs éléments en séparant les sélecteurs par des points virgules.

Exemple:

```
h1,p{
    color: blue;
}
```

Ici on applique une couleur bleue à tous nos paragraphes ainsi qu’à notre titre principal d’un coup.

Nous serons vite limités avec des sélecteurs simple. En effet il n’est par exemple pas possible d’appliquer une couleur différente à deux paragraphes différents. C’est pourquoi nous pouvons utiliser les sélecteurs #id et .class qui vont permettre de cibler un élément en particulier plutôt qu’un type d’élément.

## Les attributs id et class:

Ces deux attributs servent à cibler un élément en particulier plutôt qu’un type. Nous allons les définir à l’intérieur d’une balise ouvrante et leur attribuer une valeur.

Par exemple, dans le fichier HTML:

```html
<p id=”p1”> 1er paragraphe </p>
<p class=”p1”> 2eme paragraphe </p>
```

Pour cibler un élément possédant un attribut id, il faudra préciser la valeur de l’attribut précédé d’un dièse (#).
Pour cibler un élément possédant l’attribut class il faudra préciser la valeur de l’attribut précédé d’un point (.).
C’est pour cette raison qu’on peut tout à fait donner la même valeur à un attribut class et id sans qu’il n’y ait de risque de confusion. L’exemple à été choisi de sorte à montrer cela.

Ensuite dans le code CSS on peut par exemple appliquer deux styles à un même paragraphe:

```
/*L’élément portant l’id “p1” sera en bleu*/
#p1{
    color: blue;
}

/*L’élément portant la class “p1” sera en rouge*/
.p1{
    color: red;
}
```

_Attention_: Chaque id doit avoir une valeur unique tandis que plusieurs attributs class peuvent posséder la même valeur.
En cas de conflit l’id est prioritaire sur la classe

## L’héritage en CSS:

L’héritage est un principe important en CSS. Cela signifie que tout élément HTML enfant va hériter “en cascades” des styles de ses parents. Par exemple tous les éléments à l’intérieur de l’élément body sont des enfants de cet élément. Donc si on applique un style à body, tous les éléments à l’intérieur de cette balise en hériteront automatiquement.

Cependant, en cas de conflit, le style prioritaire va être le style le plus proche de l’élément. Ainsi si on applique la couleur violette au body et qu’on applique ensuite la couleur rouge à un paragraphe à l’intérieur du body, ce paragraphe sera affiché en rouge.

## Les éléments HTML de type block et de type inline:

En HTML, tout élément est soit de type “block” (en bloc) soit de type “inline” (en ligne). Le tableau ci-dessous classe les différents éléments dans ces deux catégories.

![exemple éléments HTML de type block et de type inline](images/img6.png)

Ce tableau va être utile pour mettre en forme les pages web car on ne peut pas appliquer les mêmes propriétés aux éléments de type block et aux éléments de type inline.

**Les éléments de type block**:

Un élément de type block va toujours commencer sur une nouvelle ligne et prendre toute la largeur de la page. L’élément p est un élément de type block par exemple.
Lorsqu’on applique une bordure au paragraphe p (grâce à la propriété border) comme ci-dessous, il prend toute la largeur de la page.

```
p{
border: 4px solid #88BB11;
}
```
**Les éléments de type inline**:

Au contraire des éléments de type block, les éléments de type inline ne vont pas commencer sur une nouvelle ligne mais s’insérer dans la ligne actuelle.
Les éléments de type inline prennent uniquement la largeur qui leur est nécessaire. Ainsi, si on applique le même code que ci-dessus à un élément strong, seul la portion de ligne contenant l’élément sera encadrée.

**Les éléments div et span**:

Ces éléments n’ont aucune valeur sémantique, ils ne servent pas à donner un sens à un contenu.

1. div est un élément de type block et va être utilisé de conteneur pour plusieurs autres éléments HTML. Nous pourrons appliquer des styles directement à l’élément div afin de faciliter la mise en forme de la page.

_Exemple d’utilisation_:

Le code HTML:

```html
<div  class=”div-para”>
    <p>L’élément p est un élément de type block</p>
    <p>Un <strong> autre</strong> paragraphe</p>
</div>
```
Le code CSS:

```
.div-para{
    background-color: #88BB11.
    font-weight: bold;
}
```

De cette manière le texte entre les bornes de l’élément div va être en gras et avec un fond de couleur hexadécimale #88BB11 c’est à dire vert.

2. Span est un élément de type inline et va servir de conteneur pour du contenu textuel. Cet élément va être utile lorsque nous voudrons mettre en forme une portion de texte à l’intérieur d’un élément.

_Exemple d’utilisation_:

Code HTML:

```html
<div class=”green”>
    <p> L’élément p est <span class=”blue”> un élément de type block</span></p>
<div>
```

Code CSS:

```
.green{
    background-color: #88BB11;
    font-weight: bold;
}

.blue{
    background-color: #1188BB.
}
```

De cette manière, le texte sera globalement sur fond vert, mais la phrase “un élément de type block” sera sur fond bleu.

_Evaluation sur les bases en CSS_:

1- Pourquoi est-il généralement conseillé d’écrire le code CSS dans un fichier séparé?

2- Écrire un code CSS permettant d’appliquer la couleur bleue aux titres h1, h2 et au paragraphe p.

3- Classer les éléments ci-après suivant s’ils sont du type block ou du type inline:
img, h1, strong, em, li, p, a.

4- En quoi consiste l’héritage en CSS ?

5- Pour cibler un élément de type class, doit-on utiliser le point (.) ou le dièse (#) ?

Correction :

1- On écrit le CSS dans un fichier séparé car va pouvoir appliquer des styles à plusieurs page HTML en même temps. Il reste ensuite à lier le fichier CSS avec le fichier HTML avec l’élément link.

2-
```html
h1, h2,p{
            color: blue;
}
```

3-
type block: h1, li, p
type inline: img, strong, em, a

4- L'héritage en CSS consiste à faire hériter “en cascades” les enfants des styles de ses parents. Par exemple tous les éléments à l’intérieur de l’élément body sont des enfants de cet élément. Donc si on applique un style à body, tous les éléments à l’intérieur de cette balise en hériteront automatiquement.

5-Pour cibler un élément de type class, on utilise le point (.)
