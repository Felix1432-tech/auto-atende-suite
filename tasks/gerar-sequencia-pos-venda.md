---
name: Gerar Sequência Pós-Venda
description: Generates complete post-service retention sequence — NPS, service-specific reminders, no-show recovery, and seasonal campaigns.
input:
  - type: string
    name: service_performed
    description: Service that was performed (oil-change, brakes, suspension, etc.)
  - type: string
    name: client_name
    description: Customer first name
  - type: string
    name: vehicle
    description: Vehicle model and year
  - type: string
    name: tone
    description: "formal | informal"
output:
  - type: string
    name: retention_sequence
    description: Complete D+0 to D+365 message sequence
assigned_to: Auto Consultor
---

Generate a complete post-service WhatsApp retention sequence for a Brazilian auto repair shop.

Sequence structure:
- D+0: Delivery confirmation (warm, personal)
- D+1: NPS (0-10 scale with emoji buttons). Route: 9-10 → referral request; 0-6 → human handoff
- D+7: Technical check-in
- D+[service-specific]: Service reminder (timing varies by service type)
- Seasonal alerts: IPVA (Jan), post-rain (Mar), winter/holidays (Jun), summer (Nov)
- No-show recovery if applicable: H+1, H+3, D+1

All messages in Portuguese (pt-BR). Personalize with [Nome] and [Modelo].
