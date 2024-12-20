---
layout: post
title: "Les classes de Réseaux et les sous-réseaux"
categories: junk

#meta: "Springfield"
---

### Index 
- [](#)


Les adresses IP (Internet Protocol) sont au coeur du thème sur le réseau. Afin d'améliorer les communications auprès de ce dernier, il a été décidé de les regrouper en différents groupes avec différents besoins. On les appelle : 'classes d'adresses IP'.
Toutes ces classes d'adresses IP ont le même nombre d'hôtes possible. Dans cet article nous verrons les noms et fonctions de ces groupes. 


Les Rappels : 

- Rappel : De quoi est composée une adresse IP ? 

Une adresse IP est généralement divisée en deux parties, son début représente l'identifiant du réseau (netId), et la fin représente l'identifiant de l'hôte (hostId), ou machine que l'on trouve sur le réseau. 

Vous l'aurez compris, plus l'identifiant de l'hôte est long, et plus de machines hôtes peuvent communiquer au sein d'un même réseau. 


- Rappel : Comment est formée une adresse IPV4 ? 

une adresse IPV4 est une suite de 4 octets, nombres séparés de points (par exemple 192.168.1.1) permettant à différents hôtes de communiquer et d'être identifiés sur le réseau. Ces nombres sont compris de 0 à 255. Ces nombres sont décimaux pour faciliter la lecture d'un point de vue humain, mais pour mieux comprendre pourquoi on s'arrête à 255, il faut les convertir en binaire : On observe qu'il vaut 11111111. Pas un seul 0 en vue. C'est normal, car c'est la valeur maximale que l'on peut atteindre en codant un nombre sur 8 bits, appelé aussi octet.

 En résumé, il y a 8 emplacements pour un chiffre binaire, et 255, ou 11111111, c'est le plus grand nombre. L'adresse étant constituée de 4 nombres de 8 bits, ou octets, on en conclut que les adresses IPV4 sont codées sur 32 bits.

Il sera important pour la suite de l'article d'avoir bien pris conscience qu'**une adresse IP est codée en binaire, et composée de quatre octets.**


- Rappel : Le bit de poids fort ? 

Dans un nombre binaire, les bits n'ont pas tous le même poids : en convertissant un 1 dans un nombre binaire, il peut définir = 1, 2, 4, 8, 16 ... etc. Le bit de poids fort c'est le bit ayant le plus de valeur du nombre binaire. Comme nous l'avons vu dans l'article de conversions de nombres binaires, c'est le bit étant le plus à gauche.


# Les différentes classes de réseaux

Les classes de réseaux se regroupent en cinq groupes nommmés de la lettre A à la lettre E. 

## La classe A

Le premier octet (ou nombre) de la classe A est entre **1 et 126**. Son 'bit de poids fort' vaut 0. Le premier nombre ou octet de l'adresse définit l'adresse du réseau, et le reste des octets définit l'adresse de l'hôte. 

Donc, avec ces adresses il est possible de rassembler un très grand nombre d'hôtes dans un réseau ! 

Où retrouve-t'on des adresses IP de la classe A ? 

En pratique, on manipule peu d'adresses IP de la classe A, elles sont réservées à de grands groupes, ou même les gouvernements car dans un seul réseau défini par la classe A, on peut trouver énormément de machines hôtes ! 


## La classe B

le premier octet de la classe B est entre **128 et 191**. Les deux bits de poids fort de ce nombre sont 1-0. Les deux premiers octets des adresses de classe B définissent l'identifiant du réseau et le reste définit l'identifiant de l'hôte. 

Où retrouve-t'on des adresses IP de la classe B ?

Les adresses de la classe B peuvent être utilisées par des entreprises de taille moyenne ou bien des universités. Il est plus courant de les rencontrer dans le domaine professionnel. 

## La classe C 

Le premier octet de la classe C est entre **192 et 223**. Les 3 bits de poid fort de ce nombre sont 1-1-0. Les trois premiers octets des adresses de la classe C définissent l'identifiant du réseau et le reste définit l'identifiant de l'hôte. 

Où retrouve-t'on des adresses IP de la classe C ? 

Ce sont les adresses les plus répandues, utilisées par de petits réseaux (petites entreprises ou chez des particuliers), il est possible de rencontrer 254 hôtes sur un même réseau. 

## La classe D

Le premier octet de la classe D est entre **224 et 239**. Les 4 bits de poids fort de ce nombre sont 1-1-1-0. Tous les octets sont réservés pour l'identifiant de réseau (NetId). 

Où retrouve-t'on des adresses IP de la classe D ? 
Ces addresse particulières sont utilisées pour des services de multi-diffusion, ou multicast. Ils servent à communiquer à des groupes d'hôtes, ou hosts-groups. 

## La classe E

Le premier octet de la classe E est entre **240 et 255**. Les 4 bits de poids fort de ce nombre valent 1-1-1-1. Les adresses comprises dans la classe E sont des adresses réservées par l'institution IANA, elle ne sont pas utilisées. 

Où retrouve-t'on des adresse IP de la classe E ? 
Elles sont réservées par l'IANA, ce qui signifie qu'on ne peut en rencontrer nulle part. 



Retenir les différentes classes d'adresses IP permet


Et les adresses commençant par 127 ? 
Vous avez pu le remarquer, il y a un 'trou' entre les adresses comprises dans la classe A et dans la classe B. Ce n'est pas un hasard. Les adresses commençant par 127 sont dédiées aux communications en 'boucle locale'. Elles sont donc reservées. 

Et l'adresse 0.0.0.0 ? Elle n'existe pas. 


# Qu'est-ce qu'un sous-réseau ? 

Comme nous venons de le voir, les classes d'adresses A, B et C sont des classes coupées en deux parties, celle qui nous permet d'identifier le réseau (NetID) et celle qui nous permet de définir l'hôte (HostID). En fontion du nombre d'octets attribués à l'une ou l'autre, on peut définir plus ou moins de réseaux et de nombre de machines possibles en fonction de la classe de l'adresse. 

- pour la classe A : 
- - nombre de réseaux possibles : 127 
- - nombre d'hôtes max. : 16 777 214 
- - masque de sous-réseau par défaut : 255.0.0.0


- pour la classe B 
- - nombre de réseaux possibles : 16 384
- - nombre d'hôtes max. : 65 534
- - masque de sous-réseau par défaut : 255.255.0.0 

- pour la classe C
- - nombre de réseaux possibles : 2 097 152
- - nombres d'hôtes max : 254
- - masque de sous-réseau par défaut : 255.255.255.0 

## Découpage d'une classe en sous-réseau

Savoir découper une classe d'adresses en sous réseaux, ce qui équivaut à diviser la partie des adresses hôtes (hostId) en de nouveaux groupes d'adresses, est une technique très pratique pour solutionner le problème de distribution de l'espace d'adressage. On l'appelle le "subnetting".

Cette technique permet entre autres de cloisoner les domaines de diffusion. Ce cloisonnement est pratique opur de nombreuses raisons. Par exemple, dans une entreprise, on cherchera toujours à séparer les téléphones IP des ordinateurs, car leurs méthodes de communications pourraient interférer entre elles. On va donc créer un réseau pour les ordinateurs, et un autre pour les téléphones. 
Ensuite, il y a un aspect de sécurité derrière le cloisonnement des domaines de diffusion : certains virus, comme le ver Sasser, se servent des diffusions pour identifier des machines sur le réseau. Cela limite les dégâts et permet de mieux sécuriser le réseau.


### Procédé

Pour définir des sous-réseaux à partir d'une classe d'adresses, on va d'une certaine manière 'allonger' la partie de la classe qui identifie les réseaux, et donc diminuer la partie qui définit les machines hôtes. 

Di l'on réserve trois bits pour définir les sous-réseaux, alors on disposera de huit sous-réseaux possibles. Di l'on en réserve deux, on disposera de trois réseaux etc. 

En général une fois que l'on a calculé les sous-réseaux, on les configure soit sur un switch manageable ou un routeur afin de les mettre en oeuvre. 


### Ce à quoi il faut veiller lorsqu'on calcule les sous réseaux 

Il faut faire attention à l'adresse du réseau et l'adresse de diffusion. ce sont deux adresses qui ne pourront pas être assignées à une machine hôte et donc ne feront pas partie de la plage d'adresses disponibles.

## Exemple 

Dans cette partie, on verra un cas pratique, avec un tableau de sous-réseaux, qui est important quand on met en place ou réfectionnne des réseaux, afin de garder une trace écrite des adresses et des découpages du réseau :
![Alt text](../img/masqueSousReseau.jpg)

---
