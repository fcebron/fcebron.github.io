---
layout: post
title: Erreurs de débutant en Arduino
---

# Liste des erreurs basiques à éviter:
 * Utiliser les entrées / sorties numériques liées au port série (pin 0 et 1 sur Arduino Uno et Nano) dans un programme utilisant le port série pour communiquer avec l'ordinateur (ces pins relayent les données du port série et sont donc inutilisables de manière binaire). 
