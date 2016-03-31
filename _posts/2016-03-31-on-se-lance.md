---
layout: post
title:  "On se lance"
date:   2016-03-30 16:00:00 +0100
categories: golang install
---

# On fait quoi ?

Nous allons apprendre dans cet article comment installer le langage Go sur sa machine et écrire notre premier programme, le grand classique "hello world". Je prendrai l'exemple de l'installation sur le système d'exploitation **OS X** mais la procédure est similaire sur tous les systèmes de type **Unix**. La procédure peut cependant varier pour les utilisateurs de **Windows**.

Nous verrons également comment compiler notre programme pour une architecture et un système d'exploitation spécifique.

# Téléchargement

La première étape consiste à télécharger le package contenant tous les éléments nécessaires au langage notamment le compilateur sur le [site officiel](https://golang.org/dl/). Le site met à disposition un installeur dédié à chaque système d'exploitation et également les fichiers sources afin de compiler pour une architecture plus exotique comme l'architecture **ARM** par exemple. Je recommande de télécharger la dernière version stable (1.6 actuellement).

# Test et configuration

Pour **Windows** et **OS X**, l'installation par l'exécutable ne devrait pas demander de configuration ultérieure, pour tester l'installation il suffit de lancer un terminal et de taper la commande `go version`. Le numéro de version devrait s'afficher.

``` shell
$ go version
go version go1.6 darwin/amd64
```

# Le GOPATH

Il convient de spécifier une variable d'environnement appelée `GOPATH` qui correspond au répertoire de travail de Go. C'est dans ce répertoire que se trouvera le code source ainsi que les fichiers binaires générés par le compilateur. Ce répertoire doit contenir un sous-répertoire appelé _src_ qui contiendra le code source des projets Go.

``` shell
$ export GOPATH=$HOME/go
$ cd $GOPATH
$ mkdir ./src
```

# Hello world !

Nous allons maintenant écrire notre premier programme Go, pour cela créons un répertoire appelé _hello_ et notre premier fichier _main.go_.

``` shell
$ cd $GOPATH/src
$ mkdir ./hello && cd ./hello
$ touch main.go
```

Le fichier _main.go_ contient le code source de notre premier programme.

``` golang
// main.go
package main

import "fmt"

func main() {
	fmt.Println("Hello world!")
}
```

Pour compiler et exécuter notre programme, il suffit de taper la commande `go run` suivi du nom du fichier à compiler.

``` shell
$ go run main.go
Hello world!
```

Il est également possible de générer un fichier exécutable avec la commande `go build`.

``` shell
$ go build
$ ls
hello main.go
$ file hello
hello: Mach-O 64-bit executable x86_64
```

Le fichier _hello_ est bien un exécutable compatible avec notre système d'exploitation.

# J'ai un Raspberry Pi

Les variables d'environnement `GOARCH` et `GOOS` permettent de spécifier l'architecture et le système d'exploitation respectivement. L'exemple suivant compile notre programme pour l'architecture **ARM** sous **Linux**.

``` shell
$ GOARCH=arm $GOOS=linux go build
$ file hello
hello: ELF 32-bit LSB executable, ARM, version 1 (SYSV), statically linked, not stripped
```

Cet exemple nous montre à quel point il est facile de compiler pour un système d'exploitation et une architecture différente. C'est un des points forts du langage Go.

# Vous êtes pressés ?

Il est possible de tester le langage Go dans son navigateur sans avoir besoin d'installer un quelconque logiciel avec le [Go Playground](https://play.golang.org/) mis à disposition par Google.

# Pour aller plus loin

+ [La documentation d'installation](https://golang.org/doc/install)
+ [Les variables d'environnement pour la compilation](https://golang.org/cmd/go/#hdr-Environment_variables)
+ [Le Go Playground](https://play.golang.org/)
