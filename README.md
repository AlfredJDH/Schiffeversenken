# Schiffe versenken

Schiffe versenken fürs Smartphone: allein gegen den Computer oder zu zweit auf zwei Handys. Zu zweit öffnen beide dieselbe Seite, einer startet ein Spiel und schickt dem anderen den Link.

**Spielen:** https://alfredjdh.github.io/Schiffeversenken/

## So geht's

1. Seite öffnen, mit − und + die Anzahl der Schiffe wählen (1 bis 10) und „Neues Spiel starten“.
2. „Link teilen“ antippen und den Link an den Mitspieler schicken. Alternativ öffnet er die Seite und tippt den Code ein.
3. Beide stellen ihre Schiffe selbst auf: Das markierte Schiff landet auf dem Feld, das man antippt, oder man zieht es aus dem Hafen aufs Blatt. Ein gesetztes Schiff lässt sich ziehen (verschieben) und antippen (drehen). „Zufällig“ stellt alles automatisch auf. Dann „Bereit“.
4. Abwechselnd ein Feld antippen und feuern. Bei einem Treffer darf man noch einmal.

Das Spielfeld steht fest auf dem Bildschirm, während des Spiels scrollt nichts. Der Spielstand wird auf dem jeweiligen Handy gespeichert. Seite neu laden oder Handy sperren ist kein Problem, das Spiel verbindet sich wieder.

## Gegen den Computer

Auf der Startseite den Regler „Können des Computers“ einstellen und „Gegen den Computer spielen“ antippen. Es gibt fünf Stufen, vom Leichtmatrosen (schießt planlos) bis zum Admiral (rechnet aus, wo die Schiffe am wahrscheinlichsten liegen). Die Stufe lässt sich vor jeder Partie beim Aufstellen noch ändern. Dieser Modus braucht keine Internetverbindung zum Mitspieler.

## Technik

- Eine einzige Datei: `index.html`, kein Build-Schritt, läuft über GitHub Pages.
- Die beiden Handys verbinden sich direkt miteinander (WebRTC). Den Verbindungsaufbau vermittelt der freie Dienst [PeerJS](https://peerjs.com); die Bibliothek wird beim Öffnen von einem CDN geladen.
- Die eigene Aufstellung verlässt das Handy erst, wenn das Spiel vorbei ist. Ob ein Schuss trifft, entscheidet immer das Gerät des Beschossenen.

## GitHub Pages einschalten

Repository → Settings → Pages → „Deploy from a branch“ → Branch `main`, Ordner `/ (root)` → Save.
