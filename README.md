# Live-Preischeck

Android-App für Whatnot-Livestreams. Eine schwebende **€-Taste** liegt über der Whatnot-App.
Ein Tipp darauf fotografiert den laufenden Stream, Claude erkennt den Artikel und das aktuelle Gebot
und blendet ein:

- Marktpreis-Spanne (ab / typisch / bis) in Euro, ohne Versand
- Bewertung des aktuellen Gebots inkl. Versand: Günstig / Fairer Preis / Zu teuer
- **Bis hierhin mitbieten**: typischer Preis minus Abschlag minus Versand
- Worauf man achten sollte und wie sicher die Schätzung ist
- Ein Tipp öffnet eBay.de *verkaufte Artikel* oder Kleinanzeigen mit passendem Suchbegriff

Die Preise sind eine KI-Schätzung, keine Live-Daten von eBay. Bei teuren Käufen mit „eBay verkauft“ gegenprüfen.

## Was du brauchst

1. **Android 10 oder neuer**
2. **Einen Anthropic-API-Schlüssel**: auf https://console.anthropic.com anmelden, unter *Billing* etwas Guthaben aufladen (z. B. 5 $),
   dann unter *API Keys* einen Schlüssel erstellen. Eine Abfrage kostet mit dem voreingestellten schnellen Modell nur Bruchteile eines Cents.

## Installation

1. Auf dem Handy die Seite **Releases** dieses Repositorys öffnen und `Live-Preischeck.apk` herunterladen.
2. Die Datei antippen. Android fragt, ob der Browser Apps installieren darf: erlauben, dann installieren.
3. Bei einem Update die alte Version vorher deinstallieren, falls Android „App nicht installiert“ meldet.

## Benutzung

1. App öffnen, API-Schlüssel einfügen, Versand und Abschlag einstellen.
2. **Starten** tippen und erlauben:
   - „Über anderen Apps einblenden“ (einmalig, in den Einstellungen)
   - Benachrichtigungen (darüber beendest du die Taste)
   - Bildschirmaufnahme (bei jedem Start; wähle „Gesamter Bildschirm“ oder die Whatnot-App)
3. Whatnot öffnen. Die rote €-Taste lässt sich verschieben.
4. Sobald der Artikel eingeblendet ist, auf **€** tippen.
5. Beenden über die Benachrichtigung oder in der App.

## Selbst bauen

Jeder Push auf `main` baut die APK automatisch über GitHub Actions und legt sie als Release ab.
Lokal: Android Studio öffnen oder `gradle assembleDebug` mit installiertem Android-SDK.
