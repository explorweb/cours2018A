# Django le framework !

1. Introduction à Django
    1. Qu’est ce qu’un framework ?
    2. Types de frameworks
    3. Frameworks : Quels avantages et quels inconvénients ?
    4. Django, c'est quoi ?
    5. Design pattern MVC/MVT
2. Créer son premier projet sur Django
    1. Créer un projet et une première application
    2. Conception des premiers modèles
    3. Le traitement des données avec les vues et le routage d'URL
    4. Présentation du contenu avec les templates
    5. Administration du projet avec le scaffolding

# I - Introduction à Django

## 1 - Qu'est ce qu'un framework ?  
Un framework est l'ensemble de composants logiciels à la base d'un logiciel ou d'une application( bibliothèques,classes, helpers..etc).Il décrit les types de programmes à concevoir et leur mode d'interaction.  
Un framework permet de **simplifier le travail des développeurs informatiques** en offrant une architecture réutilisable et adaptée à leurs besoins. En outre, il peut être amélioré par l'expérience des développeurs.Les frameworks sont utilisés pour développer une application mobile, un site web, un jeu,..etc 

## 2 - Types de frameworks  
On peut classer les frameworks de la manière suivante:  
* **Frameworks d'infrastructure système** utilisés pour le développement des systèmes d'exploitation et des interfaces graphiques (Microsoft .Net, Apache Struts,...).
* **Frameworks d'intégration intergicielle** permettent l'interconnexion de systèmes divers.
* **Frameworks d'entreprises** sont spécifiques aux applications utilisées par les entreprises. 
* **Frameworks de gestion de contenu** sont les fondations d'un système de gestion de contenu — pour la création, la collecte, le classement, le stockage et la publication de « biens numérisés ».

