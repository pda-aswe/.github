# List aller benötigten Topics

Im Allgemeinen haben die Use-Cases keine eigenen Topics. Sie arbeitet nämlich hauptsächlich mit den Topics von TTS & SST und den verwendeten Services.

## Präferenzen
- `pref/<Name der Präferenz>`: Dadurch wird die Präferenz die im Topic angegeben wird an alle Teilnehmer verschickt
- `req/pref/all` oder `req/pref/<Name der Präferenz>`: Damit wird eine Präferenz oder alle Präferenzen angefordert. Die angeforderte Präferenz wird mit dem Topic pref/* zurückgeschickt.

## TTS / STT
- `tts`: Wird verschickt mit dem Text, welcher per Sprache ausgegeben werden soll
- `stt`: Wird versickt mit dem Text, welcher durch die Spracherekennung ausgelesen wurde

### Wetter-Api
- `weather/now`: Enthält das aktuelle Wetter.
- `req/weather/now`: Damit wird das aktuelle Wetter abgefragt. Antwort mit dem Topic `weather/now`.
- `req/weather/<Datum>/<Uhrzeit>`: Anfrage für das Wetter zu einer bestimmten Uhrzeit. Antwort mit dem Topic `weather/<Tag>/<Uhrzeit>`
- `weather/<Datum>/<Uhrzeit>`: Gibt das Wetter für eine bestimmte Uhrzeit bekannt.

### Verhkehrs-Api
- `rideTime/<Latitude>/<longitude>`: Gibt die Fahrzeit zur GPS-Koordinate an. Angabe der Fahrzeit zu fuß, mit Auto, Fahrrad oder öffentlichen Verkehrsmitteln.
- `req/rideTime/<Latitude>/<longitude>`: Anfrage für die Berechnung der Fahrtzeit. Antwort mit dem Topic `rideTime/<Latitude>/<longitude>`

### Kalender-Api
- `appointment/create`: Erstellt einen Termin im Kalender. Datenformat durch Entwickler noch zu definieren.
- `appointment/now`: Gibt den aktuellen Termin aus.
- `req/appointment/<Datum des Termins>`: Damit werden alle Termine für einen Tag angefordert. Termine des Tags unter `appointment/<Datum der Termine>` zurückschicken.
- `appointment/<Datum der Termine>`: Alle Termine von diesen Tag werden hiermit versendet. 

### News-Apis
- `news/<Publisher-ID>/article`: Enthält einen Nachrichtenartikel. Artikel sollte Titel, Kurzbeschreibung und ausführlichen Artikel enthalten.
- `req/news/<Anzahl der Artikel>`: Anfrage für eine bestimmte Anzahl von Artikel. Jeder Artikel sollte einzeln mit dem Topic `news/article` versendet werden.

### Location/Bluetooth-Api
- `location/current`: Enthält die aktuelle GPS Koordinate
- `req/location/current`: Anfrage für die aktuelle GPS Koordinate. Antwort mit dem Topic `location/current`.
- `car/connected`: Enthält den Status, ob eine Verbindung zum Auto vorhanden ist.
- `req/car/connected`: Anfrage ob, eine Verbindung zum Auto vorhanden ist. Antwort mit dem Topic `car/connected`.

### Bundesliga-Api
- `sport/next`: Ausgabe des nächsten Spiels des hinterlegten Vereins. Angabe der Sportart sollte enthalten sein.
- `req/sport/next`: Anfrage für den nächsten Spieltermin. Versenden mit dem Topic `sport/next`.
- `sport/result`: Ausgabe des letzten Spielergebnisses.
- `req/sport/result`: Anfrage für das letzte Spielergebniss bzw. aktuelle Ergebnis. Versenden mit dem Topic `sport/result`.

### Football-Api
- `sport/next`: Ausgabe des nächsten Spiels des hinterlegten Vereins. Angabe der Sportart sollte enthalten sein.
- `req/sport/next`: Anfrage für den nächsten Spieltermin. Versenden mit dem Topic `sport/next`.
- `sport/result`: Ausgabe des letzten Spielergebnisses.
- `req/sport/result`: Anfrage für das letzte Spielergebniss bzw. aktuelle Ergebnis. Versenden mit dem Topic `sport/result`.

### Preisvergleich-Api
- `price/current`: Ausgabe des aktuellen Artikelpreis.
- `req/price`: Anfrage für einen Artikelpreis. Versenden mit dem Topic `price/current`.

### E-Mail-Api
- `mail/create`: Erstellt eine E-Mail die automatisch verschickt wird. Der Betreff und der Text werden innerhalb der Nachricht festgelegt. Format muss durch Entwickler noch definiert werden.
