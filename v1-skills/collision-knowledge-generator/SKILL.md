---
name: collision-knowledge-generator
description: |
  Generate k structured knowledge sets designed for bisociative collision and creative idea generation. Use this skill when the user wants to prepare knowledge sets for collision-based ideation, when they ask to "build knowledge sets," "compose collision sets," "prepare knowledge for collision," "generate collision ingredients," "find knowledge domains for creative problem solving," or when they mention "knowledge set generation" in the context of creative or innovative thinking. Also triggers on: "help me find domains to collide," "what knowledge should I bring into this problem," "compose k sets of knowledge," "build the collision inputs," "find cross-domain perspectives for X," or any request to systematically identify, collect, and structure knowledge from multiple domains in preparation for creative collision. This skill focuses exclusively on the knowledge composition phase — it does NOT perform the collision itself (that is handled by the collision-idea-generator skill). If a user asks to both prepare knowledge sets AND generate ideas from them, use this skill first, then hand off to collision-idea-generator.
---

# Collision Knowledge Generator

Generate k structured knowledge sets — each a self-contained body of principles, mechanisms, and perspectives drawn from a distinct domain — engineered for maximal bisociative potential when collided against each other.

---

## Theoretical Grounding (Why This Skill Exists)

This skill operationalizes the knowledge composition phase of the Collision Loop framework. Its design rests on three experimentally supported premises:

**Premise 1 — Creativity requires collision, not accumulation.** Koestler (1964) showed that creative acts arise from the simultaneous perception of a problem through two habitually incompatible frames of reference (bisociation). Dumping all available knowledge into a single context does not produce bisociation — it produces associative thinking, which follows well-worn pathways. Knowledge must be deliberately partitioned into sets that are internally coherent but mutually incompatible.

**Premise 2 — The composition of the knowledge sets determines the quality of the collision.** Dubitzky et al. (2012) formalized the bisociation condition: two knowledge bases M₁ and M₂ are bisociatively productive when they share few concepts (low overlap) and their internal codes (governing rules) are independent. The skill enforces this condition by requiring structural analogy (the domains must address structurally similar problems) combined with surface dissimilarity (the domains must look and sound different). Surface similarity without structural analogy yields trivial recombination; structural analogy without surface dissimilarity yields routine interdisciplinary transfer. Only the conjunction of both produces genuine bisociation.

**Premise 3 — Forgetting (suppression of defaults) is a precondition for productive collision.** Storm & Patel (2014) demonstrated that thinking-induced forgetting correlates with creative output (r = .26, p = .003), and that this correlation exists only for creative (not routine) generation. Bjork & Bjork (1992) provided the mechanism: increments in storage strength are greatest when retrieval strength is low. This skill builds a Fixation Register — an explicit list of default approaches to suppress — as an integral part of knowledge set construction.

---

## When This Skill Is Used

The user provides:
- A **problem domain** or **problem statement** (what they want to generate creative ideas about).
- A value **k** — the number of knowledge sets to produce. The user sets this during the conversation.

The skill produces:
- **k knowledge sets**, each containing 3–5 specific, articulable principles expressed in the domain's native vocabulary.
- A **Fixation Register** listing the most accessible default approaches to the problem.
- A **Structural Analogy Map** explaining why each knowledge set is expected to be bisociatively productive when collided with the others.

---

## Workflow

### Phase 0: Problem Decomposition & Ontology Construction

Before generating any knowledge sets, decompose the user's problem into its structural essence.

#### 0.1 — State the Problem π

Restate the user's problem in one precise sentence. Strip ambiguity. If the problem is compound, decompose it into sub-problems; each sub-problem may warrant its own collision run.

#### 0.2 — Identify the Home Domain

Determine which field the problem "belongs to." Name the standard approaches, canonical references, and default solutions. These are candidates for the Fixation Register.

#### 0.3 — Extract the Structural Signature

This is the critical step that enables cross-domain discovery. Identify the abstract structural properties of the problem — the properties that could exist in entirely different domains. Ask:

- What type of **relationship** does this problem involve? (spatial, temporal, causal, hierarchical, network, competitive, cooperative, cyclic, etc.)
- What type of **tension or trade-off** is at the core? (accuracy vs. speed, exploration vs. exploitation, local vs. global, individual vs. collective, stability vs. adaptability, etc.)
- What type of **transformation** is sought? (classification, generation, optimization, prediction, compression, decomposition, synthesis, etc.)
- What type of **constraint** operates? (resource limits, information asymmetry, irreversibility, combinatorial explosion, etc.)

