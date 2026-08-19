# DATIpilot: moto OGS-App

Dieses Repository ist ein eingefrorener Snapshot der moto OGS-Plattform mit Stand vom **28.02.2026**. Die Software wurde im Rahmen des Förderprojekts DATIpilot entwickelt und wird hier zum Projektabschluss als Open Source unter der GNU Affero General Public License v3.0 (AGPL-3.0) veröffentlicht.

moto ist ein DSGVO-konformes System zur NFC-gestützten Anwesenheits- und Raumverwaltung für den Offenen Ganztag (OGS) an Grundschulen.

## Komponenten

| Komponente | Technologie |
|---|---|
| Backend | Go, Chi-Router, Bun ORM |
| Frontend | Next.js, React, Tailwind CSS |
| Datenbank | PostgreSQL (Multi-Tenancy mit Row Level Security) |

Die zugehörige Terminal-Anwendung für NFC-Geräte findet sich im Schwester-Repository [dati-pilot-moto-terminal-app](https://github.com/moto-nrw/dati-pilot-moto-terminal-app).

## Lokaler Start

Voraussetzungen: Docker und Docker Compose.

```bash
cp .env.example .env          # Platzhalter-Werte anpassen
cp docker-compose.example.yml docker-compose.yml
docker compose up -d
docker compose run server go run . migrate
```

Details zur Konfiguration stehen in `.env.example`.

## Status

Dieses Repository ist ein Archiv-Stand zum Projektende und wird nicht weitergepflegt. Es werden keine Issues, Pull Requests oder Sicherheits-Patches bearbeitet. Die aktive Weiterentwicklung von moto läuft getrennt von diesem Archiv unter [moto.nrw](https://moto.nrw).

## Lizenz

GNU Affero General Public License v3.0, siehe [LICENSE](LICENSE).
