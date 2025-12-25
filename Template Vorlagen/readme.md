# Device Template (GA/GLT)
### Siemens · DEOS · Belimo · Thermokon · Metz

Dieses Repository stellt ein **standardisiertes JSON-Template** zur Verfügung,  
mit dem Geräte der Gebäudeautomation (GA/GLT) einheitlich beschrieben werden können.

Abgedeckt sind unter anderem:

- Regler (DDC / Automationsstationen)
- Antriebe (Klappen-, Ventil-, VAV-Antriebe)
- Ventile (inkl. Energieventile / PI-CCV)
- Sensoren
- E/A-Module und Gateways
- Bedien- und Managementsysteme

Ziel ist eine **konsistente, herstellerübergreifende Gerätebeschreibung**, z. B. für:
- Engineering-Standards  
- CMDB / Asset-Management  
- GLT-Projektvorlagen  
- Automatisierte Auswertungen  

---

## Datenmodell

Jedes Gerät wird über einen eindeutigen Schlüssel (`DeviceKey`) beschrieben  
und folgt einem klaren, kompakten Schema:

```json
{
  "<DeviceKey>": {
    "vendor": "Hersteller",
    "gruppe": "Produktfamilie / Gerätegruppe",
    "rolle": "Geräterolle (deutsch)",
    "protocols": [
      "BACnet/IP",
      "Modbus RTU",
      "KNX"
    ],
    "tags": [
      "frei",
      "definierbar"
    ]
  }
}
