# Dokumentation Docker 

### Inhaltsverzeichnis

- Was ist von docker?
- Instalation von Docker.
- Erster docker container.

## Was ist Docker ? 

## Installation von Docker.
Die instalation von Docker ist einfach auf Windows und Mac OS.  Sie sind auf beiden Betribssystemen gleich zu instalieren über entweder einne exe datei oder einer dmg datei. 

[Docker Seite Windows](https://docs.docker.com/desktop/install/windows-install/)

[Docker Seite Mac os](https://docs.docker.com/desktop/install/mac-install/)

## Erster Docker Container

Um einen Continer einzurichten muss man den `docker create` Befehl benützen

```sh
docker create --name apache2-container -e TZ=UTC -p 8080:80 ubuntu/apache2:2.4-22.04_beta
```

Jetzt solte ein Neuer Container mit z.b. `docker ps`
