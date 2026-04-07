---
task: gerarFluxoAtendimento()
name: Gerar Fluxo de Atendimento
description: Generates complete WhatsApp intake flow — triage menu, CARRO qualification, scheduling, confirmation, and D-1 reminder.
responsavel: Auto Consultor
responsavel_type: Agente
atomic_layer: Template
Entrada:
  - nome: shop_type
    tipo: string
    obrigatorio: true
    description: "independent-shop | autocenter | dealership"
  - nome: shop_name
    tipo: string
    obrigatorio: true
    description: Name of the shop
  - nome: services
    tipo: string
    obrigatorio: true
    description: Comma-separated list of main services
  - nome: volume
    tipo: string
    obrigatorio: false
    description: "Daily WhatsApp message volume: low | medium | high"
Saida:
  - nome: triage_flow
    tipo: string
    obrigatorio: true
    description: Complete WhatsApp flow with all messages ready to implement
Checklist:
  - Triage menu has maximum 4 options
  - Qualification uses maximum 2 questions per message
  - CARRO framework applied
  - Time slot offer includes 3 options
  - Booking confirmation includes date, time, service, address
  - D-1 reminder includes confirm/reschedule option
  - Human handoff available at every step
  - All messages in Portuguese (pt-BR)
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
