# OpenTeleCompTrol

**Überwachungs- und Steuerungssoftware für STULZ-Klimaanlagen**

OpenTeleCompTrol ist eine plattformübergreifende Desktop-Anwendung zur Fernüberwachung und -steuerung
von STULZ-Klimageräten (HVAC). Die Kommunikation erfolgt über serielle Schnittstellen
(RS-232-Modem oder RS-485-Bus) mit dem STULZ-eigenen SDC-Protokoll (Stulz Data Controller).
Dieses Protokoll ist allerdings Re-Engineered somit können Fehler bestehen.
Die gesammte Software ist noch nicht getestet, somit Achtung bei der Benutzung.
Es können durchus Fehler in diesem Programm sein.

## Funktionen

- **Alarmüberwachung** — Echtzeit-Überwachung aller angeschlossenen Klimageräte
  mit Alarmmeldung bei Störungen (Bildschirm, Logdatei)
- **Geräteverwaltung** — Konfiguration von bis zu 128 Gerätegruppen mit je bis zu 32 Geräten
- **RS-485-Bus-Kommunikation** — Einfacher Anschluss über serielle Schnittstelle
- **Benutzerverwaltung** — Drei Zugriffsstufen (Admin, Read/Write, Read Only)
- **SMS-Benachrichtigung** — Alarmweiterleitung via SMS (TAP/UCP-Protokoll)
- **Protokollierung** — Alarm-Log mit 1.000 Einträgen, Scan-Verlauf
- **Druckausgabe** — Alarm-Logs und Berichte (Plattform-spezifisch)

## Projektstruktur

```
TeleCompTrol.sln
├── src/
│   ├── TeleCompTrol.Domain/       Modelle, Enums, Konstanten (net9.0)
│   ├── TeleCompTrol.Core/         Dienste, Kommunikation, Protokolle (net9.0)
│   ├── TeleCompTrol.Avalonia/     Avalonia UI (net9.0, cross-platform)
│   └── TeleCompTrol.Wpf/          WPF UI (net9.0-windows, legacy)
└── tct/                           Original C-Quellcode (Referenz)
```

## Plattform-Unterstützung

| Plattform | Build | Laufzeit |
|-----------|-------|----------|
| Windows   | ✅    | ✅ (Avalonia + WPF) |
| macOS     | ✅    | ✅ (Avalonia) |
| Linux     | ✅    | ✅ (Avalonia) |

## Abhängigkeiten

- .NET 9 SDK
- NuGet: Avalonia 11.2.3, System.IO.Ports 9.0.0
- Kein HASP-Dongle erforderlich

## Lizenz

Die Software basiert auf dem Original von **STULZ Klimatechnik GmbH, Hamburg**.
allerdings nur auf Re-Engineering basis nicht auf dem Originalem Source Code (der ist nie vorhanden gewesen)
Alle Rechte am SDC-Protokoll und an den ursprünglichen Algorithmen liegen bei STULZ, aber da diese Re-Engineered sind in diesem Programm.
Sollte es keine Probleme mit dem Ursprung (Originalem Hersteller) geben.
# OpenTeleCompTrol
# OpenTeleCompTrol
