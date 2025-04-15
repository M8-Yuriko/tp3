**Nom :** Prévost Donovan & Hermilly Joshua

**Groupe :** C2

**Année :** 2025

**IUT Le Havre - Cours GIT**

# TP 3 : Travailler en équipe sur un depôt github distant

# 1. Inviter des collaborateurs dans un dépôt personnel
Ce tp a été réalisé en collaboration avec Donovan Prévost Groupe 12 pour représenter Porthos .
	Créer un nouveau dépôt tp3

	Ajouter un collaborateur (paramètres → collaborateur → ajouter )

Ajouter ce collaborateur.

Cloner le projet dans le réprtoire courseGIT
Commande : git clone git@github.com:M8-Yuriko/tp3.git


## Exercices :
	1. Porthos : allez dans le répertoire tp3 et mettez à jour tous les fichiers avec ceux du répertoire tp2 (README.md et src/Cryptomonnaie.java) (surtout ne copiez pas le répertoire caché .git). Synchronisez les dépôts local et distant.
	Copier coller les fichier de tp2 vers tp3 → git add → git commit → git push
	2. Athos : après que Porthos vous en informe, faissez un git pull depuis votre répertoire local tp3 pour synchroniser les changements.
	git pull
	3. Les deux : vérifiez que tous les dépôts sont bien synchronisés (ce qui est sur github correspond bien à ce que vous avez dans votre répertoire local).

# 2. Développement d’un projet java en équipe
Athos :
        ◦ Copiez les fichiers suivants dans le répertoire tp3/src, validez-les dans le dépôt local et distant :
        ◦ CryptoMarche.java
        ◦ Portefeuille.java
        ◦ TestCryptoMarche.java

Modifier le fichier respectif à votre personnage et le push sur le répertoire. 
Commande :`code Cryptomonnaie.java`
          `git add CryptoMarche.java`
          `git commit -m "Modification du CriptoMarche.java"`
          `git push`
Mettre en commun 
Commande : `git pull`

Correction des fichiers.

# 3. Gérer des nouvelles fonctionnalités à l’aide des branches
## Exercice :
        1- Athos et Porthos faire les sections 3.1 et 3.2 séparément sans synchronisation avec le dépot github.
        2- Ensuite, supprimez le fichier test.txt du dépôt, pour cela, écrivez la commande git rm test.txt puis git commit -m "test.txt supprimé".
        3- Chacun de vous va créer une branche appelée AthosCoin et PorthosCoin respectivement. Dans cette branche, vous allez créer votre crypto-monnaie (suivez l’exemple d’AramisCoin ci-dessous). Une fois la devise créée, fusionnez la branche avec la branche principale. Assurez-vous ensuite que les modifications sont synchronisées dans le dépôt github.

## 3.1. Tester le concept de branche avec un exemple simple
Commande :`tree -f`

Créer un nouvelle branche test. 
Commande : `git checkout -b test`
           `git branch`

## 3.2. Fusionner la branche de test dans la branche principale 
1. Créer un fichier test.txt : `touch test.tx`
2. Valider ces changements: `git add test.txt`
                            `git commit -m "fonction de test ajoutée "`
3. Revenir sur la branch main et taper ls :`git checkout main → ls	Le fichier test.txt n’apparait pas.`
4. Fusionner les branches : `git merge test`
5. Visualiser la fusion : `git log --graph --oneline --all --decorate –topo-order`
6. Tester avec ls, on doit retrouver le test.txt

**2. Suppression du test.txt :  git rm test.txt →  git commit -m "test.txt supprimé".**
**3. Créer une branche appelée AthosCoin  et créer votre crypto-monnaie**
Commande : `git checkout -b AthosCoin`
           `code AthosCoin.java`
           `git add AthosCoin.java`
           `git commit -m «Ajout de ma crypto-monnaie »`
           `git checkout main`
           `git merge AthosCoin`
           
**4. Synchroniser les dépôt**
`git push`
`git pull`