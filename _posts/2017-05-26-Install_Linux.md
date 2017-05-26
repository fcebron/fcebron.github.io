---
layout: post
title: Logiciels LUbuntu
---

###### Aptitude :
apt-get install aptitude

###### Logiciels de base :
sudo aptitude install mc libreoffice hunspell-fr octave scilab mat cherrytree synapse thuderbird thunderbird-locale-fr

###### Outils :
sudo aptitude install picocom bsdtar dfc htop terminator byobu tree kde-config-systemd ranger gufw gparted

###### Redshift :
sudo aptitude install redshift-gtk redshift plasma-widget-redshift 

###### Developpement :
sudo aptitude install vim build-essential meld valgrind arduino code::blocks arduino python python3 pep8 python3-pep8 python-autopep8 python-flake8 python3-flake8 git

###### LaTex :
sudo aptitude install texlive cm-super texlive-lang-french texlive-math-extra texlive-fonts-extra texmaker

###### Infographie :
sudo aptitude install dia inkscape freecad openscad sagCAD gimp gnuplot

###### multimedia :
sudo aptitude install vlc clementine kodi

###### Dactylographie :
sudo aptitude install klavaro ktouch tuxtype

###### Skype :
sudo add-apt-repository "deb http://archive.canonical.com/ $(lsb_release -sc) partner"
sudo apt-get update
sudo apt-get install skype

###### Logiciels extra a installer en allant sur le net :
opera
sublime text 2/3
vivaldi
discord
slack
nomachine


#numlockx  #### voir tuto forum ubuntu

###### Drivers NVidia GeForce GTX 750 :
sudo apt-add-repository ppa:graphics-drivers/ppa
sudo apt update
sudo apt install nvidia-375
