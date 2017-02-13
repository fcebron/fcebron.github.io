---
layout: post
title: Installer Opencv3.2.0 avec python 3.5 sur ubuntu 16.04
---

# Installer Opencv3.2.0 avec python 3.5 sur ubuntu 16.04

J'utilise aptitude comme gestionnaire de packets, donc si vous ne l'avez pas il suffit de le remplacer par apt (ubuntu 16.04 et +) ou apt-get (sinon)


## Pour installer opencv3.2.0 sur ubuntu 16.04 il faut tout d'abord effectuer ces commandes : 

```sudo aptitude install build-essential cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev```

`mkdir Install`

`cd ~/Install`

`git clone https://github.com/opencv/opencv.git`

`git clone https://github.com/opencv/opencv_contrib.git`

`cd opencv`

`mkdir build`

`cd build`

`cmake -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local -D OPENCV_EXTRA_MODULES_PATH=~/Install/opencv_contrib/modules -D PYTHON_EXECUTABLE=/usr/bin/python3 ..`


(Le chemin de python3 se trouve en tapant : 
`type python3`)


`make -j4`
compile avec 4 cœurs

`sudo make install`
