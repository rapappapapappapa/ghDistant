Partage du hook pre-commit
==========================

Ce depot contient un hook Git dans le dossier hooks/pre-commit.

Le hook demande a chaque commit :
  Enregistrer le suivi de commit (y/[n]) ?

- Si on repond y : creation du fichier suivi/commitInfo.txt
  avec le texte : commit verifie le <date et heure>
  Le fichier est ajoute au commit automatiquement.
- Si on repond n ou Entree : le commit continue sans ce fichier.

Installation (a faire une fois sur chaque machine)
-------------------------------------------------
Depuis la racine du depot :

  cp hooks/pre-commit .git/hooks/pre-commit
  chmod +x .git/hooks/pre-commit

Sous Windows (Git Bash), les memes commandes fonctionnent.

Les hooks ne sont pas partages automatiquement par Git :
il faut copier le fichier a la main (ou relancer ces commandes).
