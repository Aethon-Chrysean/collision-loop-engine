# Collision Execution Guide

Detailed guidance for executing the bisociative collision, avoiding common failure modes, and maximizing the creative yield of each collision cycle.

---

## Table of Contents

1. [The Bisociation Test](#1-the-bisociation-test)
2. [Common Failure Modes](#2-common-failure-modes)
3. [The Forgetting Mechanism in Practice](#3-the-forgetting-mechanism-in-practice)
4. [Multi-Set Collision Techniques](#4-multi-set-collision-techniques)
5. [Evaluation Calibration](#5-evaluation-calibration)
6. [Cross-Pollination Protocol](#6-cross-pollination-protocol)
7. [Bilingual Novelty Verification](#7-bilingual-novelty-verification)

---

## 1. The Bisociation Test

After generating a pre-inventive structure, apply this test to determine whether it is a genuine bisociative product or merely an associative one:

**Question 1**: Can this idea be derived from a single knowledge set alone?
- If yes → it is associative, not bisociative. It may still be useful, but it is not the kind of idea this skill is designed to produce. Flag it as "single-set derivable" and prioritize ideas that fail this test (i.e., ideas that truly require multiple sets).

**Question 2**: Does this idea require understanding the interaction between principles from different sets, or does it merely apply one set's principle while ignoring the others?
- If the idea only uses one set → it is a domain transfer, not a collision. It may be novel to the home domain, but it is not bisociative.
- If the idea requires understanding how principles from different sets interact, constrain each other, or create something that neither set alone would suggest → it is bisociative. These are the highest-value ideas.

**Question 3**: Would this idea surprise an expert in any one of the contributing knowledge sets?
- If an expert in set A would say "that's obvious" and an expert in set B would also say "that's obvious" → the idea is not bisociative. It is a known intersection.
- If an expert in set A would say "I never would have thought of framing it that way" → the idea is bisociative from set A's perspective.
- If experts in all contributing sets would be surprised → the idea is maximally bisociative.

---

## 2. Common Failure Modes

### Failure Mode 1: Sequential Application

**Symptom**: The output reads like "From the perspective of ecology, we could do X. From the perspective of game theory, we could do Y. Combining these, we could do X+Y."

**Diagnosis**: This is comparative analysis, not bisociation. The two perspectives were applied sequentially and then stapled together.

**Fix**: Instead of applying each set's principles to the problem separately, identify the specific aspect of the problem where the sets' principles point in incompatible directions. The creative tension at that point is where bisociation happens. The idea should emerge from the tension, not from the sum.

### Failure Mode 2: Surface-Level Analogy

**Symptom**: The output says something like "Just as ants follow pheromone trails to find food, our algorithm should follow gradient signals to find the optimum."

**Diagnosis**: This is a simple analogy, not a collision. It maps one domain's mechanism directly onto the other without any transformation or creative reinterpretation. The "collision" produced no new insight — it just renamed an existing idea.

**Fix**: Look for the point of friction between the analogy and the problem. Where does the analogy break? What aspect of the problem resists the analogy? That point of resistance is where the creative idea lives. The idea should emerge from resolving the friction, not from accepting the analogy at face value.

### Failure Mode 3: Fixation Leakage

**Symptom**: Despite the Fixation Register, the output is a minor variation of a default approach. For example, if "fine-tuning a pre-trained model on labeled data" is in the Register, the output proposes "fine-tuning a pre-trained model on semi-supervised data."

**Diagnosis**: The suppression was incomplete. The reasoning process reverted to the default pattern and made a small modification to disguise it.

**Fix**: Re-examine the output against every entry in the Fixation Register. For each entry, ask: "Is this output structurally the same as this default, differing only in one parameter or detail?" If yes, discard and regenerate with a more aggressive forgetting instruction: "You may not use any approach that shares the same structural logic as the suppressed approaches, even if the specific details differ."

### Failure Mode 4: Premature Translation

**Symptom**: The principles from external domains have been rephrased in the home domain's language before the collision, stripping them of their distinctive framing.

**Diagnosis**: When principles are translated prematurely, the collision cannot produce genuine surprise — the foreign perspective has already been domesticated. This is the knowledge-set equivalent of using old knowledge as hints (Storm & Patel, 2014, Experiment 2A), which eliminates thinking-induced forgetting and, with it, the creative advantage.

**Fix**: Revert the principles to their native vocabulary. The collision step is where the translation happens — organically, through the tension between incompatible frames — not before.

### Failure Mode 5: Idea Inflation

**Symptom**: The output contains many ideas, but most are trivially different from each other — variations on a theme rather than genuinely distinct approaches.

**Diagnosis**: The reasoning process found one productive collision point and then exploited it repeatedly, rather than searching for additional collision points.

**Fix**: After generating the first idea from a collision pair, add its structural mechanism to the temporary suppression list for the remainder of that cycle. Force the next idea to use a different intersection point.

---

## 3. The Forgetting Mechanism in Practice

### What Gets Suppressed and When

The Fixation Register operates in layers:

**Layer 1 — Default approaches (permanent throughout the run)**:
These are the 3–5 most obvious, most accessible approaches to the problem. They are suppressed from cycle 1 onward and never unsuppressed.

**Layer 2 — Own outputs (cumulative)**:
Each cycle's highest-scored idea is added to the suppression list. This list grows with each cycle, ensuring progressive forgetting of one's own creative outputs.

**Layer 3 — Cycle-specific suppression (temporary)**:
Within a single cycle, after the first idea is generated, its structural mechanism is temporarily suppressed to force the generation of structurally distinct ideas. This suppression is lifted at the start of the next cycle.

### Why Progressive Forgetting Matters

Bjork & Bjork's New Theory of Disuse explains the mechanism: storage strength (how well-learned something is) never decays, but retrieval strength (how accessible something is right now) fluctuates. When retrieval strength is low, increments to storage strength from new learning are largest. In the collision context: by suppressing the most recent creative output, we lower its "retrieval strength" in the reasoning process, which means the next creative output is encoded more deeply — it is more likely to be genuinely different, rather than a variation on the previous idea.

Storm et al. (2014) showed the empirical correlate: participants who forgot more of the studied uses generated more creative new uses (r = .26, p = .003), and this correlation existed only when participants were trying to generate genuinely new uses (not when using old knowledge as hints).

### The Synthesis Exception

In the final synthesis phase (Phase 4), all suppression is lifted. All prior ideas become accessible for clustering, cross-pollination, and integration. This mirrors the final phase of Bjork & Bjork's desirable difficulties framework: after progressive forgetting has forced maximum diversity during generation, full retrieval is restored for integration. The ideas generated under forgetting conditions are now recalled in a new context (the integration context), which produces — per Bjork & Bjork's Assumption 4 — larger increments in storage strength than if they had been accessible all along.

---

## 4. Multi-Set Collision Techniques

### Triple Collision (3 sets simultaneously)

When three knowledge sets are active, there are three pairwise intersections and one triple intersection. The triple intersection — the point where all three frames address the same aspect of the problem from three incompatible directions — is the rarest and often the most creative.

**Procedure**:
1. First, identify the pairwise intersections (A∩B, A∩C, B∩C). These are the entry points.
2. Then, ask: "Is there a single point where all three frames converge? Where does the problem look the same from all three perspectives, but the three perspectives suggest incompatible responses?"
3. The triple-intersection idea, if it exists, is a synthesis that resolves the three-way incompatibility. It is often more robust than pairwise ideas because it has been forced to satisfy constraints from three domains.

### Quadruple+ Collision (4+ sets simultaneously)

With more than three sets active, the cognitive load becomes extreme. Instead of looking for a single intersection of all sets, use a progressive integration approach:

1. Start with the two most distant sets. Find their intersection.
2. Introduce the third set. Ask: "Does this third set reinforce the intersection, redirect it, or contradict it?" Each response generates a different idea.
3. Introduce the fourth set. Same question.
4. After all sets are introduced, ask: "What is the single idea that best satisfies all constraints — even if it satisfies none of them perfectly?"

The final step is crucial: the idea that "satisfies none perfectly but addresses all" is typically the most novel, because it cannot be derived from any single domain's logic.

---

## 5. Evaluation Calibration

### Novelty Scale (1–5)

- **1 — Known**: This approach is standard practice in the home domain.
- **2 — Incremental**: This is a minor extension of known approaches. An expert would say "yes, that's a natural next step."
- **3 — Recombinative**: This combines elements from known approaches in a way that is not standard but could be anticipated. An expert would say "I can see how you got there."
- **4 — Unexpected**: This reframes the problem in a way that most domain experts have not considered. An expert would say "I hadn't thought of it that way."
- **5 — Paradigmatic**: This introduces a fundamentally different logic for approaching the problem. An expert would say "this changes how I think about the problem."

For retention in the final output, ideas should score ≥ 3.

### Feasibility Scale (1–5)

- **1 — Speculative**: Requires technology, data, or infrastructure that does not currently exist and has no clear path to existence.
- **2 — Aspirational**: Requires significant new development (months to years) but the path is identifiable.
- **3 — Challenging**: Requires non-trivial engineering or research but could be attempted with current tools and a dedicated effort.
- **4 — Practical**: Could be implemented as a concrete project with existing tools and data.
- **5 — Immediate**: Could be implemented now with minimal additional effort.

For retention, ideas should score ≥ 3 unless the user explicitly requests speculative ideas.

### Value Scale (1–5)

- **1 — Artificial**: Solves a problem that does not exist in practice.
- **2 — Marginal**: Addresses a real problem but the improvement over current approaches would be negligible.
- **3 — Meaningful**: Addresses a recognized limitation of current approaches and would produce noticeable improvement.
- **4 — Significant**: Addresses a major pain point or failure mode. Domain experts would immediately recognize the value.
- **5 — Transformative**: Would fundamentally change how the problem is approached, unlocking capabilities that current approaches cannot provide.

For retention, ideas should score ≥ 3.

---

## 6. Cross-Pollination Protocol

Cross-pollination (Phase 4.3) is a second-order collision: the collision outputs themselves become the inputs for a new collision. This is where the most powerful ideas often emerge.

### Procedure

1. Take the clusters from Phase 4.2.
2. For each pair of clusters (C_i, C_j):
   - Identify the structural mechanism that defines each cluster.
   - Ask: "If the mechanism from C_i operated within the framework of C_j, what would happen? And vice versa?"
   - Ask: "Is there a meta-idea that encompasses both mechanisms — a higher-order principle that subsumes both clusters?"
3. Record any ideas that emerge. These are second-order ideas.
4. Subject them to the same evaluation filters (novelty, feasibility, value).
5. If a second-order idea scores higher than any first-order idea, it should be ranked accordingly.

### Why This Works

The collision between collision outputs operates at a higher level of abstraction than the original collisions. The first-order collisions produced ideas grounded in specific domain principles. The second-order collision finds structural commonalities between ideas from different collision pairs, which is structurally analogous to what Gabora (2016) calls "convergence in the space of possible ideas" — the creative output itself becomes a new conceptual entity that can participate in further creative recombination.

---

## 7. Bilingual Novelty Verification

### Why Both Languages Are Required

A proposed idea may appear novel in English-language literature but have been explored in Chinese-language publications (or vice versa). This is particularly common in fields where Chinese and English research communities have developed partially independent literatures.

### Verification Procedure

For each idea that passes the initial novelty filter:

**Chinese verification round**:
- Search for the proposed approach using the home domain's Chinese vocabulary.
- Search for it using the external domain's Chinese vocabulary.
- Search for it using the abstract mechanism's description in Chinese.
- Check: 知网 (CNKI), 万方, Zhihu (知乎), CSDN, Baidu Scholar.

**English verification round**:
- Search for the proposed approach using the home domain's English vocabulary.
- Search for it using the external domain's English vocabulary.
- Search for it using the abstract mechanism's description.
- Check: Google Scholar, Semantic Scholar, arXiv, domain-specific databases.

**Synthesis**:
- If found in neither language → strong novelty evidence.
- If found in one language but not the other → may be novel in one community. Note the finding. Consider whether the Chinese-language prior work has been published in or translated to English (or vice versa). If truly unknown in one community, the idea may still have value as a cross-language knowledge transfer.
- If found in both languages → not novel. Discard or flag as "existing approach rediscovered through collision" (which still has value as validation of the collision framework, but should not be presented as a novel idea).
