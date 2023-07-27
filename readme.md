# Les commandes de base de Github

## Première étape

* Créer dans Github, un nouveau repository
* Nommez le comme vous le souhaitez
* Vous pouvez choisir sa visibilité 
    * Public : Si vous souhaitez que toutnle monde puisse y avoir accès
    * Private : Si vous souhaitez être le seul à y accéder
* La description  est optionnelle : remplissez la si vous le souhaitez
* Allez en bas de page, cliquez sur "Create repository"

Votre repository est maintenant créé, vous allez pouvoir faire votre premier commit.

## Faire son premier commit 


Vous allez vous rendre compte qu'il y a un petit encadré nommé "Quick setup" qui vous propose deux possibilités : HTTPS et SSH.

Si ce n'est pas fait par défaut, choississez HTTPS

### Initialisation de Github sur votre machine

Sur Visual Studio Code :
* Ouvrez un terminal (3 possibilités)
    * Menu, affichage, terminal
    * ^<
    * en bas à gauche, vous avez une icone triangle et rond. Cliquez dessus. 

Initialiser github sur le dossier qui est ouvert avec la commande ''git init ''.
Une fois que github est initialisé, vous allez devoir indiquer quel fichier vous souhaitez envoyé sur github. Pour cela, :
* ''git add * '' Pour ajouter tous les fichiers
* ''git add nomDuFichier'' pour ajouter un fichier en particulier. 

Pour info, vous ne devez pas entrer vous-même le nom complet du dossier ou du fichier. Cela augmente le risque d'erreur. Au lieu d'écrire le nom complet, vousdevez écrire les premières lettre puis appuyer sur tab. 

Dans le cas ou il existe plusieurs fichiers commençant par les mêmes lettres, il vous suffit de continuer à appuyer sur tab jusqu'à arriver au bon fichier. 
Si vous avez plusieurs fichiers à ajouter, MAIS que vous ne souhaitez pas ajouter tous les fichiers qui se trouvent dans votre dossier de travail, vous pouvez faire plusieurs foisngit add nomDuFichier. 

En résumé

* ''git init'' pour initialiser le repo github
* ``git add nomDuFichier`` - pour ajouter un fichier
* 

## Exercice 
* Initialiser le repo Github sur VSCode
* Ajoutez le fichier readme


### Faire la liaison avec le repo distant
Vous venez d'initialiser github sur votre machine maisil ne sait pas encore qu'il doit etre lié à votre repository distant. Pour cela, vous allez devoir connecter l'origine à votre reposity distant. 

Commençons par ajouter un petit message qui précise ce qu'on a fait comme modification/ajout/suppression. 

* ``git commit -m "explication du commit"``
* Exemple : 
        ''git commit -m "Ajout du fichier readme"''

Une fois que le message de commit est défini, on va choisir la branche sur laquelle on va travailler. 

Lorsque vous souhaitez stocker vos fichiers sur github, si vous le souhaitez vousnpouvez stocker différente version de vos fichiers. . Cela s'appelle des branches.

La branche principale sur laquelle vos fichiers sont enregistrés s'appelle "main".

* ``git branch -m main``

Cette commande indique qu'on selectionne la banche "main". 
Il est maintenant tant que connecter votre repo local (votr" machine) à votre repo distant (github). Pour cela, utilisez cette commande :
* ``git remote add origin LIEN_DE_VOTRE_REPO``
exemple :
        ''git remote add origin https://github.com/Samialkh/rockpaperscisors.git``

Maintenant que le repo local et distant sont connectés, il bovus reste à envoyer vos fichiers sur github. Cela se fait avec la commande ``git push -u origin main``

## En résumé 
Voici les commandes à lancer :
*``git init`` pour initailiser le repo github
* ``git add NomDuFichier`` pour ajouter un fichier
* ``git commit -m "Nom du commit"`` pour ajouter une description de la modif/ajout
* ``git branch -m main``pour choisir la branche principale
* ``git remote add origin URL_REPO_GITHUB``pour connnecter le repo local et distant
* ``git push -u origin main``pour envoyer les modif à github

## Informations :
Les commandes ``git init``, ``git branch``et ``git remote add origin``sont à lancer UNE SEULE FOIS au moment de l'initialisation du repo. 

Une fois que ces commandes ont été faites, pendant le reste du developpement de votre projet, vous pouvez utiliser les commandes suivantes : 
* ``git add nomDuFichierModifié``
* ``git commit -m "message de modif"``
* ``git push``.

C'est ces 3 commandes que vous utiliserez à chaque fois. 