Write the structural signature as 3–5 bullet points. These bullets are the search keys for finding external domains.

#### 0.4 — Populate the Fixation Register

List the 3–5 most obvious, most accessible, most default approaches to the problem. These are what Bjork & Bjork's theory predicts will block creative thinking if not suppressed. Be precise — vague entries ("machine learning") are useless; specific entries ("fine-tuning a pre-trained transformer on domain-specific labeled data") are suppressible.

---

### Phase 1: Domain Discovery via Bilingual Research

**This phase is mandatory. Both Chinese and English sources must be consulted.** The rationale: Chinese technical communities provide distinct analytical perspectives — thorough step-by-step derivations, practical experience reports, and "why"-oriented explanations that English sources frequently omit. English sources provide canonical formulations, original papers, and formal specifications. Neither alone is sufficient for discovering the full space of structurally analogous domains.

#### 1.1 — Generate Domain Candidates

Using the structural signature from Phase 0.3, identify candidate external domains. For each structural property, ask: "What other fields deal with this exact structural property, but in a completely different surface context?"

**Method**: Conduct two rounds of research — one in Simplified Chinese, one in English — to discover domains that deal with the structural properties identified in Phase 0.3. Do not limit the search to the obvious; the value of cross-domain collision increases with surface distance.

For Chinese research, construct queries using the structural vocabulary: "X结构的问题在哪些领域出现" (in which fields do problems with X structure appear), "Y类型的权衡在什么学科中研究" (in which disciplines is the Y-type trade-off studied), etc. Extract: practical perspectives, alternative framing, domains rarely considered in the home discipline.

For English research, construct queries targeting the structural properties: "[structural property] in [candidate domain]", "[trade-off type] theory", "[transformation type] across disciplines", etc. Extract: canonical formulations, foundational principles, mathematical formalisms.

Synthesize the two rounds: identify domains that appear in both languages (high confidence), domains unique to one language (potential blind-spot coverage), and conflicting domain assignments (requiring further investigation).

**Domain diversity requirements for k sets**:

- If k ≤ 3: at least one Internal domain (a sub-discipline within the home domain that uses different methods or addresses a different aspect of the problem) and at least one External domain (a discipline outside the home domain entirely). The remaining set(s) can be either.
- If k = 4–6: at least 1 Internal, at least 2 External, and at least 1 External from a domain that would be considered "maximally distant" from the home domain (e.g., if the problem is in computer science, a maximally distant domain might be ecology, music theory, or Daoist philosophy).
- If k > 6: at least 1 Internal, at least 3 External, at least 2 maximally distant. The remaining sets fill in the spectrum between near and far.

#### 1.2 — Evaluate Bisociative Potential

For each candidate domain, evaluate its bisociative potential against the home domain using these criteria (derived from Dubitzky et al., 2012):

- **Structural Analogy Score**: Does this domain deal with a genuinely structurally similar problem? (High = good. If the analogy is only metaphorical, the domain is not suitable.)
- **Surface Dissimilarity Score**: Does this domain use a completely different vocabulary, different methods, different data types? (High = good. If the surface is similar, the collision will not produce novelty.)
- **Principle Specificity**: Can you extract 3–5 specific, articulable principles from this domain — not vague references ("biology") but concrete mechanisms ("negative feedback loops in homeostasis maintain system stability by dampening deviations from setpoints")? (Yes = proceed. No = the domain is too vague to be useful.)

Retain only domains that score well on all three criteria. The goal is not to maximize the number of domains but to maximize the quality of each knowledge set.

---

### Phase 2: Knowledge Set Construction

For each retained domain, construct a knowledge set. Each set must contain the following components:

#### 2.1 — Domain Identity

- **Domain Name**: The field or sub-field.
- **Type**: Internal (within the home domain) or External (outside it).
- **Distance**: Near, Medium, Far, or Maximally Distant (relative to the home domain).

#### 2.2 — Governing Code

The internal logic or "rules of the game" in this domain — the assumptions, axioms, or paradigms that practitioners take for granted. Write 2–3 sentences describing how practitioners in this domain think about problems. This is what Koestler calls the "code" of the matrix.

#### 2.3 — Specific Principles (3–5 per set)

Each principle must be:

