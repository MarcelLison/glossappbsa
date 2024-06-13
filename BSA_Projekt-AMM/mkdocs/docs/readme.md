
Titel: "Projektarbeit - Glossapp-Entwicklung"

## Beschreibung: 


>Im Rahmen dieses Projekts erfolgt die Dokumentation zur Entwicklung der Glossar-Applikation (Glossapp) zur Verwaltung von Begriffen.
>Die Applikation wird auf einem Server gehostet und verwendet verschiedene Technologien wie MkDocs und Docker für die Bereitstellung.

>Infos zum Server:
  
> Hostname: "bsa-u22-server"
> Ip_adresse: "10.76.31.238/20"
> passwort: (Wird vom Administrator vergeben. ggf. Lehrkraft anfragen)


## Wie Fange ich an?

### 1. Aktualisierung mit erstem Befehl die Listen der verfügbaren Pakete und der zweite Befehl installiert alle verfügbaren Paketupdates.

`sudo apt-get update && sudo apt-get upgrade`

### 2. Erstellen eines ssh-keygens zum automatischen Anmelden am Server
    `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

### 3. MkDocs installieren

    Mittels `apt-get install PAKET_NAME` die benötigten Pakete installieren, wenn nicht schon vorhanden.

   - Python (pip für die Installation von MkDocs)
   - MkDocs 
   - Docker.io (für Docker Container)


#### Tutorial Videos:

[MkDocs](*https://www.youtube.com/watch?v=K2RDsWgwDTU)
[Docker](*https://www.youtube.com/watch?v=K2RDsWgwDTU)

#### Dokumentationen


[Doku Docker](*https://www.docker.com/get-started/)
[Doku MkDocs](*https://www.mkdocs.org/getting-started/)

## Wofür verwenden wir Mkdocs?
MkDocs wird verwendet, um die Dokumentation für die Glossapp zu erstellen und zu verwalten.
Die Installation erfolgt mithilfe von Pip oder Docker-Compose. In unserem Fall nutzen wir Docker-Compose.


##  Docker
    Docker wird verwendet, um die Glossapp in Containern zu isolieren und zu betreiben.
    Der Docker-Dienst wird mit Docker-Compose gestartet.
    Der Befehl hierzu ist, sofern alles richtig gemacht wurde `sudo docker-compose up -d` im zugehörigen Verzeichnis.




