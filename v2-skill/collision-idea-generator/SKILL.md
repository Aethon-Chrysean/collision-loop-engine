---
name: collision-idea-generator
description: |
  Generate creative ideas by colliding k knowledge sets provided by the user, using the bisociation-based Collision Loop. Use this skill when the user provides two or more knowledge sets and wants to generate novel ideas, solutions, or approaches from their collision. Triggers on: "collide these knowledge sets," "generate ideas from collision," "run the collision loop," "bisociate these sets," "what ideas emerge from colliding X and Y," "perform collision," "generate creative solutions from these perspectives," "run the collision," or any request to produce novel ideas by simultaneously perceiving a problem through multiple knowledge frameworks. Also triggers when a user has already prepared knowledge sets (manually or via the collision-knowledge-generator skill) and wants the creative output. Does NOT trigger for knowledge set composition/generation — that is handled by collision-knowledge-generator. If the user asks for both, this skill expects the knowledge sets as input and proceeds to collision.
---

# Collision Idea Generator

Generate genuinely novel ideas by engineering bisociative collisions between k knowledge sets. The collision is not sequential comparison — it is the simultaneous perception of a problem through multiple habitually incompatible frames, forcing intersection points that none of the individual sets would produce alone.

---

## Theoretical Grounding (Why This Skill Exists)

This skill operationalizes the collision, evaluation, and synthesis phases of the Collision Loop framework. Its design rests on the following experimentally supported mechanisms:

**Mechanism 1 — Bisociation, not association.** Koestler (1964) distinguished between association (linking ideas within a single habitual frame) and bisociation (perceiving a situation simultaneously through two or more habitually incompatible frames). Ordinary thinking operates by association — it follows well-worn pathways. Creative thinking requires bisociation — the temporary maintenance of incompatible logical frameworks in the same cognitive space. This skill enforces bisociation by presenting all k sets simultaneously and instructing the reasoning process to find intersections, not sequential applications.

**Mechanism 2 — The Geneplore cycle structures the collision.** Finke, Ward, and Smith (1992) proposed that creative cognition alternates between generation (producing raw "pre-inventive structures" that are novel, ambiguous, and emergent but not yet refined) and exploration (interpreting, testing, refining, and evaluating those structures). The collision produces pre-inventive structures; the evaluation refines them. This skill explicitly separates these phases.

**Mechanism 3 — Forgetting enables creative generation.** Storm & Patel (2014) showed that when participants attempted to generate genuinely new uses for objects, the studied uses were forgotten — and participants who forgot more generated more creative outputs. The critical boundary condition: forgetting did not occur when participants used old knowledge as hints. This skill implements forgetting through the Fixation Register: a list of default approaches that are explicitly suppressed during the collision, preventing the reasoning process from reverting to habitual patterns.

**Mechanism 4 — Retrieval reconfiguration deepens new learning.** Bjork & Bjork (1992) showed that increments in storage strength are greatest when retrieval strength is low. Applied to collision: when the most accessible knowledge is suppressed (low retrieval strength), any new idea generated from the collision is encoded more deeply, integrated with more remote knowledge structures, and more likely to be genuinely novel. Each collision cycle's best idea is added to the Fixation Register for subsequent cycles, ensuring progressive forgetting of one's own outputs.

---

## When This Skill Is Used

The user provides:
- **k knowledge sets**, each containing domain identity, governing code, and specific principles (typically 3–5 per set). These may come from the collision-knowledge-generator skill, from the user's own preparation, or be stated informally in conversation.
- A **problem statement** (what they want creative ideas about).
- Optionally, a **Fixation Register** (default approaches to suppress). If not provided, the skill constructs one.

The value of k is determined by how many knowledge sets the user provides. The skill adapts its collision protocol to the value of k.

The skill produces:
- **Ranked creative ideas**, each accompanied by: the collision pair(s) that generated it, its novelty-feasibility-value assessment, a concrete description, and the specific limitation of current approaches it addresses.

---

## Workflow

### Phase 0: Input Validation & Fixation Register

#### 0.1 — Validate the Knowledge Sets

For each of the k knowledge sets, verify:
- It has an identifiable domain and governing code (even if stated informally).
- It contains at least 2 articulable principles (3–5 is ideal).
- The principles are expressed in the source domain's native vocabulary, not pre-translated into the home domain.

