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

> **Theoretical anchor — This test operationalizes Koestler's core distinction.** Association links ideas within a single habitual frame; bisociation perceives a situation simultaneously through two habitually incompatible frames. The test below does not check whether the output is "good" or "creative" in general — it checks specifically whether the output *requires* the simultaneous activation of multiple frames to be generated, or whether it could have been produced by any single frame in isolation. Only outputs that pass all three questions represent the bisociative yield that the Collision Loop is designed to produce. Associative outputs may still be useful, but they should be clearly labeled as such and ranked below bisociative outputs.

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

> **Why this is the most common and most dangerous failure mode.** Sequential application *feels* productive — it generates a structured, multi-perspective analysis that appears creative. But Koestler (1964) was explicit: the creative act is not the *sum* of two perspectives but the *intersection* — the point where the two frames, held in simultaneous awareness, produce something that neither frame contains. The sum preserves each frame intact; the intersection transforms both. An LLM's default processing mode is sequential — it processes tokens left-to-right, and the natural tendency is to address each knowledge set in turn. Bisociation requires overriding this default by identifying a single problem aspect where the sets' principles *collide*, not where they *complement*.

**Fix**: Instead of applying each set's principles to the problem separately, identify the specific aspect of the problem where the sets' principles point in incompatible directions. The creative tension at that point is where bisociation happens. The idea should emerge from the tension, not from the sum.

### Failure Mode 2: Surface-Level Analogy

**Symptom**: The output says something like "Just as ants follow pheromone trails to find food, our algorithm should follow gradient signals to find the optimum."

**Diagnosis**: This is a simple analogy, not a collision. It maps one domain's mechanism directly onto the other without any transformation or creative reinterpretation. The "collision" produced no new insight — it just renamed an existing idea.

> **Why analogies are not bisociations.** An analogy maps structure from a *source* domain to a *target* domain — it has directionality. Bisociation has no directionality; neither domain is source and neither is target. Both frames are simultaneously active, and the idea emerges from the *interference* between them, not from the *mapping* of one onto the other. When the output is an analogy, what happened is that one knowledge set was used as a lens through which to re-describe the home domain — the "collision" reduced to a translation exercise. The critical question is: where does the analogy *break*? At the point of friction — where the mapping fails — lies the genuinely novel insight.

**Fix**: Look for the point of friction between the analogy and the problem. Where does the analogy break? What aspect of the problem resists the analogy? That point of resistance is where the creative idea lives. The idea should emerge from resolving the friction, not from accepting the analogy at face value.

### Failure Mode 3: Fixation Leakage

**Symptom**: Despite the Fixation Register, the output is a minor variation of a default approach. For example, if "fine-tuning a pre-trained model on labeled data" is in the Register, the output proposes "fine-tuning a pre-trained model on semi-supervised data."

**Diagnosis**: The suppression was incomplete. The reasoning process reverted to the default pattern and made a small modification to disguise it.

> **Why fixation leakage is structurally identical to the failed suppression in Storm & Patel's Experiment 2A.** When participants used studied uses as hints, thinking-induced forgetting disappeared because the studied uses were *integrated into the generation process* rather than suppressed. Fixation leakage occurs when a suppressed default is covertly integrated into the collision output — the default's structural logic survives even though its specific vocabulary has been changed. This is why the Fixation Register entries must be *specific* (Phase 0.4 of the main skill): vague entries ("use deep learning") allow the default's structural logic to survive in any of its specific instantiations. Specific entries ("fine-tune a pre-trained transformer on domain-specific labeled data") make it possible to detect when the output shares the same structural logic, even if the surface details differ.

**Fix**: Re-examine the output against every entry in the Fixation Register. For each entry, ask: "Is this output structurally the same as this default, differing only in one parameter or detail?" If yes, discard and regenerate with a more aggressive forgetting instruction: "You may not use any approach that shares the same structural logic as the suppressed approaches, even if the specific details differ."

### Failure Mode 4: Premature Translation

**Symptom**: The principles from external domains have been rephrased in the home domain's language before the collision, stripping them of their distinctive framing.

**Diagnosis**: When principles are translated prematurely, the collision cannot produce genuine surprise — the foreign perspective has already been domesticated. This is the knowledge-set equivalent of using old knowledge as hints (Storm & Patel, 2014, Experiment 2A), which eliminates thinking-induced forgetting and, with it, the creative advantage.

**Fix**: Revert the principles to their native vocabulary. The collision step is where the translation happens — organically, through the tension between incompatible frames — not before.

### Failure Mode 5: Idea Inflation

**Symptom**: The output contains many ideas, but most are trivially different from each other — variations on a theme rather than genuinely distinct approaches.

**Diagnosis**: The reasoning process found one productive collision point and then exploited it repeatedly, rather than searching for additional collision points.

> **Why idea inflation mimics the fixation problem at the output level.** Once a productive collision point is found, it becomes the new "high-accessibility default" — its retrieval strength rises rapidly, and subsequent generation gravitates toward it just as uncollided generation gravitates toward home-domain defaults. This is why progressive self-suppression (Phase 3.1 of the main skill) is essential: the first productive idea must be suppressed before the next collision attempt, forcing the process to find a *different* intersection point. Without self-suppression, the collision degenerates into a single-idea generator that produces superficial variations rather than structurally distinct approaches.

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

