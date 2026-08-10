# Lock&Loot Legal

Statische Rechtstexte für die Android-App **Lock&Loot** (`de.lockandloot.app`), gehostet über GitHub Pages.

## Inhalt

- [`privacy-policy/index.html`](privacy-policy/index.html) — Datenschutzerklärung (Deutsch, Hauptseite)
- [`privacy-policy/en.html`](privacy-policy/en.html) — Privacy Policy (English)
- [`privacy-policy/style.css`](privacy-policy/style.css) — Styling

## Veröffentlichen mit GitHub Pages

1. Dieses Repository nach GitHub pushen (`Jerdna3/lockandloot-legal`).
2. Im GitHub-Repo: **Settings → Pages**.
3. Unter **Build and deployment**:
   - **Source**: „Deploy from a branch“
   - **Branch**: `main`, Ordner **`/ (root)`**
4. Nach dem Deploy ist die Seite erreichbar unter:

   - Deutsch: `https://jerdna3.github.io/lockandloot-legal/privacy-policy/`
   - Englisch: `https://jerdna3.github.io/lockandloot-legal/privacy-policy/en.html`

## URL in der Google Play Console eintragen

In der Play Console unter **App-Inhalte → Datenschutzerklärung** diese URL eintragen:

```
https://jerdna3.github.io/lockandloot-legal/privacy-policy/
```

## Bei Änderungen

- Inhalt in `index.html` **und** `en.html` anpassen (beide Sprachen synchron halten).
- Das Datum „Zuletzt aktualisiert“ / „Last updated“ in beiden Dateien aktualisieren.
- Committen und pushen — GitHub Pages veröffentlicht automatisch neu.

## Wann die Erklärung angepasst werden muss

Die Erklärung beschreibt den Stand der App (v0.11.x): Firebase Auth mit **Pflicht-Google-Login**
(anonyme Konten sind abgeschafft, Commit `bd23c40`),
Cloud Firestore (europe-west3), Chat, Usage-Access nur für Bildschirm-Ereignisse, keine Werbung/Analytics.
Anpassen, wenn sich daran etwas ändert — insbesondere bei:

- Einführung von **Google Play Billing** (Abo/Käufe) → eigener Abschnitt nötig
- Einbau von Analytics/Crashlytics oder Werbung
- Wechsel der Server-Region oder des Backends
