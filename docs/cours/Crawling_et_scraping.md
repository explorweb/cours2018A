# Crawling et scrapping

## Plan du cours

Introduction

I) Le Crawling

1. définition et fonctionnement
2. limites des performances
3. architecture physique
4. architecture logicielle

II) Le Scraping

1. définition et fonctionnement
2. limites
3. architecture
4. utilisation

III) Aspect juridique

Conclusion
Réféfences

## Intro : 
Depuis la création du web le nombre des sites web connaît une croissance exponentielle  , et on estime actuellement  que ce nombre a depassé la barre des 1 milliards . L'abondance de l’information sur internet est donc un fait mais accéder à l’information rapidement et avec précision s'avère etre le challenge à relever  
## 1. Le Crawling  :
 
### 1.1   Definition et fonctionnement
 Originellement le web crawling est une technique qui permet d'explorer le web en parcourant les differentes pages afin d'en établir la cartographie .Le premier web crawler (world wide web wanderer) était utilisé pour mesurer la croissance du web . 
 Conceptuellement , l'algorithme supportant un crawler est simple et n'utilise qu'une seule structure de données qu'est les url . 
En prenant un nombre d'adresse de sites préalablment connues comme base (candidats initiaux) , le programme consulte les differentes pages et retrouve les liens qu'elle contient . 
Ensuite , pour chaque lien l'algorithme verifie si l'adresse est deja connues , si non il rajoute l'adresse à l'ensemble de pages à visiter et elle fera partie du prochain lot à consulter .
Le processus est alors répété plusieurs fois.


### 1.2 Limites des performances
Tout d’abord,le nombre de pages crawlées est limité par la bande passante et l’éspace disque. On éstime aujourd’hui à 10^10 pages indexées par
Google. Si une page fait en moyenne une taille  de 15kB, il faudrait 4 millions de dollars pour récupérer et stocker tout le Web. Pour maintenir une base relativement à jour, un crawler doit donc
télécharger chaque seconde un nombre de pages pouvant atteindre plusieurs milliers
De plus les pages sont dynamiques et en perpetuel changement , il est donc essentiel de verifier et mettre à jour les pages déja visitées . 
On souligne aussi les manoeuvre de protection commercialisées par des entreprise pour se proteger des crawlers . par exemple le fichier “robots.txt” ou la balise HTML “meta robots”sont des outils utilisé pour specifier au crawler quelles pages visiter. 
Avant d'acceder à un site web pour la première fois , le crawler télécharge le fichier robot.txt où sont specifiées les pages à ne pas télécharger .Cependant , le crawler peut decider de l'ignorer. De façon général les moteurs de recherche respecte cette convention.
 ### 1.3 Architecture physique
Pour augmenter les performances des crawlers face à une croissance exponnontielle du nombre de pages web , le stockage des pages est séparé entre plusieurs machines , situées dans des lieux géographiques différents . 
Cependant il faut s'assurer que les sites visités par chaque machine sont bien disjoint ce qui peut se faire en repartissant les espaces des adresses web![](https://i.imgur.com/OBQ2iyj.jpg)

