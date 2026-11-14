# MSFS Airport Scout — Live-Version

Web-Tool zum Filtern und Routenplanen fuer den Microsoft Flight Simulator (MSFS 2020), gehostet als GitHub-Pages-Version: https://z33r0-one.github.io/Airport-Scout/ Der Scout verarbeitet 36.779 Flughafenplaetze weltweit (MakeRwys-Scan der eigenen Installation plus OurAirports, Qualitaetsstufen AI Generated, Asobo, 3rd-Party) mit Route-Modi, SimBrief-Anbindung, Wetter-Layern und Flughistorie. Funktionsstand ist identisch mit der Desktop-Einzeldatei aus dem Repo airport-scout-desktop.

## Anwendung

Im Browser oeffnen, Filter setzen, Route waehlen, Ergebnis antippen. Ein Service Worker legt alle Dateien beim ersten Besuch im Geraetecache ab; danach laeuft die Seite auch offline. Nach jedem Update der Live-Version muss die Seite einmal neu geladen werden, damit der Service Worker die neue Versionsnummer (asc-…) uebernimmt. Einstellungen bleiben lokal im Browser (localStorage), lassen sich aber ueber die 💾-Funktion exportieren und auf anderen Geraeten importieren. Nur die optionalen Wetter-Layer (Regen NASA GPM IMERG, Wind Open-Meteo GFS 250 hPa) benoetigen Netz.

## Aufbau dieses Repositories

- index.html — Anwendung (Laufzeit-Code, identisch mit dem Template der Desktop-Version).
- d0.js, ap0-4.js, rw0-4.js, dem0-7.js, deme0-3.js, g0-1.js — Datenbasis in 25 kleinen Dateien (Flughafen, Pisten, Hoehenraester, Geometrien), aendern sich nicht.
- sw.js — Service Worker mit Versionsstand; bei jedem Update wird die Versionsnummer erhoeht.
- mockup.html — frueherer Layout-Entwurf (Archiv).

## Mobile Layout

Die Seite folgt festen Prinzipien der Touchbedienung: bildschirmbreit, kein horizontales Scrollen, inhaltlich getrennte und farblich abgesetzte Bereiche. Die Reihenfolge ist Kopfzeile mit ☰-Filter, Karte, Route-Modus-Buttons (aus, ab Start, aus Paaren, Weltumrundung), die zum Modus passenden Optionen, darunter die Ergebnisliste mit mehr als halber Bildschirmhoehe. Nur Kernspalten, Abstände und Schriftgroessen sind auf Daumenbedienung ausgelegt; der Rest der Seite ist neutraler Bildlaufbereich ohne verdeckte Bedienelemente.

## Desktop-Version

Die komplette Anwendung als eine 26 MB grosse HTML-Datei fuer die Nutzung direkt vom Dateisystem (Doppelklick, file://, komplett offline) liegt im Repo airport-scout-desktop; dort befinden sich auch Quellcode, Build und automatische Pruefungen.

## Projektstand und Roadmap

Stand November 2026 (Version asc-2026-11-15b): Filter, Kategorien mit Packages-Import, alle vier Route-Modi, SimBrief, Wetter-Layer, Flughistorie und die mobile Layout-Restrukturierung sind fertig. Roadmap: gefuehrter Filter-Fragebogen, der die haeufigsten Filter als einfache Ja/Nein-Abfragen nacheinander abfragt.

## Rechte

Alle Inhalte dieses Repositories sind geistiges Eigentum des Autors. Es ist keine Open-Source-Lizenz erteilt; Nutzung, Veroeffentlichung oder Weitergabe ausserhalb dieses Repositories nur mit ausdruecklicher Zustimmung des Autors.