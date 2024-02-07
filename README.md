# Dokumentation Docker

### Inhaltsverzeichnis

- Was ist von docker?
- Instalation von Docker.
- Erster docker container.

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

Jetzt solte ein Neuer Container mit z.b. `docker ps` oder man kann es dan auch auf der GUI in Docker Desktop zu sehhen. Es solte ein Neuer Container mit dem namen apache2-container zu sehen sein

## Docker Commands

| Befehl | Beschreibung |
| ----------- | ----------- |
| `docker ps` | Zeigt alle Laufenden Container an und mit dem arg --all auch die gestopt sind. |
| `docker start [container name]` | Es startet einen Bestimmten conatiner|
| `docker stop [container name]` | Es stopt einen Bestimmten conatiner|
| `docker rm [container name]` | Löscht einen container. Dieser muss aber ausgeschhaltet werden |
| test||