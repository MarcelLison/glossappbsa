# Inhaltsverzeichnis

- [Wo wird die Glossapp gehosted?](#wo-wird-die-glosapp-gehosted)               <!-- Wozu wird die Glossapp gehostet? -->

- [Welche Dienste laufen auf dem Server?](#dienste-glossapp)                           <!-- Welche Dienste laufen auf dem Server? -->

- [Wozu die Dienste benötigt werden und das Zusammenspiel](#wozu-dienste) <!-- Wozu werden die Dienste benötigt? -->

- [Was sollte man wissen, wenn man an der Glossapp weiter arbeiten möchte?"](#was-sollte-man-wissen)  <!-- Was sollte man wissen, wenn man an der Glossapp weiter arbeiten möchte? -->

- [Was gibt es besonders Wichtiges für den Admin/Entwickler zu wissen?](#wichtig-fuer-admins) <!-- Was gibt es besonders wichtiges für den Admin/Entwickler zu wissen?-->

- [Wer ist für was verantwortlich?](#verantwortlichkeit) <!-- Wer ist für was verantwortlich?-->

- [Welche Frameworks/Technologien kommen zum Einsatz?](#technologien-frameworks) <!-- Welche Frameworks/Technologien kommen zum Einsatz-->


# <a name="wo-wird-die-glosapp-gehosted">Wo wird die Glossapp gehosted?</a>

Die Glossapp wird über eine Kombination von Strato und Cloudfare gehosted. Strato wird für das generelle Hosting der Website benutzt, während Cloudflare für die Verwaltung und Sicherheitsoptimierung verwendet wird.

## Generelle Informationen

### Strato (Hosting)
- Webhosting: Strato bietet verschiedene Webhosting-Pakete an, die Speicherplatz, Datenbanken, E-Mail-Konten und andere Funktionen umfassen.
- Server: Die Server von Strato sind in der Regel zuverlässig und bieten eine hohe Verfügbarkeit und gute Performance.
- Support: Strato bietet Kundensupport über verschiedene Kanäle wie Telefon, E-Mail und Live-Chat.

### Cloudflare (DNS und mehr)
- DNS-Verwaltung: Cloudflare bietet eine schnelle und zuverlässige DNS-Verwaltung. Dies bedeutet, dass die DNS-Einträge deiner Domain (wie A, CNAME, MX, etc.) über - Cloudflare verwaltet werden.
- CDN (Content Delivery Network): Cloudflare kann Inhalte über seine globalen Rechenzentren zwischenspeichern und ausliefern, um die Ladezeiten der Website für Besucher weltweit zu reduzieren.
- Sicherheitsfunktionen: Cloudflare bietet eine Reihe von Sicherheitsfunktionen wie DDoS-Schutz, Web Application Firewall (WAF) und SSL/TLS-Verschlüsselung.
- Optimierung: Cloudflare bietet auch Leistungsoptimierungen wie Caching, Minifizierung von CSS/JS und Bildoptimierung.

### Integration der beiden Dienste
1. Domain-Verwaltung: Die DNS-Einträge deiner Domain werden über das Cloudflare-Dashboard verwaltet. Du richtest deine Domain so ein, dass sie auf die IP-Adresse deines Strato-Servers zeigt.
2. Webhosting: Die eigentliche Website (Glossapp) wird auf dem Strato-Server gehostet. Du lädst deine Website-Dateien auf den Strato-Server hoch und richtest dort Datenbanken und andere benötigte Dienste ein.
3. Cloudflare-Einstellungen: In Cloudflare kannst du verschiedene Einstellungen vornehmen, um die Performance und Sicherheit deiner Website zu optimieren. Dies beinhaltet die Aktivierung von SSL, das Einrichten von Page Rules und das Konfigurieren des Caches.
4. Zertifikate: Strato und Cloudflare bieten beide SSL-Zertifikate an. In den meisten Fällen wird ein "Flexible SSL"-Zertifikat von Cloudflare verwendet, um die Verbindung zwischen dem Besucher und Cloudflare zu sichern, während die Verbindung zwischen Cloudflare und deinem Strato-Server unverschlüsselt sein kann. Es ist jedoch sicherer, auch ein SSL-Zertifikat auf deinem Strato-Server einzurichten und "Full SSL" in Cloudflare zu nutzen.

# <a name="dienste-glossapp"> Dienste auf dem Server </a>

## Auf dem Server laufende Dienste:
- Datenbank Admin Lehrer und Schüler Nutzer für Webinterface: https://b11.glossapp.de/

- Datenbank Glossar: https://database-php.glossapp.de/

- gitlab: https://gitlab.glossapp.de/

- Nodered: https://nodered.glossapp.de/

- Portainer: https://services.glossapp.de/

## Externe Dienste:

- Cloudflare: https://dash.cloudflare.com/

- Strato: https://www.strato.de/apps/CustomerService/?sessionID=6b...

- RDF Outlook Glossar & Cloudflare: https://dash.cloudflare.com/

- Traffic Dashboard: URL: https://trafic.glossapp.de/



# <a name="wozu-dienste">Dienste und das Zusammenspiel</a>



## Beschreibung der Dienste

### Zusammenfassung der Rollen und Interaktionen:
- Web- und Datenbankverwaltung: Die Datenbank-Admin-Webinterfaces für Lehrer und Schüler sowie die Datenbank Glossar bieten spezifische Verwaltungsfunktionen für die Benutzer der Glossapp.

- Versionskontrolle und Entwicklungsumgebung: Gitlab und Nodered unterstützen die Entwicklung und Automatisierung von Aufgaben innerhalb der Glossapp.

- Container- und Dienstverwaltung: Portainer und das traefik dashboard ermöglichen die Verwaltung und Überwachung der Container und Netzwerkdienste.

- Externe Dienste für Performance und Sicherheit: Cloudflare und Strato stellen sicher, dass die Glossapp schnell, sicher und zuverlässig erreichbar ist. RDF Outlook Glossar & Cloudflare integriert E-Mail-Verwaltung und Sicherheit.

- Externe Dienste für Performance und Sicherheit

### Cloudflare:
- Interaktion: Cloudflare agiert als CDN und Sicherheitsdienst, der zwischen den Benutzern und den Diensten der Glossapp sitzt. Es verteilt den Datenverkehr, schützt vor DDoS-Angriffen und bietet eine Web Application Firewall (WAF).

- Nutzung von: Traefik zur Sicherstellung einer effizienten Weiterleitung des Datenverkehrs.

## Strato:
- Interaktion: Strato stellt die physische Infrastruktur und das Hosting für die Glossapp bereit. Alle Dienste laufen auf Strato-Servern.

- Nutzung von: Cloudflare für zusätzliche Sicherheits- und Performance-Dienste.

                                        
# <a name="was-sollte-man-wissen">Was sollte man wissen, wenn man an der Glossapp weiter arbeiten möchte?</a>

## Was sollte man wissen, wenn man an der Glossapp weiterarbeiten möchte?

- Technologie-Stack: Kenntnisse über die verwendeten Technologien und Frameworks (z.B., Docusaurus, Docker).

- Code-Struktur: Verstehen der Projektstruktur und des Codes.

- Deployment-Prozess: Verstehen, wie die Anwendung und die Dokumentation deployt werden.

- Zugriffsrechte: Wissen über Benutzer- und Zugriffsrechte auf dem Server.

<!-- 
Um an der Glossapp weiterzuarbeiten,
solltest du die verwendeten Technologien und Frameworks verstehen
sowie Zugang zu den entsprechenden Quellcode- und Konfigurationsdateien haben. 
Als Einstieg sollte man das gitlab Repository eingehend studieren. Ein Blick auf die Wiki sollte auch weiterhelfen.
Ansonsten bei dem Vorgänger Jahrgang und/oder bei Kommilitonen
nachfragen.

-->

# <a name="">Wissenswertes Glossapp
Was sollte man wissen, wenn man an der Glossapp weiterarbeiten möchte?
Technologie-Stack: Kenntnisse über die verwendeten Technologien und Frameworks (z.B., Docusaurus, Docker).

Code-Struktur: Verstehen der Projektstruktur und des Codes.

Deployment-Prozess: Verstehen, wie die Anwendung und die Dokumentation deployt werden.

Zugriffsrechte: Wissen über Benutzer- und Zugriffsrechte auf dem Server.

URL: [Glossapp Repository](#https://gitlab.glossapp.de/)

# <a name="wichtig-fuer-admins">Was gibt es besonders Wichtiges für Admin/Entwickler zu wissen?</a>

- Verwalten von Zugangsdaten/Berechtigungen 
- Backup & Wiederherstellungsverfahren sollten ihm bekannt sein.

# <a name="verantwortlichkeit">Wer ist für was verantwortlich?</a>

Die Verantwortlichkeiten und die Rollen der Projektteilnehmer werden in einem Meeting definiert. Im Gespräch wird ein fiktiver Kunde Anforderungen an die Glossapp stellen, mit deren Hilfe dann die Features abgeleitet werden. Es werden sicherlich Rollen und/oder Aufgaben vorhanden sein wie 

- Entwicklung
- Administration
- Datenbankentwickler
- Erstellen bzw. Aktualisieren der Dokumentation
- Projektleitung/Teilprojektleitung

Eine grobe Einteilung könnte in etwas wie folgt aussehen:

| Name, Vorname | Funktion/Rolle | 
|----------|---------- |
| Nouri, Milad   | Entwicklung   |
| X  | Y   |

| Feature | Verwantwortlichkeit | zu erledigen bis | 
|----------|---------- | ---------- |
| Konzept für ein besseres "Look and Feel" Startseite Glossapp   | Nouri, Milad   | 15.07.2024
| X  | Y   | Z

# <a name="technologien-frameworks">Welche Technologien/Frameworks kommen zum Einsatz?</a>

## Verwendung von Svelte im Glossapp-Projekt
### Einleitung
- Svelte ist ein modernes JavaScript-Framework, das für den Aufbau von reaktiven Benutzeroberflächen verwendet wird. Im Gegensatz zu traditionellen Frameworks wie React oder Vue, die die meisten ihrer Arbeit zur Laufzeit im Browser erledigen, führt Svelte den größten Teil der Arbeit zur Kompilierungszeit durch.

### Vorteile von Svelte
- Performanz: Da Svelte die Anwendungen zu hochoptimiertem JavaScript kompiliert, sind die resultierenden Anwendungen in der Regel schneller und benötigen weniger Ressourcen.

- Einfachheit: Svelte hat eine einfachere und verständlichere Syntax, was die Entwicklung von Anwendungen beschleunigt und erleichtert.

- Kompilierung: Durch die Kompilierung zur Build-Zeit wird die Laufzeitbelastung verringert, was zu schneller ladenden Anwendungen führt.

- Verwendung im Glossapp-Projekt Svelte wird in der Glossapp für die Erstellung der Benutzeroberfläche verwendet.

### Weitere Informationen
[Svelte Kit](https://svelte.dev/)



<!-- 
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


<!-- 
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
-->
