---
name: document-analyzer
description: "Analyze and summarize documents quickly. Use this skill whenever users ask to summarize, extract key points from, or analyze any document — whether it's a PDF, Word file, Markdown, or text file. The skill produces structured bullet-point summaries with key themes, topics, and main takeaways. Trigger whenever the user mentions: summarize, extract key points, analyze a document, understand the main points, get the gist of, break down, or review a document."
compatibility: ""
---

# Document Analyzer & Summarizer

When a user provides or asks you to analyze a document (PDF, Word, Markdown, plain text, etc.), use this skill to quickly extract meaning and structure.

## What This Skill Does

Given a document, produce a **structured bullet-point summary** containing:
- **Key Themes**: 3-5 main themes or topics the document covers
- **Key Topics**: Important concepts, ideas, or subjects discussed
- **Summary**: 2-3 sentence overview of the document's purpose and main argument

## Process

1. **Extract the content** from whatever file format the user provides
   - If a file path is given, read the file
   - If content is pasted directly, work with that
   - Support: PDFs, .docx, .md, .txt, .rtf, and similar text/document formats

2. **Identify themes and topics** by scanning for:
   - Repeated concepts or ideas
   - Section headings or structure
   - The document's primary purpose and scope
   - Key claims, arguments, or findings

3. **Output in this exact format:**

```
## Document Summary

**Key Themes:**
- [Theme 1]: [1-2 sentence explanation]
- [Theme 2]: [1-2 sentence explanation]
- [Theme 3]: [1-2 sentence explanation]
(3-5 total)

**Key Topics:**
- [Topic 1]
- [Topic 2]
- [Topic 3]
(5-10 total, concise)

**Summary:**
[2-3 sentences capturing the document's main purpose and takeaways]
```

## Tips for Quality Analysis

- **Scan first, extract later**: Get a sense of the document's structure before diving into details
- **Prioritize over exhaustiveness**: Focus on what matters most, not every detail
- **Use document structure**: If there are headings, sections, or clear organization, let that guide your theme identification
- **Be precise with language**: Avoid vague descriptions; use specific terms from the document
- **Handle length appropriately**: For brief documents, keep summaries proportional; for longer ones, synthesize across sections

## Example

**Input:** A research paper on machine learning model interpretability

**Output:**
```
## Document Summary

**Key Themes:**
- Model Interpretability: Methods for understanding how ML models make decisions and explaining their behavior to stakeholders
- Black Box Problem: The challenge that complex models like neural networks lack transparency in their decision-making processes
- Explainability Techniques: Various approaches including attention mechanisms, LIME, and SHAP for making models more interpretable

**Key Topics:**
- Neural networks
- Gradient-based explanations
- LIME (Local Interpretable Model-agnostic Explanations)
- SHAP (SHapley Additive exPlanations)
- Feature importance
- Model transparency
- Trust in AI systems

**Summary:**
This paper addresses the critical challenge of understanding how complex machine learning models make predictions. It surveys leading explainability techniques and discusses their trade-offs, emphasizing that interpretability is essential for building trustworthy AI systems in high-stakes applications.
```

---

## When to Use This Skill

✓ User says "summarize this document"  
✓ User asks "what are the key points in this PDF?"  
✓ User needs "a quick overview" of what they uploaded  
✓ User wants to understand a document's "main themes"  
✓ User asks to "break down" a document  

Don't use this for: Creating original analysis beyond what the document contains, or for tasks that require external research beyond the document itself.
