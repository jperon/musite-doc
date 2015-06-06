Musite
======


Présentation
------------

[Musite](https://github.com/jperon/musite) est une sorte de wiki, destiné
principalement à l'édition de documents musicaux.

Depuis la page d'accueil, vous pouvez :

- accéder à la liste des projets existants ;
- créer un nouveau projet.

Depuis la liste des projets, il est encore possible :

- de cloner un projet existant (grâce à `git`, le gestionnaire de version utilisé
  par musite ;
- d'envoyer une archive `zip` contenant un projet déjà commencé par ailleurs,
  qui sera alors intégré à musite.

Musite est traduit en anglais grâce à
[gettext](https://www.gnu.org/software/gettext) ; il est parfaitement
envisageable de le traduire en d'autres langues… dans la mesure où les
volontaires se présentent !


Projet
------

Sur la page d'accueil d'un projet, s'affichent :

- la liste des dossiers et fichiers du projet ;
- le contenu d'un éventuel `Readme.md`, situé à la racine de ce projet.

Il est possible d'avoir plusieurs `Readme`, en fonction de la langue de
l'utilisateur : si un utilisateur navigue sur la version anglaise du site et
qu'un fichier `Readme-en.md` existe, c'est ce fichier qui sera utilisé en
priorité.

Dans le menu, à gauche de la page d'accueil, s'affichent :

- un lien renvoyant… à la page du projet ! Ce lien est utile après certaines
  opérations sur le projet ;
- les différentes actions disponibles.

### Actions sur un projet

#### Utilisateur non authentifié

L'utilisateur non authentifié peut :

- accéder en lecture à l'historique du projet, où l'on peut
  suivre les modifications successives subies par les fichiers du projet ;
- télécharger le projet sous la forme d'une archive compressée au format `zip`.

#### Utilisateur authentifié

Les actions accessibles à l'utilisateur authentifié dépendent des privilèges qui
lui ont été accordés. À l'heure actuelle, il existe deux niveaux de privilèges :

- les *administrateurs* peuvent modifier des paramètres importants du site ; ceci
  fait l'objet d'une autre section de la documentation ;
- les *éditeurs* peuvent modifier les documents et dossiers contenus dans un
  projet.

Outre les actions accessibles à tout utilisateur, voici les actions que peut
effectuer un éditeur :

- copie d'un projet ;
- création de documents ou de sous-dossiers ;
- envoi/réception des modifications vers/depuis un dépôt distant ;
- intégration d'un fichier, ou d'une archive contenant des fichiers ou dossiers,
  à l'intérieur du projet ;
- accès en écriture à l'historique, de façon à revenir sur des modifications ;
- renommage du projet ;
- suppression du projet.

Toutes ces actions sont réversibles, à l'exception notable de la suppression du
projet. Le cas échéant, pensez à profiter de la possibilité de télécharger un
projet pour effectuer des sauvegardes…