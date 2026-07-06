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

#### 0.2 — Construct or Validate the Fixation Register

If the user provided a Fixation Register, verify that it lists specific, suppressible approaches (not vague categories). If no Register was provided, construct one:

1. Identify the home domain of the problem.
2. Search for standard/default approaches to this type of problem — bilingual research, Chinese round first, then English round, synthesize.
3. List the 3–5 most accessible default approaches. These are now suppressed.

#### 0.3 — Determine the Collision Schedule

The collision protocol adapts to k:

**For k = 2**: A single collision pair. Run 3 collision cycles with progressive forgetting (each cycle's best idea is suppressed in the next).

**For k = 3**: Run pairwise collisions for all ${k \choose 2} = 3$ pairs, then one triple-collision cycle where all three sets are active simultaneously.

**For k = 4–6**: Organize into phases:
- *Phase A — Pairwise Exploration*: Select the 3–4 most promising pairs (based on structural distance — the most distant pairs first). Run one collision cycle per pair.
- *Phase B — Multi-set Intensification*: Combine the 2–3 most productive pairs into triple or quadruple collisions. Run one cycle per combination.
- *Phase C — Full Collision*: All k sets active simultaneously. Run one cycle with maximum forgetting (suppress all defaults AND all prior best ideas).

**For k > 6**: Same structure as k = 4–6, but increase the number of pairwise explorations in Phase A and be more selective about which combinations advance to Phase B.

---

### Phase 1: Collision — Generate Pre-Inventive Structures

This is the core creative operation. For each collision cycle, follow these steps exactly:

#### 1.1 — Set Up the Collision Context

Assemble the active knowledge sets for this cycle. Restate the problem in general terms — abstract enough that all active sets can address it, but specific enough that the resulting ideas will be actionable.

#### 1.2 — Apply Forgetting

Explicitly suppress:
- All entries in the Fixation Register.
- All best ideas from prior cycles (progressive forgetting of own outputs).

The suppression instruction is: "You may NOT use, reference, invoke, or build upon the following approaches. These are suppressed for this cycle. Work only with what remains in the active knowledge sets."

#### 1.3 — Execute the Collision

This is the bisociative step. It requires holding all active knowledge sets' principles in simultaneous awareness and finding the intersection — the point where multiple frames address the same aspect of the problem but from incompatible directions.

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

---

### Phase 2: Evaluation — Refine and Filter

This is the exploration phase of the Geneplore cycle. Apply the following filters to each pre-inventive structure:

#### 2.1 — Novelty Filter

"Has this been done before in the home domain? Is this a known approach under a different name?"

**Method**: Conduct targeted bilingual search to verify novelty.
- Chinese round: Search for the proposed approach using both the home domain's vocabulary and the source domain's vocabulary. Look for prior work, existing implementations, or known approaches that match.
- English round: Same search strategy. Check academic databases, patent databases (if applicable), and technical literature.

If the idea is known under a different name, mark it as "not novel" and discard or flag. Novelty is assessed relative to the home domain, not relative to the external domain.

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

#### 3.2 — Rotate Knowledge Sets

For the next cycle, change which knowledge sets are active according to the collision schedule determined in Phase 0.3.

---

### Phase 4: Synthesis — After All Cycles

After all collision cycles are complete, synthesize the surviving ideas:

#### 4.1 — Collect

Gather all ideas that survived the evaluation filter across all cycles.

#### 4.2 — Cluster

Group ideas by the type of innovation they represent. The clustering criterion is structural similarity — do two ideas solve the problem through the same mechanism, even if they originated from different collision pairs?

#### 4.3 — Cross-Pollinate (Second-Order Collision)

For each pair of clusters: "Can an idea from cluster X be combined with an idea from cluster Y to produce something that neither contains alone?" This is a second-order collision — a collision between collision outputs. It often produces the most powerful ideas in the entire run.

#### 4.4 — Rank

Final ranking weights:
- **Novelty in context**: Degree of departure from current practice in the home domain.
- **Value**: Likelihood of addressing a recognized failure mode or limitation.
- **Feasibility**: Implementability with existing tools and data.
- **Robustness**: Does the idea generalize across problem variants, or does it work only for one specific case?

#### 4.5 — Self-Challenge

Before delivering the final output, run the two self-checks from the deep-inquiry philosophy:
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

1. **Bisociation, not sequential analysis.** The collision step (Phase 1.3) must hold all active knowledge sets simultaneously. "First, from the perspective of X... then, from the perspective of Y... comparing them..." is NOT bisociation. It is comparative analysis, and it will not produce genuine intersection ideas. The collision must seek the point where the frames converge on the same aspect of the problem from incompatible directions.

2. **Respect the Fixation Register.** Suppressed approaches must genuinely be suppressed — not referenced, not used as starting points, not lightly modified. The whole point of the Register is to force the reasoning process away from defaults.

3. **Progressive forgetting of own outputs.** Each cycle's best idea goes into the Register. This prevents fixation on recent creative output — the same mechanism that Storm et al. (2014) showed enables continued creative generation.

4. **Bilingual verification for novelty.** The novelty filter (Phase 2.1) requires searching in both Chinese and English to verify that an idea is genuinely new to the home domain. Chinese-language sources may reveal prior work unknown to the English-speaking community, and vice versa.

5. **Never skip evaluation.** Pre-inventive structures are raw material, not finished ideas. Every structure must pass through the novelty, feasibility, and value filters before being included in the output.

6. **Principles stay in native vocabulary during collision.** The mapping from external vocabulary to home-domain application is the collision's job — it happens organically during bisociation. Pre-translating the principles strips them of their creative potential.

7. **The skill generates ideas; it does not compose knowledge sets.** If the user asks for knowledge sets to be generated, direct them to the collision-knowledge-generator skill first.

8. **Every claimed novelty must be verified.** Do not present an idea as novel without searching for prior work. The search must be bilingual.

---

## Reference Files

- **[references/collision-execution-guide.md](references/collision-execution-guide.md)**: Detailed guidance on executing the bisociative collision step, common failure modes and how to avoid them, and examples of successful vs. failed collisions. **Read this before starting Phase 1.**
