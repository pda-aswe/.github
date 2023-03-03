Falls Github Desktop nicht funktioniert: https://github.com/desktop/desktop/issues/13226#issuecomment-1031096170


## Benötigt, um automatisch erstellte Dockercontainer herunterzuladen:
1. Personal Access Token erstellen im eigenen Profil
  - In den Accounteinstellungen > Entwicklereinstellungen > Personal Access Tokens > Tokens (classic)
  - Dort dann einen neuen Token(classic) erstellen. Dieser braucht nur die Berechtigung: read:packages
2. Im Docker Repo anmelden
  In einer Kommandozeile `docker login ghcr.io -u <Gitub Benutzername> --password <Token von Github>` ausführen
