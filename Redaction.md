# Project Plan: The Birthday Paradox and Its Applications in Discrete Mathematics

## Introduction

Le paradoxe des anniversaires est un phénomène contre-intuitif découvert en théorie des probabilités, qui a des implications surprenantes dans divers domaines tels que la cryptographie et la théorie de l'information. Ce paradoxe révèle que dans un groupe de 23 personnes, la probabilité que deux individus aient le même anniversaire est supérieure à 50%. Cette probabilité croît de manière significative avec l'augmentation du nombre de personnes dans le groupe, atteignant presque 100% pour un groupe de 70 personnes.
---

## Table of Contents
1. [Fondements théoriques](#fondements-théoriques)
2. [Expérimentation et simulation](#expérimentation-et-simulation)
3. [Généralisation du paradoxe](#généralisation-du-paradoxe)
4. [Applications pratiques](#applications-pratiques)
5. [Conclusion](#conclusion)
6. [Annexe numérique](#annexe-numérique)
7. [Bibliographie](#bibliographie)

---

## Fondements théoriques
### A. Explication du paradoxe des anniversaires
  - Définition et origine du paradoxe
Le paradoxe des anniversaires a été formulé pour la première fois par le mathématicien polonais Richard von Mises. Malgré son nom, ce n'est pas un vrai paradoxe, mais plutôt un fait mathématique non intuitif. La racine de ce paradoxe réside dans la compréhension de la manière dont la probabilité augmente avec le nombre de comparaisons possibles et non seulement avec le nombre d'individus.

  - La combinatoire derrière le paradoxe

La combinatoire, qui est l'étude des arrangements possibles d'ensembles, joue un rôle crucial dans l'explication de ce phénomène. Pour un seul individu, la probabilité d'avoir un anniversaire spécifique est de 1/365. Cependant, lorsqu'on ajoute un deuxième individu, il y a maintenant deux jours à considérer, et la probabilité que ces deux ne partagent pas leur anniversaire est de 364/365. En ajoutant des individus successivement, on crée de plus en plus de paires potentielles pour lesquelles on doit considérer la probabilité qu'ils ne partagent pas un anniversaire. La probabilité que personne ne partage un anniversaire diminue donc rapidement avec chaque nouvel ajout.

### B. La probabilité en mathématiques discrètes
  - Introduction à la probabilité discrète
La probabilité discrète étudie les situations avec un nombre fini d'événements possibles. Elle est parfaitement adaptée pour modéliser des situations comme le paradoxe des anniversaires, où chaque jour de l'année peut être considéré comme un événement discret.

  - Formule de calcul pour N personnes
Pour calculer la probabilité que dans un groupe de N personnes, au moins deux personnes aient le même anniversaire, nous utilisons la formule suivante:
P(N) = 1 - \prod_{i=1}^{N-1} \left(1 - \frac{i}{365}\right)
Cette formule nous indique que pour chaque nouvel individu ajouté, il faut multiplier la probabilité précédente par la chance que son anniversaire ne coïncide pas avec ceux déjà choisis.

---

## Expérimentation et simulation
### A. Simulation informatique
  - Présentation de l'algorithme de simulation
L'algorithme pour simuler le paradoxe des anniversaires commence par générer aléatoirement des anniversaires pour chaque personne dans le groupe et compte si des doublons apparaissent. Cela est répété plusieurs milliers, voire millions de fois, pour obtenir une estimation précise de la probabilité.L'algorithme pour simuler le paradoxe des anniversaires commence par générer aléatoirement des anniversaires pour chaque personne dans le groupe et compte si des doublons apparaissent. Cela est répété plusieurs milliers, voire millions de fois, pour obtenir une estimation précise de la probabilité.

  - Langage de programmation et outils utilisés
Python est souvent choisi pour ce type de simulation grâce à des bibliothèques comme random pour la génération de nombres aléatoires et numpy pour les calculs statistiques. La facilité d'écriture des scripts en Python et la puissance de ses bibliothèques permettent de réaliser rapidement des simulations complexes.
    

### B. Résultats expérimentaux
  - Analyse des résultats de simulation
Les résultats des simulations informatiques révèlent généralement une corrélation étroite avec les prédictions théoriques. Par exemple, dans un groupe de 23 personnes, les simulations montrent en effet que la probabilité de partager un anniversaire dépasse souvent 50%, ce qui valide notre formule mathématique.

  - Comparaison avec les résultats théoriques
La comparaison entre les résultats expérimentaux et théoriques est essentielle pour valider la fiabilité des modèles mathématiques. Les simulations servent de preuve empirique que nos formules théoriques fonctionnent dans des conditions expérimentales réalistes.


---

## Généralisation du paradoxe
### A. Le paradoxe dans un contexte généralisé
  - La formule peut être adaptée pour des cas où le nombre de jours dans l'année varie, ce qui peut être pertinent pour des applications spécifiques comme la cryptographie où l'on s'intéresse au nombre de valeurs de hash possibles.
Adaptation de la formule pour d jours différents de 365
Si on généralise le nombre de jours à d, la formule devient:
P(N) = 1 - \prod_{i=1}^{N-1} \left(1 - \frac{i}{365}\right)
Cette formule peut être utilisée pour calculer les probabilités dans des situations où l'espace des événements possibles est différent de celui du calendrier grégorien.


### B. Simulation de la généralisation
  - Modification de l'algorithme pour la généralisation
Modification de l'algorithme pour la généralisation
L'algorithme de simulation peut être adapté pour supporter un nombre d de jours en ajustant simplement la plage de génération aléatoire des anniversaires.

---

## Applications pratiques
### A. Cryptographie et fonctions de hashage
  - Principe des fonctions de hashage
Les fonctions de hashage sont essentielles en cryptographie. Elles transforment les données en une chaîne de caractères de longueur fixe. L'idée est qu'une modification minime des données d'entrée doit entraîner une modification significative du hash de sortie.

  - Paradoxe des anniversaires dans la sécurité informatique
Le paradoxe des anniversaires trouve son application dans le domaine de la cryptanalyse, où il sous-tend les attaques contre les fonctions de hashage. Ces attaques, dites "d'anniversaire", exploitent la probabilité croissante de collisions dans les espaces de hash de taille finie.


### B. Autres applications
  - Identification de suspects par empreinte génétique
En génétique forensique, le paradoxe peut être utilisé pour estimer la probabilité que deux individus aient un profil génétique similaire, ce qui est crucial pour l'identification des suspects.

  - Attaques sur les protocoles de Wifi
Dans la sécurité des réseaux, les attaques utilisant le paradoxe des anniversaires peuvent être employées pour briser certains protocoles de cryptage Wi-Fi, ce qui souligne l'importance de connaître et de comprendre ce concept.


---

## Conclusion
Le paradoxe des anniversaires est bien plus qu'une curiosité mathématique; c'est un concept puissant avec des applications pratiques dans plusieurs domaines technologiques. La simulation informatique et l'expérimentation confirment la théorie et la rendent tangible, nous rappelant que les probabilités, souvent non intuitives, régissent beaucoup de nos interactions technologiques et sociales. La compréhension et l'application de la probabilité discrète deviennent de plus en plus pertinentes dans notre monde où les données et leur sécurité jouent un rôle central.





