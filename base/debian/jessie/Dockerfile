################################
## Team  : Toroia             ##
## Image : base-debian:jessie ##
################################

# Dépendance de l'image 
FROM debian:jessie

# Mainteneur de l'image
MAINTAINER ToroiaTeam "contact@toroia.fr"

# Installation de apt utils
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install --assume-yes apt-utils

# Mise à jour du système
RUN apt-get upgrade -y && apt-get dist-upgrade -y

# Installation des programmes de base
# Nettoyage des paquets
RUN apt-get -y --no-install-recommends install curl ca-certificates nano && \
    apt-get -y -q autoclean && \
    apt-get -y -q autoremove

# Suppression des fichiers inutiles
RUN rm -Rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
