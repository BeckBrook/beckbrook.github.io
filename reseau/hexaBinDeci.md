---
layout: post
title: "Comprendre et convertir le binaire, l'héxadécimal"
categories: junk

#meta: "Springfield"
---

### Index 
- [les Systèmes de Numération](#les-systèmes-de-numération)
- [Le Décimal](#le-décimal)
- [Le Binaire](#le-binaire)
- [L'Hexadécimal](#l'hexadécimal)
- [Convertir Décimal -> Binaire](#convertir-décimal-vers-binaire)
- [Convertir Décimal -> Héxadécimal](#convertir-décimal-vers-hexadécimal)
- [Convertir Binaire -> Décimal](#convertir-binaire-vers-décimal)
- [Convertir Binaire -> Décimal](#convertir-binaire-vers-décimal)
- [Convertir Hexadécimal -> Binaire](#convertir-hexadecimal-vers-binaire)
- [Convertir Hexadécimal -> Décimal](#convertir-hexadecimal-vers-décimal)

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

Maintenant, tentons de comprendre pourquoi 1+1=10, et que 2+1=11 ! 

Pour traduire ces chiffres, puisque nous sommes en base 2, nous aurons besoin des puissances de 2. Et d'un tableau : 

| 2^...| 2^6 | 2^5 | 2^4 | 2^3 | 2^2 | 2^1 | 2^0 |
|...   |   64|   32|   16|    8|    4|    2|    1|
|...   |0 ou 1|0 ou 1|0 ou 1|0 ou 1|0 ou 1|0 ou 1|0 ou 1|

Si l'on veut un 1 en décimal, alors nous devons remplir une seule et unique case, la toute dernière. 


on arrivee avec un joli ...00000001, dans ce cas là les 0 à gauche sont inutiles, en les enlevant, on se retrouve avec : 

1 (décimal) = 1 (binaire)

maintenant pour 2, on regarde le tableau, et cette fois nous n'avons pas besoin du 1, mais du 2 de la case à gauche ! plus précisément le 2^1, donc on a 000000010, on peut enlever les 0 de gauche mais surtout pas celui de droite, qui indique que nous n'avons pas besoin du 1 ! donc cette fois : 

2 (décimal) = 10 (binaire)

pour le 3, on sait qu'il peut se former avec 2 et 1, donc on remplit deux cases du tableau : 

3 (décimal) = 11 (binaire)


Si l'on suit la même logique, on se retrouve avec ce tableau pour les chiffres de 1 à 15 par exemple : 

|décimal|binaire|
|0|0|
|1|1|
|1|01|
|3|11|
|4|100|
|5|101|
|6|110|
|7|111|
|8|1000|
|9|1001|
|10|1010|
|11|1011|
|12|1100|
|13|1101|
|14|1110|
|15|1111|



> Bonus : mention nerd 
> 
> La manière de noter en binaire ne date pas de l'ère de l'informatique, les traces les plus anciennes d'une base 2 que l'on connaisse datent...d'environ 750 av J.C ! Dans un écrit chinois, le 'Yi Jing', on y retrouve des 'hexagrammes', des caractères construits à partir de deux 'trigrammes' eux-mêmes constitués de deux possibilités : soit un trait plein, soit deux petits traits. exemple : ䷓ (l'éclatement). 



## L'Hexadécimal

Comme le décimal compte avec 10 numéros, le binaire avec 2 numéros, l'hexadécimal compte avec 16 numéros. Mais comment symbolise-t'on ces 'numéros' lorsqu'ils dépassent 9 ? 
En hexadécimal, on utilise les premières lettres de l'alphabet après avoir épuisé les numéros que l'on a récupéré du système décimal, ce qui revient à compter avec ces caractères : 

|0|1|2|3|4|5|6|7|8|9|A|B|C|D|E|F|

L'informatique est un monde fabuleux où l'on compte aussi avec des lettres. Pourquoi a-t'on décidé de compter en hexadécimal ? Parce qu'avoir autant de caractères de base pour former un nombre nous permettra de stocker plus facilement celui-ci, on a donc un gain de place ! 
On retrouve ainsi l'hexadécimal dans de nombreux cas où l'on a besoin d'avoir des tonnes de possibilités, dans un nombre de caractères réduits, par exemple : 
- Dans les addresses MAC ex. "5E:FF:56:A2:AF:15" et les adresses IPv6 ex. "2001:db8:0:85a3:0:0:ac1f:8001"
- pour coder les couleurs ! par exemple, le blanc, c'est #ffffff et le noir, c'est #000000. vous pouvez voir l'éventail de possibilités qu'offre l'héxadécimal appliqué aux couleurs sur ce [Sélecteur de couleurs (W3schools)](https://www.w3schools.com/colors/colors_picker.asp)

Mais comment compter en hexadécimal ? 

déjà, c'est très facile de compter de 1 à 9, pour des raisons évidentes, et enfin de 10 à 16, il suffit de connaître son alphabet jusqu'à F :
- 10 (décimal) = A (hexadécimal)
- 11 (décimal) = B (hexadécimal)
- ..
- 16 (décimal) = F (hexadécimal)

Un bon site pour [apprendre l'alphabet (logicieleducatif.fr)](https://www.logicieleducatif.fr/jeu/l-alphabet).

Mais une fois que l'on veut dépasser F, comment faire ? 


## Convertir Décimal vers Binaire
## Convertir Décimal vers Hexadécimal
## Convertir Binaire vers Décimal
## Convertir Binaire vers Hexadécimal
## Convertir Hexadécimal vers Binaire
## Convertir Hexadécimal vers Décimal

