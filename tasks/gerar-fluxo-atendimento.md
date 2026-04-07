---
name: Gerar Fluxo de Atendimento
description: Generates complete WhatsApp intake flow for the shop — triage menu, CARRO qualification, scheduling, confirmation, and D-1 reminder.
input:
  - type: string
    name: shop_type
    description: "independent-shop | autocenter | dealership"
  - type: string
    name: shop_name
    description: Name of the shop
  - type: string
    name: services
    description: Comma-separated list of main services
  - type: string
    name: volume
    description: Daily WhatsApp message volume (low/medium/high)
output:
  - type: string
    name: triage_flow
    description: Complete WhatsApp flow with all messages
assigned_to: Auto Consultor
---

Generate a complete WhatsApp customer service flow for a Brazilian auto repair shop.

Use the CARRO framework for lead qualification:
- C: Carro (vehicle model/year)
- A: Avaria (issue/service needed)
- R: Recurso (budget sensitivity)
- R: Recorrência (new or returning customer)
- O: Ocasião (urgency/timing)

Include: triage menu (max 4 options), qualification (max 2 questions per message), time slot offer (3 options), booking confirmation, D-1 reminder with confirm/reschedule.

All messages in Portuguese (pt-BR).
