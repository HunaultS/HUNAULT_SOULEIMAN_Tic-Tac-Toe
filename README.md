Le choix du workflow GitFlow pour ce projet présente plusieurs avantages et inconvénients.

1/Avantages :

a) Structuration claire : GitFlow divise le processus de développement en différentes phases distinctes, ce qui facilite la compréhension et la gestion du flux de travail. Les branches sont utilisées de manière organisée pour isoler les fonctionnalités, les versions stables et les correctifs. Cette organisation claire permet une meilleure gestion du travail et une séparation nette des différentes fonctionnalités en cours de développement.

b) Facilité de collaboration : GitFlow définit des conventions claires pour les branches et les actions à effectuer à chaque étape du processus, facilitant ainsi la collaboration entre les membres de l'équipe. Chaque développeur sait où travailler et comment intégrer ses modifications en toute sécurité dans le projet. Cela réduit les risques de conflits entre les développeurs et favorise une meilleure coordination dans le travail d'équipe.

2/Inconvénients :

a) Complexité : GitFlow peut sembler complexe pour les équipes moins expérimentées ou pour les projets de petite taille. La gestion des différentes branches et la compréhension des règles spécifiques à chaque étape peuvent nécessiter une certaine courbe d'apprentissage. Cela peut entraîner des difficultés initiales pour les nouveaux membres de l'équipe ou pour les projets plus simples où une approche plus légère serait préférable.

b) Rigidité : Bien que la structure claire de GitFlow puisse être un avantage, elle peut aussi être perçue comme rigide dans certains cas. Les développeurs peuvent se sentir restreints par les règles strictes définies par le modèle, ce qui peut parfois ralentir le processus de développement ou rendre difficile l'intégration de changements imprévus. Dans certaines situations, une approche plus flexible pourrait être plus adaptée pour répondre aux besoins évolutifs du projet.

c) Overhead : GitFlow peut introduire un certain overhead, surtout pour les projets plus petits ou pour les équipes où la communication est déjà très fluide. Suivre rigoureusement le modèle peut parfois nécessiter plus de temps et d'efforts que nécessaire, ce qui peut être perçu comme une inefficacité. Pour les projets plus simples ou pour les équipes où une approche plus légère serait suffisante, GitFlow peut sembler trop contraignant.

3/Conclusion :

En résumé, bien que GitFlow offre une structure claire et des conventions définies qui peuvent faciliter la gestion du développement logiciel, il peut être complexe, rigide et introduire un certain overhead, surtout pour les équipes moins expérimentées ou pour les projets de petite taille. Il est donc important de considérer attentivement les avantages et les inconvénients avant d'opter pour ce modèle dans un projet spécifique.

#------------------------------------------------------------------------------------------------------------------#

# Tic-Tac-Toe TP
Le TP est à rendre au plus tard **lundi 8 avril 2024, minuit**, par mail en signalant votre nom, prénom et le lien du repository public sur lequel se trouve vos livrables, le mail d'envoi **et** l'historique des commits faisant foi.

Il vous est possible de vous entre-aider mais votre rendu est **personnel** sauf mention contraire expresse pour les situations identifiées en amont.

## Instructions

### Préparer son environnement
- A partir du docker-compose disponible sur le repository [docker-gitlab-jenkins](https://github.com/June-Ruth/docker-gitlab-jenkins)

### Récupérer le projet en local
- Clôner le projet en local
- Mettre en place le projet sur le GitLab local avec le nom formaté selon le schéma suivant : **_nom_prenom_tic-tac-toe_**

### Création d'une pipeline d'intégration et de déploiement
La pipeline doit être formatée selon le schéma suivant : **_nom_prenom_tic-tac-toe_**
#### Outils
- La pipeline doit être éxécutée à partir de la plateforme d'intégration continue Jenkins
#### Fréquence
- La pipeline doit pouvoir être exécutée manuellement
- La pipeline doit être exécutée à chaque action de push et de merge request
##### Contenu
- La pipeline doit exécuter les tests
- Le stage de test doit mentionner le type de tests exéutés selon la pyramide des tests (soit dans son nom, soit dans la console lors de l'exécution)
- La pipeline doit fournir un rapport de couverture Clover
- La pipeline doit fournir les artefacts de distribution nécessaires au déploiement

### Correction des tests
- Les tests non-validés par la pipeline doivent être corrigés afin d'être valides

## Livrables
- Le code final sera rendu disponible sur un repository public
- La branche principale (main) sera à jour de l'ensemble des modifications
- Le code final devra conserver l'historique des branches et commits
- Le README présentera le workflow Git choisi en expliquant ses avantages et/ou inconvénients
- Le repository disposera d'un package spécifique pour les documents issus de la pipeline :
  - le rapport de couverture Clover fourni lors du dernier cycle Jenkins (format .html)
  - une copie (format .pdf) du dashboard principal de la **pipeline** sur Jenkins présentant au moins un cycle exécuté de manière automatique, les artefacts issue du build et le résumé de la couverture Clover
  - une copie (format .pdf) des paramètres mis en place sur GitLab servant à l'intégration de Jenkins
 
## Attention
- Les projets qui ne respectent pas les conventions de nommage ne seront pas évalués.
- Les projets dont l'historique git n'est pas accessible ne seront pas évalués.
- Les repository innaccessibles (adresse erronée, settings non-public) ne seront pas évaluées.
