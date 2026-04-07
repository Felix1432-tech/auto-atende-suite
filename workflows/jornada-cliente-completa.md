---
name: Jornada Cliente Completa
description: End-to-end customer journey for Brazilian auto shops — from first WhatsApp message to loyal returning customer.
---

## Workflow: Complete Customer Journey

### Stage 1 — New Customer Contact
**Trigger:** Customer sends any WhatsApp message
**Agent:** Auto Consultor
**Task:** Gerar Fluxo de Atendimento
**Output:** Triage menu sent to customer

### Stage 2 — Qualification & Scheduling
**Trigger:** Customer selects "Schedule service"
**Task:** CARRO qualification (2 questions max per message)
**Output:** Booking confirmed with date, time, service, address

### Stage 3 — Pre-Service Reminder
**Trigger:** D-1 before appointment
**Output:** Reminder with confirm/reschedule option

### Stage 4 — Post-Service Retention
**Trigger:** Service delivered (D+0)
**Task:** Gerar Sequência Pós-Venda
**Output:** Complete D+0 → D+365 retention sequence activated

### Stage 5 — No-Show Recovery (if applicable)
**Trigger:** Customer misses appointment (H+1)
**Output:** 3-message recovery sequence (H+1, H+3, D+1)

### Success Indicators
- NPS response rate > 30%
- Return rate within 6 months > 40%
- No-show recovery rate > 50%
- Referral conversion > 15%
