---
layout: post
title: "Comprendre et convertir le binaire, l'héxadécimal"
categories: junk

#meta: "Springfield"
---

### Index 
- [les Systèmes de Numération](#les-systemes-de-numeration)
- [Le Décimal](#le-decimal)
- [Le Binaire](#le-binaire)
- [L'Hexadécimal](#l'hexadecimal)
- [Convertir Décimal -> Binaire](#convertir-decimal-vers-binaire)
- [Convertir Décimal -> Héxadécimal](#convertir-decimal-vers-hexadecimal)
- [Convertir Binaire -> Décimal](#convertir-binaire-vers-decimal)
- [Convertir Binaire -> Décimal](#convertir-binaire-vers-decimal)
- [Convertir Hexadécimal -> Binaire](#convertir-hexadecimal-vers-binaire)
- [Convertir Hexadécimal -> Décimal](#convertir-hexadecimal-vers-decimal)

Il existe de nombreux systèmes de numération, mais les informaticiens n'en fréquentent en général que trois : 

- le *décimal*, un système de "base 10" 
- le *binaire*, un système de "base 2"
- l'*héxadécimal*, un système de "base 16"

Dans ce post nous verrons une petite introduction aux systèmes de numération, les définitions et dans quel contexte on rencontre ces systèmes de numération. Enfin, on verra comment effectuer des conversion d'un système de numération à un autre. 

---

## les Systèmes de Numération

Un système de numération nous permet de structurer notre manière de compter. Il repose sur une base. 
On appelle "base" l'ensemble de numéros uniques du système.

Si l'on a seulement 5 doigts d'une main pour compter, notre base sera de 5. Si l'on compte sur les deux mains, on se retrouve avec une base 10...etc. Et oui, la base 1 existe, puisque c'est celle que l'on utilise quand on trace un petit trait à chaque fois que l'on compte quelque chose.


*La légende raconte que l'inventeur de l'hexadécimal avait 16 doigts, et qu'il était un pianiste hors pair.*


## Le Décimal

Pour le décimal, rien de bien compliqué : on dispose de 10 caractères pour compter, c'est le système de numération que l'on utilise tous les jours 

|0|1|2|3|4|5|6|7|8|9|

> ATTENTION : il arrive que par erreur on considère le décimal comme 1,2,3,...10 ! On ne doit pas oublier que 0 fait partie de la base, et 10 n'a rien à faire dedans, il est composé de deux numéros. 


## Le Binaire

Le binaire est un système de numération très répandu en informatique. Concrètement, on dispose de deux possibilités : 

|0|1|

C'est aussi un langage, utilisé par les systèmes informatiques. Pourquoi ? Premièrement, c'est ce qui permet à la machine de ne pas faire de distinction entre plusieurs niveaux de tension quand elle a à faire à un signal électrique à traiter. En appliquant le binaire : soit il y a du courant (même s'il est élevé ou faible, on s'en fiche), soit il n'y en a pas. Donc on a fini par reposer sur la logique dite 'booléenne' (le fameux true ou false, vrai ou faux), pour plus de précision sur les calculs booléens, voir [l'Algèbre de Boole (logique) sur Wikipédia](https://fr.wikipedia.org/wiki/Alg%C3%A8bre_de_Boole_(logique)) (PS : on y reviendra pour le calcul des masques de sous-réseau !)

Maintenant, tentons de comprendre pourquoi 1+1=11, et que 1+1+1=101 !
Voici un tableau qui nous montre comment sont codés les chiffres que nous connaissons en binaire

|1|1|1|1|1|1|
|||||||





> Bonus : mention nerd 
> La manière de noter en binaire ne date pas de l'ère digitale, les traces les plus anciennes d'une base 2 que l'on connaisse datent...d'environ 750 av J.C ! Dans un écrit chinois, le 'Yi Jing', on y retrouve des 'hexagrammes' construits à partir de deux 'trigrammes' eux-mêmes constitués de deux possibilités : soit un trait plein, soit deux petits traits. mon préféré ressemble à un short : ䷓ (l'éclatement). Toutefois, ces caractères ne servaient pas pour le calcul et ne constituaient pas en soi un système de numération tels qu'ils sont présentés dans cette oeuvre. 



## L'Hexadécimal
## Convertir Décimal vers Binaire
## Convertir Décimal vers Héxadécimal
## Convertir Binaire vers Décimal
## Convertir Binaire vers Héxadécimal
## Convertir Hexadécimal vers Binaire
## Convertir Hexadécimal vers Décimal

