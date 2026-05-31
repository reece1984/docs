---
title: "Assessment Lifecycle"
sidebarTitle: "Assessment Lifecycle"
description: "How an assessment moves from creation to completion and reporting."
---

```mermaid
flowchart TD
    A[Create Assessment] --> B[Name + Framework + Documents]
    B --> C[Configure Preferences]
    C --> D[Run Assessment]
    D --> E{Pipeline Processing}
    E -->|Success| F[Review Findings]
    E -->|Failure| G[Failed — Retry or Investigate]
    G --> D
    F --> H{For Each Finding}
    H --> I[Accept]
    H --> J[Challenge]
    H --> K[Query AI]
    H --> L[Create Action]
    J --> M[Re-assessment]
    M --> H
    I --> N{All Requirements Decided?}
    K --> N
    L --> N
    N -->|No| H
    N -->|Yes| O[Sign Off Finding]
    O --> P{All Findings Signed Off?}
    P -->|No| H
    P -->|Yes| Q[Generate Report]
    Q --> R[Export PDF / DOCX]
    R --> S[Archive Assessment]

    style A fill:#e8f5e9,stroke:#2e7d32
    style D fill:#e3f2fd,stroke:#1565c0
    style F fill:#fff3e0,stroke:#ef6c00
    style O fill:#fce4ec,stroke:#c62828
    style Q fill:#f3e5f5,stroke:#7b1fa2
    style S fill:#eceff1,stroke:#546e7a
```

## States

| State | Description | Exit condition |
|-------|-------------|----------------|
| **Created** | Assessment named, framework selected, documents connected | User clicks "Run" |
| **Running** | Pipeline processing — ingestion, indexing, criterion matching, scoring | Pipeline completes or fails |
| **Completed** | All criteria scored, findings surfaced | — |
| **In Review** | Reviewers working through findings | All findings signed off |
| **Signed Off** | All findings have human decisions recorded | Report generated |
| **Reported** | PDF/DOCX exported with full provenance | Archived or re-run |
| **Archived** | Assessment retained for audit trail, read-only | — |

## Notes

- You can leave during pipeline processing and return later — nothing is lost
- A full assessment run takes approximately 30 minutes
- Incremental re-assessment on document changes only re-scores affected criteria
- The sign-off gate enforces that every evidence requirement has a human decision before a finding can be signed off
