# sortobot-site

Die zwei Pflichtseiten für die Veröffentlichung von **Sortobot** im App
Store und bei Google Play, plus eine Startseite. Statisches HTML: kein
Skript, kein Cookie, keine externe Ressource, kein Build-Schritt.

| Datei | Wofür |
| --- | --- |
| `support.html` | Support-URL (App Store Connect) und Kontaktdaten (Play). Enthält das **Impressum** als eigenen Abschnitt. |
| `privacy.html` | Datenschutz-URL (beide Konsolen). |
| `index.html` | Startseite, verlinkt beide. |

Live über GitHub Pages:

- https://goateeavengers.github.io/sortobot-site/support.html
- https://goateeavengers.github.io/sortobot-site/privacy.html

Dieselben URLs stehen in der App (`lib/config/legal_links.dart` im
Hauptrepo) und in beiden Store-Konsolen — die drei müssen übereinstimmen.

## Ändern

**Die Quelle ist das Hauptrepo**, nicht dieses hier: `store/web/` in
`GoateeAvengers/sortobot`. Dort liegen die Dateien neben der
Datenschutz-Dokumentation (`store/PRIVACY.md`) und den Konsolen-Vorlagen,
die dieselben Aussagen treffen. Also dort ändern, dann hierher kopieren:

```sh
cp ../sortobot/store/web/{support.html,privacy.html,index.html} .
git commit -am "Update legal pages" && git push
```

Pages baut selbst neu, das dauert ein bis zwei Minuten.

© 2026 Goatee Avengers UG (haftungsbeschränkt)
