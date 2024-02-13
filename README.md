# Dokumentation Docker

### Inhaltsverzeichnis

- [Dokumentation Docker](#dokumentation-docker)
    - [Inhaltsverzeichnis](#inhaltsverzeichnis)
  - [Was ist Docker ?](#was-ist-docker-)
  - [Installation von Docker](#installation-von-docker)
  - [Erster Docker Container](#erster-docker-container)
  - [Docker Commands](#docker-commands)
  - [Starten einer Ubuntu Conosle.](#starten-einer-ubuntu-conosle)
  - [Presisten Storage](#presisten-storage)

## Was ist Docker ?

## Installation von Docker

Die instalation von Docker ist einfach auf Windows und Mac OS.  Sie sind auf beiden Betribssystemen gleich zu instalieren über entweder einne exe datei oder einer dmg datei.

[Docker Seite Windows](https://docs.docker.com/desktop/install/windows-install/)

[Docker Seite Mac os](https://docs.docker.com/desktop/install/mac-install/)

## Erster Docker Container

Um einen Continer einzurichten muss man den `docker create` Befehl benützen

```sh
docker create --name apache2-container -p 8080:80 ubuntu/apache2:2.4-22.04_beta
```

Jetzt solte ein Neuer Container mit z.b. `docker ps` oder man kann es dan auch auf der GUI in Docker Desktop zu sehen.

## Docker Commands

| Befehl | Beschreibung |
| ----------- | ----------- |
| `docker ps` | Zeigt alle Laufenden Container an und mit dem arg --all auch die gestopt sind. |
| `docker start [container name]` | Es startet einen Bestimmten conatiner|
| `docker stop [container name]` | Es stopt einen Bestimmten conatiner|
| `docker rm [container name]` | Löscht einen container. Dieser muss aber ausgeschhaltet werden |
| `docker exec -it [container name] sh` | Der befehl öffnet eine session sh auf dem docker zum ausführen von befehlen über den eigenen Terminal |
|`docker log -f [container name]` | Gibt die logs für den Container aus|
| `docker pull [Image name]` | Lädt das vorgegebene Image runter für die weiter verwendung |
| `docker rmi [image name]` | Löschen eines Images aus dem speicher es solten keine Conainer mit dem image erstelt sein |
| `docker create`| Erstelt einenn Neuen docker Container am ende muss immer das image definiert werden wie [der anleitung hier zu sehen](#installation-von-docker) |



## Starten einer Ubuntu Conosle.

Es geht ganz einfach durch den docker run befehl mit diesne Argumenten.

`docker run -ti --rm ubuntu /bin/bash`

Das `--ti` ist dafür da um den Terminal aufzurufenn und interaktive zu machen.
Das `--rm` ist zum Löschen des  Containers nach dem Schlißen des Terminals.
`Ubuntu` Ist das Image es könnte aber auch z.b. `Alpine` benutzen.
`bin/bash` ist eine Terminal emulation von Linux.


## Presisten Storage

Die Daten liegen auf dem Host system aber es ist immer abhängig vom betribssystem wo sie ligenn wen kein voulumen angegenen ist. Und jenachdem werden sie gelöscht.

Anlegen einses Volumens
`-v /data/mysql:/var/lib/mysql` Host Pfad : Container pfad
jetzt mit diesem argument kommt man über den angegenen Pfad im Host system auf die dateien.

Die Datei wird sich auch im Container ändern.