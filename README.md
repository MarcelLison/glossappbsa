https://github.com/MarcelLison/BSA_Projekt
Info zum Server:

inet 10.76.31.238/20 metric 100 brd 10.76.31.255 scope global dynamic ens18
Password: (Wird vom Administrator vergeben. ggf. Lehrkraft anfragen)


Wie Fange ich an?
1.
Aktualisierung mit erstem Befehl die Listen der verfügbaren Pakete und der zweite Befehl installiert alle verfügbaren Paketupdates.

"sudo apt-get update && sudo apt-get upgrade"

1.1 (Optional) SSH - keygen
ssh-keygen -o -a 100 -t ed25519
    ->ssh-keygen: Befehl zum erstellen von SSH-Key

2.MkDocs installieren:
    https://www.youtube.com/watch?v=WtKa8a4uv3k

    2.1.1 python installieren       (falls nicht vorhanden)
    2.1.2 MkDocs installieren       (falls nicht vorhanden)
    2.1.3 Docker.io installieren    (falls nicht vorhanden)


schriftlich ->      https://docs.techdox.nz/mkdocs/

Tutorial Video ->   https://www.youtube.com/watch?v=K2RDsWgwDTU


2.2 -> Dockerstarten:
    Der Docker-Dienst wird mit Docker-Compose gestartet.
    Der Befehl hierzu ist, sofern alles richtig gemacht wurde "sudo docker-compose up -d"



