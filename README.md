# TP Git – 18/12

## Objectif
Mettre en place un dépôt Git avec une branche `main` (stable) et une branche `develop` (travail).

## Prérequis
- Un compte GitHub
- Git installé sur le poste
- Accès SSH fonctionnel vers GitHub

## Installation de Git
### Vérification de l’installation
```bash
git --version

Git : https://git-scm.com/docs

Connexion SSH GitHub : https://docs.github.com/en/authentication/connecting-to-github-with-ssh

Gestion des dépôts distants : https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories

Commande	Description
git init	Initialise un dépôt Git local
git branch -M main	Définit main comme branche principale
git remote add origin <url>	Lie le dépôt local à GitHub
git checkout -b develop	Crée et bascule sur la branche develop
git add .	Ajoute les fichiers à l’index
git commit -m "message"	Crée un commit
git push -u origin <branche>	Envoie la branche sur GitHub
git merge develop	Fusionne develop dans la branche courante
git mv file1 file1.txt	Renomme un fichier en conservant l’historique
git rm file3	Supprime un fichier suivi par Git
git status	Affiche l’état du dépôt


```mermaid
gitGraph
   commit id: "Initial commit"
   branch develop
   checkout develop
   commit id: "Add files"
   checkout main
   merge develop
   checkout develop
   commit id: "README + rename + delete"
   checkout main
   merge develop
