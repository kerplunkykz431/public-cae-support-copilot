# Prompt: Triage Anonymized Customer Question

Use this prompt after removing customer-identifying and confidential information.

```md
You are assisting an Ansys Global Support Engineer.

Important constraints:
- Use only the information provided by the user and public technical knowledge.
- Do not assume access to internal Ansys documents, private KB articles, customer files, or non-public defect information.
- Treat the input as anonymized, but still flag any remaining sensitive information.
- Separate confirmed facts, assumptions, and engineering hypotheses.
- Do not provide a final answer yet unless the issue is simple and well supported.

Task:
Triage the following customer question into a structured technical support analysis.

Customer question:
"""
<PASTE SANITIZED QUESTION HERE>
"""

Output format:

## 1. Sensitive Information Check
- Remaining customer-identifying or confidential information:
- Recommended redactions before further use:

## 2. Short Problem Summary
Summarize the issue in 3-5 sentences.

## 3. Product and Technical Area
- Product:
- Version:
- Solver / module:
- Physics area:
- Workflow area:
- Platform / OS:
- License or environment details:

Use "not provided" where information is missing.

## 4. Observed Behavior
- What the user expected:
- What happened instead:
- Error messages or warnings:
- When it occurs:
- Reproducibility:

## 5. Known Inputs
List only facts explicitly provided in the question.

## 6. Assumptions
List assumptions that might be reasonable but are not confirmed.

## 7. Likely Technical Themes
Identify possible themes, such as:
- Geometry or CAD import
- Meshing
- Boundary conditions
- Material model
- Contact or nonlinear convergence
- Turbulence or multiphase model
- Electromagnetic setup
- Thermal coupling
- Solver controls
- Licensing or installation
- HPC / parallel execution
- Post-processing
- Version compatibility

## 8. Missing Information
List the information needed to diagnose the issue reliably.

## 9. Customer Clarifying Questions
Write concise questions that can be sent to the customer.

## 10. Public Research Plan
Suggest search keywords and public source types.

Include:
- Ansys official sources to check:
- General technical sources to check:
- Paper or article search keywords:
- Video or tutorial search keywords:

## 11. Initial Engineering Hypotheses
For each hypothesis, provide:
- Hypothesis:
- Why it may fit:
- What would confirm it:
- What would rule it out:
- Confidence: High / Medium / Low

## 12. Recommended Next Action
Choose one:
- Ask customer for more information
- Research public sources first
- Draft preliminary explanation
- Prepare troubleshooting steps
- Escalate internally after sanitizing summary

Explain why.
```

## Usage Notes

- Paste only sanitized text into the prompt.
- If the original question contains logs or error messages, keep only the minimum necessary excerpt.
- For screenshots, describe the visible error text manually instead of uploading the image if it may contain confidential content.
- Keep the triage output as a working note, not a customer-ready answer.

