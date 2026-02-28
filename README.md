AI-Powered Dental Voice Agent

Production-Ready Prompt & System Design Specification
This project defines the reasoning layer for an AI-powered voice assistant designed to automate front-desk operations in a structured, deterministic, and production-ready manner at a dental clinic. 

Key principles:
Intent-based interaction,
Slot-filling for required data,
Dialogue state tracking,
Deterministic workflow execution,
Structured backend-ready output,
Explicit escalation conditions,
Safety guardrails,
The assistant operates within a voice pipeline:
Speech-to-Text → LLM Reasoning → Backend Integration → Text-to-Speech

Supported Capabilities:
Appointment booking,
Appointment rescheduling,
Appointment cancellation,
Appointment confirmation,
No-show follow-up,
Emergency escalation,
General clinic queries

Files:
system_prompt.txt : Production-ready master prompt,
output_schema.json : Structured backend integration schema,
conversation_examples.md : Example real-world flows,
design_notes.md : Architectural decisions and rationale,
