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

1. Sanitize the question before using Codex.
2. Run the triage prompt in `triage_question.md`.
3. Use the triage output to create a focused public research query.
4. Record sources using `trusted_sources.md`.
5. Ask Codex to summarize each source with confidence and caveats.
6. Draft a response using `draft_customer_reply.md`.
7. Review the answer manually before sending it to a customer.

## Standard Output Policy

Every support-oriented answer should separate:

- Confirmed facts: supported by public sources or clearly provided by the user.
- Engineering interpretation: reasonable technical inference.
- Assumptions: conditions that may change the answer.
- Missing information: items needed for a reliable diagnosis.
- Recommended next steps: checks, settings, experiments, or questions.
- Sources: public URLs, titles, authors or organizations, and access date when useful.

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
