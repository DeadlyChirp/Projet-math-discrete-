# Paradoxe des Anniversaires

Le paradoxe des anniversaires est un résultat célèbre et surprenant en combinatoire qui indique que dans une classe de 23 élèves, il y a environ une chance sur deux que deux élèves partagent le même anniversaire.

## Fonctions de Hashage et le Paradoxe des Anniversaires

Le paradoxe des anniversaires joue un rôle clé dans l'étude des fonctions de hashage. Une fonction de hashage `h` est une fonction qui prend en entrée un fichier `F`, potentiellement volumineux, et renvoie une chaîne de caractères beaucoup plus courte `h(F)`. La propriété fondamentale que l'on souhaite avoir est que `h(F)` permette de vérifier, avec une très bonne probabilité, qu'un document est authentique et n'a pas été modifié pendant un transfert. Par exemple, cela permet de télécharger un fichier `F`, de calculer son hash `h(F)`, et de le comparer à la valeur `v` indiquée sur le site de téléchargement. Si `h(F) = v`, alors il est très probable que le fichier téléchargé soit le correct.

Le paradoxe des anniversaires permet de quantifier la probabilité que des collisions entre deux fichiers différents `F` et `F'` se produisent, c'est-à-dire que `h(F) = h(F')`. Les fonctions de hashage étant au cœur des protocoles cryptographiques, le paradoxe des anniversaires a également de nombreuses applications dans l'étude des systèmes de chiffrement et des protocoles cryptographiques.

## Bibliographie Conseillée

- [Wikipédia - Paradoxe des anniversaires](https://fr.wikipedia.org/wiki/Paradoxe_des_anniversaires)
- [Science Étonnante - Le paradoxe des anniversaires](https://scienceetonnante.com/2012/05/28/le-paradoxe-des-anniversaires/)
- [Bibmath - Cryptographie](http://www.bibmath.net/crypto/index.php?action=affiche&quoi=chasseur/anniversaire)

## Pistes de Développement

1. Établir la formule donnant la probabilité que deux personnes aient le même anniversaire dans une classe de N élèves :

   $$
   P(N) = 1 - \prod_{i=1}^{N-1} \left(1 - \frac{i}{365}\right)
   $$

2. Écrire un programme qui simule des classes de N élèves, où l'anniversaire de chaque élève est choisi au hasard dans l'année, afin de vérifier expérimentalement la formule obtenue.

3. Généraliser la formule et la simulation au paradoxe des anniversaires généralisé, pour des années comportant un nombre différent de jours, `d ≠ 365`.

4. Décrire une méthode pour exploiter le paradoxe des anniversaires (généralisé) afin de créer une attaque sur un protocole utilisant une fonction de hashage dont la sortie est très courte pour vérifier l'authenticité d'un fichier.

5. Explorer une autre application du paradoxe, et appliquer la simulation aux paramètres correspondants à cette application. Par exemple, l'identification de suspects par la technique d'empreinte génétique, ou l'application du paradoxe des anniversaires aux attaques sur le protocole de Wifi.
