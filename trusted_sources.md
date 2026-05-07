# Trusted Public Sources

Use this file to rank public sources before drafting a support answer. Prefer official and primary sources, and clearly label weaker sources as supporting context only.

## Source Priority

### Level 1: Official Ansys Sources

Use first when available.

- Ansys customer support and help pages: https://www.ansys.com/support
- Ansys Innovation Space: https://innovationspace.ansys.com/
- Ansys Innovation Courses: https://innovationspace.ansys.com/courses/
- Ansys Learning YouTube channel: https://www.youtube.com/@AnsysLearning
- Product-specific public pages on https://www.ansys.com/

Notes:

- Some Ansys documentation may require login. Do not copy or summarize login-protected content into this personal workspace unless it is permitted for that use.
- If a source is public but version-specific, record the product version and page date if visible.
- Official sources are best for product behavior, terminology, supported workflows, and documented limitations.

### Level 2: Primary Technical Literature

Use for physics, numerical methods, validation theory, material models, turbulence models, contact mechanics, electromagnetics, optics, acoustics, HPC, and similar fundamentals.

- Peer-reviewed journal papers.
- Conference papers from reputable engineering or scientific organizations.
- Standards and technical reports from recognized bodies.
- University lecture notes from identifiable courses or faculty.
- Books or handbooks from established technical publishers.

Good places to search:

- Google Scholar: https://scholar.google.com/
- arXiv: https://arxiv.org/
- NASA Technical Reports Server: https://ntrs.nasa.gov/
- NIST: https://www.nist.gov/

### Level 3: Reputable Engineering Articles

Use as practical context, not as final proof.

- Engineering software vendor blogs.
- Consulting company technical articles.
- University lab pages.
- Application notes.
- Public benchmark writeups.

Check whether the article provides:

- Author or organization.
- Publication date.
- Product version, solver, or method version.
- Reproducible settings or equations.
- References to primary literature.

### Level 4: Forums, Q&A, and Videos

Use carefully as supporting information.

- Ansys Learning Forum on Innovation Space.
- Public engineering forums.
- YouTube tutorials and webinars.
- Community Q&A posts.

Rules:

- Do not treat forum answers or videos as authoritative unless they point to official documentation or primary literature.
- Capture the exact claim, the context, and the uncertainty.
- Prefer videos for workflow demonstrations, interface navigation, and conceptual explanation, not for final technical justification.

## Source Log Template

Use this table when researching.

```md
| Priority | Source | URL | Date Accessed | Product / Topic | Key Finding | Confidence | Notes |
|---|---|---|---|---|---|---|---|
| L1 |  |  |  |  |  | High / Medium / Low |  |
```

## Confidence Guide

High:

- Official Ansys source for the relevant product and version.
- Primary literature directly addressing the technical issue.
- Multiple independent reliable sources agree.

Medium:

- Official source is related but not exact.
- Paper is relevant but has different assumptions.
- Practical article is credible and technically detailed.

Low:

- Forum answer, personal blog, or video without references.
- Source discusses a similar but not identical solver, version, physics model, or workflow.
- Claim cannot be verified from another source.

## Red Flags

Avoid relying on a source when:

- It has no date, author, context, or version.
- It contradicts official documentation.
- It uses a different product or solver without explaining the difference.
- It gives a recipe without assumptions or limitations.
- It includes confidential-looking customer data.

## Citation Style

For each important claim, record:

```text
Source title, organization or author, URL, date accessed, relevant product/version if applicable.
```

For customer-facing drafts, cite only public links and keep wording concise. Avoid implying that a public source confirms something it does not explicitly say.

