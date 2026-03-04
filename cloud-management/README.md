# Cloud Management Concepts (ICCA)

This section focuses on how cloud environments are managed in practice: tools, operations, monitoring, and automation basics.

## Topics Covered
- Cloud management tools:
  - Web console (GUI)
  - Command Line (CLI)
  - APIs / REST APIs
  - Cloud Shell (managed CLI in the browser)
- Resource lifecycle basics:
  - Provision → Configure → Monitor → Scale → Delete
- Common operational concepts:
  - Tags and organization
  - Regions and availability zones (high-level)
  - Basic monitoring and alerts (CloudWatch-style concepts)
- Automation fundamentals (high-level):
  - Why automation matters
  - Infrastructure as Code concept (intro only)

## High-Yield Notes (Exam Focus)
- Know what each management tool is best for:
  - Console: quick changes, visual navigation
  - CLI: repeatable actions, scripting
  - API: integrations, automation, programmatic access
  - Cloud Shell: fast CLI without local setup
- Be careful with **region** selection (common lab mistake)

## Lab Mindset
When you create anything in labs, follow:
**Create → Verify → Document (if needed) → Delete**

## Files (optional)
- `notes.md` — management concepts notes
- `lab-checklist.md` — step-by-step lab playbook
- `exam-strategy.md` — time management + open-book tips
