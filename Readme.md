Musite
======


Présentation
------------

[Musite](https://github.com/jperon/musite) est une sorte de wiki, destiné
principalement à l'édition de documents musicaux. Il a été réalisé, en marge
du [projet Gregorio](https://github.com/gregorio-project), en vue de faciliter
l'édition d'ouvrages comportant des partitions grégoriennes (grâce à
[Gregorio](http://gregorio-project.github.io)), mais aussi des partitions
classiques (grâce à [Lilypond](http://lilypond.org)).

Depuis la page d'accueil, vous pouvez :

- accéder à la liste des projets existants ;
- créer un nouveau projet.

Depuis la liste des projets, il est encore possible :

- de cloner un projet existant
  (grâce à `git`, le gestionnaire de version utilisé par musite) ;
- d'envoyer une archive `zip` contenant un projet déjà commencé par ailleurs,
  qui sera alors intégré à musite.

Si vous voulez intégrer un projet pré-existant à musite, tenez compte de ce qui
suit :

- le dossier principal du projet doit être compressé au format `zip` ;
- l'archive `zip` en question ne doit contenir, à la racine, que ce dossier ;
- si ce dossier contient un sous-dossier `.git`, l'historique des modifications
  antécédentes sera disponible depuis musite ; sinon, musite initialisera un
  nouveau dépôt `git`, qui enregistrera les modifications subséquentes.

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

Pour l'intégration de fichiers ou archives pré-existants, voyez la section
suivante.


Dossier
-------

Depuis la page du projet, vous pouvez, en cliquant sur le nom d'un dossier,
accéder à ce dernier. La page d'accueil du dossier est sensiblement la même que
celle du projet. Il y a cependant des différences :

- outre le lien vers la racine du projet, un autre lien pointe vers le dossier
  parent ;
- les actions disponibles s'adaptent aux caractéristiques d'un dossier.

Notez bien ce qui suit à propos de l'intégration au sein de musite de documents
existants :

- pour l'envoi d'un **fichier isolé**, si vous ne cochez pas la case *Écraser le
  fichier s'il existe*, musite s'assurera d'abord de l'existence d'un fichier
  portant le même nom ;
- en revanche, pour l'intégration d'une **archive** contenant une arborescence
  (fichiers et dossiers), musite écrasera sans rien dire les éventuels fichiers
  pré-existants. En cas d'erreur, il vous reste la possibilité d'utiliser les
  fonctionnalités d'historique de musite…


Document
--------

Depuis un projet ou un dossier, vous pouvez accéder aux divers documents. Musite
s'adapte en fonction de l'extension du document ; si celui-ci n'a pas
d'extension, ou si son extension est inconnue de musite, il est traité si
possible comme un document texte. S'il s'agit d'un fichier binaire de type
inconnu, il n'est pas possible d'en avoir l'aperçu, mais les autres actions
sont disponibles.

La page d'accueil du document est donc, s'il est connu, un aperçu
de ce document ; s'il est inconnu, la source du document est présentée.

Les actions disponibles sur un document sont :

- pour les utilisateurs non authentifiés, l'aperçu, l'affichage de la source et
  l'accès en lecture à l'historique ;
- pour les éditeurs, l'édition, la copie, le déplacement et la suppression,
  ainsi que l'accès en écriture à l'historique.

En outre, certains types de documents proposent un export en différents
formats : ceci permet, par exemple, d'imprimer une partition dans un format
différent de celui qui est présenté sur l'aperçu du document.


Formats pris en charge
----------------------

À l'heure actuelle, les formats suivants sont pris en charge par musite :

- [gabc](http://gregorio-project.github.io/gabc/index.html) pour les partitions
  grégoriennes ;
- [lilypond](www.lilypond.org/text-input.fr.html) pour les partitions
  classiques ;
- [latex](www.latex-project.org) pour la mise en page d'ouvrages ;
- [markdown](http://commonmark.org) pour le texte enrichi ;
- txt pour les documents textes ; tout document de type inconnu peut être traité
  comme simple texte s'il n'est pas binaire.