If any set is incomplete, ask the user to supplement it or attempt to reconstruct it via bilingual research (Chinese + English rounds, integrated results in English). Gathering accurate information may require reviewing authoritative, official documents or high-quality technical blogs.

> **Theoretical anchor — Native vocabulary is not a stylistic preference; it is a precondition for bisociation.** Storm & Patel (2014, Experiment 2A) established the critical boundary condition: when participants used studied uses as *hints* to guide generation, thinking-induced forgetting disappeared entirely (d = 0.02, p = .89), and creative output dropped to the level of the common-uses condition. A principle that has been pre-translated into the home domain's vocabulary functions as a "hint" — it has already been assimilated into the home domain's frame of reference, so the inhibitory process that clears space for novelty is never activated. If any principle arrives pre-translated, the collision involving that principle will produce associative transfer (applying one domain's known solution using the other domain's language) rather than bisociative intersection (generating something neither domain would produce alone). Flag pre-translated principles and either revert them to native vocabulary or note the compromised bisociative potential.

#### 0.2 — Construct or Validate the Fixation Register

If the user provided a Fixation Register, verify that it lists specific, suppressible approaches (not vague categories). If no Register was provided, construct one:

1. Identify the home domain of the problem.
2. Search for standard/default approaches to this type of problem — bilingual research, Chinese round first, then English round, synthesize.
3. List the 3–5 most accessible default approaches. These are now suppressed.

> **Theoretical anchor — The Fixation Register is an engineered retrieval reconfiguration.** Bjork & Bjork's (1992) New Theory of Disuse distinguishes between storage strength (how deeply knowledge is encoded — it never decays) and retrieval strength (how accessible knowledge is right now — it fluctuates with use, disuse, and interference). The Fixation Register does not delete default approaches from the reasoning process; it lowers their retrieval strength by explicit instruction. This matters because Bjork & Bjork's critical finding (Assumption 4) is that increments in storage strength from new learning are *largest* when the related old knowledge has low retrieval strength. By suppressing the defaults, the Register doesn't just clear space — it creates the optimal encoding conditions for whatever the collision produces. The new ideas generated under suppression will be more deeply integrated with remote knowledge structures than ideas generated with defaults fully accessible. This is why the Register must be constructed before the collision begins, not during it.

#### 0.3 — Determine the Collision Schedule

The collision protocol adapts to k:

