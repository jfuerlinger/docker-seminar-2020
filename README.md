# Docker Seminar 2020

## Allgemein

Trainer Rainer Stropek.

Container sind aus der Informatik nicht mehr wegzudenken. Dank der Docker-Plattform wurde aus dieser schon lange existierenden Linux-Funktion eine leicht einzusetzende und enorm praktische Werkzeugsammlung, die auch im Unterricht hilfreich sein kann. In diesem Seminar lernen Sie die Grundlagen und Architektur von Docker anhand zahlreicher praktischer Beispiele kennen. Zielgruppe: Lehrer*innen für Informatik an HTL.

## Ressourcen

* [GitHub Stropek](https://github.com/rstropek/DockerVS2015Intro)
* [Kontaktkarte Stropek](rainerstropek.me)
* [Docker Reference](https://docs.docker.com/reference/)
* [Microk8s](microk8s.io)

## Aufzeichnungen

* [Tag 1 (Teil 1)](https://cddataexchange.blob.core.windows.net/data-exchange/DockerTraining/Docker-Tag-1-Teil-1.mp4)

## Tipps

1. Docker Toolbox nicht mehr verwenden -> ist deprecated
1. Visual Studio Code Extensions
   1. Remote Development Extension
   1. Docker Extension


## Erste Berührungspunkte

```sh

docker info
docker run -it --rm ubuntu # Starten eines interaktiven Terminals für Ubuntu



docker ps # Aktuell laufende Container auflisten
docker ps -a # Aktuell laufende Container auflisten (inkl. der beendeten Container)
docker exec -it <container-id> /bin/bash # Interaktive Shell in einem Container starten
docker inspect <container-id> # Details an Informationen zum Container auflisten (json-Format)
```