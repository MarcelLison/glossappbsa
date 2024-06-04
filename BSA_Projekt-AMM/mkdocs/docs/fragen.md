
---
**Info zum Server:**
---

`10.76.31.238`

`Password: bsa`




- Aktualisierung mit erstem Befehl die Listen der verfügbaren Pakete und der zweite Befehl installiert alle verfügbaren Paketupdates.

`sudo apt-get update && sudo apt-get upgrade`

- MkDocs installieren:

    `[Video ] (https://www.youtube.com/watch?v=WtKa8a4uv3k)`

  2.1.1 python installiert
  2.1.2 MkDocs installiert
  2.1.3 Docker.io installiert 


`[schriftlich](https://docs.techdox.nz/mkdocs/)`


`[Tutorial Video]   (https://www.youtube.com/watch?v=K2RDsWgwDTU)`



- inet 10.76.31.238/20 metric 100 brd 10.76.31.255 scope global dynamic ens18

2.  Dockerstarten:

`bsa@bsa-u22-server:~/mkdocs$ sudo docker-compose up -d`

##Fragen:
---
1. Wo wird die Glossapp gehostet.
2. Welche Dienste laufen auf dem Server?
3. Wozu werden die Dienste benötigt?
4. Wie greifen die Dienste ineinander?
5. Was sollte man wissen wenn man an der Glossapp weiter arbeiten möchte?
6. Was gibt es besonders wichtiges für den Admin/Entwickler zu wissen?
7. Wer ist für was verantwortlich?
8. Welche Frameworks/Technologien kommen zum Einsatz?
---



##1. Wie finde ich, wo die Glossapp gehostet wird?

    "Hostname" ->
    bsa@bsa-u22-server:~$ hostname
    bsa-u22-server
    bsa@bsa-u22-server:~$ hostname -I
    10.76.31.238 172.17.0.1 172.19.0.1 172.18.0.1
    bsa@bsa-u22-server:~$

##2. Welche Dienste laufen auf dem Server?

    systemctl list-units --type=service
->

##3. Wozu werde die Dienste benötigt?

   Funktion der Dienste -> Name der Dienste und nach Funktion rechachieren.

##4. Wie greifen die Dienste ineinander?

   docker.service und containerd.service:
   Der Docker-Dienst steuert die Docker-Engine -> arbeitet mit "containerd" zusammen, um Container zu erstellen, auszuführen und zu verwalten.


##5. Was sollte man wissen wenn man an der Glossapp weiter arbeiten möchte?

Um an der Glossapp weiterzuarbeiten,
solltest du die verwendeten Technologien und Frameworks verstehen
sowie Zugang zu den entsprechenden Quellcode- und Konfigurationsdateien haben.

##6. Ein Admin benötigt Infos wie,
Zugangsdaten, welche Berechtigungen ihm zugewiesen sind, Backup & Wiederherstellungsverfahren sollten ihm bekannt sein.

##7. Die Verantwortlichkeit auf einem Server ist im Normalfall so geregelt

Die Verantwortlichkeiten können je nach Organisation variieren.
Admins sind oft für die Wartung und Sicherheit des Servers verantwortlich,
während Entwickler für die Entwicklung und Wartung der Anwendungen zuständig sind.

##8. Welche Frameworks/Technologien kommen zum Einsatz?
base-files
base-passwd
bash
bsdutils
dash
diffutils
docker-compose
docker.io
findutils
git
grep
grub-pc
gzip
hostname
init
libdebconfclient0
libflashrom1
libftdi1-2
linux-generic
login
mkdocs
ncurses-bin
openssh-server
python3-pip
python3.10-venv
qemu-guest-agent
sysvinit-utils
ubuntu-minimal
ubuntu-server
ubuntu-server-minimal
ubuntu-standard
