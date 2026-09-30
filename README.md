# Patrick Asuquo — AI Automation Portfolio

**Role:** AI Automation Specialist  
**Core Stack:** Make.com, Google Workspace, Brevo, Google Gemini AI, Tally, n8n (learning)  
**Focus:** Building AI‑powered business workflows that eliminate manual work and unlock new capabilities.

---

## 🍔 Project 1: Meal Bridge — Automated Marketplace Dispatch System

**Executive Summary:**  
A two‑part automation that connects low‑budget customers with local restaurants, dispatches order requests, and processes restaurant responses — all without manual intervention.

**Tech Stack:** Make.com, Google Forms, Google Sheets, Brevo, Router, Filters.

**Workflow 1 – The Dispatcher:**
- Watches Google Sheets for new customer orders.
- Filters restaurants by location and budget.
- Sends order request email to the matched restaurant via Brevo.
- Sends confirmation email to the customer.
- Updates order status to `SentToRestaurant`.

**Workflow 2 – The Response Handler:**
- Watches Gmail for restaurant replies.
- Router splits into `ACCEPT` and `DECLINE` paths.
- Updates Google Sheet status to `Accepted` or `Declined`.

**Key Challenges & Solutions:**
- **Google OAuth errors:** Pivoted from Gmail to Brevo for reliable email delivery.
- **Tally nested data:** Manually mapped fields using `{{1.data.fields[n].value}}`.
- **Router filter failures:** Used `Matches pattern` regex and fallback routes.

**Outcome:** Fully automated order dispatch and response system.

---

## 📊 Project 2: AI Sales Lead Qualification Agent

**Executive Summary:**  
An AI‑powered lead qualification system that captures leads, uses Google Gemini to analyze intent, scores them as HOT/WARM/LOW, and routes them to the appropriate follow‑up action.

**Tech Stack:** Make.com, Tally (Webhook), Google Sheets, Google Gemini AI, Brevo, Router.

**Workflow:**
1. Webhook captures Tally form submission.
2. Google Sheets logs the raw lead.
3. Gemini AI analyzes the message and returns structured JSON.
4. Google Sheets updates the row with AI analysis.
5. Router sends different emails based on lead status.

**Key Challenges & Solutions:**
- **Tally nested data:** Manual mapping via `{{1.data.fields[3].value}}`.
- **Gemini model deprecation:** Switched to `gemini-2.5-flash`.
- **JSON parsing errors:** Bypassed by using Gemini's structured output directly.

**Outcome:** AI‑powered lead qualification and automated follow‑up system.

---

## 🎧 Project 3: AI Customer Support Agent

**Executive Summary:**  
An autonomous AI support agent that answers customer questions using a company knowledge base, and escalates to a human when the AI cannot answer.

**Tech Stack:** Make.com, Tally, Google Sheets, Google Docs (Knowledge Base), Google Gemini AI, Brevo, Router (with fallback).

**Workflow:**
1. Webhook captures support question from Tally.
2. Google Sheets logs the ticket.
3. Google Docs reads the Knowledge Base.
4. Gemini AI answers using the knowledge base, or replies `ESCALATE` if it cannot.
5. Router:
   - **ANSWERED path:** Sends AI's answer to the customer via Brevo.
   - **ESCALATE fallback:** Sends urgent alert to support team via Brevo.

**Key Challenges & Solutions:**
- **AI ignoring strict instructions:** Switched from `Flash-Lite` to `Gemini 2.5 Flash`.
- **Router filter not matching:** Used fallback route for escalation.
- **Missing email body:** Manually mapped `{{5.Result}}` into Brevo.

**Outcome:** Autonomous support agent with escalation logic.

---

## 🛠️ Skills Demonstrated

- **API & Webhook Integration:** Tally, Google Workspace, Brevo, Gemini.
- **AI / LLM Integration:** Prompt engineering, structured output, decision routing.
- **Automation Logic:** Routers, filters, fallback routes, conditional flows.
- **Data Management:** Google Sheets as CRM, nested data mapping.
- **Problem‑Solving:** Debugging OAuth, regex, server errors, and UI quirks.

---

## 🚀 Next Steps (Roadmap)

- **Project 4:** AI Business Operations Agent.
- **n8n Self‑Hosting:** Learning to deploy open-source automation.

---

**Contact:** asuquopatrick54@gmail.com  
**Location:** Nigeria  
**Availability:** Open to freelance and full-time automation roles.
