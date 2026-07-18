# Einrichtung: Eigene Inhaltsverwaltung für deine Website

Mit dieser Version kannst du Galerie-Bilder und Vorher/Nachher-Paare
selbst über eine eigene Login-Seite (`deine-domain.de/admin`) pflegen
– ganz ohne Programmieren. Einmalig musst du dafür drei kostenlose
Konten miteinander verbinden. Das dauert etwa 15–20 Minuten.

## Schritt 1: GitHub-Konto und Repository

1. Gehe auf github.com und erstelle ein kostenloses Konto (falls noch
   nicht vorhanden).
2. Klicke auf **"New repository"**. Name z. B. `battermann-website`.
   Sichtbarkeit: "Private" ist möglich, "Public" geht auch.
3. Auf der leeren Repository-Seite auf **"uploading an existing
   file"** klicken.
4. Alle Dateien und Ordner aus diesem Paket dort hineinziehen
   (die komplette Struktur: `index.html`, `admin/`, `content/`,
   `images/`) und mit "Commit changes" bestätigen.

## Schritt 2: Netlify mit GitHub verbinden

1. Auf netlify.com einloggen (oder Konto erstellen).
2. **"Add new site" → "Import an existing project"** wählen.
3. GitHub verbinden und das eben erstellte Repository auswählen.
4. Build-Einstellungen einfach leer lassen (kein Build-Befehl nötig,
   "Publish directory" auf `/` bzw. Hauptverzeichnis lassen) und auf
   "Deploy" klicken.
5. Deine Domain wie gehabt unter "Domain settings" hinterlegen.

## Schritt 3: Login-System aktivieren (Netlify Identity)

1. Im Netlify-Dashboard deiner Seite: **"Identity"** öffnen und
   **"Enable Identity"** klicken.
2. Unter "Registration preferences" auf **"Invite only"** stellen
   (damit sich nicht x-beliebige Personen anmelden können).
3. Unter **"Services" → "Git Gateway"** auf **"Enable Git Gateway"**
   klicken.
4. Oben unter "Identity" → **"Invite users"** deine eigene
   E-Mail-Adresse eintragen. Du bekommst eine Einladungs-E-Mail.

## Schritt 4: Einloggen und loslegen

1. Den Link aus der Einladungs-E-Mail öffnen, Passwort festlegen.
2. Du landest automatisch im Admin-Bereich unter `/admin/`.
3. Dort kannst du ab sofort:
   - Galerie-Bilder hinzufügen, austauschen, löschen, Reihenfolge
     ändern
   - Vorher/Nachher-Paare bearbeiten oder neue hinzufügen
   - Beim Elektro-Projekt das "Nachher"-Bild eintragen, sobald es
     fertig ist (dann einfach den Haken bei "Noch in Arbeit"
     entfernen)
4. Nach dem Speichern eines Eintrags im CMS aktualisiert sich die
   Website innerhalb weniger Minuten von selbst.

## Was, wenn etwas nicht klappt?

Melde dich einfach wieder im Chat – die einzelnen Schritte (vor allem
Identity/Git Gateway in Netlify) sind nicht immer sofort
selbsterklärend, das kriegen wir dann zusammen hin.
