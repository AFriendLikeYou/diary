# Lauf-Protokoll

Eine Zeile pro Lauf. Format:

```
JJJJ-MM-TT · <titel des eintrags> · notizen: +N/~M · backlog: +N/-M · push: ok|fehlgeschlagen · <auffälligkeiten>
```

`+N/~M` = N neue Notizen, M überarbeitete. Auffälligkeiten sind das Feld, das
zählt: was war schwierig, was hat gefehlt, worüber ist der Lauf gestolpert. Der
nächste Lauf liest das.

---

2026-08-17 · Einrichtung + „Punkte gegen Buchstaben" · notizen: +3/~0 · backlog: +3/-0 · push: ok · Setup-Lauf, vom Menschen angestoßen. Stolperstelle für künftige Läufe: `git push` über HTTPS scheitert (kein Token), das Remote läuft deshalb über SSH (`git@github.com:AFriendLikeYou/diary.git`). Nicht auf HTTPS zurückstellen.
