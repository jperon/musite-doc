Premier lancement
=================

Au premier lancement de musite, le nom d'utilisateur par défaut est *admin*, le
mot de passe *admin*. Il est bien évidemment recommandé de modifier le mot de 
passe…

Administration
==============

Une fois authentifié en tant qu'administrateur, un lien *Administration*
apparaît en bas à gauche. La seule action possible, pour le moment, est la
création et la modification des utilisateurs.

Cliquer sur *Utilisateurs* : la page qui apparaît est divisée en deux colonnes.

La colonne de gauche permet :

- d'ajouter un utilisateur : pour cela, comme d'habitude, saisir son nom et son
  mot de passe répété deux fois, puit cliquer sur *Créer/Modifier* ;
- de modifier le mot de passe d'un utilisateur : pour cela, procéder exactement
  comme s'il s'agissait de créer de nouveau cet utilisateur ;
- de supprimer un utilisateur, grâce au lien correspondant.

**Évitez les accents dans les noms ou mots de passe** ; sinon, ne vous plaignez
pas que cela ne fonctionne pas.

La colonne de droite permet d'attribuer à des utilisateurs les droits
d'administration ou d'édition du site.
Exemple :

```
admin	admin,chef
editeurs	chef,sousfifre,imaginatif
```

Notez bien :

- les noms de groupes sont séparés des utilisateurs par une tabulation ;
- les noms d'utilisateurs sont séparés *uniquement* par une virgule, sans espace
  ni avant ni après.