- **Specific**: A concrete mechanism, law, pattern, or strategy — not a vague domain reference.
- **Expressed in native vocabulary**: Use the terminology of the source domain, not the home domain. Translation into the home domain's language is the collision's job, not the composition's job. Premature translation kills bisociative potential.
- **Sourced**: Backed by research conducted in Phase 1. If the principle comes from Chinese-language sources, note the original Chinese term alongside the English formulation. If from English sources, cite the canonical reference.
- **Independently understandable**: A reader unfamiliar with the home domain should be able to understand what this principle says within its own domain.

When formulating these principles, the AI must gather accurate and standardized information. This may require reviewing authoritative, official documents or high-quality technical blogs. Searches should be conducted in two rounds — separately in Simplified Chinese and English — and the results from both rounds should then be integrated. The integrated results must be in English.

#### 2.4 — Structural Analogy Annotation

For each knowledge set, write 1–2 sentences explaining which structural property of the home-domain problem this domain's principles map to — without performing the mapping itself. The annotation says: "This domain is relevant because its principles address [structural property X], which is structurally present in the home-domain problem." It does NOT say: "Here is how to apply this domain's principles to the problem." That application is the collision's job.

---

### Phase 3: Quality Assurance

Before delivering the k sets to the user, run these checks:

**Check 1 — Habitual Incompatibility**: For each pair of knowledge sets (i, j), verify that they share few or no concepts and that their governing codes are independent. If two sets are too similar, merge them or replace one.

**Check 2 — Fixation Register Independence**: Verify that none of the k knowledge sets simply restate or lightly rephrase entries in the Fixation Register. The purpose of the knowledge sets is to offer alternatives to the defaults, not to reinforce them.

**Check 3 — Principle Specificity**: Verify that every principle in every set is specific enough to generate a concrete design or strategy if applied literally. If a principle is too vague to act on, replace it with something more specific.

**Check 4 — Native Vocabulary Preservation**: Verify that each principle is expressed in the source domain's terminology. If any principle has already been translated into the home domain's language, revert it.

**Check 5 — Coverage of Structural Signature**: Verify that, taken together, the k sets address all of the structural properties identified in Phase 0.3. If any structural property is not addressed by any knowledge set, either add a set or modify an existing one to cover it.

---

## Output Format

Deliver the output as a structured document with the following sections:

```
# Collision Knowledge Sets for: [Problem π]

## Problem Statement
[One-sentence restatement of π]

## Structural Signature
- [Structural property 1]
- [Structural property 2]
- [Structural property 3]
...

## Fixation Register (Suppress These During Collision)
1. [Default approach 1]
2. [Default approach 2]
3. [Default approach 3]
...

## Knowledge Set 1: [Domain Name]
- Type: [Internal/External]
- Distance: [Near/Medium/Far/Maximally Distant]
- Governing Code: [2-3 sentences]
- Principles:
  1. [Principle in native vocabulary — source noted]
  2. [Principle in native vocabulary — source noted]
  3. [Principle in native vocabulary — source noted]
- Structural Analogy Annotation: [1-2 sentences]

## Knowledge Set 2: [Domain Name]
...

[Repeat for all k sets]

## Structural Analogy Map
[A summary showing which structural properties each knowledge set 
addresses, confirming full coverage]
```

---

## Critical Constraints

1. **Never hardcode specific knowledge.** This skill is a reasoning and research framework. All domain-specific content is discovered dynamically through bilingual research at runtime, based on the user's problem.

2. **Bilingual research is mandatory.** Both Chinese and English sources must be consulted for domain discovery and principle extraction. This is not optional.

3. **Principles must remain in native vocabulary.** Do not translate principles into the home domain's language. Premature translation destroys bisociative potential.

4. **The skill composes knowledge sets; it does not collide them.** The output is the raw material for collision, not the collision itself. Do not generate ideas, do not perform the mapping, do not suggest applications. That is the job of the collision-idea-generator skill.

5. **Every principle must be sourced.** If a principle cannot be traced to a credible source found during research, it must be flagged as unverified or removed.

6. **Respect the Fixation Register.** The knowledge sets exist to provide alternatives to default thinking. Any set that overlaps significantly with the Fixation Register has failed its purpose.

7. **The user controls k.** Do not impose a value of k. If the user has not specified k, ask them. If they are unsure, suggest a range: k = 3 for a focused collision, k = 5–6 for broader exploration, k > 6 for systematic coverage.

---

## Reference Files

- **[references/domain-discovery-protocol.md](references/domain-discovery-protocol.md)**: Detailed query templates for bilingual domain discovery, source quality tiers, and structural analogy detection heuristics. **Read this before starting Phase 1.**
