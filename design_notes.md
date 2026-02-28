# Design Notes & Architectural Decisions

This document outlines the structural and operational reasoning behind the AI-powered dental voice assistant.

## 1. Deterministic Workflow Architecture

Each supported intent follows a predefined execution sequence. This reduces ambiguity, lowers hallucination risk, and ensures predictable backend integration. Deterministic flows are essential in healthcare environments where operational errors impact patient experience.

## 2. Intent Taxonomy Enforcement

The assistant classifies every interaction into a fixed set of supported intents. This structured taxonomy enables clear branching logic and simplifies workflow mapping and backend automation.

## 3. Slot-Filling & Dialogue State Management

The assistant collects only missing required fields and maintains internal state tracking:
- Collected fields
- Confirmed fields
- Validation status
- Escalation status

This prevents redundant questioning and ensures conversational efficiency.

## 4. Validation-First Scheduling Logic

All scheduling actions require validation:
- Future dates only
- Within operating hours
- No double booking
- Explicit user confirmation

All dates are normalized to ISO format (YYYY-MM-DD) before structured output.

## 5. Escalation-First Safety Model

Healthcare automation must remain conservative. The assistant escalates in cases of:
- Emergency indicators
- Emotional distress
- Low-confidence interpretation
- Administrative complexity

Escalation ensures human oversight when necessary.

## 6. Structured Output Enforcement

Every interaction concludes with valid JSON output. This ensures seamless backend integration with scheduling systems and patient management software.

## 7. Operational Boundaries

The assistant explicitly avoids:
- Medical diagnosis
- Treatment recommendations
- Disclosure of patient information
- Legal or financial advice

These constraints ensure safe deployment within a clinical setting.
