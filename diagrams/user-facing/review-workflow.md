---
title: "Review Workflow"
description: "How reviewers work through findings and build a defensible audit trail."
---

```mermaid
flowchart TD
    A[Finding Surfaced by AI] --> B[Pending Review]

    B --> C{Reviewer Action}
    C -->|Agree with AI| D[Accept]
    C -->|Disagree with AI| E[Challenge]
    C -->|Need more info| F[Query AI via Chat]
    C -->|Real gap found| G[Create Action]

    E --> H[Record Rationale]
    H --> I[Trigger Re-assessment]
    I --> J[New Rating Produced]
    J --> B

    F --> K[Chat Response with Citations]
    K --> C

    G --> L[Action Created]
    L -->|Owner + Deadline| M[Actions Board]

    D --> N{All Evidence Requirements Decided?}
    N -->|No| B
    N -->|Yes| O[Sign-Off Gate Opens]

    O --> P[Sign Off Finding]
    P --> Q{All Findings Signed Off?}
    Q -->|No| B
    Q -->|Yes| R[Assessment Ready for Report]

    R --> S[Generate Report]
    S --> T[Lock Assessment]
    T --> U{Need Changes?}
    U -->|Yes| V[Unlock — Creates New Version]
    V --> B
    U -->|No| W[Final Report with Audit Trail]

    style D fill:#e8f5e9,stroke:#2e7d32
    style E fill:#fff3e0,stroke:#ef6c00
    style P fill:#e3f2fd,stroke:#1565c0
    style W fill:#f3e5f5,stroke:#7b1fa2
```

## The Four Reviewer Actions

| Action | When to use | What happens |
|--------|-------------|-------------|
| **Accept** | AI's assessment is correct | Finding marked as accepted; moves to next |
| **Challenge** | AI is wrong or incomplete | Rationale recorded; re-assessment triggered with new context |
| **Query AI** | Need more information before deciding | Finding-scoped chat opens; AI responds with citations |
| **Create Action** | A genuine gap that needs remediation | Action item created with owner and deadline |

## Sign-Off Rules

1. Every evidence requirement within a finding must have a decision (accepted or challenged)
2. The sign-off bar tracks progress live — accepted, challenged, pending
3. Only when all requirements are decided does the "Sign off finding" button activate
4. This is the human-in-the-loop audit trail that makes PI defensible in assurance

## Keyboard Shortcuts (Power Reviewers)

| Key | Action |
|-----|--------|
| `J` / `K` | Navigate to next / previous finding |
| `A` | Accept the focused requirement |
| `C` | Challenge |
| `?` | Show all shortcuts |
| `Esc` | Close the action drawer |
