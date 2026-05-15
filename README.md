# Agentic Patient Lifecycle AI System

An AI-powered healthcare workflow automation system built in n8n.

This project automates the complete patient lifecycle using five specialized workflow agents:

- Pre-Visit Agent
- Post-Visit Agent
- Billing & Insurance Agent
- Retention Agent
- Clinical Triage Agent

The system uses webhook-based structured inputs and rule-based automation logic to support clinical operations, patient engagement, and healthcare workflow management.

---

# Architecture Overview

The platform is designed around modular workflow agents where each workflow handles a specific stage of the patient journey.

## Included Agents

### 1. Pre-Visit Agent
Handles patient intake validation before appointments.

Features:
- Mandatory field validation
- Insurance format validation
- Pregnancy status conditional logic
- High-risk intake escalation
- Nurse queue escalation

Example high-risk scenario:
- Hypertension history
- Chest pain symptoms

Triggers:
- Webhook input

Outputs:
- Intake acceptance
- Validation errors
- Follow-up requests
- High-risk escalation

---

### 2. Post-Visit Agent
Monitors patient recovery after appointments.

Features:
- Pain score assessment
- Emergency symptom detection
- Clinical red-flag detection
- Recovery monitoring
- Follow-up escalation

Emergency escalation examples:
- Shortness of breath
- Cannot breathe
- Severe pain

Outputs:
- Emergency escalation
- Clinical escalation
- Normal recovery log

---

### 3. Billing & Insurance Agent
Automates insurance and billing validation workflows.

Features:
- Missing billing field detection
- Duplicate invoice detection
- Insurance expiry validation
- Required document verification
- Coverage plan matching
- Manual override enforcement
- SLA breach escalation

Outputs:
- Claim approval
- Claim rejection
- Billing escalation

---

### 4. Retention Agent
Re-engages inactive patients safely and ethically.

Features:
- Inactive patient detection
- Patient segmentation
- Consent verification
- Suppression list checks
- Outreach frequency caps
- Personalized outreach preparation

Segments:
- Chronic
- Wellness
- One-time patients

Outputs:
- Outreach campaign preparation
- Outreach suppression

---

### 5. Clinical Triage Agent
Performs structured symptom triage and urgency classification.

Features:
- Emergency keyword detection
- Symptom normalization
- Follow-up clarification questions
- Urgency classification
- Emergency escalation

Urgency Levels:
- Emergency
- Same-Day
- Routine

Emergency examples:
- Severe chest pain
- Inability to breathe

Outputs:
- Triage classification
- Emergency escalation
- Follow-up questions

---

# Tech Stack

- n8n
- Webhooks
- PowerShell
- JSON-based workflow automation

---

# Project Structure

```text
workflows/
├── pre-visit-agent.json
├── post-visit-agent.json
├── billing-insurance-agent.json
├── retention-agent.json
└── clinical-triage-agent.json
