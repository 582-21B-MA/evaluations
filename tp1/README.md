# TP1 : Modèle entité-association

Le but de ce travail est d'évaluer votre capacité à analyser une
situation qui nécessite une base de donnée, et à traduire cette
situation en un diagramme entité-association. Pour ce faire, il vous est
demandé de produire le diagramme entité-association du domaine
d'application suivant.

## Domaine d'application

Considérons un projet suivi par le gestionnaire de version Git. Pour
chaque version d'un projet, Git prend un instantané du contenu de
l'espace de travail à ce moment précis. L'espace de travail d'un projet
contient des fichiers et des répertoires, chacun identifié par un chemin
unique.

Lors de la prise d'instantanés, Git enregistre le contenu de l'espace de
travail dans des « objets » identifiés par une somme de contrôle de 40
caractères alphanumériques. Git sauvegarde le contenu des fichiers dans
un type d'objet appelé « blob ». Un blob contient la représentation
binaire du contenu d'un seul fichier. Un blob est immuable, c'est-à-dire
que pour chaque modification faite au fichier, un nouveau blob est créé.

Le contenu des répertoires est sauvegardé dans un autre type d'objet
nommé « arbre ». Un arbre représente un seul répertoire. Un arbre
contient une liste d'entrées, chacune ayant un nom, un code numérique
qui indique ses droits d'accès, et un type. Il est impossible de
garantir l'unicité de ces attributs. Un arbre contient au moins une
entrée. Chaque entrée pointe vers l'unique blob ou arbre qu'elle
représente. Tous les blobs sont référencés par au moins une entrée. Il
en va de même des arbres, à l'exception de celui qui représente le
répertoire où se trouve l'espace de travail. Comme les blobs, les arbres
sont immuables ; chaque fois qu'une de ses entrées est modifiée, un
nouvel arbre est créé. Ceci dit, le nouvel arbre peut contenir certaines
des « anciennes » entrées si celles-ci n'ont pas changé.

Il est possible d'indiquer à Git d'ignorer certains fichiers et
répertoires. Aucun blob ni arbre ne sera créé pour ceux-ci.

Le nom technique d'un instantané est « commit ». Un commit est identifié
par une somme de contrôle[^1], et contient un message, un ou une autrice, un
ou une responsable, ainsi que la date et l'heure de sa création. Un
commit pointe toujours vers un arbre. À l'exception du premier commit,
tous les commits pointent aussi vers un ou plusieurs commits parents. Un
commit est immuable. Si on désire changer le message d'un commit, par
exemple, un nouveau commit doit être créé. Celui-ci pointera vers le
même arbre et les mêmes commits parents, mais il n'aura pas la même
somme de contrôle.

[^1]: Un commit est techniquement un type d'objet, mais il n'est pas
      nécessaire de tenir compte de cette information dans le diagramme.

Il peut être inconvénient de se référer aux commits d'un projet par les
40 caractères alphanumériques de sa somme de contrôle. C'est pourquoi
Git offre la possibilité de créer des « branches ». Une branche est un
genre d'étiquette qui pointe toujours vers un seul commit. Plusieurs
branches peuvent toutefois pointer vers le même commit, et il est
possible de changer vers lequel commit pointe une branche. Une branche
est identifiée seulement par son nom, qui doit être unique.

## Remise

La remise doit se faire sur Léa en format PNG, JPG ou SVG avant le 29
mars. Vous pouvez utiliser l'outil de votre choix pour produire le
diagramme.

## Rubrique d'évaluation (20%)

-   Toutes les entités sont identifiées.
-   Toutes les associations sont représentées.
-   Chaque entité possède une contrainte d'identifiant valide.
-   Les contraintes de cardinalité décrivent correctement le domaine
    d'application.
