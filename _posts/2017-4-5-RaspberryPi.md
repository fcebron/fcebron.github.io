---
layout: post
title: Raspberry Pi Installation de l'OS
---
# Nota
Dans toute cette page, les parties "sur l’ordinateur" correspondent aux étapes à réaliser sur la carte microSD, par l’intermédiaire d’un ordinateur. Puis les parties "Sur la Raspberry (via écran ou par UART)" correspondent aux actions qui nécessitent de travailler à même la Raspberry Pi (on ne peut pas tout de suite travailler en SSH, car elle n’est pas installée ni configuré sur l’image disque de base). 

De plus, dans ce document il est sous-entendu que nous possédons un ordinateur avec un Linux dessus (les commandes seront données pour un OS Ubuntu-like) ; car la création de cartes SD pour Raspberry Pi est une véritable horreur sous Windows, et le résultat est très rarement propre.

Lorsqu'il y a des portions de commandes bash, elles commencent soit par '$' (commande à exécuter en mode utilisateur - compte limité), soit par '#' (commande à exécuter en mode super-utilisateur - compte sudo - tapper la commande 'sudo su' au préalable).


## Le Matériel
Acheter une carte micro SD compatible : Sur le site suivant, il y a un classement non-exhaustif des cartes SD testées :

[http://elinux.org/RPi_SD_cards](http://elinux.org/RPi_SD_cards)

En général il faut une carte de classe 10 ou plus et d’au moins 8 GB. D'après mes derniers tests j'ai réussi à utiliser une carte de classe 4 sans problèmes.


## Les possibilités
Il faut savoir une chose avec la Raspberry : ses pin GPIO sont uniquement digitales (numérique), donc elles ne peuvent lire ou même écrire que des valeurs de type HIGHT et LOW. 
Pour lire un potentiomètre (valeur analogique), on est obligé de rajouter un composant pour transformer quelques GPIO en analogique. Ce composant est le MCP 3008, qui permet en utilisant 4 GPIO (dont celles de l’I2C), d’obtenir 8 pins analogiques.





# Ubuntu 14.04 LTS arm
## Sur l’ordinateur
###  Télécharger l’image disque
On peut la télécharger sur le site officiel :

[https://wiki.ubuntu.com/ARM/RaspberryPi](https://wiki.ubuntu.com/ARM/RaspberryPi)

Le compte par défaut est "ubuntu" et son mot de passe "ubuntu".


### Formater sa carte microSD
- Brancher la carte à l’ordinateur
- Démonter la carte SD (si elle est montée automatiquement (cf ubuntu,. . . )) : on peut le faire avec l’interface graphique (clic droit/démonter) ou en ligne de commandes (si le disque est répertorié comme sdd, pour trouver le nom du disque, voir partie suivante) :
    $ umount /dev/sdd
- Les étapes suivantes se font à l’aide du terminal :
    $ lsblk
(cela va lister tous les disques et leurs partitions)
On prend le nom du disque, sans le « p0 » ou « p1 » qui apparaît après son nom (le nom des
partitions) (exemple : mmcblk0 ou sdd)


Attention : ne surtout pas prendre sda (dans ce cas, c’est le disque dur de votre ordina-
teur que vous allez partitionner) ! ! ! !




# Sources :
