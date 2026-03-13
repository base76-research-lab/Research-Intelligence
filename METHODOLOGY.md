# How an Epistemic Brief is Produced

> This document describes the methodology behind Base76 Epistemic Briefs — for clients who want to understand the process, and for researchers who may collaborate on future briefs.

---

## The Five-Step Process

### Step 1: Question Analysis

Before any research begins, we deconstruct the client's question.

Most questions contain hidden assumptions, ambiguous terms, or scope problems that would cause any answer to miss the point. We make these explicit first.

**Output:** A restated operational question that all parties agree on.

**Example:** "Can we use AI in our clinical workflow?" becomes *"Can a 7B-parameter LLM, deployed in a specific triage workflow with human oversight, achieve sufficient calibration to avoid increasing patient harm risk under EU AI Act Art. 13?"*

---

### Step 2: Literature and Evidence Scan

A systematic scan of relevant sources — not a keyword dump.

**Sources used:**
- Academic literature (Semantic Scholar, arXiv, PubMed)
- Primary regulatory documents (EU AI Act, ISO standards)
- Technical documentation (model cards, benchmark reports)
- Internal Base76 experimental data (flagged explicitly as internal)

**What we do not do:** cite sources to appear thorough. Every source must justify its inclusion.

---

### Step 3: Epistemic Evaluation

Each source and each claim is assigned a **confidence score (0.0–1.0)** based on:

| Factor | Weight |
|---|---|
| Peer review status | High |
| Sample size / replication | High |
| Relevance to the specific question | High |
| Recency | Medium |
| Author/institutional track record | Medium |
| Internal vs. external data | Explicit flag |

**Knowledge gaps are named explicitly.** If the evidence does not exist, we say so — and explain why the gap matters.

---

### Step 4: Mechanistic Analysis

We go beyond *what* the evidence shows to explain *why*.

This is the layer that distinguishes an Epistemic Brief from a literature review. We draw on:

- Base76's mechanistic interpretability research (residual state geometry, RLHF dynamics, Field View reliability signal)
- Systems-level analysis of failure modes
- Architectural constraints vs. implementation choices

**If the root cause is architectural** (e.g., RLHF epistemic variance collapse in small models), fine-tuning alone will not fix it. We say that.

---

### Step 5: CognOS Proof-Engine — Source Chain and Audit Trail

Every claim in the brief is indexed and linked to its source via the [CognOS proof-engine](https://github.com/base76-research-lab/cognos-proof-engine).

This produces:
- A numbered source chain (every assertion traceable to evidence)
- A confidence envelope per section
- An audit-ready format compatible with EU AI Act documentation requirements

---

## Output Formats

| Format | Purpose |
|---|---|
| **Markdown (.md)** | Primary format — version-controlled, diff-friendly, archival |
| **Interactive HTML** | Client handoff — dark academic design, confidence score visualizations, badge system |
| **PDF** | Formal delivery — print-ready, signable |

All three formats are generated from the same source. No content divergence.

---

## Time and Cost Structure

A typical Epistemic Brief requires:

| Activity | Time |
|---|---|
| Question analysis and scope call | 1–2h |
| Literature scan | 2–4h |
| Epistemic evaluation and gap analysis | 1–2h |
| Mechanistic analysis | 1–2h |
| Writing, confidence scoring, source chain | 1–2h |
| Review and formatting (three formats) | 1h |
| **Total** | **7–13h** |

Delivery commitment: **48–72 hours** from confirmed brief scope.

---

## Confidence Score Framework

All confidence scores use a 0.0–1.0 scale:

| Score | Meaning |
|---|---|
| 0.90–1.00 | Strong consensus, multiple independent replications, primary sources |
| 0.75–0.89 | Solid evidence, minor gaps or recency limitations |
| 0.60–0.74 | Promising but limited replication or indirect evidence |
| Below 0.60 | Speculative, single-source, or internal-only — flagged explicitly |

An overall brief confidence score is computed as a weighted average across sections.

---

## What We Do Not Do

- **We do not simulate certainty.** If the evidence is thin, the confidence score reflects that.
- **We do not write to please.** A brief with verdict BLOCK is as valuable as one with PASS.
- **We do not confuse benchmark performance with real-world validity.** These are different things and we explain why.
- **We do not deliver without a source chain.** Every claim is traceable.

---

*Base76 Research Intelligence — bjorn@base76.se*
