# Lock&Loot Legal

Statische Rechtstexte für die Android-App **Lock&Loot** (`de.lockandloot.app`), gehostet über GitHub Pages.

## Inhalt

- [`privacy-policy/index.html`](privacy-policy/index.html) — Datenschutzerklärung (Deutsch, Hauptseite)
- [`privacy-policy/en.html`](privacy-policy/en.html) — Privacy Policy (English)
- [`privacy-policy/style.css`](privacy-policy/style.css) — Styling (wird von beiden Bereichen genutzt)
- [`account-deletion/index.html`](account-deletion/index.html) — Konto und Daten löschen (Deutsch)
- [`account-deletion/en.html`](account-deletion/en.html) — Delete Account and Data (English)

## Veröffentlichen mit GitHub Pages

1. Dieses Repository nach GitHub pushen (`Jerdna3/lockandloot-legal`).
2. Im GitHub-Repo: **Settings → Pages**.
3. Unter **Build and deployment**:
   - **Source**: „Deploy from a branch“
   - **Branch**: `main`, Ordner **`/ (root)`**
4. Nach dem Deploy sind die Seiten erreichbar unter:

   - Datenschutz DE: `https://jerdna3.github.io/lockandloot-legal/privacy-policy/`
   - Datenschutz EN: `https://jerdna3.github.io/lockandloot-legal/privacy-policy/en.html`
   - Kontolöschung DE: `https://jerdna3.github.io/lockandloot-legal/account-deletion/`
   - Kontolöschung EN: `https://jerdna3.github.io/lockandloot-legal/account-deletion/en.html`

## URLs in der Google Play Console eintragen

**App-Inhalte → Datenschutzerklärung:**

```
https://jerdna3.github.io/lockandloot-legal/privacy-policy/
```

**App-Inhalte → Datenlöschung** (Pflicht, weil die App Kontoerstellung anbietet) —
„Nutzer können die Löschung ihres Kontos beantragen“ + diese URL:

```
https://jerdna3.github.io/lockandloot-legal/account-deletion/
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

Die Aufbewahrungsfristen auf beiden Seiten stammen aus dem Server-Code und müssen mitgezogen werden,
wenn sich dort etwas ändert:

- Kampfberichte: 30 Tage (`AttackSubmitHandler.BATTLE_EXPIRY_SEC`)
- Transfereinträge: 31 Tage (`TransferHandler.EXPIRY_SEC`)

Die Lösch-Seite beschreibt außerdem den In-App-Weg (Profil → „Account löschen“, `PlayerDeleteHandler`)
inklusive der Clan-Sperre — auch das anpassen, wenn sich der Ablauf ändert.
