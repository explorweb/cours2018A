# ELU 525: Exploration du web

# Cours sur le web profond

## Partie théorique:

### I- GENERALITES SUR LE WEB:
**I.1- LE WEB SURFACIQUE:**
* Le web surfacique désigne la partie du web accessible au grand public.Il contient toutes les pages web indexées par les moteurs de recherche classiques.Néanmoins, il ne représente que 10% de l’information qu’on peut trouver sur Internet.Selon une statistique datée du 14 Juin 2015 , 14.5 milliards de pages web sont indexées par Google.

**I.2- LE WEB PROFOND OU DEEP WEB:**
* Le web profond est la partie du web inaccessible par les moteurs de recherche classiques, c’est-à-dire non indexée ou dont le contenu est d’accès limité. On cite par exemple les sites web accessibles via une connexion sécurisée comme les transactions bancaires sur des comptes en ligne ou bien les vidéos à la demande sur Netflix.

 *Pourquoi certains sites sont indexés et d'autres non ?*
 
 * Pour qu'un site internet soit indexé par un moteur de recherche, il faut qu'il respecte des normes. Ces normes peuvent intervenir sur le format, le contenu et l'accessibilité des robots sur les sites. Et pour que le site en question soit indexé il faut qu'il respecte ces normes instaurées par les moteurs de recherche afin de figurer dessus.
 
 * Certains sites ne sont pas indexés car le format des fichiers web est différents du HTML (HyperText Markup Language)ou bien les fichiers sont très volumineux et alors ne sont pas pris en compte. De plus si un robot d'indexation ne peut pas avoir accès au contenu de la page, cette dernière ne pourra être indexée. Il peut aussi y avoir des problèmes dans l'écriture de l'URL (une syntaxe incorrecte ou autres ).
 
 * Tous ces paramètres entrent en compte lors d'une indexation et s'ils ne sont pas respectés, le site en question ne pourra pas être indexé et son contenu ne figurera pas sur le moteur de recherche.

**I.3- LE WEB OBSCURE OU DARK WEB:**
* Le dark web est le contenu du web qui existe sur des réseaux superposés appelés  darknets. Ce sont des petits réseaux pair à pair en plus des réseaux Tor, I2P et autres gérés par des entités privées dont le partage est anonyme (les adresses IP ne sont pas partagées publiquement). Ces réseaux utilisent des protocoles spécifiques intégrant des fonctions d’anonymisation. Le dark web constitue une petite partie du web profond.Le contenu du dark web est divers mais souvent illégal: cybercrime,vente et achat de biens ou services illégaux,partage de fichiers confidentiels,...etc .
  
* Il faut bien faire la différence entre le deux termes : le Deep Web (l’Internet non indexé) et le Dark Web (les bas fonds obscurs de l’Internet).
  
