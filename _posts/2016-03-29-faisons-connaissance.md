---
layout: post
title:  "Faisons connaissance"
date:   2016-03-29 18:00:00 +0100
categories: golang getting_started
---

# Le Go ?

Le langage Go (aussi appelé Golang pour plus de commodité) est un langage de programmation système développé par Google depuis 2007 sous la direction de 3 programmeurs très connus, **Robert Griesemer**, **Rob Pike** et **Ken Thompson**.

Rob Pike et Ken Thompson sont nottamment connus pour leux travaux sur le système d'encodage `UTF-8` et les systèmes d'exploitation de type `Unix`.

Le langage Go dispose d'une mascotte : le gopher (Géomyidés ou rat à poche en français).

![Gopher, la mascotte du langage]({{ site.url }}/assets/images/gopher.png){: style="max-width: 200px; height: auto; text-align: center;"}

La première version du Go est sortie en 2009 et la dernière release 1.6 date du 17 février 2016. C'est donc un langage en constante évolution.

# Pourquoi un nouveau langage ?

L'objectif de la création de ce nouveau langage est d'être à la fois très puissant, mais aussi simple et intuitif à utiliser. Golang se veut être un langage fun où le programmeur prend plaisair à l'utiliser. Ce langage arbore donc une syntaxe simple et légère.

Le Go a été développé pour simplifier la vie du programmeur sur de nombreux points du cycle de vie du logiciel qu'il conçoit, ainsi le langage veut améliorer les points suivants :

  + la vitesse de compilation
  + la gestion des dépendances
  + améliorer la lisibilité du code
  + diminuer drastiquement la duplication de code, et donc la duplication de travail
  + diminuer le coût de maintenance et de mise à jour
  + faciliter le développement d'outils automatisés
  + permettre une compilation multi-plateforme simple

L'un des objectifs du Go est également de proposer des mécanismes permettant de gérer simplement les phénomènes de concurrence.

# Et qu'est-ce que ça donne ?

Au final, le Go est un langage compilé, cela signifie que son code source est traduit en langage machine pour un programme, appelé compilateur. Le résultat de la compilation est un exécutable pouvant être traité par l'ordinateur.

Le Go est un langage à typage statique fort, celà signifie qu'une variable ne peut pas changer de type durant l'exécution du programme et qu'il n'y a pas de conversion implicite de type. Ce choix de conception impose une plus grande rigidité au programmeur mais permet de réduire le nombre d'erreurs lors de l'exécution du programme.

Le Go possède un garbage collector, ou ramasse miettes en français. C'est un mécanisme permettant de gérer automatiquement la mémoire utilisée par le logiciel et de libérer la mémoire précédemment allouée lorsqu'elle n'est plus utilisée.

Le Go est un langage orienté objet mais dépourvu de la notion d'héritage. Le Go utilise la composition pour remplacer cette notion d'héritage. Nous verrons dans un futur article ce que celà signifie.

Le Go possède une librairie standard riche permettant au maximum de s'affranchir de l'utilisation de dépendances externes.

# Pour aller plus loin
[L'article wikipédia sur le Go](https://en.wikipedia.org/wiki/Go_(programming_language))
[Présentation du langage par Google](https://talks.golang.org/2012/splash.article)
[La documentation de la librairie standard](https://golang.org/pkg/)
