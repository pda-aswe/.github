# Allgemein
- Alle Services und Use-Cases sollten in einen eigenständigen Repo erstellt werden. Dadurch wird die Wiederverwendbarkeit erhöht.
- Zum Testen eines Services/Use-Cases muss lokal nur der Broker laufen. Dafür muss nur `docker run -it -p 1883:1883 ghcr.io/pda-aswe/broker` ausgeführt werden. Jedoch muss zuvor noch ein Personal Access Token für Github erstellt ist, wie weiter unten zu finden ist.
- Schön wäre es, wenn für jedes Issue ein eigener Branch geöffnet wird der dann nach einen Pull-Request mit main gemerged wird

## Template
Dieses Repo sollte als Grundlage verwendet werden, um weitere Services oder Use-Cases zu erstellen. Weitere Infos im Repo.

## Main
Dieses Repo ist für den Start der Dockercontainer und der Audio Eingabe und Ausgabe zuständig. Auch sollen damit die Präferenzen beim Start eingelesen werden und an alle Container verteilt werden. Weitere Infos im Repo.

## Verbindungsprobleme mit Github Desktop
Falls Github Desktop nicht funktioniert: https://github.com/desktop/desktop/issues/13226#issuecomment-1031096170

## Benötigt, um automatisch erstellte Dockerimages herunterzuladen:
1. Personal Access Token erstellen im eigenen Profil
  - In den Accounteinstellungen > Entwicklereinstellungen > Personal Access Tokens > Tokens (classic)
  - Dort dann einen neuen Token(classic) erstellen. Dieser braucht nur die Berechtigung: read:packages
2. Im Docker Repo anmelden
  In einer Kommandozeile `docker login ghcr.io -u <Gitub Benutzername> --password <Token von Github>` ausführen

# Topics
Eine Liste aller Topics zum Datenaustausch sind in folgender Datei zu finden: https://github.com/pda-aswe/.github/blob/main/Topics.md
