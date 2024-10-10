
# Soumettre un article Rzine  [<img src="https://rzine.fr/img/Rzine_logo.png"  align="right" width="120"/>](http://rzine.fr/)

**Comité éditorial Rzine**

---

Ce [document](https://rzine-reviews.github.io/rzine-doc-quarto/) présente le modèle Quarto d’un article Rzine et les consignes éditoriales élémentaires à suivre.

Le modèle quarto Rzine est accessible en saisissant cette instruction dans votre terminal :

```
quarto use template rzine-reviews/rzine-template-quarto
```


## Initier votre article avec GitHub

Ceci est un mémo des étapes nécessaires pour configurer un compte GitHub, qui servira de réceptacle à votre article. 

Le logiciel de gestion de versions décentralisé à utiliser pour la soumission est le plus connu et le plus utilisé dans le monde : [GitHub](https://fr.wikipedia.org/wiki/GitHub). 

### Création de compte

Connectez-vous à la [page de création de compte GitHub](https://github.com/)) et saisissez les informations attendues.

<p align="center">
 <img src="figures/github_crea_user.png" width="300" /> 
</p>

### Création d'un dépôt

Cliquez sur “Start a project” ou “Create repository” pour créer un dépôt qui hébergera votre fiche.

<p align="center">
 <img src="figures/crea_repo.png" width="600" /> 
</p>

Vous pouvez également créer un nouveau dépôt en cliquant sur “+” puis “New repository” en haut à droite de la fenêtre :

<p align="center">
 <img src="figures/crea_repo2.png" width="300" /> 
</p>

Un fois sur la page de création d’un nouveau dépôt, saisissez un nom de dépôt (sans espaces ni caractères spéciaux) et éventuellement une description. Initialisez ce dépôt comme Public et demandez l’ajout automatique d’un fichier README.md, puis cliquez sur "Create repository".

<p align="center">
 <img src="figures/crea_repo3.png" width="600" /> 
</p>

 Votre dépôt, uniquement rempli d’un fichier README.md, a été créé.
 
<p align="center">
 <img src="figures/crea_repo4.png" width="600" /> 
</p>

### Mettre à jour le dépôt

Vous pouvez désormais y ajouter le répertoire contenant tous les fichiers (et sous-répertoires) de votre Fiche.

Il existe plusieurs méthodes pour téléverser des fichiers sur GitHub (en ligne de commande ou en clic-bouton). Nous présentons ici la méthode clic-bouton depuis l’interface de GitHub. Pour le réaliser dans l'environnement RStudio, voir [cette documentation](https://sigr2021.github.io/git/#1), ou [celle-ci](https://docs.github.com/en/get-started/using-git/about-git) si vous souhaitez effectuer ces opérations directement dans le terminal.

Pour cela, cliquez sur “Add file”, puis sur “Upload files”.

<p align="center">
 <img src="figures/update_repo1.png" width="300" /> 
</p><br>

Faîtes glisser l’ensemble des fichiers et sous-répertoires de votre fiche dans le dépôt.

<p align="center">
 <img src="figures/update_repo2.png" width="600" /> 
</p><br>

Chaque mise à jour doit être associée à un [commentaire](https://www.conventionalcommits.org/en/v1.0.0/) permettant de traiter la nature de la modification réalisée. Ajoutez un commentaire et cliquez sur “Commit changes”.

<p align="center">
 <img src="figures/update_repo3.png" width="600" /> 
</p><br>

L’ensemble des fichiers sont désormais stockés sur le dépôt. Ce dépôt étant paramétré comme Public, tout le monde peut désormais consulter et récupérer ces fichiers.

<p align="center">
 <img src="figures/update_repo4.png" width="600" /> 
</p><br>


### Déploiement de l'article

Les fichiers sont consultables à l’état brut, mais une manipulation supplémentaire va permettre de mettre en ligne votre fiche (format HTML). Votre fiche mise en page sera ainsi consultable par tout le monde sur le web, sans avoir à gérer un serveur ou un site web. 

Concrètement, cette opération crée un *workflow* via [GitHub Actions](https://docs.github.com/fr/actions) qui forme un *pipeline CI/CD*, soit une série de tâches automatisées qui aident les équipes DevOps à réduire les tâches manuelles :

- **Continuous Integration** (intégration continue, CI) : crée, teste et intègre automatiquement les modifications de code dans un référentiel partagé. 
- **Continous delivery & deployment** (livraison et déploiement continu, CD) : transmet les modifications de code aux enironnements prêts pour la production et déploie les modifications de code directement sur un serveur. 

Ces opérations sont rendues possibles aisément avec les GitHub Pages. Cliquez sur “Settings > Pages > Source (none)” et sélectionnez la branche “. **Pour que cela fonctionne, le fichier html à déployer (et le rmd pour plus de cohérence) doivent impérativement avoir été renommés “index”**. 

<p align="center">
 <img src="figures/deploy1.png" width="600" /> 
</p><br>

Ne modifiez pas le répertoire ciblé par défaut (“root”) qui indique la racine du dépôt. Cliquez sur “save”.

<p align="center">
 <img src="figures/deploy2.png" width="450" /> 
</p><br>

Votre fiche est désormais consultable en ligne depuis votre compte GitHub. La page html est alors distribuée à l’adresse `https://username.gitub.io/repository_name/`. Vous pouvez retrouver cette URL dans le menu “Settings > Pages”.

<p align="center">
 <img src="figures/deploy3.png" align="center" width="600" /> 
</p><br>

Cliquez sur le lien affiché pour consulter la fiche mise en ligne :

<p align="center">
<img src="figures/deploy3.png" " width="600"/> 
</p><br>

### Readme.md

Le fichier markdown “README” est utilisé pour présenter les informations importantes à propos du dépôt. Son contenu est automatiquement affiché (et mise en forme grâce à la syntaxe markdown) en dessous des fichiers listés du dépôt.

Vous pouvez éditer et modifier facilement ce fichier depuis l’interface GitHub en cliquant sur le symbole crayon.

<p align="center">
<img src="figures/readme1.png" width="600" /> 
</pr><br>

Vous pouvez alors personnalisez le fichier en modifiant : le titre, le sous-titre, le.s auteur.e.s (et affiliation.s), ainsi que l’URL de consultation de la fiche. Par exemple : 

<p align="center">
<img src="figures/readme2.png" align="center" width="600" /> 
</p><br>

Une fois les modifications terminées, commentez votre commit, puis cliquez sur Commit changes pour enregistrer les changements effectués.

<p align="center">
 <img src="figures/readme3.png" width="450" /> 
</p><br>

Vous avez terminé la mise en ligne de votre article. Désormais, un lien vers votre article déployé est affiché à la racine du dépôt.

<p align="center">
 <img src="figures/readme4.png" width="600" /> 
</p><br>

Il ne vous reste plus qu’à contacter le comité de lecture Rzine pour soumettre votre fiche à évaluation. Pour toute question relative au processus de soumission et de relecture d’une fiche, vous pouvez contacter le comité éditorial en envoyant un courriel à l’adresse contact@rzine.fr

<p align="center"
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-sa/4.0/)
</p>
