# M300 Dokumentation
Bessere Ansicht auf meiner [Github Page](https://0xah.github.io/M300/)
## Lernthemen
### Vagrant
Vagrant init: eigenes Vagrant file initialiseren

Vagrant up: startet VM's aus Vagrantfile

Vagrant halt: stopt VM's

Vagrant destroy: zerstört VM's

Vagrant ssh [vmname]: Verbindet per ssh auf VM

### Versionsverwaltung / GIT
git add -A : Änderungen im aktuellen Verzeichnis zum Zwischenspeicher hinzufügen

git commit : Änderungen auf dem lokalen Git speichern

git push : Lokales Git auf Github synchronisieren

git clone : Github Repo herunterladen

git init : Repo initialisieren

### Docker
docker run
* Startet ein Container, das Startverhalten des Containers kann angepasst werden wie was für ein Kommando ausgeführt oder welches Verzeichnis vom Host geshared werden soll.

docker run -d
* Startet einen Container im Hintergrund

docker run -it {container} /bin/bash
* Startet einen Contianer mit einer Shell der sich nicht direkt beendet, weil eine Bash gestartet wird.

docker ps -a
* Zeigt alle Container an

docker images
* Zeigt alle lokal gespeicherten Images

docker rm {id, name}
* Entfernt Container

docker rmi {Name}
* Docker Images entfernen

docker start/stop/kill
* Startet, stoppt oder erzwingt einen stop auf einen Container.



## Lernschritte
Ich interessiere mich für Ansible und versuche meine Vagrant VM's damit zu provisionieren und eine Loadbalancer Webserver Umgebung zu starten. Allerdings sind im Internet dafür keine wirklich brauchbaren Beispiele. Darum versuche ich dies einfach selber aus den verschiedenen Versionen zusammenzukonfigurieren.
Am schwierigsten finde ich die Loadbalancer im Ansible vollständig zu deklarieren.

## Dockerumgebung
### K3
Ich möchte mehrere Container bereitstellen:
MariaDB Datenbank
Nextcloud

Die Datenbank dient als Backend für den Nextcloud Share. Beide erhalten ein vom Host bereitgestelltes Presistant Storage.
### K4
Für die Überwachung der Container richte ich Prometheus und CAdvisor ein. Damit könne die Lasten der einzelnen Container auf einem Webfrontend eingesehen werden.
