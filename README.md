AI-CRM-Voice-Automation
Production AI system converting unstructured voice and text into structured CRM records. Built with Gemini API, Make.com, and AppSheet
[Uplo# AI-Powered CRM Voice-to-Record Automation

**Production System — Converts Unstructured Voice and Text into Structured CRM Records**

## The Problem

Field sales and SMB teams capture leads through voice notes, texts, and informal conversations. Turning those into clean CRM records means 10-15 minutes of manual data entry per lead. Reps skip it. The CRM becomes dirty, incomplete, and untrusted.

## The Solution

A three-layer production pipeline that takes any unstructured input — voice note, text message, conversation summary — and converts it into a structured, clean CRM record with automated follow-up. Zero manual data entry.

## Architecture

**Layer 1 — Intelligence (Google Gemini API)**

Engineered structured prompts that extract specific data fields from unstructured text: contact name, company, role, intent signals, budget indicators, and next action. Returns clean JSON. Handles edge cases including incomplete information, mixed languages, and informal phrasing.

**Layer 2 — Workflow Orchestration (Make.com)**

Webhook integration triggers on new input, passes to Gemini API, parses the structured response, writes the record to the CRM front-end, and fires automated email follow-up sequences — all without human involvement.

**Layer 3 — Front-End (Google AppSheet)**

Mobile-friendly CRM interface where reps interact with the system. Input capture, record viewing, and approval workflows all happen here.

## Key Design Decisions

- **Reliability over capability.** Error handling and fallback logic at every stage. If Gemini parsing confidence is below threshold, the system flags the record for human review rather than silently writing bad data.
- **RAG-based decision logic.** Lead scoring and follow-up triggers grounded in verified business data, eliminating hallucinations.
- **Human-in-the-loop safety gate.** Approval requests sent via encrypted channel before any automated action executes.

## Tech Stack

- **AI Engine:** Google Gemini API (1.5 Pro)
- **Workflow Automation:** Make.com (webhooks, modules, API calls)
- **Front-End:** Google AppSheet
- **Cloud:** Google Cloud Console
- **Data Format:** Structured JSON output

## Results

- Lead capture time reduced to under 2 minutes (from 10-15 minutes)
- 80% reduction in manual lead capture effort
- Production system — actively used, not a prototype
- Automated follow-up sequences triggered without human involvement

## Workflow

1. Rep captures lead via voice note, text, or conversation summary
2. Input hits webhook trigger in Make.com
3. Make passes unstructured text to Gemini API
4. Gemini extracts structured fields and returns clean JSON
5. Make parses response, validates required fields
6. If confidence is high — record written to AppSheet CRM automatically
7. If confidence is low — record flagged for human review
8. Automated follow-up email sequence fires based on intent category
9. Approval request sent to rep via encrypted channel

## What This Project Demonstrates

- End-to-end AI system design from business requirement to production deployment
- Prompt engineering for structured data extraction from unstructured input
- Workflow automation architecture connecting multiple APIs and services
- Production reliability design — error handling, fallback logic, confidence thresholds
- Human-in-the-loop governance in AI-automated workflows

---

*Built by Ranjit Ramanujam — 2025*
ading CRM_README.md…]()
