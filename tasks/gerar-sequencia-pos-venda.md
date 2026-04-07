---
task: gerarSequenciaPosVenda()
name: Gerar Sequência Pós-Venda
description: Generates complete post-service retention sequence — NPS, service-specific reminders, no-show recovery, and seasonal campaigns.
responsavel: Auto Consultor
responsavel_type: Agente
atomic_layer: Template
Entrada:
  - nome: service_performed
    tipo: string
    obrigatorio: true
    description: "oil-change | brakes | suspension | electrical | ac | bodywork | alignment | full-service"
  - nome: client_name
    tipo: string
    obrigatorio: true
    description: Customer first name
  - nome: vehicle
    tipo: string
    obrigatorio: true
    description: Vehicle model and year (e.g. Civic 2021)
  - nome: tone
    tipo: string
    obrigatorio: false
    description: "formal | informal"
Saida:
  - nome: retention_sequence
    tipo: string
    obrigatorio: true
    description: Complete D+0 to D+365 message sequence ready to implement
Checklist:
  - D+0 delivery message is warm and personal
  - NPS sent at D+1 with 0-10 emoji scale
  - NPS routing defined (9-10 → referral, 0-6 → human)
  - D+7 technical check-in included
  - Service-specific reminder timing applied
  - No-show recovery included (H+1, H+3, D+1)
  - At least 1 seasonal alert for BR calendar
  - All messages personalized with [Nome] and [Modelo]
  - All messages in Portuguese (pt-BR)
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
