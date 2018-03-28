---
layout: post
title: Look@Lan
---

Pour lister les IP d'un réseau local, on peut utiliser différents outils :
- Look@Lan
- AngryIPScanner
- nmap
- ...

Sous Linux, je privilégie AngryIpScanner (fonctionnel), sous Windows le meilleur est Look@Lan.
Mon problème avec Look@Lan sous Windows 7 était qu'il ne me renvoyait que ma machine (dans le cas d'un réseau local peuplé).
La solution se trouve sur [ce site](https://superuser.com/questions/609290/old-looklan-software-gives-no-packet-to-read-log-error-then-wont-ping), cependant elle n'est pas bien adaptée (trop de chose inutiles).
Pour résumer, voici la solution :
1. LookAtLan ne supporte pas l'IP V6 et l'entrée du pare-feux n'est pas bonne.
2. Il faut supprimmer les entrées look@lan et look@host (elles sont inutiles)
3. Lancer l'éditeur d'entrées pare-feux avancé : faire windows + r, taper "wf.msc"
4. Cliquer sur les règles de traffic entrant (colone de gauche)
5. Click droit sur règles de traffic entrant (colone de gauche), choisir Nouvelle entrée
6. Créer une entrée personnalisée
7. Au programme ayant pour chemin d'accès Look@Lan (C:\ProgrammesFiles\Look@Lan\Look@Lan.exe)
8. Le type de protocole est ICMPv4 (ping en IPv4)
9. Pour toutes les IP
10. Autoriser la connection.

Remarque : Il se peut que Look@Lan requiert les droit d'administrateurs par défaut ainsi que le mode de compatibilité XP_sp3, pour cela, aller dans le dossier d'install, faire click droit, propriétés / Compatibilité et choisir d'exécuter en tant que XP Sp3 et avec les droits d'administrateurs.
