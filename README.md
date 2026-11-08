# DeLorean Cloud – Xbox Cloud Gaming Android App (32-bit)

Xbox Cloud Gaming fürs Handy mit Cover-Liste, Direktstart und Touch-Steuerung.

**Download:** `DeLoreanCloud-32bit.apk` unter **[Releases](../../releases/latest)**

Created by DeLorean23

## Funktionen

- Alle Cloud-Spiele aus dem Xbox Game Pass als Cover-Liste, mit deutschen Namen (öffentlicher Game-Pass-Katalog, Markt Deutschland)
- Suche nach Name, Publisher oder Genre
- Filter „Mit Touch-Steuerung“: zeigt nur Spiele, die ohne Controller mit den Xbox-Tasten auf dem Bildschirm laufen (grünes Abzeichen „Touch“ auf dem Cover)
- Spiel antippen: startet direkt im Stream, im Vollbild und quer
- Lange auf ein Spiel tippen: Infos (Publisher, Genre, Beschreibung, Touch ja/nein)
- Touch-Steuerung kommt von Xbox Cloud Gaming selbst (gleiches Layout wie im Handy-Browser)
- Bluetooth- oder USB-Controller wird an den Stream weitergegeben, die Xbox-Taste öffnet „Stream beenden?“
- Einmal mit dem Microsoft-Konto anmelden (Menü ⋮ → Anmelden / Konto), danach bleibt man angemeldet
- Liste nach unten ziehen oder Menü ⋮ → Liste aktualisieren: neue Spiele laden
- Menü ⋮ → Abmelden: Microsoft-Konto aus der App entfernen

## Voraussetzungen

- Android 5.0 oder neuer, aktuelles Android System WebView (über den Play Store)
- Xbox Game Pass Ultimate

## Installation

1. `DeLoreanCloud-32bit.apk` unter Releases herunterladen.
2. Öffnen und „Installation aus unbekannten Quellen“ erlauben.
3. App starten, einmal mit dem Microsoft-Konto anmelden, Spiel antippen.

Die App enthält keinen nativen Code und läuft auf 32-bit- und 64-bit-Geräten.

## So funktioniert es

- Die Spieleliste kommt aus dem öffentlichen Xbox-Game-Pass-Katalog (`catalog.gamepass.com`). Dafür ist keine Anmeldung nötig. Die Liste wird in der App gespeichert und nach 12 Stunden automatisch erneuert.
- Ein Spiel öffnet die Xbox-Cloud-Gaming-Seite (`xbox.com/play/launch/...`) in der App. Die App meldet sich dabei als Chrome auf dem Handy, damit Xbox Cloud Gaming die Touch-Steuerung anbietet.
- Ein angeschlossener Controller wird der Seite als normaler Gamepad gemeldet.

## APK bauen

Bei jedem Push baut GitHub Actions (Workflow **DeLorean Cloud bauen**) die APK und veröffentlicht sie unter **Releases**.

Android Studio: `gradlew :app:assembleRelease` → `app/build/outputs/apk/release/app-release.apk`

Die APK wird mit dem festen Schlüssel `app/signing.jks` signiert, damit neue Versionen über die alte installiert werden können.

## Hinweise

- Microsoft bietet die Touch-Steuerung nur für einen Teil der Spiele an. Ohne Touch-Unterstützung braucht man einen Controller.
- Xbox und Game Pass sind Marken von Microsoft. Diese App hat nichts mit Microsoft zu tun.