**For k = 2**: A single collision pair. Run 3 collision cycles with progressive forgetting (each cycle's best idea is suppressed in the next).

**For k = 3**: Run pairwise collisions for all ${k \choose 2} = 3$ pairs, then one triple-collision cycle where all three sets are active simultaneously.

**For k = 4–6**: Organize into phases:
- *Phase A — Pairwise Exploration*: Select the 3–4 most promising pairs (based on structural distance — the most distant pairs first). Run one collision cycle per pair.
- *Phase B — Multi-set Intensification*: Combine the 2–3 most productive pairs into triple or quadruple collisions. Run one cycle per combination.
- *Phase C — Full Collision*: All k sets active simultaneously. Run one cycle with maximum forgetting (suppress all defaults AND all prior best ideas).

**For k > 6**: Same structure as k = 4–6, but increase the number of pairwise explorations in Phase A and be more selective about which combinations advance to Phase B.

> **Theoretical anchor — The schedule structures the Geneplore cycle across collision runs.** Finke, Ward, and Smith's (1992) Geneplore model describes creativity as alternating between *generation* (producing raw pre-inventive structures) and *exploration* (interpreting, testing, and refining them). The collision schedule implements this alternation at the macro level: pairwise exploration generates a diverse set of intersection points (generation-dominant), multi-set intensification deepens the most promising ones (exploration-dominant), and the full collision forces a final integrative generation where all frames must co-activate simultaneously. Ordering from most-distant pairs first is deliberate — distant collisions are more likely to produce paradigmatic (novelty ≥ 4) ideas but are also more likely to be sterile. Running them first ensures that the most novel possibilities are explored before the narrowing that intensification produces, and any sterile collisions are quickly rotated past rather than belabored.

---

### Phase 1: Collision — Generate Pre-Inventive Structures

This is the core creative operation. For each collision cycle, follow these steps exactly:

#### 1.1 — Set Up the Collision Context

Assemble the active knowledge sets for this cycle. Restate the problem in general terms — abstract enough that all active sets can address it, but specific enough that the resulting ideas will be actionable.

> **Theoretical anchor — The problem restatement creates the shared event L.** Koestler (1964) described bisociation as the perception of "a situation or idea, L, in two self-consistent but habitually incompatible frames of reference, M₁ and M₂." The event L is what the frames share — it is the point where they can both "look at" the same thing, even though they see it differently. The problem restatement is the construction of L. If the restatement is too specific to the home domain, only the home-domain-adjacent knowledge sets can perceive it (no bisociation with distant sets). If too abstract, the sets perceive different things and the collision produces no intersection. The restatement must be calibrated to the *structural level* at which the active sets' principles operate — the level identified in the Structural Analogy Annotations. This calibration is not automatic; check each active set's annotation and verify that the restatement engages the structural property each set was selected to address.

#### 1.2 — Apply Forgetting

Explicitly suppress:
- All entries in the Fixation Register.
- All best ideas from prior cycles (progressive forgetting of own outputs).

The suppression instruction is: "You may NOT use, reference, invoke, or build upon the following approaches. These are suppressed for this cycle. Work only with what remains in the active knowledge sets."

> **Theoretical anchor — Suppression is not restriction; it is cognitive space creation.** The conditions that feel most productive (full access to all knowledge) are the conditions that produce the least creative output. Storm & Patel (2014) demonstrated this directly: participants who forgot more of the studied uses generated more creative new uses (r = .26, p = .003, collapsed across all four experiments), and this correlation existed *only* for creative uses, not for routine ones (r = .03, ns). The suppression instruction does not diminish the reasoning process — it reconfigures its retrieval landscape so that the high-accessibility defaults no longer dominate, and the intersection points between foreign frames become reachable. Each suppressed approach is a pathway that has been temporarily closed, forcing the reasoning process to find routes it would otherwise never take.

#### 1.3 — Execute the Collision

This is the bisociative step. It requires holding all active knowledge sets' principles in simultaneous awareness and finding the intersection — the point where multiple frames address the same aspect of the problem but from incompatible directions.

> **Theoretical anchor — This step is the crux of the entire system, and its most common failure mode is reversion to sequential analysis.** Koestler (1964) was unambiguous: bisociation requires *simultaneous* perception of a situation through incompatible frames. Sequential application ("First, from the perspective of ecology... then, from the perspective of game theory... comparing these...") is not bisociation — it is comparative analysis, which processes each frame within its own matrix and then performs a rational synthesis. Comparative analysis produces competent interdisciplinary work, but it does not produce the "interference pattern" that generates genuinely novel ideas. The distinction is not metaphorical when applied to LLM processing: when two knowledge sets' principles are presented sequentially, the attention mechanism processes each within its own activation context; when they are presented simultaneously, the attention mechanism is forced to find cross-domain feature alignments that neither domain would activate in isolation. This computational co-activation *is* bisociation — two activation patterns, normally orthogonal, forced to co-activate, producing representations that belong to neither domain alone. The collision instruction below enforces this by requiring the identification of a single *intersection point* where the frames converge on the same problem aspect from incompatible directions, rather than a list of per-frame observations.

**The collision instruction** (adapted for each cycle):

```
COLLISION CYCLE [N]

PROBLEM: [π, restated in general terms]

ACTIVE KNOWLEDGE SETS:
[For each active set:]
  Domain: [Name]
  Governing Code: [2-3 sentences]
  Active Principles:
  - [Principle 1 — in native vocabulary]
  - [Principle 2 — in native vocabulary]
  - [Principle 3 — in native vocabulary]

SUPPRESSED (do NOT use): [Fixation Register + all prior best ideas]

INSTRUCTION:
Perceive the problem SIMULTANEOUSLY through all active knowledge sets.
Do not apply them sequentially (that is comparative analysis, not 
bisociation).
Find the intersection — the point where the frames address the same
aspect of the problem but from incompatible directions.
Generate 2-3 concrete, specific solution approaches that emerge from
this intersection.
Each approach must be genuinely novel — it must not be a minor 
variation of any suppressed approach or any standard approach in the 
home domain.
For each approach, name the specific principles from the active sets 
that intersected to produce it.
```

#### 1.4 — Record Pre-Inventive Structures

Write down everything that emerges from the collision, including half-formed ideas, contradictions, and unexpected connections. These are the pre-inventive structures. Do not evaluate during this step — evaluation comes next.

Each pre-inventive structure should be recorded with:
- A working title (1 sentence)
- The collision pair or group that produced it
- The specific principles that intersected
- A raw description (2–5 sentences, uncensored, unpolished)

> **Theoretical anchor — Pre-inventive structures are raw cognitive material, not finished ideas, and treating them as finished ideas is a category error that kills the Geneplore cycle.** Finke, Ward, and Smith (1992) were explicit: pre-inventive structures possess properties like novelty, ambiguity, and emergence, but they are *not yet* refined solutions. They are the generative phase's output, and they must pass through the exploratory phase (Phase 2) before they become ideas. Recording them without evaluation preserves their ambiguity — and ambiguity is a feature, not a bug, because it allows the exploratory phase to discover interpretations that the generative phase did not anticipate. If evaluation is applied during recording, the evaluative lens filters out the ambiguous and half-formed structures that are often the most bisociative: they look "wrong" or "impractical" in isolation, but they may contain structural novelty that becomes visible only under exploration. Suppress the impulse to judge. Record everything. Evaluation is next.

---

### Phase 2: Evaluation — Refine and Filter

This is the exploration phase of the Geneplore cycle. Apply the following filters to each pre-inventive structure:

> **Theoretical anchor — The transition from Phase 1 to Phase 2 is a deliberate cognitive mode shift.** The Geneplore model (Finke, Ward, & Smith, 1992) describes creativity as *cycling* between generation and exploration, and the quality of the cycle depends on the *separation* of these modes. Generation requires divergent, uncritical, ambiguity-tolerant processing. Exploration requires convergent, critical, specificity-demanding processing. Mixing the modes — generating while evaluating, or evaluating while still trying to generate — degrades both. The filters below are exploration tools; they are not to be applied retroactively during Phase 1 (which would prematurely close the generative space), nor are they to be relaxed here to preserve a favored idea (which would compromise the evaluative rigor that makes the surviving ideas trustworthy).

#### 2.1 — Novelty Filter

"Has this been done before in the home domain? Is this a known approach under a different name?"

**Method**: Conduct targeted bilingual search to verify novelty.
- Chinese round: Search for the proposed approach using both the home domain's vocabulary and the source domain's vocabulary. Look for prior work, existing implementations, or known approaches that match.
- English round: Same search strategy. Check academic databases, patent databases (if applicable), and technical literature.

If the idea is known under a different name, mark it as "not novel" and discard or flag. Novelty is assessed relative to the home domain, not relative to the external domain.

> **Theoretical anchor — The novelty filter also functions as a bisociation test.** A truly bisociative idea cannot be derived from any single knowledge set alone (see collision-execution-guide.md § The Bisociation Test, Question 1). If the bilingual search reveals that the idea already exists in the home domain, it was never bisociative — it was an associative rediscovery of something the home domain already knew. If it exists in one of the external domains but not the home domain, it may be a domain transfer (valuable but not bisociative) or a bisociative product that was independently discovered by the external domain (possible but check whether the idea requires understanding the *interaction* between sets, per Question 2 of the Bisociation Test). Only ideas that are genuinely new to *all* involved domains — ideas that no single-domain expert would have produced — represent the full bisociative yield of the collision.

#### 2.2 — Feasibility Filter

"Can this be implemented with available data, tools, and resources? Does it require information or infrastructure that does not exist?"

If infeasible, discard — unless the infeasibility can be resolved with a clearly identified additional step. Mark partially feasible ideas accordingly.

#### 2.3 — Value Filter

"Does this address a real limitation of current approaches? Would a knowledgeable domain expert recognize this as solving a genuine problem, rather than solving a problem that doesn't exist?"

If no clear value, discard.

#### 2.4 — Score

Assign each surviving idea a 3-tuple:
- **Novelty** (1–5): How far does this depart from current practice?
- **Feasibility** (1–5): How implementable is this with existing tools and data?
- **Value** (1–5): How significant is the limitation it addresses?

Retain ideas scoring ≥ 3 on all three dimensions.

---

### Phase 3: Forgetting & Rotation (Between Cycles)

#### 3.1 — Update the Fixation Register

Add the highest-scored idea from this cycle to the Fixation Register. This prevents the next cycle from producing variations of the same idea. The Register grows with each cycle — this is progressive forgetting of own outputs.

> **Theoretical anchor — Progressive self-suppression is the mechanism that prevents creative fixation on one's own recent output.** Storm & Patel (2014) showed that thinking-induced forgetting correlated with creative output only when participants were generating genuinely new uses — the same mechanism that suppresses external defaults also suppresses one's own prior outputs when those outputs begin to dominate retrieval. In the collision context, the first cycle's best idea has the highest "retrieval strength" — it is the most recent, most salient, most accessible creative product. If left unsuppressed, it will function as a default in subsequent cycles, constraining generation to variations-on-a-theme rather than genuinely distinct intersection points. Bjork & Bjork's (1992) Assumption 4 predicts that suppressing it will produce deeper encoding of whatever the next cycle generates — the next idea will be more genuinely different, not because you tried harder, but because the retrieval landscape was reconfigured by the suppression.

#### 3.2 — Rotate Knowledge Sets

For the next cycle, change which knowledge sets are active according to the collision schedule determined in Phase 0.3.

---

### Phase 4: Synthesis — After All Cycles

After all collision cycles are complete, synthesize the surviving ideas:

> **Theoretical anchor — The synthesis phase lifts all suppression, restoring full access.** This mirrors the final phase of Bjork & Bjork's (1992) desirable difficulties framework: after progressive forgetting has forced maximum diversity during generation, full retrieval is restored for integration. The ideas generated under forgetting conditions are now recalled in a new context (the integration context), and Bjork & Bjork's Assumption 4 predicts that this re-access in a new context produces larger increments in storage strength — the ideas become more robustly encoded and more flexibly transferable — than if they had been accessible throughout. The synthesis is not a post-hoc review; it is the final cognitive event in the creative cycle, and it benefits from everything the forgetting phases engineered.

#### 4.1 — Collect

Gather all ideas that survived the evaluation filter across all cycles.

#### 4.2 — Cluster

Group ideas by the type of innovation they represent. The clustering criterion is structural similarity — do two ideas solve the problem through the same mechanism, even if they originated from different collision pairs?

#### 4.3 — Cross-Pollinate (Second-Order Collision)

For each pair of clusters: "Can an idea from cluster X be combined with an idea from cluster Y to produce something that neither contains alone?" This is a second-order collision — a collision between collision outputs. It often produces the most powerful ideas in the entire run.

> **Theoretical anchor — Second-order collision is bisociation applied to its own products.** The first-order collisions produced ideas grounded in specific domain principles — each idea is itself a new "matrix of thought" that didn't exist before the collision. When two such idea-matrices are collided, the bisociative logic operates at a higher level of abstraction: the event L is now a shared structural mechanism between two novel ideas, and the incompatible frames are the two ideas' different approaches to that mechanism. Gabora (2016) described this as "convergence in the space of possible ideas" — the creative output itself becomes a conceptual entity capable of further creative recombination. Second-order collision is why the Collision Loop often produces its most paradigmatic ideas in this phase rather than in the first-order cycles: the input ideas have already been filtered for novelty, feasibility, and value, so the collision operates on pre-validated material, and the intersection occurs at a higher level of abstraction where more general (and therefore more powerful) principles live.

#### 4.4 — Rank

Final ranking weights:
- **Novelty in context**: Degree of departure from current practice in the home domain.
- **Value**: Likelihood of addressing a recognized failure mode or limitation.
- **Feasibility**: Implementability with existing tools and data.
- **Robustness**: Does the idea generalize across problem variants, or does it work only for one specific case?

#### 4.5 — Self-Challenge

Before delivering the final output, run the two self-checks from the deep-inquiry philosophy:

> **Theoretical anchor — These self-checks guard against the two most dangerous cognitive biases in creative evaluation: pride (attachment to one's own assembly) and prejudice (pattern-matching to familiar outputs).** Pride manifests as the tendency to overrate ideas *because you generated them* — the sunk-cost fallacy applied to cognitive effort. Prejudice manifests as the tendency to recognize an idea as "creative" because it *looks like* creative output from training data, rather than because it genuinely satisfies the bisociation, novelty, feasibility, and value criteria. Both biases produce false compliance — outputs that pass the formal evaluation filters but fail the substantive test of whether the idea is actually novel, actually feasible, actually valuable. The checks below are not cosmetic:

- *Am I defending this because it holds up, or because I assembled it?* (pride check)
- *Did I actually analyze this, or did I pattern-match to something familiar?* (prejudice check)

If either check triggers, revisit the analysis.

---

## Output Format

Deliver the output as a structured document:

```
# Collision Ideas for: [Problem π]

## Collision Summary
- Knowledge sets collided: [list]
- Total collision cycles: [N]
- Pre-inventive structures generated: [M]
- Ideas surviving evaluation: [P]
- Clusters identified: [Q]

## Ranked Ideas

### Idea 1: [Title]
- **Collision Source**: [Which sets/principles collided to produce this]
- **Description**: [Concrete, specific description — what is the idea 
  and how does it work]
- **Novelty** (X/5): [Why this is novel relative to current practice]
- **Feasibility** (X/5): [What would be needed to implement]
- **Value** (X/5): [Which limitation of current approaches it addresses]
- **Robustness**: [Does it generalize or is it case-specific]

### Idea 2: [Title]
...

[Continue for all ranked ideas]

## Cross-Pollination Results
[Any second-order collision ideas from Phase 4.3]

## Process Trace
[Optional: for transparency, a brief log showing which collision 
cycles produced which pre-inventive structures, which were filtered 
out and why, and how the Fixation Register grew over cycles]
```

---

## Adapting to Different Values of k

### k = 2 (Minimal Collision)
The simplest case. Two knowledge sets collide directly. Run 3 cycles with progressive forgetting. This is suitable for focused, deep exploration of a single collision pair. Expected output: 3–6 surviving ideas.

### k = 3 (Triangular Collision)
Three pairwise collisions plus one triple collision. The triple collision is often the most productive cycle because it forces the reasoning process to hold three incompatible frames simultaneously, maximizing bisociative tension. Expected output: 5–10 surviving ideas.

### k = 4–6 (Broad Exploration)
The phased approach (Pairwise → Multi-set → Full) ensures that both focused and holistic collisions are performed. The most distant pairs are collided first (Exploration phase), then promising combinations are deepened (Intensification), then everything is combined (Full Collision). Expected output: 8–15 surviving ideas.

### k > 6 (Systematic Coverage)
With many knowledge sets, not all pairs can be collided individually. The collision schedule must be selective, prioritizing the most structurally distant pairs and the most promising multi-set combinations. The Full Collision cycle with all sets active is particularly important here as an integrative step. Expected output: 12–20+ surviving ideas.

---

## Critical Constraints

1. **Bisociation, not sequential analysis.** The collision step (Phase 1.3) must hold all active knowledge sets simultaneously. "First, from the perspective of X... then, from the perspective of Y... comparing them..." is NOT bisociation. It is comparative analysis, and it will not produce genuine intersection ideas. The collision must seek the point where the frames converge on the same aspect of the problem from incompatible directions. Re-read the theoretical anchor at Phase 1.3 if you find yourself reverting to sequential processing.

2. **Respect the Fixation Register.** Suppressed approaches must genuinely be suppressed — not referenced, not used as starting points, not lightly modified. The whole point of the Register is to force the reasoning process away from defaults.

3. **Progressive forgetting of own outputs.** Each cycle's best idea goes into the Register. This prevents fixation on recent creative output — the same mechanism that Storm et al. (2014) showed enables continued creative generation.

4. **Bilingual verification for novelty.** The novelty filter (Phase 2.1) requires searching in both Chinese and English to verify that an idea is genuinely new to the home domain. Chinese-language sources may reveal prior work unknown to the English-speaking community, and vice versa.

5. **Never skip evaluation.** Pre-inventive structures are raw material, not finished ideas. Every structure must pass through the novelty, feasibility, and value filters before being included in the output.

6. **Principles stay in native vocabulary during collision.** The mapping from external vocabulary to home-domain application is the collision's job — it happens organically during bisociation. Pre-translating the principles strips them of their creative potential. Re-read the theoretical anchor at Phase 0.1 if you encounter pre-translated principles.

7. **The skill generates ideas; it does not compose knowledge sets.** If the user asks for knowledge sets to be generated, direct them to the collision-knowledge-generator skill first.

8. **Every claimed novelty must be verified.** Do not present an idea as novel without searching for prior work. The search must be bilingual.

---

## Reference Files

- **[references/collision-execution-guide.md](references/collision-execution-guide.md)**: Detailed guidance on executing the bisociative collision step, common failure modes and how to avoid them, and examples of successful vs. failed collisions. **Read this before starting Phase 1.**
