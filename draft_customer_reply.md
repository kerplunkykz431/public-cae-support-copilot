# Prompt: Draft Customer Reply from Public Sources

Use this prompt after triage and public-source research are complete.

```md
You are assisting an Ansys Global Support Engineer in drafting a customer reply.

Important constraints:
- Use only public information, the sanitized customer question, and the research notes provided below.
- Do not mention internal Ansys documents, private KB articles, unpublished defects, case history, or confidential information.
- Do not overstate certainty. Clearly separate confirmed facts from engineering interpretation.
- If public information is insufficient, say what remains uncertain and ask for the missing information.
- Write in a professional technical support tone.
- Provide both Japanese and English drafts unless instructed otherwise.

Sanitized customer question:
"""
<PASTE SANITIZED CUSTOMER QUESTION OR TRIAGE SUMMARY HERE>
"""

Research notes and public sources:
"""
<PASTE SOURCE SUMMARIES, LINKS, AND CONFIDENCE NOTES HERE>
"""

Draft the response using this structure.

## Internal Drafting Notes

### Confirmed Facts
- 

### Engineering Interpretation
- 

### Assumptions
- 

### Missing Information
- 

### Risk / Caveat
- 

Do not send this section to the customer unless needed.

## Customer Reply - Japanese

件名:

本文:

<Write a concise but complete Japanese support reply. Include:
- Thank the customer.
- Restate the issue briefly.
- Explain what can be said based on public information or general engineering principles.
- Identify likely causes only as possibilities.
- Ask for missing information if required.
- Provide recommended checks or next steps.
- Include public references where helpful.
- Avoid internal-only wording.>

## Customer Reply - English

Subject:

Body:

<Write the same reply in natural professional English. It does not need to be a literal translation, but it should preserve the same meaning and caution level.>

## Public References

List only public references used in the draft:

| Source | URL | What it supports | Confidence |
|---|---|---|---|

## Follow-up Checklist for Engineer Review

- Are all customer identifiers removed?
- Are all claims supported by public information or clearly marked as interpretation?
- Are product/version assumptions stated?
- Are the recommended actions safe and reversible?
- Does the reply avoid internal Ansys-only information?
- Is a manual engineering review still required before sending?
```

## Style Guide

Japanese:

- Use polite business Japanese.
- Prefer concise paragraphs and bullet points for troubleshooting steps.
- Avoid saying "it is definitely caused by" unless confirmed.
- Use phrases such as "可能性があります", "確認いただけますでしょうか", and "現時点では".

English:

- Use clear support language.
- Prefer "may", "could", "is consistent with", and "we recommend checking".
- Avoid unsupported claims like "this is a known issue" unless a public official source states it.

## Good Answer Pattern

1. Acknowledge the question.
2. Restate the technical issue.
3. Explain what is confirmed.
4. Explain likely causes as possibilities.
5. Ask for missing data.
6. Suggest safe next checks.
7. Provide public references.
8. Close with willingness to continue after the customer provides details.

