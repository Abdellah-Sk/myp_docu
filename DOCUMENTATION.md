# Documentation du projet MYP (Make Your Portfolio)

Un excellent moyen de se familiariser avec MYP est de suivre ce didacticiel, qui vous guide tout au long de la construction de votre propre portfolio. Nous décrivons ici toutes les informations et nous vous fournissons tous les détails dont vous avez besoin pour utiliser MYP. L'application MYP que vous allez créer permet de mettre en place simplement un catalogue de vos projets de developpement et d'en afficher les détails.

## Sommaire

1. Introduction
2. Prérequis 
3. Installation
4. Démarrage 
6. Présentation du projet
    * Organisation du dossier
    * Modèle de base de données
7. Personnaliser le projet
    * Base de données
    * Mailing
    * Css
    * Templates
8. Hebergement

## Prérequis


Projet développer avec:

* [Django](https://www.djangoproject.com/) - Framework web Python
* [npm](https://www.npmjs.com/) - Gestionnaire de paquets Node.js
* [Pillow](https://pillow.readthedocs.io/en/stable/) - Librairie de traitement d'image Python
* [Webpack](https://webpack.js.org/) - Module bundler Javascript


## Installation


Les étapes pour installer le projet.

Après avoir cloner le projet avec ``git clone https://github.com/Abdellah-Sk/myp-django.git``.

Executez la commande ``cd myp-django`` pour vous rendre dans le dossier depuis le terminal.

Ensuite taper la commande ``source venv/bin/activate`` pour activer l'environnement virtuel.

Puis ``cd src`` pour vous rendre dans le dossier de developpement.

Enfin lancer l'application grâce a la commande suite : ``python manage.py runserver``.


## Démarrage


Une fois sur l'application, il ne vous reste plus qu'a vous connecter au back-office en ajouter dans l'URL ``/admin``.

Nom d’utilisateur :  ``admin``

Mot de Passe: ``admin`` 


## Présentation du projet

Cette section contient les différentes options générales du projet.

### Organisation du dossier

Dans cette partie, nous allons vous presentez la structure du projet MYP en Django.
Après avoir pull le projet, vous allez avoir une arborescence qui va ressembler ça ceci :

```
├── img
│   └── projet1.png
├── db.sqlite3
├── manage.py
├── projects
│   ├── admin.py
│   ├── forms.py
│   ├── __init__.py
│   ├── models.py
│   ├── static
│   │   ├── projects
│   │   │   ├── style.css
│   │   │   ├── index.js
│   │   │   └── img
│   ├── templates
│   │   └── projects
│   │       └── index.html
│   ├── tests.py
│   └── views.py
└── PortfolioDjango
    ├── settings.py
    ├── urls.py
    └── wsgi.py
```

A la racine:
* __img__ : Dossier d'upload des images des projets
* __db.sqlite3__ :

Le dossier d'application :
* __projects__ :
* __static__ :
* __templates__ :
* __views__ :
* __models__ :

Le dossier du projet :
* __PortfolioDjango__ :
* __settings__ :
* __urls__ :


### Modèle de base de données

La base donnée est composé de trois tables principal plus une table de relation ManyToMany.

On retrouve donc une table User, une table Projects, une table Technologies, et une table Projects_technologies qui fait office de relation ManyToMany entre les projets et les technologie.

Ci-dessous, le modèle de la base donnée :

![Modèle de la base de données](assets/images/db_model.png)
