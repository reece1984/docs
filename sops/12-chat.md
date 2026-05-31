# Chat with Your Assessment
> Ask natural-language questions about your documents, criteria, or findings and get answers grounded in your actual evidence with clickable citations.

## Before you start
- An assessment must exist with documents uploaded and at least one assessment run completed.
- Chat uses RAG (retrieval-augmented generation) so answers are only as good as the documents in your assessment. Ensure documents have been fully parsed before starting a conversation.
- Any workspace member can use chat; no special role is required.

## Steps

1. Open an assessment and click **Chat** in the sidebar (or from the assessment header actions).
   [screenshot: 16-chat.png]

2. The chat interface has three panels:
   - **Left panel** -- thread list showing your previous conversations.
   - **Centre panel** -- the active conversation thread.
   - **Top bar** -- scope selector to focus the conversation.

3. Use the **scope selector** at the top to set the conversation context:
   - **Assessment** -- broad scope; the AI can reference any document or finding in the assessment.
   - **Document** -- narrow the AI's context to a single uploaded document.
   - **Criterion** -- focus on a specific criteria requirement.
   - **Finding** -- drill into one finding for detailed investigation.

4. Type your question in the message box and press Enter. The AI returns an answer drawn from your source documents.

5. Every answer includes **citations** -- exact paragraph references from source documents. Each citation is clickable: selecting it opens the document viewer scrolled to the relevant passage.

6. Follow up in the same thread to dig deeper. The AI maintains conversation context so you can ask "what about section 4?" without restating the full question.

7. To start a fresh conversation, click **New Thread** in the left panel. Previous threads are preserved and searchable.

### Example use cases

- **Investigate a finding**: scope to a specific finding and ask "What evidence supports this rating?" or "Why was this marked Amber?"
- **Explore a document**: scope to a document and ask "Summarise the key risks identified in this document" or "Does this document address climate resilience?"
- **Ask about criteria**: scope to a criterion and ask "Which documents provide evidence for this requirement?" or "What gaps exist against this criterion?"

## What happens next
- Insights from chat can inform your review decisions -- navigate to the finding detail to accept or challenge (see [SOP 07 -- Finding Detail](/sops/07-finding-detail)).
- If chat reveals a missing document, upload it via the documents page (see [SOP 02 -- Documents](/sops/02-documents)).

## Common questions

**Q: Are chat answers saved?**
A: Yes. Every thread is persisted and appears in the thread list on the left. You can return to any previous conversation at any time.

**Q: How does scoping affect the quality of answers?**
A: Narrower scope means the AI searches a smaller, more relevant set of documents. If you are investigating a specific finding, scoping to that finding produces more precise citations than asking at the assessment level.

**Q: Can the AI hallucinate or make things up?**
A: The AI is grounded in your uploaded documents via RAG. Every claim is backed by a citation you can verify. If the documents do not contain relevant information, the AI will say so rather than fabricate an answer.
