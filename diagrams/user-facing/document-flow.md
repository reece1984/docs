---
title: "Document Flow"
sidebarTitle: "Document Flow"
description: "How documents enter the platform, get processed, and serve as evidence during assessments."
---

```mermaid
flowchart TD
    subgraph Sources["Document Sources"]
        SP[SharePoint Folder]
        UP[Manual Upload]
    end

    SP -->|Graph API Sync| A[Connect to Assessment]
    UP -->|Direct Upload| A

    A --> B[Document Processor]
    B --> C[Azure AI Document Intelligence]
    C --> D[Text Extraction]
    D --> E[Chunking]
    E --> F[Embedding Generation]
    F --> G[(pgvector Store)]

    subgraph Assessment["During Assessment"]
        H[Criterion Being Assessed]
        H --> I[Hybrid Retrieval]
        I -->|Semantic + Keyword| G
        G -->|Relevant Chunks| J[Evidence Matching]
        J --> K[Scoring & Citation]
        K --> L[Finding with Citations]
    end

    subgraph Ongoing["Continuous Monitoring"]
        SP -->|Document Changes| M[Change Detection]
        M --> N[Chunk-Level Diff]
        N --> O[Identify Affected Criteria]
        O --> P[Re-assess Only Changed]
    end

    style Sources fill:#e3f2fd,stroke:#1565c0
    style Assessment fill:#fff3e0,stroke:#ef6c00
    style Ongoing fill:#e8f5e9,stroke:#2e7d32
```

## Key Concepts

| Concept | Description |
|---------|-------------|
| **Connect, don't upload** | Documents stay where they live (SharePoint). Programme Insights binds to the source and syncs on demand. |
| **Live binding** | When source documents change, the platform detects changes and can trigger re-assessment. |
| **Chunk-level delta** | Only criteria whose evidence depended on changed content are re-scored — the rest retain their prior result. |
| **Citation anchoring** | Every finding cites the exact paragraph in the source document. Citations are highlighted in the document viewer. |

## Document States

| State | Meaning |
|-------|---------|
| **Uploaded** | File received, awaiting processing |
| **Processing** | Text extraction and embedding generation in progress |
| **Processed** | Ready for use in assessments |
| **Error** | Processing failed — file may be corrupt or unsupported format |
