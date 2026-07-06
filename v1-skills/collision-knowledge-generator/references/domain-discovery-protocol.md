# Domain Discovery Protocol

Detailed guidance for the bilingual domain discovery and principle extraction phases of the Collision Knowledge Generator.

---

## Table of Contents

1. [Structural Signature Extraction Heuristics](#1-structural-signature-extraction-heuristics)
2. [Chinese Research Templates](#2-chinese-research-templates)
3. [English Research Templates](#3-english-research-templates)
4. [Source Quality Tiers](#4-source-quality-tiers)
5. [Structural Analogy Detection](#5-structural-analogy-detection)
6. [Principle Extraction Standards](#6-principle-extraction-standards)
7. [Synthesis Rules](#7-synthesis-rules)

---

## 1. Structural Signature Extraction Heuristics

The structural signature is the bridge between the home domain and all candidate external domains. Extracting it well is the single most important step in the entire skill.

### What Makes a Good Structural Property

A structural property is good if it is **abstract enough to exist in multiple domains** but **specific enough to constrain the search**. 

- Too abstract: "This problem involves optimization." (Almost every problem involves optimization. This does not narrow the search.)
- Too specific: "This problem involves optimizing the learning rate schedule of an Adam optimizer." (This exists only in deep learning. No external domain addresses this exact thing.)
- Just right: "This problem involves balancing the rate of exploration against the rate of exploitation under a fixed time budget." (This exists in reinforcement learning, evolutionary biology, venture capital, military strategy, foraging theory, pharmaceutical R&D, etc.)

### Extraction Procedure

For each problem, extract structural properties across five dimensions:

1. **Relationship Structure**: What entities interact, and how? (network, hierarchy, sequence, field, competition, symbiosis, flow, etc.)
2. **Core Trade-off**: What tension drives the problem? (accuracy vs. speed, local vs. global, depth vs. breadth, stability vs. adaptability, individual vs. collective, short-term vs. long-term, etc.)
3. **Transformation Goal**: What change is sought? (classification, generation, optimization, compression, decomposition, synthesis, alignment, translation, prediction, control, etc.)
4. **Constraint Architecture**: What limits the solution space? (resource scarcity, information asymmetry, irreversibility, combinatorial explosion, noise, partial observability, non-stationarity, etc.)
5. **Temporal Dynamics**: How does the problem evolve? (static, cyclical, progressive, phase-transitional, decaying, accumulative, etc.)

Not every dimension will be relevant to every problem. Extract 3–5 properties total, choosing the dimensions that most sharply characterize the problem.

---

## 2. Chinese Research Templates

Chinese technical communities excel at: practical experience reports, "why"-oriented explanations, step-by-step derivations, and alternative approaches not prominent in English discourse.

### Query Construction Templates

For domain discovery:
- "[结构属性] 在哪些领域/学科中出现" — In which fields/disciplines does [structural property] appear
- "[核心权衡] 问题在什么领域有研究" — In which fields is the [core trade-off] problem studied
- "[转换目标] 的跨学科方法" — Cross-disciplinary methods for [transformation goal]
- "类似 [抽象问题描述] 的问题在其他领域" — Problems similar to [abstract problem description] in other fields

For principle extraction from a specific domain:
- "[领域名] 的核心原理/机制" — Core principles/mechanisms of [domain name]
- "[领域名] 中 [结构属性] 是如何处理的" — How is [structural property] handled in [domain name]
- "[领域名] 最新进展 权威综述" — Latest developments in [domain name], authoritative reviews

### Preferred Chinese Platforms

- Zhihu (知乎): Expert explanations, practical insights, "why" answers
- CSDN / 博客园: Technical implementation details, step-by-step guides
- Chinese academic databases (CNKI 知网, Wanfang 万方): Peer-reviewed Chinese-language research
- WeChat public accounts (微信公众号) of university research groups: Latest research summaries

### What to Extract from Chinese Sources

- Practical implementation experience and failure cases
- "Why"-oriented explanations — especially phrases like:
  - "本质上是..." (essentially is...)
  - "直觉上..." (intuitively...)
  - "背后的原因是..." (the reason behind this is...)
  - "这个方法的关键在于..." (the key to this method is...)
- Alternative approaches not prominent in English discourse
- Cross-disciplinary connections made by Chinese researchers

---

## 3. English Research Templates

English sources provide: canonical formulations, original papers, official documentation, mathematical formalisms, and formal specifications.

### Query Construction Templates

For domain discovery:
- "[structural property] in [candidate domain]"
- "[core trade-off] theory applications"
- "domains dealing with [abstract problem description]"
- "[transformation goal] across disciplines survey"
- "structural analogy [home domain] [candidate domain]"

For principle extraction from a specific domain:
- "[domain name] fundamental principles mechanisms"
- "[domain name] [structural property] review survey"
- "[domain name] canonical formulation textbook"

### Preferred English Platforms

- Google Scholar: Peer-reviewed papers, citation tracking
- Semantic Scholar: AI-powered paper discovery
- arXiv: Preprints in STEM fields
- Domain-specific authoritative sources (textbooks, handbooks, official documentation)
- High-quality technical blogs from recognized experts or institutions

### What to Extract from English Sources

- Authoritative definitions and canonical formulations
- Original papers and the authors' stated motivations
- Mathematical properties, proofs, and formal guarantees
- Benchmarks, empirical evidence, and comparative analyses
- Named principles, laws, or theorems with precise formulations

---

## 4. Source Quality Tiers

When evaluating sources, apply this hierarchy:

**Tier 1 (Highest reliability)**:
- Peer-reviewed journal articles in top venues
- Official documentation and specifications
- Textbooks from recognized authorities
- Standards and RFCs

**Tier 2 (High reliability)**:
- Conference papers in top venues
- Technical reports from reputable institutions
- Books by recognized domain experts

**Tier 3 (Moderate reliability)**:
- Well-regarded technical blogs (e.g., Distill.pub, institution-affiliated blogs)
- Expert answers on curated platforms (e.g., high-reputation Zhihu answers, Stack Exchange)
- Preprints with institutional affiliations

**Tier 4 (Use with caution)**:
- General blog posts
- Forum discussions
- Social media posts
- Sources without clear authorship

For principle extraction, prefer Tier 1–2 sources. Tier 3 is acceptable for practical insights and alternative perspectives. Tier 4 should only be used to generate leads for further investigation, never as the sole source of a principle.

---

## 5. Structural Analogy Detection

### The Structural Analogy Test

A candidate domain has structural analogy with the home domain if and only if:

1. **There exists a mapping** from the entities and relationships in the home-domain problem to entities and relationships in the candidate domain, such that:
   - The mapped relationships are the same type (e.g., both are competitive exclusion, both are resource allocation under scarcity, both are signal propagation through a noisy channel).
   - The mapped entities play the same structural roles (e.g., both are agents competing for a finite resource, even if one domain's agents are firms and the other's are species).

2. **The mapping is non-trivial**: The two domains do not share a common parent discipline at a low level of abstraction. (If both are sub-fields of the same parent, the analogy is too close to be useful for bisociation.)

3. **The mapping is actionable**: Principles from the candidate domain, when applied through the mapping, would suggest concrete strategies or designs for the home-domain problem — not just vague inspirations.

### Common Structural Analogy Pairs

These are examples to prime the search, not an exhaustive list. The AI should discover domain-specific analogies dynamically for each problem.

- **Optimization under constraints** ↔ ecology (foraging theory), economics (resource allocation), logistics (vehicle routing), materials science (energy minimization)
- **Network construction** ↔ neuroscience (connectomics), social network analysis, transportation engineering, mycorrhizal networks in forest ecology
- **Signal detection in noise** ↔ radar engineering, epidemiology (outbreak detection), financial fraud detection, immune system pattern recognition
- **Multi-scale phenomena** ↔ physics (renormalization group), fractal geometry, urban planning (neighborhood → city → region), genomics (nucleotide → gene → chromosome → genome)
- **Cooperation vs. defection** ↔ game theory, evolutionary biology (mutualism vs. parasitism), international relations, microbiome ecology

---

## 6. Principle Extraction Standards

### What Counts as a Principle

A principle is a specific, articulable statement about how something works in a domain. It must be:

- **Falsifiable**: It makes a claim that could, in principle, be wrong.
- **Actionable**: It suggests a concrete strategy, mechanism, or design pattern.
- **Non-trivial**: It conveys genuine domain expertise, not common sense.

### Examples of Good vs. Bad Principles

**Bad** (too vague): "Ecology studies how organisms interact with their environment."
**Good**: "Competitive exclusion principle (Gause, 1934): two species competing for the same limiting resource cannot coexist indefinitely; the superior competitor will eventually displace the other — unless they differentiate their niches."

**Bad** (too home-domain-specific): "Gradient descent converges to local minima in non-convex landscapes."
**Good** (from a structural-analogy domain): "Simulated annealing (Kirkpatrick et al., 1983): accepting worse solutions with a probability that decreases over time allows escape from local optima — the 'temperature' parameter controls the trade-off between exploration and exploitation."

**Bad** (already translated into home-domain language): "We should use a divide-and-conquer approach like cells do."
**Good** (in native vocabulary): "Cellular compartmentalization: eukaryotic cells partition biochemical reactions into membrane-bound organelles, allowing incompatible reactions (e.g., protein synthesis and protein degradation) to proceed simultaneously without interference. Each compartment maintains its own chemical environment."

### Principle Count

Each knowledge set must contain 3–5 principles. Fewer than 3 leaves the set too thin for productive collision. More than 5 risks diluting the set's internal coherence.

---

## 7. Synthesis Rules

After both research rounds are complete, synthesize the findings:

1. **Identify convergence**: Where do Chinese and English sources agree on a domain's structural relevance? High convergence increases confidence in the domain's bisociative potential.

2. **Identify divergence**: Where do they disagree or emphasize different aspects? Divergence often reveals that a domain has more nuance than either community alone has captured — this is valuable.

3. **Fill gaps**: Did one language's sources discover domains that the other missed? Merge the coverage.

4. **Resolve conflicts**: When sources directly conflict on whether a domain has structural analogy with the home domain, apply the Structural Analogy Test (Section 5) rigorously. If resolution is not possible, include the domain but flag the uncertainty.

5. **Integrate**: The final output is in English, but it carries the combined depth of both research rounds. When a principle originates from or is enriched by Chinese-language sources, note the original Chinese terminology alongside the English formulation.