![](https://i0.wp.com/www.himanshutech.com/wp-content/uploads/2018/06/Deep-Web-and-Dark-Web-Explained.png?resize=696%2C464&ssl=1)

### II- LE DEEP WEB OU WEB PROFOND:
**II.1-  COMMENT ACCEDER AU DEEP WEB?**  

*VPN:*  

![](https://upload.wikimedia.org/wikipedia/commons/0/0f/VPN_site-to-site.jpg)  
* Un réseau privé virtuel, abrégé VPN – Virtual Private Network , est un système permettant de créer un lien direct entre des ordinateurs distants, en isolant ce trafic. Toutes les données que vont s’échanger les utilisateurs seront donc cryptées, à l’aide de différents protocoles(PPTP, L2TP, …) et passeront par un tunnel sécurisé reliant leurs machines.

 * Intérêt des VPN : Utiliser un VPN permet aux utilisateurs de garder leur identité cachée. En effet, un VPN permet de ne pas dévoiler son adresse IP ainsi que ses informations personnelles, telles que les mots de passe, sur le Deep Web. Notre adresse IP va être remplacée par une adresse IP étrangère délivrée par un serveur situé à l’étranger. Ainsi, lorsque l’on surfe sur internet, seule cette adresse IP est visible. Un VPN peut également être utilisé d’un point de vue professionnel car il permet de réaliser du travail à distance, en accédant à un réseau interne depuis une autre machine.Toutefois, l’utilisation d’un VPN ne permet pas d’être totalement anonyme sur le Web, les fournisseurs de VPN pouvant toujours avoir accès à nos données personnelles.[4]

*Proxy:*  

*	C’est un serveur qui fait les requêtes sur Internet. L’utilisation d’un service proxy permet de ne pas utiliser votre propre adresse IP et donc de ne pas vous identifier.Si on établit une connexion à un proxy par un VPN , le contenu des  paquets qu’on lui envoie est inexploitable par une personne qui décide de les intercepter puisque le VPN chiffre le contenu des paquets.  

*Tor:*
* Tor est un réseau informatique superposé mondial et décentralisé. Il se compose d’un ensemble de proxies, appelés relais . Ce réseau permet d’anonymiser les paquets TCP .  
Dans un réseau Tor, la requête d’un internaute quitte son ordinateur et passe par plusieurs autres ordinateurs présents dans le même réseau et utilisant Tor jusqu’au serveur à qui est adressé la requête. Il est le seul à pouvoir déchiffrer le contenu cette requête .C’est le principe du routage en oignon (qui donne son nom à Tor).Contrairement à un réseau normal, les paquets tor prennent un chemin aléatoire. Le client négocie un ensemble de clés de chiffrement pour chaque nœud emprunté par les paquets.Les figures ci-dessous schématisent le fonctionnement de Tor et le fonctionnement d’un réseau normal:  
Réseau normal:  
![](https://www.supinfo.com/articles/resources/171562/3109/3.png)  
Réseau Tor:  
![](https://www.supinfo.com/articles/resources/171562/3109/4.png)  
* Tous les échanges entre relais Tor  sont sécurisés et cryptés. Tor propose également à ses utilisateurs un ensemble de services cachés sur internet en masquant l’identité (adresse IP, …) du serveur qui les héberge ; ce dernier recevra de Tor une adresse avec l’extension ".onion" (comme par exemple "nomdusite.onion") et ne pourra être accessible que par des internautes du réseau Tor. L’accès d’utilisateurs à un service web caché se fait selon un protocole défini par Tor. 
* Pour accéder au réseau Tor il faut utiliser le navigateur du même nom : Tor Browser. Le logiciel Tor Browser permet d’aller sur le réseau Tor, et donc de consulter les sites du deep web.  

*Fonctionnalités de TOR:*  

Tor propose à ses utilisateurs des fonctions axées sur la vie privée:  

1. Suppression des cookies après chaque session – Tor supprime tous  les cookies d’une session juste après sa fermeture.Cette suppression s’assure de ne laisser aucune trace de vos navigations.  
2. Des niveaux de sécurité: Différents  niveaux de sécurité sont conçus afin de  neutraliser les attaques contre votre navigateur.  
3. Une nouvelle identité :Il est possible de changer totalement votre session de navigateur. Si vous utilisez d’utiliser cette fonction, le navigateur TOR va redémarrer en effaçant toutes les informations de votre navigation.  
4. Accéder à des sites en .onion :C’est l’une des particularités de TOR. Il propose des sites avec une adresse en .onion accessibles uniquement via le navigateur TOR. 

### III-LE CONTENU DU DEEP WEB:  

* Cette couche internet, possède sa propre monnaie(les Bitcoins)qui est un type de paiement "peer To Peer",immédiat et sécurisé, ses propres codes(Confiance) et ses propres modes d’accès (TOR).Afin d’atteindre la majorité des sites non référencés, il faut également passer par TOR, un navigateur anonyme. Aussi, il faut connaître à l’avance les adresses que l’on souhaite visiter qui ressemblent souvent à cela :kpvz7kizv5agwt35.onion . Parmi ces pages on retrouve des plateformes de vente en toute forme ( drogue, armes...) et certaines personnes proposent des services (assassinats...).
Tout au long de la recherche on peut souvent tomber sur des plateformes de e-commerce comme Silkroad.
Tout comme Amazon Marketplace, il suffit de créer un compte sans informations personnelles, ensuite laisser le moteur de recherche remuer la base de données des différents produits mis en ligne par les vendeurs. On pourra facilement repérer le produit qui nous intéresse.
Par exemple, il est possible de choisir parmi les quelques milliers de drogues proposées : hash, héroïne, cocaïne ou LSD… Tout d’abord il faut se mettre en relation avec le vendeur, ensuite, lui envoyer l’adresse de livraison cryptée, il sera la seule personne en mesure de lire et enfin lui payer en Bitcoins : une monnaie 100% virtuelle développée par un japonais « Satoshi Nakamoto ».  


![](https://upload.wikimedia.org/wikipedia/en/4/42/Silk_Road_Marketplace_Item_Screen.jpg)  

![](http://www.thehiddenwiki.net/wp-content/uploads/2013/05/silk-road.jpg)  

* Silkroad une plateforme d’e-commerce appartenant au Deep Web pose un gros problème aux forces de l’ordre vue que premièrement il n’y a pas de trace postale : adresse cryptée connue que par le marchand, deuxièmement il n’y a pas de trace digitale : Tor presque intraçable et enfin et surtout il n’y a pas de trace de transaction monétaire : les bitcoins passent de compte en compte sans arrêt et sont impossible à suivre.
Les fondateurs de Silkroad ont décidé d’ouvrir the Armory, car comme bons entrepreneurs, ils cherchent à se diversifier. Mêmes principes les vendeurs proposent dans cette plateforme des biens qui sont des armes.
On peut donc selon les stocks acheter un AK-47, que l’on pourra se faire livrer par la poste, ou en dead-drop (on donne des références GPS et le vendeur pose/enterre/cache le produit aux coordonnées).  
* Le deep Web ne se limite pas uniquement sur Silkroad, mais on fait assez de découvertes en passant de lien en lien.
on peut également trouver de petites annonces de tueurs  avec des tarifs différenciés selon les tâches demandées et selon le type de personne : prenons comme exemple 10 000 euros pour une personne normale, 50 000 pour les politiciens...de plus, on peut acheter des numéros de cartes bancaires ou de “clones” avec le code PIN  dans le but de l’utiliser en magasin ou pour des retraits.  
En outre, on peut également acheter un diplôme: avec inscription dans la base de données de l’école concernée, faire des faux papiers, faire disparaître une personne de tout base de donnée (de son compte en banque, de la sécurité sociale)...   

## Aspect juridique du deep web :  

L'anonymat protège la vie privée et la liberté fondamentale des utilisateurs mentionnées dans le code civil(article 9) et la Convention européenne des droits de l’homme (article 8).Ainsi, l'utilisation du deep web est tout à fait légitime et n'est pas à l'origine illicite.Les dissidents ou les défenseurs de droits s'y rendent pour communiquer librement dans des Etats qui limitent la liberté d'expression.
Néanmoins, les lois sont transgressées au moment où on achète des biens ou des services illicites sur cette plateforme.Par ailleurs, avant d'effectuer un achat en Bitcoin, il faut s'assurer que les exigences réglementaires sont respectées.Les lois concernant le commerce de données par des moyens illicites, le vol de données et leur usage frauduleux sont aussi applicables sur le deep web.  
N'oubliez pas que sur le deep web il y a du bon mais aussi le pire, donc soyez extrêmement prudent, patient et choisissez bien les sites que vous souhaitez visiter. Sur le deep web **vous êtes seul responsable de vos actes**. 

## Partie pratique:

Dans cette partie, vous allez apprendre à naviguer dans le deep web.  
Voici les prérequis pour ce TP:  

* Installer un VPN(comme [Hotspot Shield](https://www.hotspotshield.com/fr/) ou [CyberGhost](https://www.cyberghostvpn.com/fr_FR/?media_source=google_adwords&campaign=France-Search-Brand&adgroup=CyberGhost&keyword=cyberghost&matchtype=e&extension=&gclid=Cj0KCQiA2o_fBRC8ARIsAIOyQ-l1BRIpVVZZl-P2vQV1LK1jIO0Jc_tCvUmhgtZW7szXtRfBvdzBZpoaAqHqEALw_wcB)).Ce VPN assurera une confidentialité totale en masquant votre adresse IP et toutes vos données personnelles.
* Installer un antivirus si ce n'est pas déjà fait ([Norton internet security ](https://support.norton.com/sp/fr/fr/home/current/solutions/kb20090708112600EN_EndUserProfile_fr_fr))
* Télécharger un Pare-Feu ([Peer block](https://peerblock.fr.uptodown.com/windows/telecharger)) qui permettera de bloquer des connexions à votre ordinateur provenant d’adresses IP suspectes  
* Installer [Tor Browser](https://www.torproject.org/download/download-easy.html.en)  
Sur votre navigateur habituel, vérifiez votre adresse IP.Pour ce faire, rendez-vous sur le site https://www.whatismyip.com
![](https://screenshots.firefox.com/UXRhOls1Pj08lFKm/www.whatismyip.com). Il existe d'autres sites qui permettent d'afficher votre adresse IP.  

Maintenant que vous avez téléchargé et installé tous les logiciels, vous allez démarrer votre Tor browser.  
Vous vous renderez sur le même site qu'avant depuis Tor pour vérifier que __votre adresse IP est masquée__.  
Si l'adresse IP indiquée  par le site est différente de votre vraie adresse, démarrez votre VPN et votre pare-feu.L'antivirus doit être actif.  
A présent, vous êtes prêts pour naviguer dans le deep web :wink:  

La principale adresse sur Tor est bien __The Hidden Wiki__. Du même genre que Wikipedia – à l’exception du contenu – The Hidden Wiki vous propose des liens vers différents sites du réseau TOR.C'est un site très essentiel lorsque l’on souhaite explorer le deep web car il permet d’éviter que l’on accède malencontreusement aux sites indésirables.  
Pour aller sur le Hidden Wiki, vous n’allez pas entrer au niveau de la barre des titres  de notre navigateur une URL de la forme http://www.nomdusite.domaine comme d’habitude dans un navigateur classique, mais plutôt une URL constituée d’une combinaison de lettres et de chiffres suivi de .onion.  
Pour se rendre sur le Hidden Wiki, *tapez* l’adresse « zqktlwi4fecvo6ri.onion » dans la barre des titres de Tor Browser et appuyez sur la touche « Entrée » de votre clavier. Le navigateur vous ouvre une page où est présent  un lien (comme le montre la capture ci-dessous), qui vous permettra d’accéder au Hidden Wiki :  

![](https://i.imgur.com/ZbN1BYR.png)

Une fois vous cliquez sur le lien « Hidden Wiki », vous êtes redirigés vers la page d’accueil du Hidden Wiki : 

![](https://i.imgur.com/EPGKXks.png)

Vous y retrouvez un ensemble de liens vers des sites du deep web classés par catégorie (services financiers, services commerciaux, réseaux sociaux, …). 

Si vous essayez d’entrer l’URL qui permet d’accéder au Hidden Wiki dans un navigateur conventionnel (comme mozilla firefox, internet explorer, …), le navigateur ne trouvera pas la page désirée :

![](https://i.imgur.com/bv8Na1R.png)

En parcourant la page d’accueil du Hidden Wiki, vous trouverez un lien vers l’un des meilleurs moteurs de recherche du deep web : Not Evil.

![](https://i.imgur.com/eA35xhs.png)

En cliquant dessus le navigateur vous redirige vers le moteur de recherche Not Evil :

![](https://i.imgur.com/4khXK8j.png)

Lorsque vous effectuez une recherche sur le moteur de recherche Not Evil, par exemple le mot « deepweb », vous constatez que les liens vers les pages retournées par notre requête ont toutes pour extensions .onion : 

![](http://3.bp.blogspot.com/-JX5_btlREns/Va4ZvAahw8I/AAAAAAAAAX8/NosP6vJPc14/s1600/c27.PNG
)


A présent vous savez comment explorer le deep web!
## Références ##  
  1-Article sur Wikipédia: Le web surfacique disponible sur https://en.wikipedia.org/wiki/Surface_web  
  2-Article sur Investopedia: Deep web disponible sur https://www.investopedia.com/terms/d/deep-web.asp  
  3-Article sur Wikipédia:Darknets disponible sur https://en.wikipedia.org/wiki/Darknet#Uses   
  4-Article sur wikipédia :VPN https://fr.wikipedia.org/wiki/R%C3%A9seau_priv%C3%A9_virtuel   
  5-Tutoriel sur openclassrooms https://openclassrooms.com/fr/courses/2939276-surfez-incognito-sur-internet-avec-le-reseau-tor/2954671-vers-un-debut-danonymat-notion-de-proxy   
  6-Le deep web https://www.supinfo.com/articles/single/3109-deep-web    
  7-Fonctionnalités de Tor https://meilleurvpn.net/19119/navigateur-tor/  
  8-COMMENT ACCEDER AU WEB INVISIBLE (DEEP WEB) EN TOUTE SECURITE http://jacquesgoueth.blogspot.com/2015/07/comment-acceder-au-web-invisible-deep.html  
  

