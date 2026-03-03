# Diplomprojekt – Phishing Simulation Platform

Dieses Projekt entstand im Rahmen einer Diplomarbeit an der **HTL Wien** (5AHIF, Schuljahr 2025/26) und umfasst die Konzeption, Entwicklung und Evaluierung einer Plattform zur kontrollierten Durchführung simulierter Phishing-Angriffe.

## Ziel

Ziel der Plattform ist es, das Sicherheitsbewusstsein von Zielpersonen durch realistische Smishing-Kampagnen (SMS-Phishing) messbar zu machen und auf Basis der gewonnenen Telemetrie-Daten wissenschaftlich auswertbare Erkenntnisse zu generieren.

## Systemarchitektur

```
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│  Dashboard   │    │    Backend    │    │ Landing Page │
│  (Vue 3)     ├───►│  (Express +  ├───►│   (Vue 3 +   │
│  Admin UI    │    │  MongoDB)    │    │  Tracking)   │
└──────────────┘    └──────────────┘    └──────────────┘
                              ▲
                    ┌──────────────┐
                    │  AI-Generator│
                    │  (Phishing   │
                    │  Mail Content)│
                    └──────────────┘
```

## Repositories

| Repository | Beschreibung | Technologie |
|---|---|---|
| [backend](https://github.com/Diplomprojekt-Phishing/backend) | REST API, Datenbankanbindung, Kampagnenverwaltung | Express.js, MongoDB |
| [landing-page](https://github.com/Diplomprojekt-Phishing/landing-page) | Phishing-Frontend mit Interaction-Tracking | Vue 3, Tailwind CSS |
| [dashboard](https://github.com/Diplomprojekt-Phishing/dashboard) | Admin-Panel für Kampagnensteuerung & Auswertung | Vue 3 |
| [AI](https://github.com/Diplomprojekt-Phishing/AI) | KI-gestützte Generierung von Phishing-Inhalten | Python / AI API |

## Team

Dieses Projekt wurde im Rahmen einer Diplomarbeit von einem 5-köpfigen Team entwickelt.

---

> ⚠️ **Hinweis:** Alle Aktivitäten dieser Plattform erfolgen ausschließlich im Rahmen kontrollierter, ethisch genehmigter Sicherheitssimulationen. Eine missbräuchliche Verwendung ist nicht gestattet.