Dans ce cas, le crawler en lui-même n’utilise qu’une seule machine mais plusieurs interfaces
réseau afin de bénéficier d’une plus grande capacité de téléchargement.Le stockage des
informations récoltées est effectué sur plusieurs machines différentes accessibles en réseau
local.
### 1.4 Architécture logicielle
![](https://i.imgur.com/Let43Sx.jpg)

L'ordonnanceur sert à prioritiser certaines adresses et permet de mieux gerer les temps mort entre les telechargements
exemple : grouper les pages d’un même site web et utiliser le temps nécessaire à leur téléchargement pour émettre les requêtes de résolution DNS des URLs qui suivent dans la file. 
Au début , le but des crawlers était de cartographier  le web , et le contenu des pages n'était utilisé que pour récuperer les autres URL mais par la suite les appliactions utilisant ces données ont progresser et le contenu est devenu analysé , notamment à des fins d'indexation .c’est la naissance des moteurs de recherche.






## 2.Le Scraping   


### 2.1 Definition & fonctionnement

Le mot vient de l'anglais 'scrape' qui signifie gratter. L'idée est donc de gratter des pages web pour récolter l'information voulue. Cela revient à faire des copier coller. Cependant le scraping est en général assuré par des bots, ou robots, qui s’occupent de ce travail périodiquement.

![](https://i.imgur.com/Uo6IN8q.png) 

*Principe en image. :http://www.luxury-concept.com/dev-blog/346-le-scaping-des-donnees-pourquoi-et-comment.html*

Le principe de base du scraping est simple : transformer des informations non structurées présentes dans des pages web en données structurées facilement exploitables. On désigne par scraper le nom du programme qui effectue cette action.

Contrairement à un crawler (programme vu plus haut) qui découvre lui-même les sites parcourus et les pages web téléchargées, le scraper travaille sur un site ou ensemble de sites connus par avance. Le scraper pourra alors être  paramétré de façon à récupérer les données
souhaitées sur le site en question ou bien un programme développé spécifiquement pour cette tâche et donc parfaitement adapté au site. 

Les avantages sont donc :

-Automatiser cette action qui est fastidieuse pour un humain.

-Possibilité de structurer nos données sortantes.

-Possiblité de choisir le format des données sortantes.



Par exemple dans l'exemple ci contre ou l'on illustre un exemple de scrapping possible sur une page du [Monde](https://www.lemonde.fr/).

![](https://i.imgur.com/TASipK5.png)



### 2.2 Limites du scraping : 

Le support de travail des scrapers étant le même que les crawlers, les pages web, on
retrouve les mêmes limites que précédemment. De plus le scraping est plus contraingant que le crawling car nécessite de connaître au préalable l'architecture du site. Il existe d'ailleurs des mesures spécifiques pour l’empêcher.
Certains sites changent régulièrement la structure du code html de leurs pages. S’il est
possible que cela ne change rien visuellement dans un navigateur web, cela va empêcher le
programme d’en extraire les données. Bien entendu, le créateur du scraper pourra toujours
le corriger pour prendre en compte les modifications mais il ne sera pas à l’abri d’autres changements. Cela en revanche ne perturbe pas le travail d'un crawler.

### 2.3 Architecture

Contrairement aux crawlers pour lesquels le domaine exploré est possiblement illimité, les scrapers sont destinés à agir sur un nombre réduit et connu par avance de sites
web. S’il sera possible de rencontrer des crawlers utilisant un parc de plusieurs milliers de machines, un scraper n’aura en général besoin que d’une seule machine, en tout cas pour la
partie chargée du téléchargement des données.

### 2.4 Utilisation

Les moyens employés pour scrapper sont variés en raison des larges possibilités que propose le scrapping. Il y a des logiciels, des frameworks ainsi que des librairies, des addons mise à disposition. En Voici plusieurs exemples :

1. Via navigateur : 
En visualisant la page et avec de simples copier/coller, un utilisateur peut récupérer les données d’une ou plusieurs pages afin de les réutiliser dans un autre contexte, ce qui correspond à la définition du scraping. Bien entendu c'est trop fastidieux, il existe donc des addons pour ce faire (ex : [DownThemAll](https://www.downthemall.net/) pour Firefox). 

2. Via un logiciel : 


    Import.io : logiciel disponible en ligne est très simple d'utilisation mais très limité. Il permet, selon une liste d’URL de page web, de scraper automatiquement toute l’information. Celle-ci est alors disponible sous la forme d’un tableau exportable en .csv, .xlmls ou .sheets pour analyse. Import.io est très simple et ne demande pas de connaissances en programmation.


3. Via un framework : 

     Scrapy est un framework collaboratif et open-source pour extraire des données. Il est rapide, et facilement extensible, mais il s’adresse aux développeurs ayant des connaissances en python et connaissant XPath. Le framework possède en plus une documentation extensive pour comprendre son fonctionnement. Parmi les composants du framework – scrapy engine, scheduler, downloader, spiders, item pipeline -, seuls les spiders sont à écrire par l’utilisateur.
     Les spiders sont des scripts appelant les différents composants qui spécifient où scraper les données, quoi scraper et comment le faire.
Les données, sous la forme d’item, peuvent être exportées sous un format spécifique avec un peu de programmation.
![](https://i.imgur.com/4vrwZhv.png)                     
*Fonctionnement de scrapy  http://www.luxury-concept.com/dev-blog/346-le-scaping-des-donnees-pourquoi-et-comment.html*

   Scrapy est donc un excellent outil pour scraper des données, quoiqu’il s’adresse à des utilisateurs avancés. 

4. Les libraires
La plupart des langages de programmation disposent au moins d’une librairie basique permettant de travailler avec le web.
-PHP : [Goutte](https://github.com/FriendsOfPHP/Goutte) 
-Java : [Jaunt](https://jaunt-api.com/)
-Python : [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)


Mise en oeuvre : 

Voici un tuto très simple utilisant la bibliothèque [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) de python. Et qui a pour finalité d'extraire des données de wikipedia 
https://code.tutsplus.com/fr/tutorials/scraping-webpages-in-python-with-beautiful-soup-the-basics--cms-28211

## Apect juridique


Nous venons de voir les différents concepts et technique sur les façon de récuperer des données sur internet. Il reste à se questionner sur la réglementation de ces pratique.

Premièrement il faut bien comprendre que scraper ou crawaler n'a pas pour but de voler des données. L'idée est plus de récupérer de manière périodique des données sur un site. Ces dernières osnt en grande partie accessible à un utilisateur qui naviguerait de manière régulière sur le site. L'intérêt de ces pratiques et donc d'automatiser et de structurer les données. Ce qui fait que cette activité n'est pas illégale, cette pratique est même facilité et mise à disposition sur plusieurs site.

Cependant, il reste normal que des entreprises possédant des sites ne veuillent pas laisser certaines donnée en libre récolte à leur concurrents. Pour se défendre on peut rédiger des conditions d'utilisation plus ou moins strictes, ces dernières doivent être claires et visibles. Mais il est très difficile d'interdire totalement le scraping et il s'agit donc en géneral d'en faire une utilisation prudente et peu instrusive.

Il y a un manque certain dans la réglementation pour définir ce qui est autorisé et ce qui est
interdit. Internet est un outil encore trop jeune et son développement est tellement rapide qu’il est impossible que la juridiction suive le rythme. 

Certaines entreprises qui sont sans défense d’un point de vue légal se tournent vers une protection technique. [Impreva](https://www.imperva.com/) propose un outil qui détecte et bloque les accès automatisés. Cependant certaines de leurs solutions peuvent rendre un site web peu ergonomique. Comme l'utilisation de CAPTCHA, qui souvent est peu appréciée par les internautes.

Dans le cadre de l'open data, il y a une réglementation plus rigoureuse. Il est indispensable de vérifier la provenance des données et le cadre juridique dans lequel se place son propriétaire. Au sein des pays
membres de l’UE, les données du secteur publique sont réutilisables pour un coût très faible ou nul depuis une directive de décembre 2011. 
Pour terminer, la finalité d’une action détermine le caractère publique d’une information : les données produites par un opérateur privé dans le cadre d’une mission de service publique, sont des données publiques, à l’exception des missions industrielles, commerciales et de sécurité nationale.




## Conclusion

La taille du Web ne cesse de grossir, et les technologies qui l'entourent se multiplient. Les données sont aujourd'hui le nouveau pétrole et peuvent être un moyen considérable d'expansion pour les entreprises. 
Le crawling, le scraping et l’open data n’en sont qu’au début d’une croissance certaine. Cependant, il faut savoir rester prudent car la quantité d’information est telle qu’il serait très facile de s’y perdre. De nouvelles problématiques se posent pour pouvoir gérer et réglementer cette masse de données.



## Références : 

1. http://www.luxury-concept.com/dev-blog/346-le-scaping-des-donnees-pourquoi-et-comment.html
2. https://code.tutsplus.com/fr/tutorials/scraping-webpages-in-python-with-beautiful-soup-the-basics--cms-28211
3. https://www.downthemall.net/
http://stanford.edu/~wpmarble/webscraping_tutorial/webscraping_tutorial.pdf
4. https://zestedesavoir.com/billets/2057/scraper-des-donnees-sur-une-page-web-en-python-avec-beautifulsoup-1/
5. http://www.acme.byu.edu/wp-content/uploads/2017/08/WebScraping2.pdf
6. http://www.acme.byu.edu/2018-2019-materials/
7. https://yanfei.site/docs/dpsa/references/PyWebScrapingBook.pdf
8. http://stanford.edu/~wpmarble/webscraping_tutorial/webscraping_tutorial.pdf
