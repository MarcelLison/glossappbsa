"Projektarbeit -  Glossapp-Entwicklung"

Beschreibung: >

Im Rahmen dieses Projekts erfolgt die Entwicklung der Glossar-Applikation (Glossapp) zur Verwaltung von Begriffen.
Die Applikation wird auf einem Server gehostet und verwendet verschiedene Technologien wie MkDocs und Docker für die Bereitstellung.

Infos zum Server:

  Hostname: "bsa-u22-server"
  Ip_adresse: "10.76.31.238/20"
  passwort: (Wird vom Administrator vergeben. ggf. Lehrkraft anfragen)


Wie Fange ich an?

1. Aktualisierung mit erstem Befehl die Listen der verfügbaren Pakete und der zweite Befehl installiert alle verfügbaren Paketupdates.

´"sudo apt-get update && sudo apt-get upgrade"´

1.1.  (Optional) SSH - keygen
ssh-keygen -o -a 100 -t ed25519
    ->ssh-keygen: Befehl zum erstellen von SSH-Key

2. MkDocs installieren:
    https://www.youtube.com/watch?v=WtKa8a4uv3k
    2.1.1 python installieren       (falls nicht vorhanden)
    2.1.2 MkDocs installieren       (falls nicht vorhanden)
    2.1.3 Docker.io installieren    (falls nicht vorhanden)


schriftlich ->      https://docs.techdox.nz/mkdocs/

Tutorial Video ->   https://www.youtube.com/watch?v=K2RDsWgwDTU

Wofür verwenden wir Mkdocs?
MkDocs wird verwendet, um die Dokumentation für die Glossapp zu erstellen und zu verwalten.
Die Installation erfolgt mithilfe von Pip oder Docker-Compose. In unserem Fall nutzen wir Docker-Compose.


2.2 -> Dockerstarten:
    Docker wird verwendet, um die Glossapp in Containern zu isolieren und zu betreiben.
    Der Docker-Dienst wird mit Docker-Compose gestartet.
    Der Befehl hierzu ist, sofern alles richtig gemacht wurde "sudo docker-compose up -d" im zugehörigen Verzeichnis.