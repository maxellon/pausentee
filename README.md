# Pausentee

VfB-Tipprunde fürs Kollegium: https://maxellon.github.io/pausentee/

Die Daten liegen in derselben Firebase-Datenbank wie das Foto-Quiz und die JGA-App (Projekt `quiz-de-titte`, Knoten `pausentee`). Die Datenbankregeln werden im Repository `jga-ferdi` gepflegt (`database.rules.json`).

- **Daten:** Spielplan, Anstoßzeiten, Stadion, Live-Stand, Endergebnis, Aufstellung, Tabellen und Wappen kommen von der offenen ESPN-Schnittstelle (Bundesliga, DFB-Pokal, Europapokal; Testspiele werden ignoriert). Das erste Handy, das nach Abpfiff die App offen hat, schreibt das Ergebnis in die Datenbank, ab dann sehen alle dasselbe.
- **Anmeldung:** VfB-Legende als Spitzname (jede nur einmal), freiwillig Vorname, vierstellige PIN für weitere Geräte. Schutz gegen Zufall, keine echte Sicherheit.
- **Punkte:** Tendenz 2, Tordifferenz 1, VfB-Tore 1, Gegentore 1 (exakt = 5). Joker einmal pro Hinrunde (Juli bis Dezember) und Rückrunde (Januar bis Juni), doppelte Punkte. Gleichstand: mehr exakte Tipps. Endstand nach Verlängerung, ohne Elfmeterschießen. Gewertet wird ab dem 25.11.2026 (`START` oben im Script), Nachzügler starten bei 0.
- **Reiter:** Spiele (Countdown, Tippen, Joker, wer noch fehlt mit WhatsApp-Erinnerung, Live mit vorläufigen Punkten, gespielte Spiele mit allen Tipps), Tabelle (Pfeile, 🏆 👑 🥒 🏮, Punkte im letzten Spiel je Person, Tippverlauf, Optimisten und Schwarzseher), Spieler (Top 3 des Spiels nach Abpfiff bis zum nächsten Anpfiff, 3-2-1, Spieler der Saison), Wettbewerb (Tabelle des aktuellen Wettbewerbs, beim Pokal die Runde), Mehr (Regeln, Einladen, Admin).
- **Admin:** Unter Mehr → Admin. Wer den Code zuerst festlegt, ist Admin. Notfall-Knopf für Ergebnisse (von Hand hat Vorrang, „Automatik“ gibt zurück), PIN zurücksetzen, Teilnehmer löschen.
- Tipps der anderen werden erst ab Anpfiff angezeigt. Wer sich in der Datenbank auskennt, könnte sie vorher lesen.