Source : [Wikipedia](https://fr.wikipedia.org/wiki/Framework)

## 3 - Frameworks : Quels avantages et quels inconvénients ?  
En utilisant les frameworks, les développeurs codent de façon homogène. Ainsi, quand un développeur rejoint un projet basé sur un framework qu'il connaît, la compréhension de l'architecture lui sera plus simple et plus rapide que s'il avait dû s'approprier les outils au préalable. De plus, l'adoption d'une structure commune garantit un code organisé et facilement réutilisable. 

En revanche, les frameworks doivent être souples et modulables afin qu'ils soient adaptés à différents projets. Certains nécessitent cependant un temps d'apprentissage plus long que d'autres. 

Source: [Openclassrooms](https://openclassrooms.com/fr/courses/1871271-developpez-votre-site-web-avec-le-framework-django/1871361-creez-vos-applications-web-avec-django)  

## 4 - Django, c'est quoi ?  

Django est l'un des  frameworks applicatifs Python destinés au développement d’applications web. Créé en 2003 dans une agence de presse, Lawrence Journal-World, le framework est proposé au grand public deux ans plus tard. En 2008, la fondation Django Software a été créée. Aujourd'hui, Django est très populaire. Il est utilisé dans des applications web très célèbres comme *Instagram* ou *Pinterest*.  

Django permet le développement rapide de meilleures et plus performantes applications web. Il automatise des tâches répétitives  telles que l'écriture de requêtes destinées à une base de données. Il propose d'autres fonctionnalités comme une bibliothèque de traduction on un espace membres. 

## 5 - Design pattern MVC/MVT

### Introduction aux ORM

Avant de voir les spécificités des design pattern MVC et MVT, il convient de s'intéresser aux ORM. C'est terme anglais signifiant _Object Relational Mapping_, littéralement _Mappage objet-relationnel_. Il s'agit d'un programme informatique qui se place entre la couche de stockage des données dans la base de données relationelle et la couche applicative. Elle permet une abstraction des données et une représentation sous forme d'objets. Ainsi dans la conception de notre application, nos informations seront stockées sous forme d'objets informatiques, et l'ORM s'occupera tout seul de la correspondance avec la base de données.

### Design pattern MVC/MVT

Un _design pattern_, ou _patron de conception_ en français, est une façon de concevoir une application informatique qui est considérée comme bonne et efficace.

Le _design pattern_ Modèle-Vue-Contrôleur ou MVC est un type d'architecture logicielle destiné aux interfaces graphiques lancé en 1978 et très populaire pour les applications web. Le motif est composé de trois types de modules assurant différents rôles:  
   * Le modèle (Model) représente, souvent sous forme d'objet, les données à utilisée par l'application et utilise un ORM pour l'interaction avec la base de données.
   * La vue (View) contient la présentation des données via  une interface graphique.  
   * Un contrôleur (Controller) contient la logique concernant les actions effectuées par l'utilisateur.

   L'idée importante dans ce design pattern est de séparer distinctement les tâches effectuées par les différents éléments. Ainsi la conception et la maintenance sont simplifiées.

   ![](https://upload.wikimedia.org/wikipedia/commons/b/b4/MVC_Diagram_%28Model-View-Controller%29.svg)  
   Source : [Wikipédia:MVC](https://fr.wikipedia.org/wiki/Mod%C3%A8le-vue-contr%C3%B4leur)  
   
   Django utilise l'architecture MVT (modèle-vue-template) qui s'inspire de MVC:   
   * Le **modèle** interagit avec une base de données via un ORM. Tous les modèles sont réunis dans un fichier python `models.py`.  
   * La **vue** reçoit [une requête HTTP](https://openclassrooms.com/fr/courses/1118811-les-requetes-http) et renvoie une réponse HTTP convenable (par exemple si la requête est une interaction avec une base de données, la vue appelle un modèle pour récupérer les items demandés). Les vues se trouvent dans le fichier `views.py`
   * Le **template** est un fichier [HTML](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3/1604361-votre-premiere-page-web-en-html) récupéré par la vue et envoyé au visiteur avec les données des modèles.  
   
   La figure ci-dessous montre comment les différents composants de l'architecture MVT de Django interagissent pour répondre à la requête d'un utilisateur. Ici le contrôleur ne correspond pas au contrôleur du MVC, mais à Django en lui même qui gère en interne tout ce qui est liée au choix de la vue à laquelle envoyer la requête HTTP,...
   ![](https://camo.githubusercontent.com/2fd581466b72e4b92e5893ea842b0ee085fff68d/68747470733a2f2f646f63732e676f6f676c652e636f6d2f64726177696e67732f642f314c456f30356854445f45435a355647356f664d6468327434445f4c6769416e626c752d65305435386645342f7075623f773d39363026683d373230)  
   Source: [GitHub](https://github.com/emencia/emencia-django-training/wiki/Mod%C3%A8le-MVT)  


# II - Créer son premier projet sur Django
## 1 - Créer un projet et une première application

Après avoir installé Django, nous pouvons créer un nouveau projet.
La première étape est de créer un répertoire qui contient des fichiers utiles au fonctionnement du projet. Pour créer ce répertoire, on tape la commande suivante:
```shell
$ django-admin.py startproject mon_projet
``` 
Ce répertoire *mon_projet* contient un script `manage.py` qui permettra d'exécuter des commandes utiles au sein du projet. Il contient aussi des fichiers propres au projet: `settings.py` contient la configuration globale du projet, `urls.py` est le contrôleur frontal du projet et `wsgi.py` est un fichier de configuration relatif au serveur qui executera le projet.
Nous pouvons vérifier que le projet fonctionne avec la commande :  
```shell
$ python manage.py runserver
```
Cette commande lance le serveur de développement Django et affiche des informations dont l'URL du projet Django que nous venons de créer.

__Création d'une application au sein du projet__

Créer une application est très simple. Il faut tout d'abord se placer dans le répertoire du projet puis taper la commande suivante :
```shell
$ django-admin.py startapp chistera
```
Un répertoire *chistera* a été créé dans le répertoire du projet et contient plusieurs fichiers: le fichier `models.py` qui est destiné à accueillir les modèles de l'application, le fichier `views.py` qui sert à accueillir les contrôleurs de l'application et le fichier `tests.py` qui va accueillir les tests.

## 2 - Conception des premiers modèles
Les modèles Django sont des classes héritées de la classe `Model` du framework de base, qui leur confère ainsi les propriétés et méhodes relatives aux modèles. 
Afin de créer notre premier modèle, il nous faut démarrer dans le fichier `models.py` de l'application (voir point précédent pour la création d'une application). 

```python
from django.db import models

class MonPremierModel(models.Model):
    """
    La documentation de mon modèle.
    """
    un_exemple_de_texte = models.CharField(max_length=150)
```
Lorsque vous créez un modèle Django, vous utilisez le système d'ORM du framework, ce qui signifie que Django vous propose certains types de champs disponibles pour la création de vos modèles. On ne les listera pas ici, mais on peut citer pour exemple _CharField_ (pour un champ de texte, mappé vers un VARCHAR en BDD) ou encore _ForeignKey_ (pour une référence à un objet d'un autre modèle.)

Pour plus d'informations concernant les champs utilisables pour la création d'un modèle, n'hésitez pas à suivre la documentation officielle de Django, section _Model field reference_.

Pour chaque type de champ, on peut lister un grand nombre d'_options_ différentes, qu'on ne listera pas non plus ici.
Pour y voir plus clair, voici un exemple de déclaration de modèle utilisant certaines options:

```python
from django.db import models

class MonPremierModel(models.Model):
    un_exemple_de_texte = models.CharField(max_length=150, null=True, blank=True, default="Coucou")
```
Désormais, vous connaissez les principales caractéristiques des modèles.

## 3 - Le traitement des données avec les vues et le routage d'URL

### Ecriture des contrôleurs  

En Django, on écrit tous les contrôleurs d'une application dans un seul fichier, appelé `views.py`. Lors de la création de notre application chistera avec la commande djangoadmin.py (voir partie II-1), Django a placé un fichier `views.py` vide dans le répertoire de l'application que nous pouvons compléter.

Notre fichier `urls.py` définit les routes vers deux contrôleurs:

```python
from django.conf.urls import patterns, url

urlpatterns = patterns('',
    url(r'^dashboard/$', 'chistera.views.dashboard', name='dashboard'),
    url(r'^backlog/(?P<backlog_id>[0-9]+)/$', 'chistera.views.backlog', name='backlog'),
)
```
Ainsi il y a deux destinations à définir: un contrôleur dashboard et un contrôleur backlog. Ces deux contrôleurs vont avoir besoin de modèles, il faut donc les importer dans le fichier `views.py` :  
```python
from chistera.models import *
```
__Ecriture du contrôleur (vue) dashboard__  

Ce contrôleur doit récupérer les équipes et les backlogs pour pouvoir invoquer ensuite une vue (template) qui les affichera à l'écran. Pour celà on écrit la déclaration suivante:  

```python
from django.shortcuts import render_to_response

from chistera.models import *

@login_required
def dashboard(request):
    backlogs = ProductBacklog.objects.all()
    teams = Team.objects.all()
    return render_to_response('chistera/dashboard.html', {'backlogs': backlogs, 'teams': teams})
    
 ```
En Django, tous les contrôleurs doivent retourner un objet de type *HttpResponse*. Ce sont eux qui seront transmis aux templates. La dernière ligne de la fonction permet de créer cet objet. Après celà, les contrôleurs seront en place et nous pourrons afficher la page  correspondant au contrôleur dans un navigateur. De plus, notre contrôleur sera "protégé" par le décorateur `@login_required`. Seules les requêtes provenant d'utilisateurs authentifiés pourront aboutir.  

__Ecriture du contrôleur (vue) backlog__  

De même nous allons écrire dans le fichier views.py la fonction contrôleur backlog.  

```python
@login_required
def backlog(request, backlog_id):
    backlog = get_object_or_404(ProductBacklog, pk=backlog_id)
    stories = UserStory.objects.filter(product_backlog=backlog)
    return render_to_response('chistera/backlog.html', {'backlog': backlog, 'stories': stories})

```

La différence ici est que nous avons une variable nommée `backlog_id` qui est automatiquement passée au contrôleur `backlog` par Django.  
De plus une fonction `get_object_or_404` retourne une erreur 404 si l'objet est introuvable.  

### Routage d'URL: écriture du contrôleur frontal  

L'idée ici est d'associer des patterns d'URL aux contrôleurs d'une application. C'est ce que va faire le contrôleur frontal. Chaque projet dispose d'un contrôleur frontal. Dans le fichier `urls.py`, on écrit:  

```python
from django.conf.urls import patterns, include, url

from django.contrib import admin
admin.autodiscover()

urlpatterns = patterns('',
    url(r'^admin/', include(admin.site.urls)),
)
```

Cela permet de dire à Django : « Je veux que tu rediriges toutes les requêtes faites à la racine (^) vers le contrôleur frontal de l'application chistera  qui est défini dans le module *chistera.urls* ».  

Il ne reste plus qu'à écrire les règles de routage dans le fichier `urls.py` :  

```python
from django.conf.urls import patterns, url

urlpatterns = patterns('',
    url(r'^dashboard/$', 'chistera.views.dashboard', name='dashboard'),
    url(r'^backlog/(?P<backlog_id>[0-9]+)/$', 'chistera.views.backlog', name='backlog'),
)
```

Le contrôleur frontal est donc en place et permet le routage d'URL.


## 4 - Présentation du contenu avec les templates

Commençons par présenter le moteur de templates de Dango, qui vous permettra d'écrire des vues de qualité. Ce moteur fait partie des nombreux points forts de Django qui le distinguent des autres frameworks de même type.
Le langage de template permet la manipulation de variables au sein d'un contenu textuel. 

Pour afficher une variable dans un template, il faut utiliser des doubles accolades à l’intérieur desquelles on placera le nom de la variable.

Voici un bout de code d'exemple : 

```django
Bonjour {{ nom }}
```
et maintenant le rendu
```
Bonjour Anthony
```
Le moteur de template permet également l'utilisation de nombreux filtres afin d'appliquer des traitements de mise en forme aux variables. Ces filtres sont appelés de la manière suivante, au sein des doubles accolades:
```django
{{ variable|filtre }}
```
Prenons un exemple pour éclaircir l'utilisation de ces filtres.
Voici un bout de code d'exemple, 

```django
Bonjour {{ nom|capfirst }}
```
et maintenant le rendu
```
Bonjour Anthony
```
Le filtre `capfirst` utilisé ici convertit le nom de la personne, qui a pour valeur "anthony" en "Anthony" avec majuscule.

Comment fait on pour itérer cette méthode sur une liste? Nous allons pour cela utiliser la boucle `for` de Django, assez proche de celle proposée en Python.

Voici un exemple de code.
```django
<ul>
{% for personne in personnes %}
    <li>{{ personne }}</li>
{% endfor %}
</ul>
```
et le rendu
```
Anthony
Bastien
Amine
```
Pour une liste plus détaillée des différentes fonctionnalités offertes par ce langage, n'hésitez pas à faire un tour sur la documentation officielle, ne serait que pour apprendre les extensions de templates.

## 5 - Administration du projet avec le scaffolding

### Installation

Une des grandes forces de Django est de proposer la création très rapide d'une interface permettant d'administrer son site. Pour cela on va utiliser les fonctionnalités de _scaffolding_ (littéralement _échaffaudage_ ou _structure_) de Django.

La première étape est d'ajouter l'application d'administration dans la liste des applications utilisées dans notre projet. Pour ce faire il faut modifier la variable `INSTALLED_APPS` dans le ficher `settings.py` du projet :

```python
INSTALLED_APPS = (
    ...,
    'django.contrib.admin',
    ...,
)
```

Maintenant que l'application est active, il faut permettre son accès. Pour ce faire il faut rajouter une route pointant vers l'interface d'administration. Modifiez le fichier `urls.py` du projet (et non de l'application) pour rajouter ces lignes :

```python
from django.contrib import admin

admin.autodiscover()

urlpatterns = [
    ...,
    path('admin/', admin.site.urls),
    ...,
]
```

Ne vous attardez pas trop sur la ligne `admin.autodiscover()`, il nous permet simplement _"d'ajouter"_ tous nos modèles dans l'interface d'administration.

Afin de pouvoir utiliser notre interface, il nous faut créer un utilisateur qui a les droits d'accès à l'interface. Dans une console, se placer dans le dossier de notre projet, là où se trouve le fichier `manage.py` et taper : `python3 manage.py createsuperuser` puis suivez les étapes affichées. Une fois cette étape effectuée, vous pouvez lancer le serveur pour tester votre interface. Vous devriez arriver sur une interface comme celle-ci :
![Connexion à la plateforme d'administration](http://formation-django.fr/media/images/cms/authentification-interface-administration.png)
Source : [formation-django.fr](http://formation-django.fr/framework-django/scaffolding/mise-en-oeuvre.html)

Django gérant lui même toutes les questions de sécurité et d'authentification, il vous suffit de vous connecter avec les identifiants créés précédemment et vous avez accès à l'interface de gestion.
![Interface d'administration](http://formation-django.fr/media/images/cms/django-scaffolding-accueil.png)
Source : [formation-django.fr](http://formation-django.fr/framework-django/scaffolding/mise-en-oeuvre.html)

On a accès à la gestion des groupes d'utilisateurs, ainsi qu'au utilisateurs eux-mêmes, mais pas à la gestion de notre application en elle même, ce qui rends l'interface peu utile. Rajoutons donc nos modèles dans l'administration.

Pour ce faire, il faut modifier le fichier `admin.py` de notre application pour rajouter les lignes suivantes :

```python
from django.contrib import admin
from chistera.models import *

admin.site.register(Team)
admin.site.register(Project)
admin.site.register(ProductBacklog)
admin.site.register(Sprint)
admin.site.register(UserStory)
```

(L'importation du module à la deuxième lignes ainsi que les modèles utilisé sont à adapter selon votre application).

En rafraichissant simplement la page d'administration (avec le serveur lancé), nous voyons tous nos modèles dans l'interface : 
![Interface d'administration mise à jour avec les modèles](http://formation-django.fr/media/images/cms/django-application-admin.png)
Source : [formation-django.fr](http://formation-django.fr/framework-django/scaffolding/mise-en-oeuvre.html)

### Paramétrage avancé

Vous l'avez peut-être remarqué, l'interface est en anglais par défaut. Une des grandes qualités de Django est sa gestion des différentes langues et des différents fuseaux horaires. Pour en profiter, il faut modifier les variables `TIME_ZONE` et `LANGUAGE_CODE` dans le fichier `settings.py` du projet :

```python
TIME_ZONE = 'Europe/Paris'
LANGUAGE_CODE = 'fr-FR'
```

Avec ceci, notre application est en français, et utilise le fuseau horaire de Paris. Cependant les noms des modèles sont toujours en anglais. Ceci vient du fait que nos modèles sont nommés en anglais et que Django n'a rien pour _deviner_ la traduction, et utilise simplement le Camel Case (voir [Camel Case sur Wikipédia](https://fr.wikipedia.org/wiki/Camel_case) pour plus d'explications) pour _deviner_ le nom des modèles. Pour traduire les noms affichés de nos modèles, il y a deux possibilités :
1. On change le nom de la classe qui définie le modèle dans le fichier `models.py`
2. On utilise une classe interne dans notre modèle où l'on définit les noms à utiliser pour l'interface d'administration

La première solution n'est pas à préférer parce que si on est ammené à changer le nom d'usage de notre modèle par la suite, il serait à changer dans tous les fichiers où on l'utilise ce qui peut poser des problèmes. 

Pour implémenter la deuxième solution, il suffit de rajouter dans le modèle que l'on souhaite _traduire_ une classe interne de la manière suivante :

```python
class ProductBacklog(models.Model):
    # ...
    
    class Meta:
        verbose_name = 'Backlog de produit'
        verbose_name_plural = 'Backlogs de produit'
```

Ainsi on a la possibilité de définir la façon dont s'affiche notre modèle, à l'infinitif comme au pluriel.

L'étape suivante est d'adapter l'affichage des listes d'enregistrement à nos besoins.

Si on retourne sur notre interface d'administration, en cliquant sur un modèle, on tombe sur une liste assez similaire à la suivante : 
![Extrait de l'interface d'administration](http://formation-django.fr/media/images/cms/django-admin-liste-par-defaut.png)
Source [formation-django.fr](http://formation-django.fr/framework-django/scaffolding/parametrage-avance-interface-admin.html)

La visualisation est assez classique avec une liste des éléments ainsi que la possibilité de rechercher, d'ajouter ou de supprimer des éléments.

Le seul problème est que notre liste n'est pas très détaillée, affiche un nom étrange pour nos entrées et qu'il manque des fonctionnalités de tri ou de recherche. Voyons comment remédier à tous ces problèmes.

Notre premier point à régler est que Django n'affiche plus _Project object_, mais bien le nom de notre projet. Pour ce faire retournons dans notre fichier `models.py` et rajoutons une méthode `__str__()` qui nous permettra de récupérer facilement le nom de notre projet.

```python
class Project(models.Model):
    name = models.CharField(max_length=150)
    # ...
    
    def __str__(self):
        return self.name
```

L'affichage est déjà un peu plus clair : 
![Affichage des projets](http://www.formation-django.fr/media/images/cms/django-admin-personnalisation-noms-objets.png)
Source [formation-django.fr](http://formation-django.fr/framework-django/scaffolding/parametrage-avance-interface-admin.html)

Pour l'instant, dans la liste on voit uniquement le noms des projets. Cela dit il pourrait être intéressant de voir d'autres infos sur les projets, comme l'équipe assignée. Pour ce faire, il faut modifier le fichier `admin.py`.

Pour rappel, il ressemble à ceci : 

```python
from django.contrib import admin
from chistera.models import *

admin.site.register(Team)
admin.site.register(Project)
admin.site.register(ProductBacklog)
admin.site.register(Sprint)
admin.site.register(UserStory)
```

Les cinq dernières lignes reviennent simplement à daire à Django : « Je souhaite que tu prennes en charge les modèles Team, Project, ProductBacklog, Sprint et UserStory dans l'interface d'administration de mon application : fais au mieux ! ». En faisant ceci, Django va définir lui même les informations à afficher dans la liste ainsi que la possibilité de faire un tri ou non, etc...

Il est possible de choisir tous ces paramètres nous même, et donc de manière plus précise. Django offre cette possibilité en créant un modèle spécifique à notre interface d'administration où l'on va renseigner les paramètres que l'on veut pour personnaliser notre interface à notre manière.

Par exemple, pour afficher, en plus du nom, l'équipe assignée à un projet dans notre modèle de projet il faut créer une classe `ProjectAdmin` (ou un autre nom tout aussi parlant) qui hérite de la classe `admin.ModelAdmin` et a comme attribut `list_display = ('name', 'team')`. L'étape suivante est de dire à Django d'utiliser ce modèle comme paramétrage de nore modèle originel. Le code complet serait :

```python
from django.contrib import admin
from chistera.models import *

class ProjectAdmin(admin.ModelAdmin):
    list_display = ('name', 'team')

admin.site.register(Project, ProjectAdmin)
admin.site.register(ProductBacklog)
admin.site.register(Sprint)
admin.site.register(UserStory)
admin.site.register(Team)
```

En actualisant l'interface d'administration, on obtient bien la liste que l'on souhaitait avoir 
![Interface d'administration actualisée](http://www.formation-django.fr/media/images/cms/django-admin-ajout-colonnes.png)
Source [formation-django.fr](http://formation-django.fr/framework-django/scaffolding/parametrage-avance-interface-admin.html)

La classe `admin.ModelAdmin` offre plein de possibilités de paramètrage de l'interface d'administration. Ainsi pour rajouter un champ qui permette de rechercher un projet par son nom, il suffit de rajouter l'attribut `search_fields = ('name',)` dans notre classe créée précédemment. Pour rajouter un tri des projets selon leur équipe assignée, il suffit de rajouter l'attribut `list_filter = ('team',)`.

Avec tous ces ajouts notre fichier devient :

```python
from django.contrib import admin
from chistera.models import *

class ProjectAdmin(admin.ModelAdmin):
    list_display = ('name', 'team')
    search_fields = ('name',)
    list_filter = ('team',)

admin.site.register(Project, ProjectAdmin)
admin.site.register(ProductBacklog)
admin.site.register(Sprint)
admin.site.register(UserStory)
admin.site.register(Team)
```

En actualisant la page de gestion, on voit les changements qui se sont effectués :
![Page d'admin mise à jour avec la recherche et le tri](http://www.formation-django.fr/media/images/cms/django-admin-filtre.png)
Source [formation-django.fr](http://formation-django.fr/framework-django/scaffolding/parametrage-avance-interface-admin.html)

La documentation de Django contient l'ensemble des attributs qu'il est possible de renseigner afin de paramétrer l'interface d'administration, n'hésitez pas à aller la consulter.
