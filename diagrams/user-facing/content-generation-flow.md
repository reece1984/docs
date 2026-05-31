---
title: "Content Generation Flow"
description: "How the platform drafts remediation content for RED and AMBER findings."
---

```mermaid
flowchart TD
    A[Finding with RED or AMBER Rating] --> B[Select 'Generate Content']

    B --> C[Context Assembly]
    C --> C1[Finding Details + Evidence Gaps]
    C --> C2[Criterion Definition + Requirements]
    C --> C3[Framework Terminology]
    C --> C4[Related Findings for Cross-Reference]

    C1 & C2 & C3 & C4 --> D[Prompt Rendering]
    D --> D1[Template Selection by Criterion Type]
    D --> D2[Tone + Length Parameters]

    D1 & D2 --> E[LLM Streaming]
    E --> F[Draft Output]

    F --> G[Per-Field Confidence Score]
    G --> H{User Review}

    H -->|Content is good| I[Accept]
    H -->|Needs changes| J[Revise]
    H -->|Start fresh| K[Regenerate]

    J --> L[Edit Draft]
    L --> H

    K --> D

    I --> M[Content Saved to Finding]
    M --> N[Available in Reports]

    style A fill:#fce4ec,stroke:#c62828
    style F fill:#e3f2fd,stroke:#1565c0
    style I fill:#e8f5e9,stroke:#2e7d32
```

## How It Works

| Stage | What happens |
|-------|-------------|
| **Context Assembly** | The system gathers the finding's cited evidence, the criterion definition, evidence requirements, framework-specific language, and related findings to build a comprehensive prompt context. |
| **Prompt Rendering** | A template is selected based on the criterion type and rendered with the user's tone and length preferences. |
| **LLM Streaming** | Azure OpenAI GPT-4o generates the draft content with streaming output so you see it being written. |
| **Confidence Scoring** | Each field in the output gets a confidence score indicating how well-supported the draft is by the evidence. |
| **User Review** | You can accept the draft as-is, revise it manually, or regenerate with different parameters. |

## Output Types

Content generation can draft:
- Revised paragraphs addressing evidence gaps
- New risk register entries
- Gap-closing responses to criteria
- Remediation recommendations

## Provenance

Every generated piece of content tracks:
- What evidence was used as input
- Which criterion it addresses
- The confidence score at generation time
- Whether it was accepted as-is or revised
