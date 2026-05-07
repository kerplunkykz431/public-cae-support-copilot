# PublicCAE Support Copilot

PublicCAE Support Copilot is a lightweight Codex workspace for supporting Ansys Global Support Engineer work on a personal PC.

The core rule is simple: use only public, non-confidential information. Codex should help organize questions, research public technical sources, draft responses, and prepare notes, but it must not handle customer-identifying information, internal Ansys documents, private case details, source code, licensed model files, NDA screenshots, or non-public defect information.

## Purpose

Use Codex to support these daily tasks:

- Triage and structure customer questions after they have been anonymized.
- Identify missing information needed for engineering diagnosis.
- Build public-source research plans.
- Summarize public documentation, papers, articles, videos, and forum discussions.
- Draft customer-facing replies in Japanese and English.
- Create technical notes, FAQ drafts, and slide outlines from public information.

Codex is not the final authority. Every output must be reviewed by an engineer before it is used with a customer.

## What Can Be Used

Allowed inputs:

- Anonymized customer questions.
- Product names, version numbers, solver names, physics areas, and generic error messages.
- Public Ansys pages, public learning content, public documentation pages, and official videos.
- Public academic papers, conference papers, preprints, university lecture notes, and textbooks.
- Public technical articles, vendor blogs, forums, and YouTube videos.
- Small synthetic examples created specifically for explanation.

Do not input:

- Customer names, company names, emails, phone numbers, addresses, host IDs, license details, account IDs, or case numbers.
- Customer geometry, meshes, project archives, result files, logs, screenshots, or command outputs unless they are fully sanitized.
- Internal Ansys KB articles, internal emails, private release notes, unpublished defects, roadmap information, or support-only procedures.
- Anything covered by NDA, export control, or customer confidentiality.

## Recommended Workflow

PublicCAE Support Copilot uses a five-agent workflow. Each agent has a narrow responsibility so that the final answer is easier to review.

| Agent | Role | Main File | Output |
|---|---|---|---|
| Agent 1: Intake Sanitizer | Remove or flag sensitive information and turn the case into a generic technical question. | `triage_question.md` | Sanitized question and redaction notes |
| Agent 2: Triage Engineer | Structure the issue, identify missing information, and create initial hypotheses. | `triage_question.md` | Triage summary and customer questions |
| Agent 3: Public Researcher | Search public sources and rank evidence quality. | `trusted_sources.md` | Source log and research memo |
| Agent 4: Reply Drafter | Draft Japanese and English customer replies from the triage and research notes. | `draft_customer_reply.md` | Customer-ready draft with references |
| Agent 5: QA Reviewer | Review the draft for confidentiality, unsupported claims, unclear assumptions, and customer-readiness. | `draft_customer_reply.md` | Review checklist and revision requests |

Recommended sequence:

1. Agent 1 sanitizes the question before any analysis.
2. Agent 2 runs the triage prompt in `triage_question.md`.
3. Agent 3 uses the triage output to create and execute a focused public research plan.
4. Agent 3 records sources using `trusted_sources.md`.
5. Agent 4 drafts a response using `draft_customer_reply.md`.
6. Agent 5 reviews the answer before it is used with a customer.
7. The engineer performs the final technical and business review.

## Standard Output Policy

Every support-oriented answer should separate:

- Confirmed facts: supported by public sources or clearly provided by the user.
- Engineering interpretation: reasonable technical inference.
- Assumptions: conditions that may change the answer.
- Missing information: items needed for a reliable diagnosis.
- Recommended next steps: checks, settings, experiments, or questions.
- Sources: public URLs, titles, authors or organizations, and access date when useful.

## Agent Operating Rules

- Each agent should only work from sanitized inputs.
- Agents must label uncertainty instead of hiding it.
- Agents must not invent product behavior, known issues, case history, or internal guidance.
- Agent 3 must rank sources by the levels in `trusted_sources.md`.
- Agent 4 must not remove caveats just to make the reply sound more confident.
- Agent 5 should challenge the draft and request revisions when evidence is weak.
- The human engineer remains responsible for the final answer.

## Suggested Folder Growth

The minimum project starts with four files. If this becomes useful, add folders like these:

```text
cases/
  sanitized_input/
  research_notes/
  draft_replies/
outputs/
  reports/
  slide_outlines/
sources/
  source_logs/
templates/
  technical_note.md
  paper_summary.md
  video_summary.md
```

## Practical Safety Checklist

Before giving Codex any case content, check:

- Is the customer identifiable?
- Is the model, mesh, log, screenshot, or result file confidential?
- Does the text mention internal systems, private case numbers, or support-only knowledge?
- Could the content reveal a customer's design, material, process, performance target, or failure mode?
- Can the question be rewritten as a generic technical issue?

When in doubt, rewrite the input into a generic technical question first.
