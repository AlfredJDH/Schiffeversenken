# Schiffe versenken

Schiffe versenken für zwei Smartphones. Beide öffnen dieselbe Seite, einer startet ein Spiel und schickt dem anderen den Link.

**Spielen:** https://alfredjdh.github.io/Schiffeversenken/

## So geht's

1. Seite öffnen, Flotte wählen (klassisch mit 10 Schiffen oder kurz mit 5) und „Neues Spiel starten“.
2. „Link teilen“ antippen und den Link an den Mitspieler schicken. Alternativ öffnet er die Seite und tippt den Code ein.
3. Beide stellen ihre Schiffe auf: ziehen zum Verschieben, antippen zum Drehen. Dann „Bereit“.
4. Abwechselnd ein Feld antippen und feuern. Bei einem Treffer darf man noch einmal.

Der Spielstand wird auf dem jeweiligen Handy gespeichert. Seite neu laden oder Handy sperren ist kein Problem, das Spiel verbindet sich wieder.

## Technik

- Eine einzige Datei: `index.html`, kein Build-Schritt, läuft über GitHub Pages.
- Die beiden Handys verbinden sich direkt miteinander (WebRTC). Den Verbindungsaufbau vermittelt der freie Dienst [PeerJS](https://peerjs.com); die Bibliothek wird beim Öffnen von einem CDN geladen.
- Die eigene Aufstellung verlässt das Handy erst, wenn das Spiel vorbei ist. Ob ein Schuss trifft, entscheidet immer das Gerät des Beschossenen.

## GitHub Pages einschalten

Repository → Settings → Pages → „Deploy from a branch“ → Branch `main`, Ordner `/ (root)` → Save.
