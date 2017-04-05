---
layout: post
title: Raspberry Pi Installation de l'OS
---
# Nota
Dans toute cette page, les parties "sur l’ordinateur" correspondent aux étapes à réaliser sur la carte microSD, par l’intermédiaire d’un ordinateur. Puis les parties "Sur la Raspberry (via écran ou par UART)" correspondent aux actions qui nécessitent de travailler à même la Raspberry Pi (on ne peut pas tout de suite travailler en SSH, car elle n’est pas installée ni
configuré sur l’image disque de base). 
De plus, dans ce document il est sous-entendu que nous possédons un ordinateur avec un Linux dessus (les commandes seront données pour un OS Ubuntu-like) ; car la création de cartes SD pour Raspberry Pi est une véritable horreur sous Windows, et le résultat est très rarement propre.


## Le Matériel
Acheter une carte micro SD compatible : Sur le site suivant, il y a un classement non-exhaustif des cartes SD testées :

[http://elinux.org/RPi_SD_cards](http://elinux.org/RPi_SD_cards)

En général il faut une carte de classe 10 ou plus et d’au moins 8 GB. D'après mes derniers tests j'ai réussi à utiliser une carte de classe 4 sans problèmes.

## Les possibilités
Il faut savoir une chose avec la Raspberry : ses pin GPIO sont uniquement digitales (numérique), donc elles ne peuvent lire ou même écrire que des valeurs de type HIGHT et LOW. 
Pour lire un potentiomètre (valeur analogique), on est obligé de rajouter un composant pour transformer quelques GPIO en analogique. Ce composant est le MCP 3008, qui permet en utilisant 4 GPIO (dont celles de l’I2C), d’obtenir 8 pins analogiques.


# Sources :
