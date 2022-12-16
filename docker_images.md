# Docker Images

## Tranfer a Docker image between computers

1. Save a Docker image to a `tar.gz` file

`` $ docker save myimage:latest | gzip > myimage.tar.gz ``

2. load an image from a tar archive 

`` $ dokcer load < myimage.tar.gz  ``

## Remove Docker Images

`` $ docker rmi image1 image2 ... ``

