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

# Ecrire un bon message de commit
Ecrire un bon message de commit estb essentiel pour la maintenance et la compréhension d'un projet. Cela aide à suivre l'évolution du projet et à comprendre les raisons derrière chaque modification.

Voici une norme généralement acceptée pour rédiger des medssages de commit.

## Structure d'un message de commit
Un message de commit se compose généralement de deux parties :

* un titre ou en-tête: c'est une brève description des modifications. Il doit être concis idéalement et ne pas dépasser les 50 caractètres. Il doit commencer par une majuscule.
* un corps : Il donne des détails supplémentaires sur les modif. Il est séparé du titre par une ligne blanche.

```
Titre court et description

Corps du message : ici, on explique en détail le pourquoi et le comment 
des changements si nécessaires. Essayez de garder chaque ligne à - 
de 72 caractères.
```

## Conseils pour un bon message de commit
Utilisez l'impératif : le titre doit être idéalement à l'impératif (ex: Ajoute, Corrige, Refactorise au lieu d'Ajouté...)
* Titre clair et concis : doit être court et descriptif
* Séparez les sujets : si vous avez plusieurs modif qui n'ont pas de rapport entre elles, envisagez de les séparer en plusieurs commits
* Expliquez le pourquoi, pas le comment : le code lui-même montre comment une certaine chose a étté faite . Ce qui n'est pas toujhours clair, c'ets pourquoi cetteb modification a été apportée. Assurez-vous d'expliquer les raisons dans le corps du message.
* Evitez les messages vagues :"correvctions diverses" ou "mise à jour" ne sont pas des messages utiles. Soyez aussi descriptif que possible.
* Utilisez des réf à une issues/ tracker : si votre commiut fait référence à une issue ou à un ticket, ajoutez cette réf dans le corps du message. 
* Respectez les conventions de l'équipe : si votre équipe a des conventions spécifiques pour les messages commity, suivez-les.

### Exemple d'un bon message de commit

Ajoute une focntionnalité de recherche

La page d'accueil avait besoin d'une fonctionnalité de recherche pour aider les utilisateurs à trouvers des contenus spécifiques
Cette modif ajoute un moteur de recherche et utilise l'API de recherche pour récupérer les résultats.

Relatif à l'issue #123,
```
# En savoir plus sur le langage markdown 
Pour la rédaction des fichiers readme, n'hésitez pas à vous penschez sur la documentation markdown. Voici un lien pour vous aider :
[Lien pour apprendre markdown](https://programminghistorian.org/fr/lecons/debuter-avec-markdown)


Pour la rédaction de vos fichier Readme, n'hésitez pas à vous pencher sur la doc makdown. Voici un lien pour vous aider. 


# Pull Request (PR)

C'ets une fonctionnalité clé des systèmes de gestion de versions basées sur un github, Gitlab , Bitbucket... Elle représente une demande de fusion des modifs (commits) d'une branche vers une autre, h-généralement de la branche d'une fonctionnalité vers la branche principale d'un projet.

## Concept de la Pull Request (PR)

Collaboration et revue du code : La PR n'est pas seulement un mécanisme de fusion de code. C'est aussi un outil de collaboration. Lorsqu'un developpeur soumet un PR, d'utres memebres de l'équipe peuvent le consulter, laisser des comms, suggérer des mofis et meme proopser des commits pour améliorer la PR avant qu'elle ne soit fusionnée. 

## Point de contrôle : ** Avant la fusion, la PR fournit un point de contrôle pour s'assurer que le code respecte les nombres de qualité, passe tous les test et n'introduit pas de régression (perte de fonctionnalité).

** Intégration avec CI/CD :** Les PR sont souvent intégrer avec de soutils d'Intégration Continue et de Livraison Continue (CI/CD). Lorsqu'une PR est soumis des test automatisés peuvent être déclenchés, et le résultat de ces test est souvent signalé directement dans l'interface de la PR. 

## Faire une PR
## Fork du repository
Avant de pouvoir soummettre une PR, vous devez avoir une copie du repository sur votre compte? Si ce n'ets pas deja fait :
1. Rendez-vous sur la page GitHub du projet auquel vous voulez contribuer.
2. Cliquez sur le bouton "Fork" en haut à droite de la page.
Cela créera une copie du projet sur votre compte GitHub personnel. 

## Clonez votre Fork
Clonez bvotre Fork sur votre machine :
```
git clone URL_DU_REPO_A_CLONER
git clone https://github.com/JackAdamsJenkins/rockpaperscisors.git
```

## Créer une nouvelle branche
Il est conseillé de créer une nouvelle branche pour chaque novelle fonctionnalité ou correction. Cela vous permet de garder le travail organisé et séparé. 

Pour créer une nouvelle branche, vous devez utiliser la commande ``git checkout -b``

```
git checkout -b nom_de_la_branche
git checkout -b fonctionnalite_timer
```
## Apportez les modifications
Modifiez les fichiers nécessaires et ajoutez-les à l'index :
```
git add nom_du_fichier
```

Ou pour ajouter tous les ficheir modifiés :
```
git add * 
```
Ensuite faites un commit de vos modifications :
```
git commit -m "Description des modifications"
```
## Pousser la branche vers le Fork

```
git push origin nom_de_la_branche
```
## Créer la Pull Request

1. Aller sur la page Github de votre fork
2. Cliquez sur le bouton "New pull request"
3. Sélectionner votre nouvelle branche dans le menu déroulant "compare"
4. Assurez-vous que la branche de base(**main**) est celle du projet original et non celle de votre fork
5. Vérifier vos modifs et cliquez sur "Create pull request"
6. Donnez un titre à votre PR et décrivez vos modifs ou les raisons de vos PR
7. Cliquez sur "Create pull request" pour soumettre votre PR