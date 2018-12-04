# Présentation Bootstrap 

Bootstrap est un ensemble d'outils qui sert à la création du design (graphisme, animation et interactions avec la page dans le navigateur ... etc. ...) de sites et d'applications web. Il contient des codes HTML et CSS, des formulaires, boutons, outils de navigation et autres éléments interactifs, ainsi que des extensions JavaScript en option. C'est l'un des projets les plus populaires sur la plate-forme de gestion de développement GitHub. 
Il permet de facilement installer et mettre à jour les paquets, régler le problème des dépendances. 

# Installation Bootstrap

IL existe plusieurs méthodes pour l’installation de Bootstrap, pour cela il faut aller sur le site [suivant](https://getbootstrap.com/docs/4.1/getting-started/download/).
La plus simple c’est celle du CSS et js compilés, pour cela :  Téléchargez la version prête de Bootstrap v4.1.3 et mettez-la dans votre projet, le lien du téléchargement est figurant [ci-dessous](ci-dessous).
Créez dans le répertoire ELU525, un fichier HTML nommé index.html
```
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link href="bootstrap/css/bootstrap.min.css" rel="stylesheet">
        <title>ELU-525</title>    
    </head>
    <body>
        <h1>Bonjour tout le monde!!!</h1>

        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
        <script src="bootstrap/js/bootstrap.min.js"></script>
    </body>
</html>
```
Il s’agit d’une page Web classique avec quelques éléments spécifiques.

-    une balise ```<link>``` vers la feuille de style Bootstrap.
-    une balise ```<meta name="viewport">``` définissant le viewport, c’est-à-dire la surface de la fenêtre du navigateur qui affiche la page. Cela va permettre à la page de s’adapter à la dimension du terminal client.
-  une balise ```<meta>``` permettant un affichage correct sur le navigateur Internet Explorer.
- une balise ```<script>``` qui activent les plugins jQuery de Bootstrap. Ces plugins sont nécessaires pour animer les composants Bootstrap.

Ouvrez cette page dans votre navigateur Web favori. Vous obtenez le résultat ci-dessous.
![]( images/1.png )


# Quelques composants de Bootstrap
Bootstrap fournit de nombreux composants prêts à être intégrés dans pages Web.
- Images et icônes: Bootstrap est livré avec environ 200 mini-images (glyphicons) librement utilisables.
```
Je boirais bien un <span class="glyphicon glyphicon-glass"></span> avant  d'aller écouter de la <span class="glyphicon glyphicon-music"></span> avec ma <span class="glyphicon glyphicon-heart"></span>
``` 
 ![](images/2.png)


De plus, Bootstrap fournit une classe img-responsive qui permet aux images (balises HTML < img>) de se redimensionner automatiquement à la taille de leur conteneur parent.

- Boutons
Bootstrap fournit un moyen simple d’obtenir des boutons élégants et personnalisables.
```
<button type="button" class="btn btn-default">Action</button>
<button type="button" class="btn btn-warning btn-lg">Attention</button>
<button type="button" class="btn btn-danger btn-xs">Danger</button>
<button type="button" class="btn btn-primary"><span class="glyphicon glyphicon-shopping-cart"></span> Panier</button>
```
![](images/3.png)


- Messages
Bootstrap permet de définir des messages faciles à repérer dans une page Web.
```
<div class="alert alert-success">Bravo !</div>
<div class="alert alert-info">Terminé</div>
<div class="alert alert-warning">Attention...</div>
<div class="alert alert-danger">Erreur !</div>
```
![](images/4.png)


- Menus de navigation
Il existe deux possibilités pour concevoir un menu de navigation: utiliser la classe nav, utiliser la classe list-group.Le code ci-dessous définit une mise en page sur trois colonnes, avec deux menus et une zone de contenu.
```
<div class="row">
    <div class="col-xs-3">
        <ul class="nav nav-pills nav-stacked">
            <li class="active"><a href="">Menu avec nav</a></li>
            <li><a href="">Profil</a></li>
            <li><a href="">Messages</a></li>
        </ul>
    </div>
    <div class="col-xs-3">
        <div class="list-group">
            <a class="list-group-item" href="">Menu avec list-group</a>
            <a class="list-group-item active" href="">Profil</a>
            <a class="list-group-item" href="">Messages</a>
        </div>
    </div>
    <div class="col-xs-6">
        Contenu
    </div>
</div>
```
![](images/5.png)

- Barre de navigation
On peut ajouter facilement une barre de navigation horizontale grâce à la classe Bootstrap navbar.

```
<nav class="navbar navbar-default" role="navigation">
    <a class="navbar-brand" href="#">Mon site Web</a>
    <ul class="nav navbar-nav">
        <li class="active"><a href="#">Rubrique 1</a></li>
        <li><a href="#">Rubrique 2</a></li>
    </ul>
    <ul class="nav navbar-nav navbar-right">
        <li><a href="#">Rubrique 3</a></li>
    </ul>
</nav>
```

![](images/6.png)


# Système de Grille 
L'organisation spatiale des pages web est l'une des premières préoccupations lorsque l'on crée un site web. Prévoit-on une bannière ? Faut-il un espace pour un menu à gauche ou en haut ? Y aura-t-il des blocs sur un des côtés pour recevoir certaines fonctionnalités comme la connexion ou des infos ? Faut-il prévoir un bas de page ?

Bootstrap ne répond évidemment pas à ces questions, mais il peut grandement vous faciliter la tâche, avec son système de grille, pour obtenir le résultat que vous souhaitez. En résumé:
1. Bootstrap propose une grille pour positionner tous les éléments des pages web
2.  La grille est versatile et permet de nombreuses combinaisons comme des inclusions, des sauts de colonnes.
3.  La grille rend possible également une adaptation selon les dimensions du support de visualisation en réorganisant les éléments ou en masquant certains.

Bootstrap fournit une classe CSS container utilisée pour regrouper d’autres éléments.

```
<div class="container">
  <!-- ... -->    
</div>
```

A l’intérieur d’un container, Bootstrap gère la zone d’affichage sous la forme d’une grille de 12 colonnes. La classe Bootstrap row crée une ligne dans cette grille, et chaque classe Bootstrap col-* crée une cellule qui regroupe * colonnes dans cette ligne.

Dans chaque ligne, la taille totale des colonnes doit être égale à 12. On peut donc choisir de diviser la surface d’affichage en 12 colonnes de taille 1, ou bien en 3 colonnes de taille 4, ou encore en une colonne de taille 4 et une colonne de taille 8.
![](images/7.png)


- Démonstration
Créez dans le monstrationrépertoire hello-world-bootstrap un fichier CSS style.css contenant le code ci-dessous.
```
.row {
    margin-bottom: 15px;
}

.row [class^="col-"] {
    padding-top: 10px;
    padding-bottom: 10px;
    background-color: #eee;
    border: 1px solid #ddd;
    background-color: rgba(86,61,124,.15);
    border: 1px solid rgba(86,61,124,.2);
}
```

Ce fichier permettra de mieux visualiser les éléments de la grille Bootstrap.

Ensuite, éditez le fichier index.html comme indiqué ci-dessous.
```
<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="bootstrap/css/bootstrap.min.css" rel="stylesheet">
    <link href="style.css" rel="stylesheet">
    <title>Hello world with Bootstrap</title>
</head>
<body>
    <div class="container">
        <h1>Hello world!</h1>
        <div class="row">
            <div class="col-md-3">
                Zone de gauche
            </div>
            <div class="col-md-7">
                Zone du centre
            </div>
            <div class="col-md-2">
                Zone de droite
            </div>
        </div>
    </div>

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
    <script src="bootstrap/js/bootstrap.min.js"></script>
</body>
</html>

```
On remarque au passage que le total des tailles des colonnes (3+7+2) est bien égal à 12. Ouvrez cette page dans un navigateur Web. Le placement des colonnes s’adapte à la surface d’affichage disponible.

Voici le rendu avec une surface d’affichage importante.
![](images/8.png)



Voici le rendu lorsque la surface d’affichage diminue.
![](images/9.png)



# TRAVAUX PRATIQUES

# Dropdowns
Menu contextuel commutable permettant d'afficher des listes de lien. il faut ajouter le code suivant dans son code Html à la position souhaitée.
- Exemple
Création d'un menu déroulant avec des liens vers des pages.

```
<div class="dropdown">
  <button class="btn btn-default dropdown-toggle" type="button" id="dropdownMenu1" data-toggle="dropdown" aria-haspopup="true" aria-expanded="true">
    Dropdown
    <span class="caret"></span>
  </button>
  <ul class="dropdown-menu" aria-labelledby="dropdownMenu1">
    <li><a href="#">Action</a></li>
    <li><a href="#">Another action</a></li>
    <li><a href="#">Something else here</a></li>
    <li role="separator" class="divider"></li>
    <li><a href="#">Separated link</a></li>
  </ul>
</div>
```
on obtient le résultat ![](images/10.png)



# Les Onglets 

Notez que la .nav-tabsclasse nécessite la .navclasse de base.
Exemple: 
```
<ul class="nav nav-tabs">
  <li role="presentation" class="active"><a href="#">Home</a></li>
  <li role="presentation"><a href="#">Profile</a></li>
  <li role="presentation"><a href="#">Messages</a></li>
</ul>
```

# A vous de jouer 
En vous servant de ce cours et de la documentation sur boostrap [ici](https://getbootstrap.com/docs/4.1/getting-started/introduction/), réalisez cet exercice.
Il s'agit de réproduire la meme page en utilisant les différentes notions de bootstrap.

![](images/11.png)




# Référence
http://prof.bpesquet.fr/tutoriel/premiers-pas-framework-bootstrap/


http://www.opentuto.com/informatique/maitriser-bootstrap-3-par-la-pratique/


https://getbootstrap.com/docs/4.0/getting-started/introduction/
