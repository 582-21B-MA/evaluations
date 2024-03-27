# TP2 : Pokédex

Le but de ce travaille est d'évaluer votre compréhension du langage de
définition et de manipulation de données SQL. Pour ce faire, il vous est
demandé de créer une base de données à propos des 151 premières créatures
de la franchise Pokémon.

## Exigences

*   La base de données doit contenir le nom, le ou les types, le numéro
    national, la taille et le poid de chaque Pokémon, ainsi que les
    différentes attaques que ceux-ci peuvent apprendre.
*   La base de données doit contenir les attaques que peuvent effectuer
    les Pokémon. Pour chaque attaque, on connait le type, la catégorie,
    la description, ainsi que la force.
*   La base de données contient des informations quant aux évolutions
    des Pokémon : le niveau auquel l'évolution est possible, l'item
    requis (s'il y a), et le nom du ou des évolutions immédiates.
*   La base de données contient des informations sur les types : chaque
    type d'attaque est *très efficace* contre un ou plusieurs types de
    Pokémon, et *peu efficaces* contre un ou plusieurs types de Pokémon.

## Questions

De plus, vous devez rédiger les requêtes qui permettent de répondre aux
questions suivantes :

1.  Quel est le nom des Pokémon qui peuvent utiliser l'attaque nommée
    « Growl » ?
2.  Quel est le nom des Pokémon qui n'ont pas d'évolution ?
3.  Quel est le nom du Pokémon dont l'évolution immédiate se nomme 
    « Charizard » ?
4.  Quel est la taille minimum, maximum et moyenne des Pokémon de chaque
    type ?
5.  Quel est le nom de tous les Pokémon dont le type est « Ghost » et
    « Poison » ?
6.  Quels sont les différentes évolutions du Pokémon nommé « Eevee »,
    leur type, ainsi que l'item nécessaire pour évoluer ?
7.  Quel est le nom et la description des attaques très efficaces et
    contre les Pokémon de type « Grass » et contre ceux de type 
    « Steel » ?
8.  Quelle est la force moyenne des attaques du Pokemon nommé 
    « Snorlax » ?
9.  Listez le nom des attaques ainsi que leur force en ordre croissant
    de leur force et de leur nom.

## Remise

Le travail doit être remis avant le 12 avril. La remise se fera sur
GitHub. Pour créer le dépôt, suivez les instructions à l'adresse
suivante : https://classroom.github.com/a/m6ZoJuxq. La remise doit être
faite à l'aide de l'interface textuelle de Git, et non sur le site Web
de GitHub.

Le schéma des tables doit être enregistré dans un fichier nommé «
pokedex.sql », tandis que les requêtes doivent être enregistrées dans un
fichier nommé « requetes.sql ». Les requêtes doivent être identifiées
par leur numéro.


## Rubrique d'évaluation

-   Les consignes sont respectées.
-   Le schéma respecte les exigences.
-   Le code est agréable à lire : la longueur des clauses ne dépasse pas
    80 caractères, et les clauses complexes sont séparées sur plusieurs
    lignes. 
-   Le code est formaté et indenté de façon consistante.
-   Les colonnes du tableau de résultat sont bien nommées à l'aide du
    mot-clé `AS`.
-   La base de donnée respecte les critères des deux premières formes
    normales : elle ne contient pas de redondances, et aucun attribut
    non-identifiant ne dépend d'une partie de l'identifiant primaire.
-   Les requêtes permettent de répondre aux questions de l'énoncé.