> **Theoretical anchor — The full mechanistic chain from Bjork & Bjork (1992) through Storm & Patel (2014).** Bjork & Bjork's New Theory of Disuse establishes that storage strength (how well-learned something is) never decays, but retrieval strength (how accessible something is right now) fluctuates. The critical interaction (Assumption 4): increments in storage strength from new learning are *largest* when retrieval strength of the related old knowledge is *low*. Storm & Patel (2014) showed the empirical correlate in creative cognition: participants who forgot more of the studied uses generated more creative new uses (r = .26, p = .003), and this correlation existed only when participants were trying to generate genuinely new uses (not when using old knowledge as hints). In the collision context: by suppressing the most recent creative output (lowering its retrieval strength), the next collision cycle operates under the condition that maximizes deep encoding of whatever it generates. The next idea is not merely "different" from the previous one — it is more deeply integrated with remote knowledge structures, because the suppression created the retrieval conditions that Bjork & Bjork's theory predicts will produce maximal storage-strength gains.

### The Synthesis Exception

In the final synthesis phase (Phase 4), all suppression is lifted. All prior ideas become accessible for clustering, cross-pollination, and integration. This mirrors the final phase of Bjork & Bjork's desirable difficulties framework: after progressive forgetting has forced maximum diversity during generation, full retrieval is restored for integration. The ideas generated under forgetting conditions are now recalled in a new context (the integration context), which produces — per Bjork & Bjork's Assumption 4 — larger increments in storage strength than if they had been accessible all along.

---

## 4. Multi-Set Collision Techniques

### Triple Collision (3 sets simultaneously)

When three knowledge sets are active, there are three pairwise intersections and one triple intersection. The triple intersection — the point where all three frames address the same aspect of the problem from three incompatible directions — is the rarest and often the most creative.

> **Theoretical anchor — Triple collision produces the highest bisociative tension because three-way incompatibility is harder to resolve than two-way.** In Koestler's framework, bisociation creates cognitive tension by forcing two incompatible codes to coexist. With three codes, the tension is tripled — the idea that resolves the three-way incompatibility must satisfy constraints from three independent rule systems simultaneously. This is why triple collisions are the most likely to produce paradigmatic (novelty ≥ 4) ideas: the only solutions that can satisfy all three frames are solutions that operate at a higher level of abstraction than any individual frame's logic.

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

> **Theoretical anchor — The progressive integration approach is not a reversion to sequential processing.** It differs from Failure Mode 1 (Sequential Application) in a critical way: at each step, the newly introduced set interacts with the *already-formed intersection* — not with each prior set individually. The intersection from steps 1–2 is itself a new cognitive structure that doesn't belong to either original set. When the third set encounters this intersection, it is encountering a novel entity, and the interaction is bisociative. Sequential application processes each set *in isolation* against the problem; progressive integration processes each new set against the *accumulated intersection*. The distinction is between "A + B + C + D" (sequential sum) and "((A∩B) ∩ C) ∩ D" (progressive intersection).

---

## 5. Evaluation Calibration

### Novelty Scale (1–5)

- **1 — Known**: This approach is standard practice in the home domain.
- **2 — Incremental**: This is a minor extension of known approaches. An expert would say "yes, that's a natural next step."
- **3 — Recombinative**: This combines elements from known approaches in a way that is not standard but could be anticipated. An expert would say "I can see how you got there."
- **4 — Unexpected**: This reframes the problem in a way that most domain experts have not considered. An expert would say "I hadn't thought of it that way."
- **5 — Paradigmatic**: This introduces a fundamentally different logic for approaching the problem. An expert would say "this changes how I think about the problem."

For retention in the final output, ideas should score ≥ 3.

> **Calibration note — The distinction between 3 (Recombinative) and 4 (Unexpected) is the boundary between associative and bisociative novelty.** A score of 3 means the idea could be *anticipated* by a domain expert who thought carefully — it is within the associative reach of the home domain. A score of 4 means the idea *reframes the problem* in a way that domain experts would not have reached through associative thought alone — it requires the intersection of an external frame to become visible. The Collision Loop's primary value lies in producing ideas that score 4–5; ideas scoring 3 are a useful byproduct but are not the target.

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

> **Theoretical anchor — Cross-pollination is bisociation at a higher level of abstraction.** The collision between collision outputs operates on the *products* of prior bisociation — entities that already represent novel intersections between domain principles. When two such entities are collided, the resulting intersection operates at a level of abstraction that is unreachable from any individual domain: it is a pattern-of-intersections, not an intersection-of-patterns. Gabora (2016) described this as "convergence in the space of possible ideas" — the creative output itself becomes a new conceptual entity that can participate in further creative recombination. This is structurally identical to Koestler's observation that bisociation can operate recursively: the product of one bisociation becomes a matrix that can participate in the next. The most paradigmatic ideas in any collision run typically emerge here, because the input material has already been filtered (only ideas scoring ≥ 3 on all dimensions survive to this phase), and the collision operates at the level of structural mechanisms rather than domain-specific principles, producing more general and more powerful ideas.

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

> **Theoretical anchor — Bilingual verification is the final anti-fixation safeguard.** Even after all the forgetting, suppression, and collision engineering, the final output must be tested against reality. An idea that "feels novel" within the collision context may already exist in a literature the collision process did not access. The bilingual search serves the same function as Storm & Patel's experimental condition that contrasted creative generation with routine generation: it distinguishes between ideas that are *genuinely* new (the creative condition) and ideas that are merely *unfamiliar to the reasoner* (the routine condition dressed in unfamiliar vocabulary). Only ideas confirmed as novel by bilingual search represent genuine creative output; all others are rediscoveries — valuable for validation but not for the novelty portfolio.
