
# Familienapp Leni – Technische Architektur

## 1. Ziel

Die Familienapp Leni ist eine gemeinsame, transparente und sichere PWA zur Organisation aller Angelegenheiten rund um Leni.

Sie wird von zwei gleichberechtigten Elternteilen genutzt: Matthias und Natalie.

## 2. Grundprinzipien

- Beide Eltern haben gleichberechtigten Zugriff auf die Familiendaten.
- Die Anwendung bleibt kostenlos nutzbar.
- Der Quellcode ist öffentlich einsehbar.
- Persönliche Daten bleiben geschützt.
- Keine einseitigen Entscheidungen über gemeinsame Familiendaten.
- Änderungen müssen nachvollziehbar sein.
- Die Anwendung bleibt neutral und organisatorisch.

## 3. Technische Trennung

### GitHub
Öffentliches Repository für:
- Programmcode
- Datenbankstruktur und Migrationen
- Sicherheitsregeln
- Technische Dokumentation
- Versionshistorie

### Supabase
Private Speicherung von:
- Benutzerkonten
- Familiendaten
- Kosten und Belegen
- Kalenderdaten
- Aufgaben und Übergaben

### Geheimnisse und Zugangsdaten
- Passwörter und API-Schlüssel werden niemals im Repository gespeichert.
- Zugangsdaten werden über geschützte Umgebungsvariablen verwaltet.
- Keine echten Familiendaten in Testdateien oder Beispielen.

## 4. Benutzer und Berechtigungen

- Genau zwei Elternkonten in Version 1.0.
- Beide Eltern sind gleichberechtigte Familienmitglieder.
- Matthias erstellt die Familie und lädt Natalie ein.
- Nach Annahme der Einladung haben beide dieselben Rechte.
- Ausschließlich angemeldete Familienmitglieder dürfen auf Familiendaten zugreifen.

## 5. Funktionsbereiche

- Dashboard
- Kosten und Belege
- Gemeinsamer Kalender
- Aufgaben
- Übergaben
- Besondere Familientage
- Einstellungen und Datenschutz

## 6. Datenschutz und Sicherheit

- Supabase Row Level Security (RLS) für alle relevanten Daten.
- Zugriff nur für authentifizierte Mitglieder der jeweiligen Familie.
- Keine öffentlichen Datenbankzugriffe auf private Familiendaten.
- Nachvollziehbare Änderungen und Löschvorgänge.
- Sicherungen und Wiederherstellungsmöglichkeiten.
- Datenexport für beide Eltern.

## 7. Entwicklung und Änderungen

- Entwicklung mit GitHub.
- Neue Funktionen werden möglichst in separaten Branches entwickelt.
- Änderungen werden über Pull Requests dokumentiert.
- Beide Eltern können Änderungen vorschlagen und prüfen.
- Vor Veröffentlichung werden Änderungen in einer Testumgebung geprüft.
- Produktivdaten dürfen nicht durch Testläufe verändert werden.

## 8. Kosten

Die Anwendung soll dauerhaft ohne kostenpflichtige GitHub- oder Supabase-Tarife betrieben werden, soweit die jeweiligen kostenlosen Nutzungslimits ausreichen.

Kostenpflichtige Dienste werden nur nach vorheriger gemeinsamer Zustimmung eingesetzt.

## 9. Versionsstand

Projektstatus: Technische Vorbereitung

Version: 0.1.0
