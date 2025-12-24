<div align="center">

# TopologieManager

**Netzwerktopologien für technische Anlagen – planen, dokumentieren, exportieren.**  
Fokus: Segmentierung (BACnet/IP, MS/TP, Modbus, KNX, M-Bus …), Geräteverwaltung und sauberer PDF-Report.

</div>

---

## Überblick

**TopologieManager** ist ein Desktop-Tool zur Erstellung und Verwaltung von Netzwerktopologien in Anlagen der Gebäude-/Industrieautomation.

Kernziel: **übersichtliche Darstellung pro Netzwerksegment** und eine **professionelle Dokumentation als PDF** – auch bei großen Anlagen.

---

## Highlights

- **Anlagenverwaltung**: Anlegen, öffnen, umbenennen, löschen  
- **Netzwerksegmente**: BACnet/IP, BACnet MS/TP, Modbus TCP/RTU, KNX, M-Bus, …  
- **Farbkodierung pro Segment** für schnelle Orientierung  
- **Geräteverwaltung**: inkl. IP/MAC/Adresse & optional BACnet Instanznummer  
- **Links/Verbindungen**: intern und segmentübergreifend  
- **PDF-Dokumentation**: segmentweise, skalierbar für große Anlagen  
- **Templates (global)**: komfortabel in der UI editierbar (ohne JSON-Frust)  
- **Anlage Import/Export**: ZIP inkl. Assets (z. B. Logo)

---

## Funktionsumfang im Detail

### Anlagen
- Jede Anlage besitzt eine eigene Konfiguration (JSON) und optional Assets (Logo)
- Export/Import einer kompletten Anlage als **ZIP** (inkl. `assets/` und `exports/`)

### Netzwerksegmente
- Erstellung mehrerer Segmente pro Anlage
- Segmenttyp (z. B. BACnet/IP, Modbus RTU, …)
- **Eigene Farbe je Segment** für bessere Lesbarkeit in Topologie und Report

### Geräte
- Geräte anlegen/bearbeiten/löschen
- Zuordnung zu einem Netzwerksegment
- Felder je nach Typ:
  - **IP** (z. B. BACnet/IP, Modbus TCP)
  - **MAC/Adresse/Slave** (z. B. MS/TP, RTU)
  - **BACnet Instanznummer** (optional)

### Links (Verbindungen)
- Verbindungen zwischen Geräten, inklusive Medium (ethernet/mstp/rtu/knx/mbus/router/gateway/…)
- Saubere Darstellung in der Topologie (innerhalb des Segments)

### Templates (global)
- Templates definieren Standardwerte wie Vendor/Family/Role/Protocols/Tags
- Verwaltung direkt über die UI
- Import/Export (je nach Projektstand) bzw. zentrale Speicherung in `templates.json`

---

## PDF-Dokumentation

Der PDF-Export ist auf **große Anlagen** ausgelegt und erzeugt eine strukturierte Dokumentation:

### Pro Anlage
- Titelseite mit optionalem Logo
- Übersicht (Netzwerke, Geräte, Links)

### Pro Netzwerksegment (automatisch mit Seitenumbrüchen)
- **Topologie-Seite(n)** (bei großen Netzen automatisch in Ausschnitte/Kacheln aufgeteilt)
- **Geräte-Tabelle** (übersichtlich je Segment)
- **Externe Links (nummeriert)**

#### Segmentübergreifende Links (Cross-Network)
Um unübersichtliche Linien quer über die Seite zu vermeiden, werden Cross-Links im PDF so dargestellt:

- **Keine durchgehenden Linien über mehrere Segmente**
- Stattdessen: **nummerierte Marker direkt an den Endgeräten**  
  Beispiel: „1“ auf Gerät A und „1“ auf Gerät B
- Details erscheinen in der Tabelle **„Externe Links (nummeriert)“** pro Segment

---
