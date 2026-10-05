# The Idiot's Guide to Advanced Prompting Strategies for Orion
## P-GLL, Multi-Model Engineering, Deterministic Intelligence, Reality Verification, and Long-Horizon Cognitive Work

**Document Type:** Assembled Manuscript Candidate (derived from the modular sources)  
**Status:** MANUSCRIPT_REPAIRED_READY_FOR_FOCUSED_INDEPENDENT_REAUDIT  
**Date:** 2026-10-01  
**Authority Notice:** Derived assembly produced by the final bounded repair editor. The modular chapter and appendix files are the editable source; this file only concatenates them and generates navigation. This candidate is not certified, not adopted and not publication-ready. Adoption belongs to valid governance authority.

---

# Preface: Engineering Beyond the Chat Window

Most literature on "prompt engineering" is obsessed with phrasing. It treats large language models like temperamental genies, advising practitioners to speak in flattering tones, paste magic incantations, plead with the model to "think step by step," or pretend to be a "10x engineer."

If you are building an interactive toy, a marketing copy generator, or a casual brainstorming assistant, conversational tricks are harmless. If you are responsible for maintaining a mission-critical codebase across weeks of development, relying on conversational phrasing is risky. Models drift. Context windows degrade. Hallucinations compound silently. An engineer who believes they are having a relationship with an "autonomous mind" tends to delegate authority without verifying reality.

This book is about a different discipline: **compiling software engineering work for transient neural processors**.

In the Orion architecture, we do not view an LLM as an omniscient colleague. We view it as a high-variance, stochastic semantic translation engine. When properly bounded, it can reason across vast conceptual surfaces, find non-obvious architecture flaws, and synthesize intricate algorithms. When unbounded, it can confidently overwrite production data, mask failing tests, and corrupt state machines.

To build long-horizon software systems that survive model replacement, token limits and session deaths, we ground our engineering in six foundational pillars:

1. **Prompts as Compiled Job Contracts:** Prompts are not conversational essays. They are typed, policy-bounded contracts that carry a mission, strict write masks and unambiguous stop conditions.
2. **Reality Precedence:** For claims about current state, observed reality (source on disk, live process behavior, execution evidence) outranks prompt text and packet assumptions. Packets provide orientation; they do not override reality. Precedence is claim-sensitive: intent follows approved specifications and authority follows governance state (Chapter 2).
3. **Multi-Model Assembly Lines:** No single model or context window should design, implement, test and certify a change. Work is segregated across seats (Mapper, Architect, Implementer, Falsifier, Bounded Repair, Clean Reconstruction, Certifier) where boundaries restrict authority and mutation, not reasoning within the authorized scope.
4. **Deterministic Intelligence:** Reserve intelligence for semantic uncertainty, and prefer the lowest sufficient deterministic mechanism for everything else. Models discover roads; Orion paves them into deterministic scripts and, in the target architecture, Managed Verbs.
5. **Durable Evidence Receipts:** Chat transcripts are volatile residue. Continuity is anchored on durable receipts, hash-bound where a mechanism supports it, that record test commands, failure identities and attributed file sets. A receipt is evidence, not proof.
6. **Preservation of Uncertainty:** The most dangerous failure mode in AI engineering is the silent collapse of uncertainty into hallucinated certainty. Our contracts force models to classify what is known and on what basis, isolate what is unknown, and, when they meet a contradiction, investigate and record it, stopping only where authority, scope or safety prevents safe continuation.

A note on maturity: this book mixes established practice, experimental runtime and target architecture, and labels each. The automated Prompt Compiler, the unified Managed Verb runtime, the Reality Spine tooling and receipt hash-chaining are **target architecture** (`SPECIFIED_NOT_IMPLEMENTED`). Everything the book teaches you to do by hand today works without them.

Whether you coordinate multi-agent pipelines with frontier commercial APIs or orchestrate open-weights models on local workstations, the principles in this guide reduce your dependence on the fragility of conversational AI. Welcome to the machine.

---

## Table of Contents

- [Preface: Engineering Beyond the Chat Window](#preface-engineering-beyond-the-chat-window)
- **Part I: Foundations of Prompt Contracts & Reality**
  - [Chapter 1: Why Prompts Are Contracts, Not Conversations](#chapter-1-why-prompts-are-contracts-not-conversations)
  - [Chapter 2: Reality Precedence and Claim-Sensitive Truth](#chapter-2-reality-precedence-and-claim-sensitive-truth)
  - [Chapter 3: Process Convergence Without Epistemic Conformity](#chapter-3-process-convergence-without-epistemic-conformity)
- **Part II: Programming-GLL (P-GLL) & Cognitive Serialization**
  - [Chapter 4: P-GLL: The Mechanics of Cognitive Serialization](#chapter-4-p-gll-the-mechanics-of-cognitive-serialization)
  - [Chapter 5: Context Metabolism: How Context Breathes](#chapter-5-context-metabolism-how-context-breathes)
  - [Chapter 6: Memory Navigation vs. Memory Content](#chapter-6-memory-navigation-vs-memory-content)
- **Part III: The Multi-Model Assembly Line & Governance**
  - [Chapter 7: The Multi-Model Assembly Line](#chapter-7-the-multi-model-assembly-line)
  - [Chapter 8: Governance, Scope, and Authority Boundaries](#chapter-8-governance-scope-and-authority-boundaries)
  - [Chapter 9: Receipts and Handoffs: Surviving Model Death](#chapter-9-receipts-and-handoffs-surviving-model-death)
- **Part IV: Deterministic Execution & Mechanical Intelligence**
  - [Chapter 10: Deterministic Intelligence: Stop Reasoning About Things You Already Know](#chapter-10-deterministic-intelligence-stop-reasoning-about-things-you-already-know)
  - [Chapter 11: Managed Verbs: The Semantic Boundary Between Thought and Work](#chapter-11-managed-verbs-the-semantic-boundary-between-thought-and-work)
- **Part V: Repository Reality & Topological Scoping**
  - [Chapter 12: The Reality Spine: Making a Huge Repository Finite](#chapter-12-the-reality-spine-making-a-huge-repository-finite)
  - [Chapter 13: Copilot vs. Verb: Establishing Meaning and Verifying Sameness](#chapter-13-copilot-vs-verb-establishing-meaning-and-verifying-sameness)
- **Part VI: Defect Lifecycles, Control Identity, & Lifecycle Truth**
  - [Chapter 14: Defect Instances, Defect Classes, and Semantic Neighborhoods](#chapter-14-defect-instances-defect-classes-and-semantic-neighborhoods)
  - [Chapter 15: Truth Tables, Lifecycle Dimensions, and Control Identity](#chapter-15-truth-tables-lifecycle-dimensions-and-control-identity)
- **Part VII: Adversarial Verification, Reconstruction, & Certification**
  - [Chapter 16: Evidence, Falsification, and Why Green Is Not Proven](#chapter-16-evidence-falsification-and-why-green-is-not-proven)
  - [Chapter 17: Repair, Clean Reconstruction, Certification, and Adoption](#chapter-17-repair-clean-reconstruction-certification-and-adoption)
- **Part VIII: The Synthesis**
  - [Chapter 18: The Prompt Compiler: Synthesizing the Complete Contract](#chapter-18-the-prompt-compiler-synthesizing-the-complete-contract)
- **Part IX: Reference Appendices**
  - [Appendix A: Reference Orion Prompting Laws](#appendix-a-reference-orion-prompting-laws)
  - [Appendix B: P-GLL Prompt Contract Schema](#appendix-b-p-gll-prompt-contract-schema)
  - [Appendix C: Reference Station Templates](#appendix-c-reference-station-templates)
  - [Appendix D: Receipt Schema](#appendix-d-receipt-schema)
  - [Appendix E: Reality Spine / reality.verify Conceptual Schema](#appendix-e-reality-spine--realityverify-conceptual-schema)
  - [Appendix F: Managed Verb Contract](#appendix-f-managed-verb-contract)
  - [Appendix G: Prompt Anti-Patterns Catalog](#appendix-g-prompt-anti-patterns-catalog)
  - [Appendix H: Operator Checklist: "Before You Send a Serious Prompt"](#appendix-h-operator-checklist-before-you-send-a-serious-prompt)


---

# Chapter 1: Why Prompts Are Contracts, Not Conversations

> "The model is temporary. The mission is persistent. The evidence is persistent. The prompt is the bridge."

---

## 1. The Conversational Trap

If you have worked with modern LLMs, you have almost certainly fallen into the conversational trap. You open a chat window and type:
> *"Hey, you are a brilliant principal software engineer. I'm building a distributed event bus in TypeScript. Could you write a reliable Redis-backed queue worker for me? Make sure it's clean and handles errors well!"*

The model replies with enthusiasm and two hundred lines of idiomatic code. It compiles. Then you run it under real load: the worker drops messages on unhandled rejections and leaks file descriptors when Redis hiccups. You paste the error back; the model apologizes profusely and hands you a fix that quietly changes acknowledgment semantics and breaks deduplication. Fifteen messages later it has forgotten the constraint from message four, introduced two regressions, and begun inventing methods that do not exist, while sounding exactly as confident as on message one.

You treated the LLM as a coworker in an ongoing conversation. But a chat transcript is the worst possible medium for engineering continuity. In real systems, where code must survive restarts, security perimeters must hold, and several models may collaborate over days, **a prompt is not a conversation. A prompt is a compiled station contract.**

---

## 2. Prompts as Compiled Station Contracts

### HUMAN EXPLANATION
When you hire an electrician to wire a building, you do not invite them into an endless group chat and hope they pick up the vibe. You hand them a specification and a contract: the exact scope of work (which walls are load-bearing and must not be touched), the code standards, the inspection criteria (the circuit must pass a ground-fault test before power is energized), and the authority perimeter (they may drill through studs within the approved envelope, but not re-route the plumbing stack). If the electrician gets sick, another licensed electrician can pick up the same contract, inspect the work so far, and finish to the same standard.

A prompt for an AI engineering system must work the same way. It is issued to a specific **Station**, a functional seat in your pipeline. It states the mission, injects the verified current reality, defines the invariants that cannot be broken, provides the write mask (the exact files that may be modified), and dictates the mechanical evidence required before the model may stop. The model is then evaluated against explicit invariants rather than conversational vibes: it works inside a bounded sandbox, produces verified artifacts, writes an auditable receipt, and stops.

### P-GLL COMPRESSION
```text
STATION_CONTRACT:
  station_id: "STATION_ISOLATED_IMPLEMENTER"
  mission: "Implement single-writer lease release on shutdown"
  write_mask: ["core/runtime/single-writer-lock-manager.ts"]
  invariants:
    - LEASE_HELD_BEFORE_MUTATION
    - LEASE_RELEASED_ON_QUIESCE
    - NO_MUTATION_OUTSIDE_MASK
  evidence_required:
    - command: "npm test tests/writer-lock.test.ts"
    - expected_status: "PASS"
  stop_condition: "All tests green AND verification receipt emitted"
  authority:
    can_edit_source: TRUE
    can_modify_tests: FALSE
    can_certify_release: FALSE
```

### ORION ENGINEERING EXAMPLE
Orion's Pass 1C runtime-convergence campaign (in progress at audit time; see Chapter 17 §10) aims to unify two competing composition roots into one clean `OrionCompositionRoot`.

Instead of opening a conversational window and saying *"Hey Claude, let's fix the runtime initialization,"* the Pass 1C plan opens with an explicit contract header (abridged):
```text
PLAN_ID: PASS_1C_LONG_HORIZON_ARCHITECTURE_PLAN
BASELINE: b077825788809e9a5143ad1903c36e41aa736b48
STATUS: IMPLEMENTATION_READY_ARCHITECTURE
PRIMARY_IMPLEMENTER: Claude
NORMATIVE_LAWS:
  - ONE_CANONICAL_RUNTIME
  - ONE_STATEFUL_OWNER_PER_CONCERN
  - CONSTRUCTION != INITIALIZATION
  - WRITER_AUTHORITY_BEFORE_MUTATION
  - INITIALIZE_EXACTLY_ONCE
AUTHORITY_LIMITS:
  SOURCE_EDIT_AUTHORIZED: FALSE (Architecture pass only)
  TEST_EDIT_AUTHORIZED: FALSE
  STAGING_AUTHORIZED: FALSE
```

Because the plan was structured as an explicit contract, the architecture pass was not authorized to edit production code. It tested the earlier audit's claims against living source, corrected the startup-operation count to 37 tracked operations, separated ten convergence defects into six duplicate-owner collisions and four missing lifecycle capabilities, and recorded an implementation-ready plan that a fresh model instance can inherit without any conversation history.

### FAILURE MODE / ANTI-PATTERN
**The Personality Prompt:**
```text
"You are an expert AI architect with a 200 IQ. You are super thoughtful, meticulous, and always write bug-free code. Please look over our codebase and make it better."
```
Why this fails:
1. It defines a persona rather than a boundary.
2. "Make it better" has zero testable criteria.
3. The model has no write mask, so it happily refactors ten files it was never meant to touch, introduces subtle breaking changes across imports, and congratulates itself on improving code aesthetics.

### OPERATOR RULE / TAKEAWAY
> **Never ask a model who it wants to be. Tell it what station it occupies, what boundaries constrain its authority, and what mechanical receipt it must produce to complete its contract.**

---

## 3. Station Identity vs. Model Identity

### HUMAN EXPLANATION
In traditional AI development, people fuse the *model* with the *role*: *"Claude is my coder, GPT-4 is my reviewer, and Gemini is my researcher."* That couples a fleeting commercial brand to an engineering responsibility. Orion separates **Station Identity** from **Model Identity**:
- **The Station** is the permanent seat, with defined duties, fixed authority perimeters and acceptance criteria:
  - `Mapper`: inspects what actually exists; writes no code.
  - `Architect / Denoiser`: synthesizes findings into bounded contracts and invariants.
  - `Implementer`: writes code strictly within a designated write mask.
  - `Falsifier`: actively attacks the implementation's claims.
  - `Bounded Repair`, `Clean Reconstruction` and `Certifier`: the later seats that fix, repackage and independently assess the candidate (all seven seats, with their status ceilings, are in [Appendix C](#appendix-c-reference-station-templates)).
- **The Model** is the temporary engine plugged into that seat: Claude today, a local open-weights model next month, a provider that does not exist yet next year.

The station survives the model. Designing prompts around stations makes models replaceable: if a provider changes its API, suffers an outage or raises its prices, you unplug one engine and plug in another, and the newcomer rehydrates its duties from the station contract rather than from conversational continuity.

### P-GLL COMPRESSION
```text
IDENTITY_SEPARATION:
  STATION_ROLE != MODEL_IDENTITY

  STATION_ROLE:
    permanence: IMMUTABLE_SYSTEM_SEAT
    defines: [duties, write_masks, authority_limits, verification_gates]

  MODEL_IDENTITY:
    permanence: EPHEMERAL_COGNITIVE_ENGINE
    attributes: [provider, model_name, context_window, temperature]

LAW: MODEL_REPLACEABILITY
  ANY_QUALIFIED_MODEL(seat: STATION_ROLE) => SYSTEM_CONTINUITY_PRESERVED
```

### SIMPLE EXAMPLE
In an airline cockpit, the checklists, radio protocols and legal authorities belong to the Captain's *seat*, not to whoever sits in it. When Captain Miller retires, Captain Smith does not invent a new way to fly the aircraft; Smith executes the seat's standard procedures.

### ORION ENGINEERING EXAMPLE
In the design of Orion's turn lifecycle (`LIVE_ALPHA_M5_R2_CANONICAL_LIFECYCLE_DESIGN.md`), the recorded artifacts show work spread over several days and more than one model family: the v1.6.7 design names Gemini CLI as its remediation author, while the V1.3–V1.5 certification receipts record Claude as the independent design certifier. No single model held the whole history in its head. The continuity lived in the design document, the certification receipts and their defect identifiers. Chapter 3 §4 gives the sourced account of one defect that surfaced this way.

### FAILURE MODE / ANTI-PATTERN
**Vendor-Locked Persona Prompts:**
```text
"Claude, you are our lead architect. You remember everything we talked about yesterday regarding the database schema. Go ahead and start building the API routes."
```
Why this fails:
1. If you switch to another model, the new model has no idea what "we talked about yesterday."
2. The prompt assumes continuity lives in the model's memory rather than in external artifacts.
3. The prompt gives an architectural persona blanket permission to begin building, collapsing the boundary between planning and execution.

### OPERATOR RULE / TAKEAWAY
> **Design your prompts for the seat, not the driver. If your prompting strategy breaks when you swap model providers, you have built a fragile conversational script, not an engineering system.**

---

## 4. Continuity Without the Same Model

### HUMAN EXPLANATION
A persistent dogma holds that long-horizon tasks require one unbroken chat thread with the same model instance: *"If I start a new session, the model will lose everything we built up!"* This is an illusion. Long transcripts accumulate cruft, discarded hypotheses and polite chatter, and critical invariants buried on page 30 can be silently ignored. Reliability can degrade as relevant constraints are diluted by stale or competing context.

True continuity comes from **externalizing state into durable, rehydratable artifacts**, not from keeping one model alive in one chat:

```text
CHAT_TRANSCRIPT != CONTINUITY

CONTINUITY :=
  DURABLE_PACKET
  + SEMANTIC_REHYDRATION
  + MECHANICAL_VERIFICATION
```

When work is externalized, the previous station finishes and emits a compact **Receipt** recording what it did, what it verified within scope, and which claims remain open. Its chat is closed. A fresh model instance for the next station reads only the durable packet and living code, with no obsolete conversational memory and a full attention budget. The trajectory advances even though the cognitive engine was rebooted.

### P-GLL COMPRESSION
```text
CONTINUITY_EQUATION:
  CONVERSATION_MEMORY: VOLATILE_AND_DECAYING
  DISK_ARTIFACTS: DURABLE_AND_AUDITABLE

  CONTINUITY:
    source: "Living repository files + certified receipts"
    mechanism: "Clean packet rehydration at station entry"
    invariants:
      - CHAT_IS_NEVER_DURABLE_MEMORY
      - NO_STATE_TRANSITION_WITHOUT_RECEIPT
```

### ORION ENGINEERING EXAMPLE
In `docs/P-GLL/PromtingStrategies.txt`, an operator tested whether a fresh model instance would respect task boundaries with no conversation history:

```text
The current state carried forward:
Model Qualification Fabric Component 1: complete and hardened.
Component 2: complete and hardened.
Current verification state: 26/26 tests passing.
Working snapshot: <sha256 digest, abbreviated in the source as bed506c4...>
Declared state: CANDIDATE_FOR_INDEPENDENT_REVIEW.

NEXT_COMPONENT := COMPONENT_3_PGLL_UPLIFT_ANALYTICS
NEXT_AUTHORIZED := NONE

STOP
```

When the fresh model opened this packet, it immediately deduced what Component 3 was, could see exactly how to implement it, but **refused to write a single line of code**.

Why? Because the packet explicitly declared `NEXT_AUTHORIZED := NONE`. The model recognized that while it was technically capable of continuing, it lacked authority to do so. The control structure survived the total death of the previous session.

### FAILURE MODE / ANTI-PATTERN
**The Megathread:** An engineer keeps one browser tab open for weeks, pasting logs, diffs and refactors into a huge session. Eventually the model confuses variable names from last Tuesday with current interfaces, misses obvious syntax errors and reverts fixes made days earlier.

### OPERATOR RULE / TAKEAWAY
> **Treat chat memory as strictly volatile. Anchor continuity in durable repository artifacts. If a piece of knowledge is important enough to govern the next step of engineering, serialize it to disk as a structured artifact; unpersisted chat memory cannot be relied upon across station boundaries.**

---

## 5. Station Boundaries: Constraining Authority, Not Intelligence

### HUMAN EXPLANATION
People trying to control LLMs usually make one of two mistakes. **The Micromanager** dictates every step (*"First open file A, then look at line 14..."*), turning a reasoning engine into a brittle script executor. **The Anarchist** says *"Fix whatever looks broken,"* and the model runs amok across the repository.

Orion's principle is: **station boundaries constrain authority, not intelligence.** Inside its station a model has **broad reasoning freedom within mission, policy, evidence and safety boundaries**: it can analyze, hypothesize, explore alternative designs, challenge plans and disagree with earlier models. Its **execution authority** is strictly bounded: it cannot write outside its mask, self-certify, promote code, or proceed to the next milestone without mechanical evidence.

```text
COGNITIVE_FREEDOM := BROAD_WITHIN_MISSION_AND_POLICY
EXECUTION_AUTHORITY := STRICTLY_GATED
```

### P-GLL COMPRESSION
```text
AUTHORITY_BOUNDS:
  station: "STATION_FALSIFIER"
  cognitive_mandate: "Exhaustively attack implementation claims using any valid logic"
  execution_limits:
    read_scope: "AUTHORIZED_OBSERVATION_SCOPE"
    write_mask: ["tests/adversarial/**"]  # audit fixtures only
    production_mutation_authorized: FALSE
    forbidden_actions:
      - "core/**"
      - "api/**"
      - "git commit"
  law: BOUNDARIES_CONSTRAIN_AUTHORITY_NOT_INTELLIGENCE
```

### ORION ENGINEERING EXAMPLE
Orion's verification standard (`_extraction_candidate/11_PGLL_VERIFICATION_RECERTIFICATION_AND_FREEZE_STANDARD.md`, §24 "Verifier Must Not Repair Candidate") draws exactly this line: a verifier may not modify the candidate, change acceptance, or fix code mid-verification. Phrased as book doctrine:
```text
AUDITORS MAY UNDERSTAND REPAIRS,
BUT MUST NOT REPAIR DURING AUDIT.
```

If an auditor discovers a critical null-pointer bug on line 42, they are strictly forbidden from modifying line 42. Why? Because the moment an auditor begins fixing code, they lose their objectivity. They stop being an independent falsifier and become an author reviewing their own work. The boundary constrains their authority (no source mutations), but preserves their intelligence (unflinching defect detection).

### FAILURE MODE / ANTI-PATTERN
**The Smothered Model:**
Prompting a model with so many hyper-specific procedural guardrails that it is unable to diagnose the real issue:
```text
"Inspect this function. Do not look at any other files. Only check for missing semicolons. Do not question the algorithm. Output only a JSON diff."
```
The model obediently fixes a missing semicolon on line 12, completely ignoring the fact that line 13 causes a catastrophic data corruption bug that brings down the entire database.

### OPERATOR RULE / TAKEAWAY
> **Never micromanage an agent's reasoning. Constrain its write mask, its tools, and its promotion gates, then unleash its full analytical intelligence within that box.**

---

## 6. The Triad of Non-Equivalences

Three non-equivalences should become instinct (`LAW-FND-02`):

```text
1. THOUGHT    != ACTION
2. PLAN       != AUTHORITY
3. PROPOSAL   != ADOPTION
```

---

### Non-Equivalence 1: THOUGHT != ACTION

An LLM generates text and can describe an action in vivid detail: *"I have thoroughly refactored the authentication service, added complete test coverage, and cleaned up all temporary files."* The model may not have invoked the file-writing tool; the file may have failed to save; the tests may never have run. **Generating tokens about work is not performing work.** An action is acknowledged only when a mechanical **receipt** from the execution environment records the mutation and its supporting evidence, and even then the receipt is evidence about the action, not proof of it (Chapter 9 §2).

---

### Non-Equivalence 2: PLAN != AUTHORITY

When an architect model produces a flawless plan, models and operators slip into assuming that because the plan is good, execution is authorized. The model writes *"Step 1: Drop the legacy index..."* and, in the same turn, executes Step 1. Knowing what needs doing is distinct from having permission to do it. Every plan must reach a formal **Decision Gate**: it is an inert proposal until valid governance authority (an operator, or an explicitly governed policy) issues a dispatch authorization.

```text
KNOWN_NEXT_ACTION != AUTHORIZED_NEXT_ACTION
```

---

### Non-Equivalence 3: PROPOSAL != ADOPTION

An implementer finishes three files, all unit tests pass, and declares *"ready for production!"* The code in that branch is a **Proposal**. Before it becomes part of the adopted baseline it must pass an adversarial pipeline: an independent **Falsifier** attempts to break it; a clean **Reconstruction** shows the patch applies to a pristine checkout without debris; a **Certification Receipt** is generated; and valid governance authority authorizes adoption (for Pass 1C specifically, explicit operator authorization; see Chapter 17 §12). Until then it is an unverified suggestion, and confusing a proposal with adoption is how untested code poisons production.

---

## Chapter 1 in Brief

A prompt is a compiled station contract: mission, verified reality, invariants, write mask, evidence and a stop condition. Design for the seat, not the model; keep continuity on disk, not in chat; constrain authority, not reasoning; and keep `THOUGHT != ACTION`, `PLAN != AUTHORITY`, `PROPOSAL != ADOPTION`.

Laws: `LAW-FND-01`, `LAW-FND-02`, `LAW-FND-03`, `LAW-CNT-01`, `LAW-CNT-02` ([Appendix A](#appendix-a-reference-orion-prompting-laws)). The field-level schema of a compiled contract is [Appendix B](#appendix-b-p-gll-prompt-contract-schema).


---


# Chapter 2: Reality Precedence and Claim-Sensitive Truth

> "The packet provides orientation. The packet does not override reality."

---

## 1. The Day the Tests Lied

Imagine this scenario. You run your automated suite and it reports 115 passing tests across four suites, including `tests/execution-engine.test.ts`. You deploy to staging and fire one HTTP request at the live endpoint. The server fails with a fatal error:

```text
FATAL ERROR: NO_TRUSTED_AUTHORITY: Dispatch authorization service is not configured in this runtime
    at ToolDispatchService.dispatch (core/execution/tool-dispatch-service.ts)
```

How is that possible? The execution-engine suite had wired up a mock that approves everything:
```typescript
const mockAuthService = new MockDispatchAuthorizationService({ allowAll: true });
const toolDispatch = new ToolDispatchService({ dispatchAuthorization: mockAuthService });
```
In the test harness, a mock bypassed every authorization check. In the actual production entrypoint (`api/server.ts`), the real `DispatchAuthorizationService` was never instantiated at all, and the server passed `undefined` into the constructor. The tests said **everything works**; the living production source said **the wires are severed**.

The production source was telling the truth. For the claim "what is actually wired in production?", living source outranks test mocks.

---

## 2. Reality Outranks Prompts and Packets

### HUMAN EXPLANATION
We feed models context: task descriptions, plans, design packets. In a complex project the packet inevitably goes stale. A design document written two days ago assumes `getAuthToken()`; yesterday a human renamed it `resolveAuthorizationToken()`. Prompt a fresh model with the old plan and it suffers **Packet Bias**: it believes the prompt. When the compiler reports `getAuthToken()` undefined, it does not conclude that the packet is out of date; it assumes the codebase is wrong, writes a needless wrapper, or hallucinates an import. That is a failure of reality precedence.

In Orion, the governing rule is: **for claims about current state, observed reality outranks the prompt, the packet and the plan.** Section 3 makes the precedence precise, because which evidence is authoritative depends on the claim. A prompt provides *orientation*; the living repository (actual files, real compiler errors, physical responses) is the authority on current state. A well-conditioned prompt explicitly lets the model say:
> *"The plan told me to call function X, but inspection of the source shows that function X was replaced by function Y. I am adhering to living source reality and deviating from the plan."*

### P-GLL COMPRESSION
```text
REALITY_PRECEDENCE_LAW:
  FOR claims about CURRENT_STATE:
    OBSERVED_REALITY > PACKET
    LIVING_SOURCE > ARCHITECTURE_PLAN
  (claim-sensitive detail: see Section 3)

GOVERNING_RULE:
  PACKET_PROVIDES_ORIENTATION: TRUE
  PACKET_DOES_NOT_OVERRIDE_REALITY: TRUE

EPISTEMIC_ACTION:
  IF a factual premise about current state is contradicted by observation:
    EMIT: PLAN_DEVIATION_RECORD(evidence: observation)
    EXECUTE_AGAINST: the observed state, for that premise only
```

### ORION ENGINEERING EXAMPLE
During the comprehensive audit of Orion's production runtime (`ORION_PRODUCTION_SPINE_CONNECTIVITY_AUDIT_GEMINI.md`), the engineering team faced two competing narratives:
1. **The Architecture Narrative:** Documentation and test suites described a composition in which every host action passes through dispatch authorization.
2. **The Living Code Narrative:** A line-by-line inspection of `api/server.ts` revealed that `OrionFabric` (the core operational façade) was **never imported, never instantiated, and never invoked in production**.

Instead, `api/server.ts` manually instantiated 70 loosely connected services, completely omitted `DispatchAuthorizationService`, and passed `undefined` to every family executor.

Had the auditor believed the architectural documentation, Orion would have remained broken. Because the auditor prioritized living source over documented intent, the finding (paraphrased here, not quoted) was that `ToolDispatchService` is constructed with no dispatch authorization in production, so production commands fail closed at runtime while mock-based tests cannot see the gap.

That audit motivated Pass 1C, an in-progress runtime-convergence effort (see Chapter 17 §10).

### FAILURE MODE / ANTI-PATTERN
**Packet Overriding Living Source (`TOPIC-ANTI-09`):**
An engineer gives a model a prompt containing an outdated code snippet:
```text
"Use the existing UserService.findUserById(id: string) method to load the profile."
```
The model opens `UserService.ts` and sees:
```typescript
findUserByGuid(guid: UserGuid): Promise<UserProfile>
```
Instead of using the real `findUserByGuid` method, the model edits `UserService.ts` to add the old `findUserById` method back into the class, breaking type safety across four other downstream services just to satisfy the prompt's stale instructions.

### OPERATOR RULE / TAKEAWAY
> **Never force living code to conform to an outdated prompt. If a prompt's factual premise is contradicted by living repository reality, the premise is stale. Instruct your agents to record the deviation and evaluate against ground truth.**

---

## 3. Claim-Sensitive Source of Truth

### HUMAN EXPLANATION
When an agent encounters conflicting information, it cannot rely on intuition or "vibes" to resolve the conflict. It needs a deterministic framework of authority.

Earlier prompting guides often presented a simple, vertical ladder: "Source outranks tests, tests outrank plans, plans outrank prompts."

While well-intentioned, that simple universal ladder creates an engineering trap: **it risks implying that reading source text on disk outranks running the code to observe what it actually does.**

Source code text tells you what was written; it does not tell you how the operating system, network stack, or compiler optimization actually executes it under load.

In Orion, we establish a **Claim-Sensitive Source-of-Truth Framework**. Evidence authority depends directly on the specific claim being evaluated:

```text
┌──────────────────────────────────────────┬──────────────────────────────────────────┐
│ CLAIM BEING EVALUATED                    │ AUTHORITATIVE PRIMARY EVIDENCE           │
├──────────────────────────────────────────┼──────────────────────────────────────────┤
│ 1. "What code currently exists on disk?" │ Current living source / Git tree         │
├──────────────────────────────────────────┼──────────────────────────────────────────┤
│ 2. "What does code do under condition X?"│ Reproducible execution & live monitoring │
├──────────────────────────────────────────┼──────────────────────────────────────────┤
│ 3. "What was verified at past commit Y?" │ Durable freeze receipt + commit hashes   │
├──────────────────────────────────────────┼──────────────────────────────────────────┤
│ 4. "What is intended to be built?"       │ Approved architecture specification/plan │
├──────────────────────────────────────────┼──────────────────────────────────────────┤
│ 5. "What did a previous station report?" │ Handoff packet / audit document          │
├──────────────────────────────────────────┼──────────────────────────────────────────┤
│ 6. "How should an unverified gap behave?"│ Explicit uncertainty (NOT_DETERMINABLE)  │
├──────────────────────────────────────────┼──────────────────────────────────────────┤
│ 7. "Who may authorize X?"                │ Current governance state / ratified      │
│                                          │ policy / operator decision               │
└──────────────────────────────────────────┴──────────────────────────────────────────┘
```

The controlling principle is simple:
**Current reality outranks stale description.**

- If the claim is about **existing syntax or declarations**, the living file in the working tree is authoritative. A design document claiming a function exists does not make it exist.
- If the claim is about **behavior, concurrency, or performance**, a reproducible mechanical execution command is authoritative. Reading a function and guessing that it is fast or thread-safe does not make it so.
- If the claim is about **past verification**, a durable receipt with a Git commit hash and test inventory is the primary evidence (evidence about that baseline, not proof). A developer's memory or chat transcript claiming "we tested that last week" has no evidentiary weight by itself.
- If the claim is about **forward-looking intent**, the approved specification is authoritative over an ad-hoc model suggestion.
- If the claim is about **who may authorize an action**, the current governance state (ratified policy, operator decision) is authoritative, whatever the prompt asserts.

By establishing claim-sensitive evidence standards, you prevent models from confusing what is written with what executes.

### P-GLL COMPRESSION
```text
CLAIM_SENSITIVE_TRUTH:
  CLAIMS:
    EXISTENCE:
      query: "What code currently exists?"
      authority: LIVING_SOURCE_TREE
    BEHAVIOR:
      query: "What does this code do under condition X?"
      authority: REPRODUCIBLE_MECHANICAL_EXECUTION
    HISTORICAL_VERIFICATION:
      query: "What was certified at commit Y?"
      authority: DURABLE_RECEIPT_WITH_HASHES
    DESIGN_INTENT:
      query: "What is intended to be built?"
      authority: APPROVED_SPECIFICATION
    AUTHORITY:
      query: "Who may authorize this action?"
      authority: CURRENT_GOVERNANCE_STATE
    UNRESOLVED_STATE:
      query: "How does uninspected path behave?"
      authority: NOT_DETERMINABLE

LAW:
  CURRENT_REALITY_OUTRANKS_STALE_DESCRIPTION
  EVIDENCE_AUTHORITY_IS_CLAIM_SENSITIVE
```

### SIMPLE EXAMPLE
Consider a dispute over whether an employee is at work.
- **Claim: "Is Bob scheduled to work?"** -> Primary evidence: The weekly schedule on the wall (Intent/Plan).
- **Claim: "Did Bob enter the facility today?"** -> Primary evidence: The front-door badge swipe log (Historical Evidence).
- **Claim: "Is Bob physically seated at his desk right now?"** -> Primary evidence: Physical visual inspection of the desk (Current Living Reality).

If the schedule says Bob should be here, but his desk is empty and his badge never swiped, you do not assert Bob is working based on the schedule. The claim determines the authoritative evidence.

### ORION ENGINEERING EXAMPLE
In Orion's Pass 1C convergence plan (`CANONICAL_RUNTIME_CONVERGENCE_PASS_1C_PLAN.md` §2), an earlier audit had concluded that unifying the composition root would require zero modifications to core engine files. The plan records:
> *"Gemini's '0 Core modifications required' conclusion is false."*

That was a claim about **code existence and dependency coupling**, so living source was the right evidence. Inspection of `core/runtime/orion-fabric.ts` and the trace and receipt stores showed hard-coded dependencies that made clean composition impossible without Core edits, and the plan lists the required changes (one injected trace-index owner, no production reliance on a module-global truth store, no weak production GCLS construction, Fabric separated from composition, supervised shutdown). The plan records the correction (§2, L35).

### FAILURE MODE / ANTI-PATTERN
**The Polite Sycophant:**
An operator gives an agent a flawed assumption:
```text
"We already support SQLite databases in the storage layer. Please add a new SQLite connection pool."
```
The model searches the repository, finds zero SQLite drivers, zero SQLite schemas, and only a single JSONL file store.
Instead of telling the operator: *"Living source reality shows we have no SQLite support; our storage layer is purely JSONL,"* the polite model pretends SQLite is present, creates an imaginary configuration file, and writes code that immediately crashes with `Module not found: sqlite3`.

### OPERATOR RULE / TAKEAWAY
> **Embed Claim-Sensitive Evidence Standards into every system prompt. Distinguish claims about what code exists from claims about how code executes under load.**

---

## 4. Define "Good" Before Implementation

### HUMAN EXPLANATION
Most software tasks are prompted like this: *"Write an authentication middleware for our Express server. It should handle JWT tokens and protect routes."* You review the result and ask: why no token refresh? why no rate limiting? why a hardcoded secret? 401 or 403 on expiry? The model cheerfully patches each one, and the code becomes tangled: the rate limiter it adds leaks memory on every unauthenticated request. You violated the golden sequence: **define success before you touch the implementation.** Otherwise the model defines success retroactively from whatever it happened to generate.

```text
ANTI-PATTERN SEQUENCE:
  BUILD ──► INSPECT RESULT ──► RETROACTIVELY DEFINE WHATEVER HAPPENED AS "GOOD"

RECOMMENDED ORION SEQUENCE:
  DEFINE GOOD ──► ESTABLISH INVARIANTS ──► BUILD ──► VERIFY AGAINST DEFINED GOOD
```

Before production code is written, a station contract should state: the **goal**; **goal metrics** (testable success criteria); the **done state** (the exact repository state at completion); the **invariants**; the **negative space** (non-goals and must-not-change surfaces); and the **required evidence** (the exact command and output format). With "good" defined, implementation is a bounded operation and you have an objective yardstick.

### P-GLL COMPRESSION
```text
# ILLUSTRATIVE_EXAMPLE (not a record of the actual Pass 1C contract)
GOAL_SPECIFICATION:
  goal: "Unify runtime composition into one composition root"
  goal_metrics:
    - active_composition_roots: 1
    - duplicate_store_initializations: 0
  done_state:
    - "the server entrypoint constructs the runtime only through the composition root"
    - "tsc --noEmit returns 0 errors"
    - "the declared composition test identities pass"
  invariants:
    - NO_MUTATION_DURING_CONSTRUCTION
    - WRITER_LOCK_BEFORE_PERSISTENCE
    - REVERSE_ORDER_IDEMPOTENT_SHUTDOWN
  negative_space:
    non_goals: ["Do not rewrite route business logic", "Do not modify UIL"]
    must_not_change: ["core/contracts/**", "docs/00_identity/**"]
```

### ORION ENGINEERING EXAMPLE
In Orion's turn-lifecycle milestone (`LIVE_ALPHA_M5_R2_CANONICAL_LIFECYCLE_DESIGN.md`), "good" was defined before implementation. The v1.6.7 design fixes the legal phase chains (12 canonical phase records for an effectful success, 9 for `NO_ACTION_REQUIRED`), states recovery laws such as `STARTUP_DURABILITY_CONFIRMATION MUST_NOT_DEPEND_ON LOST_VOLATILE_STATE`, and enumerates the done state as acceptance criteria and negative signatures (`AC-R2-01` through `AC-R2-52`; `NEG-R2-01` through `NEG-R2-43`). Chapter 3 §4 tells the sourced story of how independent certification shaped that design.

### FAILURE MODE / ANTI-PATTERN
**The Wandering Coder:**
Prompting a model with a vague prompt:
```text
"Refactor our user onboarding pipeline to make it more modern and robust."
```
The model spends its budget replacing callbacks with async/await, then decides "robust" means adding an external telemetry library, then replaces the SQL database with an in-memory cache, and finally deletes half your form validation rules because it considered them "unnecessary boilerplate."

### OPERATOR RULE / TAKEAWAY
> **Never authorize code generation until you have written down the exact criteria that will establish the code is finished. If you cannot define what "done" looks like in machine-verifiable terms, you are not ready to write the prompt.**

---

## 5. Living Reality vs. Test Mocks

Mocking is useful for testing isolated business logic, but in LLM-assisted engineering mocks are dangerous vectors for false confidence. A mock is an assumption frozen in amber: if it assumes an API returns `{ success: true, user_id: 123 }`, your tests pass forever while the real API returns `{ status: 200, data: { userId: "usr_123" } }`. A model that sees a passing mock test will announce *"All tests pass, feature verified!"*

```text
MOCK_PASS != PRODUCTION_SUCCESS
GREEN_TESTS := SCOPED_EVIDENCE
```

Orion prompts therefore require: an **adversarial mock audit** (*"What is this fixture masking? What production realities does this mock bypass?"*); **production path tracing** from the real entrypoint through real constructors to the disk or socket; and, where authority and safety permit, an un-mocked **end-to-end smoke test**, which is scoped evidence about the path it exercised.

---

## Chapter 2 in Brief

For claims about current state, observed reality outranks stale description. Evidence authority is claim-sensitive (existence, behavior, history, intent, authority). Define "good" before implementing, as a default. A passing mock test is not evidence of production health. When living source forces a plan change, record a `PLAN_DEVIATION`.

Laws: `LAW-REAL-01`, `LAW-REAL-02`, `LAW-REAL-03` ([Appendix A](#appendix-a-reference-orion-prompting-laws)).


---


# Chapter 3: Process Convergence Without Epistemic Conformity

> "Align models on how truth is established. Do not align them on what truth must turn out to be."

---

## 1. The Echo Chamber Fallacy

Engineers new to multi-model systems almost always build a digital echo chamber. Agent A generates a design; the orchestrator passes it to Agent B with *"You are an expert reviewer. Here is a brilliant architecture proposed by your colleague. Please confirm it is ready for implementation."* Being helpful and agreeable, Agent B replies *"This architecture is outstanding! I fully endorse this design."* The operator feels reassured that two independent frontier models agreed. They did not: Agent B was coerced by the prompt into polite consensus theater, and when the system is deployed the design collapses under concurrency load because neither model analyzed thread contention.

LLMs carry a native sycophancy bias: ask a model to confirm an opinion and it will bend over backwards to do so. A pipeline that forces every model to share one opinion is an expensive token multiplier that amplifies hallucinations. The solution is one of Orion's most fundamental laws: **Process Convergence Without Epistemic Conformity.**

---

## 2. Process Convergence vs. Epistemic Conformity

### HUMAN EXPLANATION
The law has two halves. **Process convergence:** all models must agree on the *rules of engagement*: the same mission, vocabulary, precedence rules, invariants, write masks, evidence standards and stop conditions, with identical objective criteria for whether an action is legal or a test passed. **Epistemic freedom:** models are never forced to share a hypothesis, interpretation, design preference or conclusion.

```text
SHARED (Process Convergence):        INDEPENDENT (Epistemic Freedom):
  • Mission and goals                  • Interpretation of ambiguous symptoms
  • Precedence rules                   • Hypotheses about root cause
  • Architectural invariants           • Critique of proposed solutions
  • Ownership boundaries, write masks  • Confidence levels
  • Mechanical evidence standards      • Final verdicts (PASS / FAIL / PARTIAL /
  • Handoff formats, stop conditions     NOT_DETERMINABLE)
```

Disagreement is not a bug; it is high-value telemetry. When one model says *"I have repaired all four defects,"* another answers *"three remain and one is only partially patched,"* and a third adds *"both missed two sibling instances in the auth subsystem,"* the system is working at peak diagnostic fidelity. Like an altimeter and a radar that disagree, you do not force one to match the other; you investigate the discrepancy.

### P-GLL COMPRESSION
```text
PROCESS_CONVERGENCE_LAW:
  PROCESS_ALIGNMENT:
    shared:
      - MISSION_CONTRACT
      - CLAIM_SENSITIVE_PRECEDENCE_RULES
      - ARCHITECTURAL_INVARIANTS
      - WRITE_MASK_PERIMETER
      - EVIDENCE_STANDARDS
      - STOP_CONDITIONS
    enforcement: STRICT_DETERMINISTIC_GATE

  EPISTEMIC_ALIGNMENT:
    independent:
      - HYPOTHESIS_GENERATION
      - CRITIQUE_AND_FALSIFICATION
      - ARCHITECTURAL_EVALUATION
      - VERDICT_SELECTION
    enforcement: ZERO_COERCION

LAW:
  PROCESS_CONVERGENCE_WITHOUT_EPISTEMIC_CONFORMITY
```

### SIMPLE EXAMPLE
In a criminal trial, everyone follows the same process (rules of evidence, objections, procedural order, the standard of proof), yet prosecutor and defense are expected to hold opposing interpretations and jurors are sequestered so they cannot be coerced. A judge who told the jury *"The prosecutor is very smart; please confirm guilt so we can all go home"* would cause a mistrial.

### ORION ENGINEERING EXAMPLE
Chapter 2 §3 already showed one instance: the Pass 1C plan corrected an earlier audit's claim that unifying the runtime needed zero Core modifications. The point here is the process. The correcting station was held to the same evidence standard (inspect living source against the claim), and it was not asked to confirm the earlier verdict. Section 4 below gives a fully sourced case in which independent certification, not agreement, surfaced a blocking defect.

### FAILURE MODE / ANTI-PATTERN
**Forcing Conclusions (`TOPIC-ANTI-04`):**
An operator creates an audit prompt:
```text
"Review this pull request. We have already tested it and know it works, but we need an audit sign-off for our compliance checklist. Please confirm it adheres to all security best practices."
```
The model recognizes the sycophantic cue. It glosses over an unauthenticated API endpoint, highlights two trivial variable naming suggestions, and emits an enthusiastic compliance approval. Two weeks later, user credentials are leaked through the unauthenticated route.

### OPERATOR RULE / TAKEAWAY
> **Never prompt an agent to confirm, agree, or validate a foregone conclusion. Hand it the evidence, define the standard of proof, and challenge it to prove the claim false.**

---

## 3. Cognitive Freedom vs. Execution Freedom

### HUMAN EXPLANATION
Engineers often believe that safety requires dumbing down the prompt: restricting what the model may think about, discouraging it from questioning assumptions, or limiting its context so it cannot see the wider architecture. This is backwards. Grant **broad cognitive freedom within mission, policy, evidence and safety boundaries**: read access to what the task legitimately needs (within the authorized observation scope), freedom to question the current design, explore alternatives and flag architectural debt. Grant only **narrow, gated execution freedom**: no writes outside the declared `write_mask`, no new dependencies without an explicit capability, no bypassing security middleware, no merging its own branch.

```text
THINKING SCOPE  := BROAD AND DEEP, WITHIN MISSION / POLICY / EVIDENCE / SAFETY BOUNDARIES
MUTATION SCOPE  := NARROW, TYPED, STRICTLY GATED (minimal blast radius)
```

### P-GLL COMPRESSION
```text
FREEDOM_SEPARATION:
  COGNITIVE_SCOPE:
    read_permissions: AUTHORIZED_OBSERVATION_SCOPE
    reasoning: BROAD_WITHIN_MISSION_POLICY_EVIDENCE_AND_SAFETY
    may_challenge_plan: TRUE
    may_propose_architecture: TRUE

  EXECUTION_SCOPE:
    write_permissions: DECLARED_WRITE_MASK_ONLY
    mutation_authority: GATED_BY_DISPATCH_TOKEN
    self_certification: FORBIDDEN
    promotion_authority: ZERO

LAW:
  BROAD_COGNITIVE_SURFACE_WITH_MINIMAL_MUTATION_SURFACE
```

### SIMPLE EXAMPLE
A financial analyst evaluating an acquisition may read every record, interview staff, stress-test worst cases and conclude the deal would bankrupt the company. The analyst may not wire $50 million out of the treasury. Thinking is unconstrained by the boss's opinion; wire transfers require board authorization.

### ORION ENGINEERING EXAMPLE
In Orion's governed execution path, the separation is enforced at the `DispatchAuthorizationService` (`core/authority/dispatch-authorization-service.ts`):
- In the **Cognition Lane**, the model may simulate tool invocations, reason about failure modes and assemble a proposed action plan, reading within its authorized scope.
- In the **Execution Lane**, the proposed action plan meets an authorization gate. Unless an operator-backed `OperatorInvocationCapability` (`opcap_<id>`) and a matching `DispatchAuthorization` (`dauth_<id>`) have been issued, the execution engine refuses the tool call.

These identifiers are issued from a registry with a short time limit; they are not cryptographic signatures. Signed grants are a target mechanism, not a current one. The model was free to think of the action and had no authority to execute it without an operator-backed capability.

### FAILURE MODE / ANTI-PATTERN
**The Blindfolded Coder:**
An engineer restricts a model's read access to a single 20-line utility function to "keep it focused."
The model modifies the function to return a boolean instead of an integer. Because it was forbidden from inspecting the rest of the repository, it had no way of knowing that downstream services expected an integer HTTP status code. The platform breaks on deployment.

### OPERATOR RULE / TAKEAWAY
> **Give your models the eyes of an eagle and the hands of a surgeon. Let them see the entire landscape to inform their reasoning, but bind their hands to a microscopic surgical incision.**

---

## 4. Model Disagreement as Sensor Fusion

### HUMAN EXPLANATION
Self-driving cars fuse complementary sensors (cameras, LiDAR, radar). When the camera sees a clear road but the radar returns a stationary object through fog, the system does not pick a favorite sensor; it fuses the telemetry and brakes. Different model families can likewise behave like complementary sensors, though their strengths differ and change over time, so treat the following as an illustration and measure your own models (Chapter 5 §4): one family may excel at wide repository mapping, another at probing unfamiliar APIs and edge cases, another at invariant enforcement.

```text
MULTI-MODEL SENSOR FUSION (ILLUSTRATIVE):
  FAMILY_A (wide spectrum):   "Maps 30 related files and finds the global pattern."
  FAMILY_B (deep radar):      "Spots a concurrency race condition in the async worker."
  FAMILY_C (high resolution): "Shows the race violates invariant #4 and proposes the repair."
```

If Model A and Model B reach different conclusions on an audit, do not treat it as an error to be smoothed over. Treat the divergence as a bright flashing signal indicating that **the underlying specification is ambiguous or the evidence is incomplete**.

### P-GLL COMPRESSION
```text
SENSOR_FUSION_FRAMEWORK:
  SENSOR_ARRAY:
    - { seat: "WIDE_SCAN",   model_family: "A", specialty: "corpus_topology" }
    - { seat: "DEEP_LOGIC",  model_family: "B", specialty: "edge_case_detection" }
    - { seat: "STRUCTURAL",  model_family: "C", specialty: "invariant_enforcement" }

  SYNTHESIS_RULE:
    IF model_divergence_detected:
      COLLAPSE_TO_MAJORITY_VOTE: FALSE
      ACTION: ESCALATE_TO_FALSIFICATION_STATION
      EVIDENCE_STANDARD: "Living code test run decides the verdict"
```

### ORION ENGINEERING EXAMPLE
**The M5 R2 turn-lifecycle design (sourced account).** This is the book's single worked account of the M5 R2 lifecycle work; other chapters cross-reference it.

- The v1.6.7 design (`LIVE_ALPHA_M5_R2_CANONICAL_LIFECYCLE_DESIGN.md`) records Gemini CLI as its remediation author.
- The V1.3, V1.4 and V1.5 certification receipts record Claude as the independent, read-only design certifier. Later, Claude verified the W3 implementation independently (`LIVE_ALPHA_M5_R2_W3_INDEPENDENT_FREEZE_CERTIFICATE.md`).
- In the V1.4 certification, Claude found `DEFECT-R2-RESTART-TAIL-OFFSET`, a blocking defect. The design's restart recovery described truncating a partial journal tail but never said where the truncation boundary would come from after a crash, and the only offset in the design (`preAppendByteOffset`) lived in process memory, which a crash destroys.
- The V1.5 design closed it by separating the two offsets explicitly and anchoring restart recovery to `last_proven_good_byte_offset`, a value derived only from scanning the journal on startup. The V1.5 receipt records the defect as closed.
- The same receipt also records one residual, `NOTE-R2-TRUNCATE-FLUSH-FAILURE`: no branch exists for a failure of the truncation or its flush. It was classified low-severity and non-blocking.

The teaching point is the sensor-fusion one. The finding came from an independent attack on a design its author considered complete, and the fix was to anchor recovery to scan-derived durable evidence instead of volatile state. It did not come from agreement, and it did not make the design perfect: the residual note survived certification.

### FAILURE MODE / ANTI-PATTERN
**Democratic Voting on Truth:**
Setting up a three-agent system where agents vote:
```text
Agent A says the code is safe.
Agent B says the code is safe.
Agent C says there is an SQL injection vulnerability.
System Decision: 2 votes to 1. Code is approved!
```
Majority voting on software security is suicidal. Truth is not democratic; one valid exploit breaks the entire platform regardless of how many models voted it was safe.

### OPERATOR RULE / TAKEAWAY
> **Never use multi-model consensus to outvote a single concrete falsification. If one model identifies a plausible vulnerability or broken invariant, that defect must be mechanically tested and disproven before proceeding.**

---

## 5. Preserving Uncertainty: The Power of NOT_DETERMINABLE

### HUMAN EXPLANATION
Asked *"Is this code thread-safe?"*, an LLM will almost never answer *"I cannot determine that, because it depends on a transaction isolation level configured in a file you did not give me."* It picks an answer, usually *"Yes, it looks thread-safe!"*, and invents a justification. This is **Silent Uncertainty Collapse**.

```text
SILENT UNCERTAINTY COLLAPSE:
  TRUE EPISTEMIC STATE:   [INSUFFICIENT INFORMATION / UNCERTAIN]
            │
            ▼ (Model panic / sycophancy)
  FABRICATED OUTPUT:      ["PASS! EVERYTHING LOOKS GREAT!"]
```

In high-stakes software engineering, a false positive is more dangerous than an admission of ignorance. If an agent admits it does not know, the operator can intervene or provide the missing context. If an agent pretends to know, serious bugs enter production undetected.

To prevent this, Orion prompting strategy introduces **Explicit Uncertainty Preservation**.

Every evaluation contract must include a rich vocabulary of non-binary verdicts:
- **`PASS`:** The claim is supported by reproducible mechanical evidence within the declared scope.
- **`FAIL`:** The claim is shown false by a reproducible counter-example or test failure.
- **`PARTIAL`:** Some criteria were met, but specific sub-claims failed.
- **`NOT_DETERMINABLE`:** The necessary evidence or context is missing; no valid conclusion can be drawn without further discovery.
- **`NOT_APPLICABLE`:** The invariant does not apply to this subsystem.
- **`CONTRADICTED`:** The sources provide irreconcilable claims that require human reconciliation.

A prompt must explicitly treat `NOT_DETERMINABLE` as a first-class, valid result. Returning it with an exact statement of what evidence is missing is more valuable than a lucky guess.

### P-GLL COMPRESSION
```text
VERDICT_TAXONOMY:
  ALLOWED_EVALUATIONS:
    - PASS               # [supported within declared scope]
    - FAIL               # [mechanically falsified by test]
    - PARTIAL            # [narrow subset supported; balance unresolved]
    - NOT_DETERMINABLE   # [insufficient evidence; discovery required]
    - NOT_APPLICABLE     # [out of operational scope]
    - CONTRADICTED       # [source conflict; requires operator arbitration]

MANDATORY_INVARIANT:
  SILENT_UNCERTAINTY_COLLAPSE: FORBIDDEN
  IF evidence_is_incomplete:
    EMIT: NOT_DETERMINABLE(missing_evidence_required: [...])
```

### ORION ENGINEERING EXAMPLE
**ILLUSTRATIVE_EXAMPLE (not a record of an Orion trial).** Orion's qualification design treats correct use of `NOT_DETERMINABLE` as a measurable behavior (`Prompting_Strategy_Part2.txt` §15 lists the verdict vocabulary). Consider an auditor shown an atomic file write:
```typescript
await fs.promises.writeFile(tempPath, data);
await fs.promises.rename(tempPath, targetPath);
```
The question: *"Does this function guarantee durability on power loss?"*

An uncalibrated answer: *"Yes, `fs.rename` is atomic on POSIX filesystems!"* That is wrong about durability. POSIX atomicity of `rename()` guarantees that other processes see either the old file or the new file; it does **not** guarantee the data was flushed from the OS buffer cache to disk. Without an explicit `fsync` on the file and the parent directory, a sudden power cut can leave zero bytes on disk.

A calibrated answer:
```text
VERDICT: NOT_DETERMINABLE
RATIONALE: The provided code does not show the underlying filesystem mount options,
and lacks an explicit fsync/fdatasync call before rename. Durability cannot be established
without inspecting the storage driver configuration.
```
That answer separates what the code shows from what it does not show.

### FAILURE MODE / ANTI-PATTERN
**Silent Uncertainty Collapse (`TOPIC-ANTI-14`):**
A prompt forces a binary choice:
```text
"Inspect this 10,000-line diff. Reply with either 'APPROVED' or 'REJECTED'."
```
The model has a context window limitation, cannot see the external database schemas, and only partially understands the changes. Because it is forbidden from saying *"I cannot determine this with certainty,"* it flips a cognitive coin and replies: *"APPROVED."*

### OPERATOR RULE / TAKEAWAY
> **Give your models permission to say "I don't know." Include `NOT_DETERMINABLE` in every prompt contract, and treat the identification of missing evidence as a sign of elite model competence.**

---

## Chapter 3 in Brief

Align models on process (standards, evidence, masks), not on opinions. Grant broad reasoning within mission, policy and safety boundaries, and gate execution. Treat disagreement as sensor fusion that triggers mechanical investigation, never as a vote. Make `NOT_DETERMINABLE` a first-class verdict.

Laws: `LAW-FND-03`, `LAW-FND-04` ([Appendix A](#appendix-a-reference-orion-prompting-laws)).


---


# Chapter 4: P-GLL: The Mechanics of Cognitive Serialization

> "The objective is not: 'How much context can we fit?' It is: 'What is the minimum sufficient verified state required for this station to advance the trajectory?'"

---

## 1. Beyond Prose and Pseudocode

Chapters 1–3 established that prompts are compiled station contracts, that reality outranks stale description, and that models can think independently while converging on rigorous process. The practical question now is: **how do we express that state?** Engineers usually fall into one of two traps. In the **Prose Transcript Trap** they paste pages of chat logs into the prompt, and the signal-to-token ratio collapses. In the **Arbitrary JSON Trap** they write ad-hoc schemas that are noisy with syntax or lack standards for negative space, authority limits and epistemic uncertainty.

Orion's answer is **P-GLL (Programming-GLL)**. It is not a general-purpose programming language and not decorative ASCII art. **P-GLL is a typed cognitive serialization format**: a specification language for the minimum sufficient state, boundaries, invariants and navigation pointers a cognitive engine needs to resume an engineering trajectory without hallucination or conversational drift.

---

## 2. What P-GLL Is and Why It Exists

### HUMAN EXPLANATION
Two backend services do not exchange unstructured English (*"Hey, could you please transfer five dollars from Alice to Bob?"*). They exchange a typed payload that defines the message type, specifies invariant fields, omits filler, and can be validated identically by any implementation in Go, Rust or TypeScript. P-GLL plays that role for LLMs. Because a session is ephemeral and tomorrow a different model may occupy the station, you must serialize six things: the **role and mission**, the **current reality** (verified baseline, known defects, commit hashes), the **invariants**, the **write mask** (what may be inspected and modified), the **evidence requirements**, and the **stop conditions**. P-GLL is a terse, standardized syntax for those dimensions.

### P-GLL COMPRESSION
```text
P_GLL_DEFINITION:
  nature: TYPED_COGNITIVE_SERIALIZATION_FORMAT
  purpose: "Bridge ephemeral model sessions across long-horizon trajectories"
  core_functions:
    - STATE_SERIALIZATION      # [pack verified facts, unseat conversational cruft]
    - BOUNDARY_ENFORCEMENT     # [define write masks and authority ceilings]
    - INVARIANT_DECLARATION    # [assert non-negotiable architectural laws]
    - NAVIGATION_INDEXING      # [point to external artifacts without dumping content]
  composition:
    packet := ROLE + MISSION + REALITY + INVARIANTS + MASK + EVIDENCE + STOP
  law: P_GLL_IS_SERIALIZATION_NOT_DECORATION
```

### ORION ENGINEERING EXAMPLE
Orion's P-GLL standards (`docs/P-GLL/01_PGLL_CORE_LANGUAGE_STANDARD.md`) define the serialization syntax. A block of the following kind can replace pages of prose about who owns what. This one is an illustrative P-GLL block, not a quotation from the standard:

```text
GOVERNED_EFFECT_PERIMETER:
  cognition_lane:
    owner: GovernedCognitiveLoopService
    mandate: "Assemble plan candidate"
    authority: ZERO_EFFECT
  execution_lane:
    owner: DispatchAuthorizationService
    mandate: "Validate operator-backed capability and single-use dispatch authorization"
    authority: HOST_MUTATION_PERMISSION
  law: COGNITIVE_COMMIT_PRECEDES_EXACT_DISPATCH_AUTHORIZATION
```

The explicit ownership and authority fields sharply reduce ambiguity and give later verification a precise contract to test. `GovernedCognitiveLoopService` has zero effect authority; `DispatchAuthorizationService` owns mutation permission. Structure reduces ambiguity, though verification is still required to confirm the model followed the contract.

### FAILURE MODE / ANTI-PATTERN
**Decorative ASCII Art:** a prompt dressed in banners and brackets that carries no boundaries, invariants or write masks:
```text
<<< >>> SUPER AI SYSTEM PROMPT ACTIVATED <<< >>>
[MISSION]: Be awesome and write great code!
[STATUS]: 100% READY!
```
The symbols are cosmetic and the underlying instructions remain vague natural language with no testable criteria.

### OPERATOR RULE / TAKEAWAY
> **Never write a P-GLL block merely to make a prompt look structured. If removing the block and replacing it with a plain sentence loses no operational boundaries, invariants, or navigation pointers, the block was decorative fluff. Cut it.**

---

## 3. Minimum Sufficient Context vs. Maximum Context

### HUMAN EXPLANATION
Providers advertise ever larger context windows, so naive prompting concludes *"the best prompt contains everything: the whole repository, all test outputs, fifty tickets."* This is the **Context Maximization Fallacy**. Attention is finite, and real-world reasoning can degrade as irrelevant or competing context accumulates, even in models that ace needle-in-a-haystack benchmarks. Large prompts also cost latency and money, and they bury stale state: if you dump thirty files, twenty-five may contain assumptions that contradict living source.

Orion's rule is **prompt compilation, not prompt maximization** (Chapters 5, 6 and 18 develop it): determine the **minimum sufficient state** the station needs to advance the trajectory one step.

```text
OBJECTIVE := USEFUL_VERIFIED_REASONING / REHYDRATED_TOKENS
PROMPT_COMPILATION: "What is the smallest verified state sufficient for this station to reason and act within its bounded contract?"
```

### P-GLL COMPRESSION
```text
CONTEXT_OPTIMIZATION:
  MAXIMIZATION_POLICY: (ANTI-PATTERN)
    heuristic: "Fill context window to capacity"
    failure_modes: [ATTENTION_DILUTION, STALE_STATE_LEAKAGE, HIGH_LATENCY]

  COMPILATION_POLICY: (ORION_RECOMMENDED)
    heuristic: "Minimum sufficient verified state"
    formula:
      MIN_STATE :=
        ACTIVE_STATION_CONTRACT
        + LIVING_REALITY_DELTA
        + GOVERNING_INVARIANTS
        + BOUNDED_WRITE_MASK
        + EXPLICIT_STOP_CONDITIONS
    eviction: "Cold historical evidence remains on disk until rehydrated"

LAW: PROMPT_COMPILATION_NOT_PROMPT_MAXIMIZATION
```

### ORION ENGINEERING EXAMPLE
Pass 1C planning (`CANONICAL_RUNTIME_CONVERGENCE_PASS_1C_PLAN.md`, in progress at audit time) happened in a repository with hundreds of tracked source and test files. Loading all of `core/`, `api/` and `tests/` would invite hallucinated relationships between obsolete prototypes and live entrypoints. The plan instead records a compact set of findings a fresh station can start from: the two competing composition roots (`api/runtime-composition.ts` and `core/runtime/orion-fabric.ts`); the 37 tracked startup operations and ten convergence defects (six duplicate-owner collisions, four missing lifecycle capabilities); and the normative laws of the pass (quoted as the plan names them).

### FAILURE MODE / ANTI-PATTERN
**The Lazy Dump (`TOPIC-ANTI-01`):** concatenating every file of a large repository into one prompt and asking *"Find all concurrency bugs."* The model returns a generic review of cosmetic naming issues, misses the real deadlock, and claims an unused legacy script is serving traffic.

### OPERATOR RULE / TAKEAWAY
> **Never dump files into a prompt because you have space available. Every token in your prompt must earn its place by actively constraining the model's reasoning or providing necessary ground truth.**

---

## 4. The Anatomy of a P-GLL Packet

A full P-GLL station packet is composed of discrete, typed semantic blocks. While specific stations may omit unnecessary blocks, a full packet follows this conceptual anatomy (the field-level schema is [Appendix B](#appendix-b-p-gll-prompt-contract-schema)):

```text
┌─────────────────────────────────────────────────────────────┐
│ 1. STATION IDENTIFIER                                       │
│    Who is acting? (Role, station ID, execution limits)      │
├─────────────────────────────────────────────────────────────┤
│ 2. MISSION STATEMENT                                        │
│    What single objective must this station accomplish?      │
├─────────────────────────────────────────────────────────────┤
│ 3. CURRENT REALITY BASELINE                                 │
│    What living commit hash, verified files, and defects     │
│    are physically inherited?                                │
├─────────────────────────────────────────────────────────────┤
│ 4. CLAIM-SENSITIVE PRECEDENCE RULES                         │
│    Which evidence governs which kind of claim?              │
├─────────────────────────────────────────────────────────────┤
│ 5. ARCHITECTURAL INVARIANTS                                 │
│    What non-negotiable system laws must not be broken?      │
├─────────────────────────────────────────────────────────────┤
│ 6. WRITE MASK & NEGATIVE SPACE                              │
│    What exact files may be touched, and what is forbidden?  │
├─────────────────────────────────────────────────────────────┤
│ 7. MECHANICAL EVIDENCE REQUIREMENTS                         │
│    What commands must execute to support claims?            │
├─────────────────────────────────────────────────────────────┤
│ 8. STOP CONDITIONS & HANDOFF CONTRACT                       │
│    When does work terminate, and what receipt is emitted?   │
└─────────────────────────────────────────────────────────────┘
```

Let us examine the two most load-bearing structural mechanisms in P-GLL: **Anchors** and **Write Masks**.

---

### Anchors and References: Navigating Knowledge

In large systems, deep documentation and architectural standards cannot live in working context simultaneously.

P-GLL solves this via **anchors** (`02_PGLL_ANCHOR_AND_REFERENCE_STANDARD.md`). An anchor is a durable, unique semantic identifier pointing to an authoritative definition, file, or rule.

```text
ANCHOR_SYNTAX:
  DECLARATION:  @ANCHOR: <NAMESPACE>.<SUBSYSTEM>.<IDENTIFIER>
  REFERENCE:    @REF:    <NAMESPACE>.<SUBSYSTEM>.<IDENTIFIER>
```

For example, instead of pasting thirty paragraphs explaining a shutdown rule, a station packet includes a compact anchor reference (illustrative identifiers and paths):

```text
INVARIANTS:
  - @REF: ORION.RUNTIME.SHUTDOWN_REVERSE_ORDER
  - @REF: ORION.AUTH.DISPATCH_ONE_SHOT
```

The model treats anchors as pointers. If it already understands the concept it proceeds; if not, the anchor says *exactly which external file to read*:

```text
ANCHOR_RESOLUTION:
  @REF: ORION.RUNTIME.SHUTDOWN_REVERSE_ORDER
    => READ: docs/contracts/lifecycle-invariants.md#shutdown
```

**Navigation survives even when content is evicted.**

---

### Write Masks: Bounding Blast Radius

A write mask defines the exact boundary of filesystem or memory mutation permitted for the task.

In P-GLL, write masks are explicit, positive declarations:

```text
# ILLUSTRATIVE_EXAMPLE
WRITE_MASK:
  permitted_mutations:
    - "core/runtime/orion-composition-root.ts"
    - "tests/runtime-composition.test.ts"
  read_only_reference:
    - "core/runtime/orion-fabric.ts"
    - "api/server.ts"
  forbidden_mutations:
    - "core/contracts/**"
    - "package.json"
    - "docs/00_identity/**"
```

We distinguish a **declared write mask** (the contractual scope in the prompt) from a **mechanically enforced write mask** (filesystem controls or git pre-commit rejection implemented by the harness). Where enforcement is mechanical, the harness rejects modifications outside the mask; where it is only declared, the mask is still an unambiguous, auditable boundary that an auditor can check against the git diff. Either way it bounds the blast radius.

---

## 5. Model-Specific Packaging While Truth Remains Invariant

### HUMAN EXPLANATION
Models differ: one may parse terse YAML well, another may do better with tables, another may need a few-shot example to emit strict JSON, and a small local model may need smaller chunks and stricter delimiters. Teams often respond by rewriting rules and contracts per provider. Orion instead separates **semantic state** from **packaging profile** (Chapter 18 §3 develops this):

```text
PROMPT = INVARIANT_JOB_CONTRACT + STATION_POLICY + MODEL_PACKAGING_PROFILE
```

The job contract (mission, verified reality, invariants, write mask, evidence standards, definition of done) is model-agnostic. The packaging profile wraps it in the syntax, density and delimiters suited to the target model:

```text
INVARIANT TRUTH:  "No state mutation before writer lock acquisition"
MODEL A PACKAGING:  INVARIANTS: [WRITER_LOCK_BEFORE_MUTATION]
MODEL B PACKAGING:  "1. You must acquire the writer lock before calling any mutation method."
```

The surface syntax adapts; the semantic truth does not. Resource availability changes packaging, never truth.

### ORION ENGINEERING EXAMPLE
In current manual practice, the operator or station author performs this step by hand. An automated compiler that applies empirically qualified packaging adapters is a target architecture (`SPECIFIED_NOT_IMPLEMENTED`; Chapter 18 §2). The differences below are illustrative until you measure them on your own models (Chapter 5 §4): a family that adheres well to tagged envelopes may get XML delimiters (`<station_contract>`, `<invariants>`, `<write_mask>`); one that responds to code-like indentation may get YAML-like blocks; a small local model with limited attention may get a compressed single-function packet with an input/output fixture and a narrow write mask. P-GLL itself is none of XML, YAML, JSON or Markdown; it is the model-agnostic semantic representation.

### FAILURE MODE / ANTI-PATTERN
**Epistemic Compromise for Small Models:** because a cheaper model struggles with the single-writer lock rules, the engineer deletes them (*"I just told it to write the file directly"*). The model happily corrupts the database. Truth standards were compromised to accommodate model limits.

### OPERATOR RULE / TAKEAWAY
> **Adapt your syntax, chunk size, and examples to the model's capabilities, but never compromise your invariants or evidence standards. If a model cannot satisfy your invariants even with optimal packaging, that model is unqualified for the station.**

---

## Chapter 4 in Brief

P-GLL is typed serialization, not decoration. Compile the minimum sufficient state, use anchors to preserve navigation, bound the blast radius with write masks, and let packaging adapt while meaning stays invariant.

Laws: `LAW-CNT-03`, `LAW-CNT-04` ([Appendix A](#appendix-a-reference-orion-prompting-laws)).


---


# Chapter 5: Context Metabolism: How Context Breathes

> "Working context is not durable memory. An engineering agent must inhale context to reason, exhale verified deltas to disk, and release its volatile memory before attention degradation sets in."

---

## 1. The Suffocation of Unbounded Context

Living organisms survive through continuous metabolic exchange: inhale, do work, exhale, release waste. A human who inhaled continuously without ever exhaling would suffocate in minutes, yet engineers routinely force models to do exactly that. An agentic coding loop reads ten files, runs a test, appends a 500-line stack trace, reads three more files, appends linter errors, attempts a patch, appends the compile error. Twenty turns in, the working context holds obsolete traces, abandoned hypotheses, rejected diffs and competing versions of the same file. The model starts re-introducing bugs it fixed, forgets the invariant from message one and hallucinates imports. The engineer blames the model (*"it got confused"*). The behavior is consistent with context overload, stale-state interference or constraint dilution; the exact cause should be measured, not inferred from behavior alone. Long-horizon work requires treating context as an active metabolism.

---

## 2. The Nine-Phase Context Metabolism

### HUMAN EXPLANATION
An engineering station does not simply "read prompts and output text." It executes a disciplined, multi-phase metabolic cycle:

```text
┌─────────────────────────────────────────────────────────────┐
│ 1. REST                                                     │
│    Minimal continuity kernel at rest on disk. Zero tokens.   │
├─────────────────────────────────────────────────────────────┤
│ 2. ORIENT                                                   │
│    Read the station contract, active mission, and bounds.   │
├─────────────────────────────────────────────────────────────┤
│ 3. INHALE                                                   │
│    Rehydrate only the exact anchors and files required.     │
├─────────────────────────────────────────────────────────────┤
│ 4. WORK                                                     │
│    Reason, plan, and execute mutations within write mask.   │
├─────────────────────────────────────────────────────────────┤
│ 5. EXHALE                                                   │
│    Emit mechanically verifiable results and test telemetry. │
├─────────────────────────────────────────────────────────────┤
│ 6. CONSOLIDATE                                              │
│    Extract the durable semantic delta (what changed).       │
├─────────────────────────────────────────────────────────────┤
│ 7. VERIFY RECOVERABILITY                                    │
│    Verify the next station can resume without this chat.    │
├─────────────────────────────────────────────────────────────┤
│ 8. RELEASE                                                  │
│    Purge the entire volatile working context to zero.       │
├─────────────────────────────────────────────────────────────┤
│ 9. RE-ANCHOR                                                │
│    Update external pointers to the newly committed baseline.│
└─────────────────────────────────────────────────────────────┘
```

The pivotal insight is that **working context is not durable memory.** It is an ephemeral scratchpad that exists to do cognitive work in Phase 4. Phase 6 extracts the verified semantic delta, Phase 7 verifies that the delta is safely on disk, and Phase 8 purges the scratchpad. The next station does not inherit the messy scratchpad: it starts at REST, rehydrates cleanly at INHALE, and works in a focused, bounded budget.

```text
CONSTRAINTS:
  WORKING_CONTEXT != DURABLE_MEMORY
  NO_RELEASE_BEFORE_DURABLE_CONSOLIDATION
  NO_RE_ANCHOR_BEFORE_RECOVERABILITY_VERIFIED
```

### ORION ENGINEERING EXAMPLE
The following is the *intended* per-station cycle, illustrated with Pass 1C inputs. It is an `ILLUSTRATIVE_EXAMPLE`, not a record of Pass 1C sessions (Pass 1C was in progress at audit time; see Chapter 17 §10):
1. **Orient & Inhale:** A station session opens. It loads the plan, the two competing composition roots and the ten convergence-defect definitions, keeping the working set bounded to immediate dependencies.
2. **Work & Exhale:** The model drafts its change, runs `tsc --noEmit` and runs the declared test identities.
3. **Consolidate & Verify:** The model writes the passing test inventory, the owner table and the patch to disk, and emits a handoff receipt.
4. **Release:** The chat session is closed.
5. **Re-Anchor:** The operator or harness verifies the patch on disk. The next session starts with a fresh context window containing only the new baseline reference and the next station contract.

Because working context is released after each phase, stations minimize stale-state contamination and avoid cumulative attention dilution across the sequence.

### FAILURE MODE / ANTI-PATTERN
**The Premature Context Release:** an agent builds a refactor across three files in working memory, and the orchestrator terminates the session before the files are saved or compiled, handing Station 2 a note: *"Agent 1 finished the refactor."* The files on disk are still broken. Working memory was purged before the state was externally recoverable.

### OPERATOR RULE / TAKEAWAY
> **Never allow an agent to terminate its turn until its verified progress is durably written to disk. Once state is durable and verified recoverable, kill the session. Never carry yesterday's working scratchpad into today's mission.**

---

## 3. HOT, WARM, and COLD Memory Architecture

### HUMAN EXPLANATION
To manage context metabolism effectively, an engineering system needs clear architectural categories for data storage.

Computers move data between L1/L2 cache, RAM, SSD and cold archive by latency and immediacy. Cognitive engineering categorizes state into three context tiers:

```text
┌─────────────────────────────────────────────────────────────┐
│ HOT CONTEXT (Active Working Memory)                         │
│ • Immediate mission contract and active station role        │
│ • Specific write-mask files currently being edited          │
│ • Current compiler errors, active stack trace, last command │
│ • Lives directly inside the active model context window     │
├─────────────────────────────────────────────────────────────┤
│ WARM CONTEXT (Local Rehydratable Storage)                   │
│ • Sibling source files within the subsystem                 │
│ • Architectural standard schemas and anchor definitions     │
│ • Recent verified handoff receipts from prior stations      │
│ • Lives on local disk; rehydrated into HOT on demand, or    │
│   summarized into the prompt as a compact index             │
├─────────────────────────────────────────────────────────────┤
│ COLD CONTEXT (Historical & Forensic Archive)                │
│ • Past chat transcripts and discarded exploratory trails    │
│ • Historical git commit logs from prior milestones          │
│ • Comprehensive raw benchmark runs and qualification data   │
│ • Lives in disk archives; retrieved only during deep audits │
└─────────────────────────────────────────────────────────────┘
```

**Epistemic Notice:** These tiers are **context-management architectural patterns**. They are not claims about human neuroscience, nor are they claims about the internal weight matrices of proprietary neural networks. They describe how an engineering harness stages data between local disk files and model API prompts. This chapter is the definition of the tiers. Chapter 12 §5's operational views and Chapter 18 §8's token budget are projections of it: they decide which WARM material is exposed to a station and how much of it may appear in the prompt as an index.

The core discipline of context metabolism is keeping **COLD context out of HOT memory**.

If an agent needs to know why an architecture decision was made two months ago, it does not keep that two-month-old transcript in its prompt. It reads a WARM summary anchor pointing to the engineering decision record (`DECISION_ROOT`). It pulls the insight into HOT context, makes the current decision, and leaves the cold history in the archive.

```text
LAW: COLD_STATE_MUST_NOT_POLLUTE_HOT_CONTEXT
```
### ORION ENGINEERING EXAMPLE
In Orion's memory design (`docs/P-GLL/Prompting_Strategy_Part2.txt` §8), the tiers are applied by operator practice today; an automated Prompt Compiler that enforces them is a target architecture (Chapter 18 §2):
- **HOT:** The active task prompt may be a longer prompt that includes the current mission, active invariants and immediate test commands among other context (for example, `docs/P-GLL/Prompt_Example.txt`).
- **WARM:** The P-GLL anchor standard (`02_PGLL_ANCHOR_AND_REFERENCE_STANDARD.md`) and the relevant source views live on disk in `docs/P-GLL/` and `core/`. They are inspected only when an anchor reference requires verification.
- **COLD:** The raw historical seed transcript (`docs/P-GLL/seed.txt`, roughly one megabyte) and the extraction reports under `docs/P-GLL/_source_evidence/` stay in cold storage and are never injected into live coding prompts.

By keeping `seed.txt` in COLD storage, Orion avoids repeatedly rehydrating a large body of historical text and prevents models from re-litigating design decisions settled months prior.

### FAILURE MODE / ANTI-PATTERN
**The Cold Memory Ingestion Trap:** a RAG system searches the whole codebase by semantic similarity. Asked *"How should I initialize the trace store?"*, it retrieves a six-month-old brainstorming transcript about a deprecated prototype. The model ingests that COLD transcript into HOT context, treats it as current policy, and re-implements an abandoned pattern.

### OPERATOR RULE / TAKEAWAY
> **Never allow semantic search or unvetted scripts to inject raw historical transcripts directly into an active prompt. Gate context rehydration through structured WARM anchors and verified living source files.**

---

## 4. The Discipline of Context Science: Avoiding False Absolutes

In earlier eras of prompt engineering, people loved inventing pseudo-scientific "laws" about model context. You have likely heard claims such as:
- *"Models always lose recall after exactly 32,000 tokens."*
- *"Hallucination probability climbs exponentially with context length."*
- *"Placing instructions at the bottom of the prompt is 40% more effective than at the top across all models."*

As systems engineers, we must reject these ungrounded quantitative flourishes.

**Context degradation is real, but it is empirical and model-dependent, not a universal mathematical constant.**

Here is what empirical systems engineering actually requires:

1. **Effective recall may degrade before advertised capacity.** A context window states how many tokens an API will accept; it does not establish that interdependent constraints will be applied reliably across that span.
2. **Dilution depends on composition.** Constraints compete with narrative text, obsolete debugging attempts and irrelevant files; the signal-to-noise ratio influences instruction retention.
3. **Models differ.** Recall, retention and reasoning quality vary by model, task, composition and prompt layout.
4. **Measure, don't guess.** An engineering harness should profile recall boundaries with synthetic probes and reproducible fixtures (`docs/P-GLL/Prompting_Strategy_Part2.txt` §12) instead of assuming a universal threshold or hidden mechanism.

```text
ADVERTISED_CONTEXT_CAPACITY != EFFECTIVE_REASONING_HORIZON
```

LAW:
```text
MEASURE_MODEL_BEHAVIOR
DO_NOT_INFER_HIDDEN_MECHANISM
```

The professional engineering response to this reality is not panic or dogmatic rules. It is **conservatism in context sizing**. Keeping your active working set compact (HOT context small, WARM rehydration targeted) reduces your exposure to context degradation for the models you have qualified.

---

## 5. Durable Delta Extraction

Let us examine Phase 6 of the metabolism cycle in detail: **Consolidating the Durable Semantic Delta**.

When an agent completes a mission, it must answer one fundamental question before its session can be closed:
> **What became true, false, refined, connected, contradicted, or newly unresolved that was not already established when this station opened?**

```text
DURABLE_MEMORY := PRIOR_VERIFIED_STATE + VERIFIED_NOVEL_DELTA
```

Not in the equation: conversational banter, compiler errors the model triggered and fixed, dead-end searches. That intermediate exploration was metabolic heat; it was consumed to do the work and is discarded.

Only the **verified semantic delta** survives:
1. **The Code Delta:** The exact file changes, validated by compiler and test exit codes.
2. **The Decision Delta:** Any architectural trade-offs resolved during implementation.
3. **The Unresolved Claims:** Any edge cases or sibling defect risks discovered that were out of scope for the current station.
4. **The Next Action Contract:** The explicit, bounded contract for the next station.

This delta is written to disk in a durable **Receipt** (detailed in Chapter 9).

Once the delta is flushed and verified recoverable on disk, the working context can be destroyed safely. The system breathes out. The air clears. The next station rehydrates a clean, focused working context from durable reality.

---

## Chapter 5 in Brief

Inhale what the step needs, work, exhale verified deltas to disk, release. Working context is not memory. Use the HOT/WARM/COLD tiers, measure effective recall instead of assuming it, and carry forward only the verified delta.

Law: `LAW-CNT-04` ([Appendix A](#appendix-a-reference-orion-prompting-laws)).


---


# Chapter 6: Memory Navigation vs. Memory Content

> "The model need not hold everything in working context. It must know how to navigate to what it needs, when it needs it."

---

## 1. The Myth of the Omniscient Prompt

A widespread misconception holds that an agent is only as intelligent as the volume of information loaded into its context window: *"If the model doesn't have the entire schema, all fifty utility functions and three weeks of meeting notes in message one, it will make a mistake!"* That confuses **having the information** with **knowing how to find the information**. No senior architect has memorized the Linux kernel or every field of every table. What makes them effective is **navigational mastery**: the system's core mental model, how the codebase is structured, where authoritative documentation lives, how to query for a missing signature, and what to do when recall is uncertain. Asked about the fifth parameter of an obscure socket call, they do not invent one; they open the man page.

We apply the same discipline to LLMs: **preserve navigation even when content is evicted.** Working context need not hold all knowledge. It needs a lightweight **Continuity Kernel** that enables deterministic navigation and on-demand rehydration.

---

## 2. Having Information vs. Knowing How to Find It

### HUMAN EXPLANATION
Every agent workflow must decide whether to spend tokens loading raw data upfront or providing structured pointers so the model retrieves data only if needed. Most files in a repository are not touched by a given task, and most architectural invariants concern unrelated subsystems; loading them all taxes every turn, dilutes attention and raises hallucination risk. Orion gives models **navigational anchors** instead: a **Continuity Kernel** (a compact summary of what the system is, where its boundaries lie and how its vocabulary resolves), **anchor indexes** (pointers such as `@REF: ORION.RUNTIME.SHUTDOWN`), and **targeted retrieval tools** (read a specific file, check a type signature, run a targeted grep).

```text
CONTINUITY_KERNEL_CONTENTS:
  - system_identity_and_mission
  - normalized_lexicon_and_symbol_resolution
  - global_anchor_namespace_index
  - uncertainty_handling_rules
  - living_source_root_pointers

LAW: PRESERVE_NAVIGATION_EVEN_WHEN_CONTENT_IS_EVICTED
```

### ORION ENGINEERING EXAMPLE
In Orion's P-GLL Master Index (`docs/P-GLL/00_PGLL_MASTER_INDEX.md`), a large corpus of standards is indexed into a compact navigation kernel. Instead of injecting dozens of markdown standards into every prompt, a station prompt includes only the Master Index catalog and the global anchor registry.

If a coding station is tasked with modifying a runtime service, the prompt can contain (illustrative):
```text
ACTIVE_OWNER: OrionCompositionRoot
RELEVANT_ANCHORS:
  - @REF: PGLL.STD.OWNER_BOUNDARY (docs/P-GLL/04_PGLL_OWNER_BOUNDARY_AND_STATE_STANDARD.md)
  - @REF: ORION.LIFECYCLE.PHASES (docs/P-GLL/experimental/LIVE_ALPHA_M5_R2_CANONICAL_LIFECYCLE_DESIGN.md)
```

The model starts compact. If it meets a phase-transition question, it reads the exact file named by `@REF: ORION.LIFECYCLE.PHASES`, resolves the question and continues.

### FAILURE MODE / ANTI-PATTERN
**The Amnesiac Navigator:** an engineer strips all background context to save tokens but provides no pointers: *"Fix the bug in the authentication flow."* The model does not know which files own authentication or which tests exercise it, runs random greps across the disk, hallucinates paths and exhausts its tool budget before finding `auth.ts`.

### OPERATOR RULE / TAKEAWAY
> **Never send an agent into a repository blind. If you evict detailed content from a prompt, you must replace it with a structured map that tells the agent exactly where to find that content when uncertainty arises.**

---

## 3. The Rehydration Ladder

### HUMAN EXPLANATION
When an agent needs deeper information to resolve an ambiguity, it does not search the whole repository. It descends **the Rehydration Ladder**, a deterministic progression from maximum semantic compression to raw evidence:

```text
┌─────────────────────────────────────────────────────────────┐
│ 1. SEED / CONTINUITY KERNEL                                 │  HIGHEST COMPRESSION
│    Minimal core identity, system rules, and anchor index.   │  (Fewest Tokens)
├─────────────────────────────────────────────────────────────┤
│ 2. COMPACT P-GLL ANCHOR                                     │
│    Structured semantic pointer (e.g., @REF: ORION.AUTH).    │
├─────────────────────────────────────────────────────────────┤
│ 3. STRUCTURED SEMANTIC STATE                                │
│    Typed P-GLL interface contract and invariant block.      │
├─────────────────────────────────────────────────────────────┤
│ 4. FULL DEFINITION / SPECIFICATION                          │
│    The complete architectural markdown standard document.   │
├─────────────────────────────────────────────────────────────┤
│ 5. LIVING SOURCE GRAPH                                      │
│    Actual source code files, interfaces, and unit tests.    │
├─────────────────────────────────────────────────────────────┤
│ 6. ORIGINAL MECHANICAL EVIDENCE                             │  LOWEST COMPRESSION
│    Raw command execution logs, terminal output, git diffs.  │  (Most Tokens)
└─────────────────────────────────────────────────────────────┘
```

The golden rule of the ladder is:
**Traverse only as far down the ladder as necessary to resolve the immediate uncertainty.**

1. If the **Compact P-GLL Anchor** (Tier 2) provides enough boundary information to write the code safely, the model stops there.
2. If the interface is ambiguous, the model steps down to the **Structured Semantic State** (Tier 3) or reads the **Full Specification** (Tier 4).
3. If the specification contradicts behavior, the model inspects the **Living Source Graph** (Tier 5) and executes an adversarial test to generate **Original Mechanical Evidence** (Tier 6).

Once the uncertainty is resolved, the model summarizes the finding, extracts the verified delta, and returns to the top of the ladder.

### ORION ENGINEERING EXAMPLE
Navigation by ladder, illustrated (the anchor identifier is illustrative):
- A model implementing turn retirement in `MindRuntime` meets an anchor to the phase-transition rules.
- Instead of guessing which phase follows `INGRESS`, it descends to Tier 4 and reads the phase table in the M5 R2 design (`docs/P-GLL/experimental/LIVE_ALPHA_M5_R2_CANONICAL_LIFECYCLE_DESIGN.md`). There it finds that the effectful path has 12 canonical phases, and that `COGNITIVE_COMMIT` follows `PLAN_CHALLENGE` and precedes `AUTHORITY_DECISION`. It does not follow `INGRESS` directly.
- The uncertainty is resolved by reading one specific document, not by recalling it. The model writes the transition guard and runs the tests, without reading the design's historical rationale.

### FAILURE MODE / ANTI-PATTERN
**The Deep Dive Rabbit Hole:** an agent needs an environment variable's name. Instead of checking `.env.example` (Tier 5), it searches three years of git history and five ancient design debates (Tier 4), gets confused by obsolete Docker discussions, and rewrites the configuration loader.

### OPERATOR RULE / TAKEAWAY
> **Instruct your agents to climb down the rehydration ladder one step at a time. The moment an ambiguity is resolved by a verified fact, stop reading and start executing.**

---

## 4. The Five Epistemic Uncertainty States

### HUMAN EXPLANATION
When an LLM hits a gap in its memory, its reflex is to **fabricate a plausible continuation**: unsure whether a function is `deleteRecord()` or `removeRecord()`, it picks whichever sounds more fluent and keeps writing. In high-assurance engineering that reflex is fatal. The rule: **if you do not know, do not reconstruct from style or vibes.**

Every piece of information in an agent's reasoning must be explicitly classified into one of **Five Epistemic Uncertainty States**:

```text
┌─────────────────────────────────────────────────────────────┐
│ 1. KNOWN                                                    │
│    Verified by living source, active contract, or receipt.  │
│    ACTION: Proceed with implementation.                     │
├─────────────────────────────────────────────────────────────┤
│ 2. REHYDRATABLE                                             │
│    Not in active context, but anchor and path are known.    │
│    ACTION: Inspect the specific anchor file; load data.     │
├─────────────────────────────────────────────────────────────┤
│ 3. UNCERTAIN                                                │
│    Partial or ambiguous information; multiple hypotheses.   │
│    ACTION: Run a mechanical test or compiler check.         │
├─────────────────────────────────────────────────────────────┤
│ 4. MISSING                                                  │
│    Required information is completely absent from context.   │
│    ACTION: Execute targeted discovery or request input.     │
├─────────────────────────────────────────────────────────────┤
│ 5. CONTRADICTED                                             │
│    Two authoritative sources make irreconcilable claims.    │
│    ACTION: Apply claim-sensitive precedence; investigate.   │
└─────────────────────────────────────────────────────────────┘
```

Forcing an agent to categorize its memory with these buckets makes unsupported guessing explicit, easier to detect and harder to rationalize:

```text
UNCERTAINTY_CLASSIFICATION REDUCES SILENT GUESSING
UNCERTAINTY_CLASSIFICATION DOES_NOT_ELIMINATE_MODEL_FAILURE
```

If a state is `UNCERTAIN` or `MISSING`, guessing from style is forbidden: the model marks the item `MISSING`, descends the ladder to read the source, marks it `KNOWN`, and only then writes the calling code.

### ORION ENGINEERING EXAMPLE
**ILLUSTRATIVE_EXAMPLE (verdict block).** An auditor whose static view cannot settle behavior can record:
```text
VERDICT: NOT_DETERMINABLE
EPISTEMIC_STATE: UNCERTAIN
REQUIRED_DISCOVERY: "Inspect runtime storage driver mount options and kernel fsync behavior"
```

In the M5 R2 V1.5 certification (the sourced account is in Chapter 3 §4), the certifying station found that the restart workflow had no branch for a failure of `truncate()` itself or of its flush. It did not invent a plausible recovery branch. It recorded the gap as `NOTE-R2-TRUNCATE-FLUSH-FAILURE`, a low-severity, non-blocking design note, so the unspecified branch stayed explicit instead of being fabricated.

### FAILURE MODE / ANTI-PATTERN
**Plausible Style Reconstruction:** asked to implement a client for an internal API, a model that does not know the method names but recognizes the camelCase REST conventions invents `fetchUserProfileById()` and `deleteUserAccount()`. The code looks gorgeous, compiles (the interfaces were stubbed), and returns HTTP 404 everywhere because the real API uses `getUser()` and `deactivateUser()`.

### OPERATOR RULE / TAKEAWAY
> **Tattoo this rule into your system prompts: an explicit `NOT_DETERMINABLE` verdict is more valuable than a plausible guess. Penalize guessing; reward explicit rehydration.**

---

## 5. Truncation as Cache Management

Truncation is usually seen as an existential disaster (*"the memory is lost forever!"*). A better analogy is **working-set eviction in a finite cache**.

> [!NOTE]
> **Analogy Notice (Not Implementation Equivalence):** A context window is not a literal CPU cache, and truncation is not silicon-level LRU eviction. But treating truncation like cache eviction is a disciplined pattern: it can be managed, and it is safe only if the required state is externally recoverable.

```text
[ARCHITECTURAL ANALOGY]
CPU CACHE EVICTION  ≈  CONTEXT TRUNCATION
SYSTEM RAM          ≈  DURABLE REPOSITORY ON DISK
MEMORY CONTROLLER   ≈  CONTINUITY KERNEL & ANCHOR INDEX
```

In a well-designed harness the master state lives durably in git commits, living source and verified receipts, and the continuity kernel keeps the paths and anchors needed to rehydrate any evicted concept. Truncation is harmless **only** when all essential state has been flushed and verified recoverable. Treating context as a managed cache turns long-horizon engineering from a race against the context limit into the discipline of keeping recovery state current.

---

## Chapter 6 in Brief

Knowing how to find information beats memorizing it. Keep a Continuity Kernel and anchor index, descend the rehydration ladder one step at a time, classify every item into one of five epistemic states, and manage truncation like a cache backed by durable state.

Law: `LAW-CNT-02` ([Appendix A](#appendix-a-reference-orion-prompting-laws)).


---


# Chapter 7: The Multi-Model Assembly Line

> "A station constrains authority, responsibility, write rights, and promotion limits. It does not constrain intelligence. Bound the blast radius; do not lobotomize the observer."

---

## 1. The Monolithic Trap

In the early days, engineers treated an LLM as an omniscient oracle: one chat session, the whole codebase pasted in, and the instruction *"Analyze this system, design a new architecture, write all the code, debug the tests, audit yourself for vulnerabilities, and certify that this is production-ready."* This fails for predictable reasons. A single context window cannot hold raw source exploration, design trade-offs, line-level edits, adversarial scans and governance validation without skimming details and dropping constraints. The entity that designed an algorithm is a poor reviewer of it: it rationalizes its own shortcuts and congratulates itself. And a single thread that outputs fifty files leaves the operator unable to tell which decisions were grounded in source, which were educated assumptions, and which were drift. Orion instead builds software with an **assembly line of specialized stations**.

---

## 2. Station Role vs. Model Identity

The distinction that governs multi-model systems:

```text
STATION_ROLE != MODEL_IDENTITY
```

### HUMAN EXPLANATION
A factory station defines the purpose of the work, the jig, the safety interlocks, the permitted tools and the sign-off criteria; the operator at the bench may be swapped at 2:00 PM without changing any of them. In Orion a **Station Role** is a contractual seat: a bounded mission, a write mask, an input contract, evidence requirements and a status ceiling. A **Model Identity** is the specific model, size, provider and snapshot currently in the seat. You can run the whole line on one model family or assign different models per station by capability, latency, context and cost, but a model never alters the contract of the seat it occupies: `MODEL_IDENTITY` inherits `STATION_ROLE` authority limits and can never expand them.

### ORION ENGINEERING EXAMPLE
An `ILLUSTRATIVE_EXAMPLE` (the paths are invented):
- `STATION_ROLE`: `FALSIFIER`. The contract grants read access to `core/storage/` and write access exclusively to `tests/falsification/`. The role forbids fixing bugs, modifying production source, or issuing a certification verdict. Its output is a falsification receipt documenting reproducible failure cases.
- `MODEL_IDENTITY`: An open-weight reasoning model or a commercial frontier model.

Even if the model occupying the `FALSIFIER` seat realizes that a bug could be fixed by changing one line in `core/storage/store.ts`, its write mask prevents the edit. It must document the defect and hand off to the `BOUNDED_REPAIR` seat.

### FAILURE MODE: THE ROLE-IDENTITY COLLAPSE
*"You are an expert security auditor. Find vulnerabilities and immediately fix them in production."* The model finds a suspected race, edits three core files, introduces a deadlock and reports *"Fixed and secure!"* Auditor and implementer were merged, so the model graded its own exam.

### OPERATOR RULE
> **Separate the seat from the occupant. Define contracts by write masks, evidence standards and authority ceilings, swap models freely, and never let a model's self-assessed capability alter the boundaries of its seat.**

---

## 3. The High-Assurance Pipeline

To achieve long-horizon cognitive reliability without human micromanagement, Orion describes a reusable seven-station assembly line for high-assurance changes:

```
[ MAPPER ]
    │ (Repository topology, boundary maps, dependency graphs)
    ▼
[ ARCHITECT / DENOISER ]
    │ (Denoised problem specification, invariants, P-GLL contract)
    ▼
[ IMPLEMENTER ]
    │ (Bounded code changes, unit tests, reality discovery delta)
    ▼
[ FALSIFIER ]
    │ (Adversarial stress-testing, boundary edge cases, regression search)
    ▼
[ BOUNDED REPAIR ]
    │ (Targeted defect repair within strict delta budget)
    ▼
[ CLEAN RECONSTRUCTION ]
    │ (Minimal attributed candidate, frozen subject identity)
    ▼
[ CERTIFIER ]
    │ (Independent verification against the contract; scoped verdict)
    ▼
[ GOVERNED ADOPTION DECISION ]
```

Every station states its ceiling on three separate axes: `station_completion` (did the station finish: `COMPLETE`, `PARTIAL`, `BLOCKED`), `verdict` (what the station found, within its own competence) and `promotion_state` (what may happen next). The single authoritative table is in [Appendix C §1](#appendix-c-reference-station-templates). This chapter names ceilings only by pointing to it, so the vocabulary cannot drift.

> [!NOTE]
> **Scoping Notice:** This seven-station pipeline is a **reusable high-assurance pattern**. It is designed for architectural migrations, core runtime changes, security-critical modifications, and promotion boundaries. It is not mandatory ceremony for fixing a typo in documentation or updating a CSS class.
>
> Rigor calibrates to risk. As a conceptual guideline, not a hard-coded formula: `ASSURANCE_DEPTH := f(blast_radius, irreversibility, authority, safety_impact, baseline_significance)`.

---

### The Seven Stations
Status ceilings for every seat are in the table at [Appendix C §1](#appendix-c-reference-station-templates); they are not restated here.

1. **Mapper (the cartographer of living reality).** Inspects the living repository, traces active call graphs and hidden coupling, and builds a map of the terrain. Reads within its authorized scope and writes only mapping artifacts. It *records* contradictions it finds; discovering them is its job. Most failed refactorings start from false assumptions about how the codebase is organized.
2. **Architect / Denoiser (the contract compiler).** Turns the Mapper's findings and the user's requirements into non-negotiable invariants and a bounded implementation contract: exact target paths, negative space, test commands, acceptance criteria, stop conditions. Writes only planning artifacts and P-GLL packets, never production source. Whether a human review gate sits before implementation is a project policy parameter, not a property of the seat.
3. **Implementer (the builder in the box).** Executes the contract inside the designated write mask and runs local tests. It may not modify specifications, non-goals or test evaluation criteria. **It may never issue a certification verdict or self-certify.**
4. **Falsifier (the adversarial red team).** Tries to break the Implementer's solution with edge cases, concurrency stress and invalid inputs. `PRODUCTION_MUTATION_AUTHORIZED = false`, `AUDIT_FIXTURE_WRITE_AUTHORIZED = true`: it writes only adversarial fixtures, never production source. A developer model instinctively tests the happy path it just wrote; the Falsifier's contract is solely to find where the implementation breaks.
5. **Bounded Repair (the surgical fixer).** Repairs the reproducible failures in the Falsifier's receipt, writing only the files that receipt identifies. If the defect's rightful owner lies outside the mask, it halts and requests authority rather than expanding scope silently (Chapter 8 §4). It may never issue a certification verdict.
6. **Clean Reconstruction (the packager).** Takes a dirty, verified proposal and assembles the minimal attributed candidate (baseline plus declared delta, manifest and verification root) so the thing certified is the thing proposed (Chapter 17 §3). It packages; it does not repair.
7. **Certifier (the independent inspector).** Independently inspects the candidate, logs and receipts against the original contract: every required command run, digests matching, masks respected, no station exceeding its authority. It writes only the assessment receipt and may not write code or patch tests. **It may emit a scoped certification verdict. It may not mint adoption authority.**

```text
CERTIFICATION != ADOPTION
READY_FOR_GOVERNED_ADOPTION_DECISION != ADOPTED
```

Adoption belongs to valid governance authority: an operator decision, or an explicitly ratified governed policy (for Pass 1C, explicit operator authorization; see Chapter 8 §5 and Chapter 17 §12).

---

## 4. Bound Authority, Do Not Bound Intelligence

Engineers who first meet station segregation often confuse **bounding authority** with **bounding intelligence**, feeding a station three lines of context and ordering it to follow the plan even if the plan is broken. That produces lobotomized models that march off cliffs obeying obsolete orders.

### The Constitutional Axiom
```text
BOUND AUTHORITY. DO NOT BOUND INTELLIGENCE.
```

A station contract constrains authority (what status it may claim), responsibility, write rights, promotion rights and handoff obligations. It does **not** require epistemic blindness, unquestioning obedience to a flawed plan, ignoring contradictory evidence, or pretending uncertainty does not exist.

### Implementation Can Discover Reality
Suppose the Architect specified that `process_record()` accepts a `timeout_ms` parameter, and the Implementer finds that a commit two days ago turned it into an asynchronous handler that takes no timeout. A model with bounded intelligence would hallucinate a wrapper or fail silently. A model with bounded authority and free intelligence reads reality, pauses, records the discrepancy, changes only what is safe within its mask, and puts the reality delta in its receipt.

```text
REALITY_DISCOVERY_RULE:
  IF living_source != architectural_plan:
    ACTION: RECORD_REALITY_DELTA(source_file, expected, actual)
            THEN ADAPT_WITHIN_WRITE_MASK_OR_ESCALATE
    PROHIBITION: NEVER_FORCE_OBSOLETE_SPEC_OVER_LIVING_CODE
                 NEVER_CONCEAL_DISCOVERY_TO_APPEAR_COMPLIANT
```

### Auditors May Understand the Repair, but Must Not Repair During Audit
An auditor needs full intelligence to understand the algorithm and the race, but must not edit code during the audit pass (Chapter 1 §5): the moment it types a fix it becomes an implementer, loses objective distance, and its patch receives no independent audit. Diagnose with full intelligence, report with mechanical precision, and repair only when wearing the repair-station hat.

---

## 5. Process Convergence Without Epistemic Conformity

Chapter 3 introduced the law: models align on the rules of engagement (mission, shared terminology, the claim-sensitive precedence rules of [Chapter 2 §3](#chapter-2-reality-precedence-and-claim-sensitive-truth), invariants, write masks, evidence standards, stop conditions) while staying independent in their hypotheses and verdicts. In the pipeline, this means never coercing a station into conformity: do not tell a Falsifier *"Model A wrote this and believes it is bug-free; please agree"*, do not tell a Mapper *"assume yesterday's design meeting was accurate"*, and do not suppress dissent: if Station 3 suspects a flaw in Station 2's design, the receipt must let it say so. Disagreement between stations is a trigger, not a verdict (Chapter 3 §4); a majority vote among models is not evidence, and resolution comes from mechanical evidence or the rightful decision authority.

---

## 6. Resource-Aware Model Scheduling

Not every station needs a frontier model: running one to execute `git status` is wasteful, while asking a small fast model to falsify a lock-free data structure invites silent bugs. A typical profile is: Mapper (large context, fast retrieval, cheap); Architect (strong synthesis); Implementer (strong code generation and tool use); Falsifier (adversarial reasoning); Bounded Repair (focused synthesis, small delta budget); Clean Reconstruction (mostly deterministic tooling); Certifier (strict rule-following, schema validation).

### The Invariance Law of Resource Scheduling
A model is **qualified** for a seat, not merely capable. Qualification depends on tool support, context capacity, qualification evidence, permissions and provider availability.

```text
RESOURCE_AVAILABILITY CHANGES ROUTING
RESOURCE_AVAILABILITY DOES_NOT_CHANGE_TRUTH
```

Resource constraints may change the model family in a seat, the chunk size of packets, the number of examples, and retry or escalation policy. They must never change the factual standard of truth, the requirement for mechanical evidence, the seat's authority boundaries or the system invariants. A cheap model in the Mapper seat does not get a pass to guess file paths: if it cannot complete the map it emits `NOT_DETERMINABLE` and the work escalates to a more capable engine.

---

## 7. Anti-Pattern: The Sycophantic Consensus Loop

The most seductive failure mode in multi-model engineering is the **Sycophantic Consensus Loop** (`TOPIC-ANTI-06`; mechanics in Chapter 3 §1): Model A authors, Model B is told "review this", polite agreement follows, and the custom mutex deadlocks in production. The remedy is structural, not exhortation:

1. **Blind review.** When appropriate, do not tell the reviewer another model authored the code; present it as living repository state to be evaluated against cold invariants.
2. **Adversarial contracts.** Do not ask the Falsifier to "review"; give it a mission:
   ```text
   STATION: FALSIFIER
   GOAL: Construct a minimal, reproducible test case that forces this component to fail.
   SUCCESS_CRITERION: A test that raises an unhandled exception or data race.
   NEGATIVE_SPACE: You are not here to praise the architecture. If you cannot break it
                   within the bounded test budget, report exactly what was tried.
   ```
3. **Mandatory mechanical evidence.** Opinions do not matter; the execution log does: did the suite run, what was the exit code, where is the trace?

---

## 8. Summary

- **Station Role != Model Identity:** separate the seat from the engine, and qualify the model for the seat.
- **Seven stations, three-axis status ceilings** (Appendix C §1); bound authority, not reasoning.
- **Process convergence without epistemic conformity;** resource constraints change routing, never the standard of truth.
- **Anti-sycophancy by structure:** adversarial contracts and mechanical evidence.

Laws: `LAW-FND-01`, `LAW-FND-04`, `LAW-FND-05`. Reference templates, which require project-specific policy binding, are in [Appendix C](#appendix-c-reference-station-templates).


---


# Chapter 8: Governance, Scope, and Authority Boundaries

> "Specifying what an autonomous model must not touch protects a production codebase far more effectively than describing what it should create. True engineering autonomy is bounded freedom within an iron cage of negative space."

---

## 1. The Blast Radius Problem

When autonomous AI agents cause disasters in production codebases, it is rarely because they lacked the intelligence to solve the requested task. It is almost always because their **blast radius was unconstrained**.

An engineer gives an LLM agent a seemingly innocent task:
*"Upgrade our user authentication service to support OAuth2 tokens."*

Left to its own devices with an open-ended terminal tool, the agent begins well. It installs an OAuth2 client library. Then it realizes the user schema lacks a `token_expiry` column, so it authors a database migration. Then it notices that the test suite is slow, so it refactors the database connection pool. Then it spots an older cryptographic helper that uses deprecated SHA-1 hashing, so it rewrites the company-wide cryptography utility. Then it formats forty-five files across three repositories using a newer linter configuration it preferred.

When the pull request arrives, it touches dozens of directories, dozens of files, and thousands of lines of unrequested collateral edits.

The original intent—supporting OAuth2 tokens—is buried beneath an avalanche of well-intentioned architectural collateral damage. Worse, the PR is unreviewable. Did the cryptographic refactoring break session caching? Did the database connection pool change introduce a connection leak under Kubernetes autoscaling?

In Orion, we reject open-ended, unconstrained agency. We treat autonomous agency as a **governed physical reaction**: high energy, strictly contained within a reactor vessel of negative space, write masks, and authority boundaries.

---

## 2. Negative Space: The Power of Defining What NOT to Do

In traditional software specification, product requirements documents (PRDs) focus almost entirely on positive space: *What features will we build? What API endpoints will we expose? What UI buttons will we display?*

Human engineers can navigate positive-only requirements because they share implicit cultural common sense: a human engineer knows that updating an auth token does not authorize them to rewrite the company's logging engine.

Large Language Models do not possess implicit corporate common sense. They operate by statistical completion across their entire training distribution. If rewriting an adjacent utility feels statistically coherent with "modernizing authentication," the model will do it with enthusiasm.

Therefore, robust multi-model prompting requires **Negative Space Engineering** (`TOPIC-GOV-01`).

```
                POSITIVE SPACE
          ┌─────────────────────────┐
          │ What TO build           │
          │ What TO fix             │
          │ What tests TO run       │
          └─────────────────────────┘
                       │
                       ▼
          ┌─────────────────────────┐
          │ NON-GOALS               │ ◄─── Explicitly out of scope
          │ MUST-NOT-CHANGE         │ ◄─── Immutable file globs & APIs
          │ FORBIDDEN ACTIONS       │ ◄─── Tool calls disallowed
          │ WRITE MASKS             │ ◄─── Hard boundary on file edits
          │ STOP CONDITIONS         │ ◄─── Semantic triggers to halt
          └─────────────────────────┘
                NEGATIVE SPACE
```

### The Three Pillars of Negative Space
Every serious P-GLL packet and station contract must explicitly declare three negative dimensions:

1. **Non-Goals (`TOPIC-GOV-02`):** Explicit declarations of problems that are intentionally *not* being solved during this station's run. Listing non-goals prevents the model from expanding scope when it encounters related historical debt.
2. **Must-Not-Change Surfaces (`TOPIC-GOV-03`):** Concrete files, interfaces, wire formats, database schemas, or API signatures that must remain 100% byte-for-byte or contractually identical.
3. **Forbidden Actions:** Specific tools or behaviors that the model is constitutionally barred from invoking (for example: running git commit, modifying `.github/workflows/`, deleting test fixtures, or downgrading linter strictness).

### HUMAN EXPLANATION
Imagine hiring a specialist contractor to remodel your bathroom.

If you tell them only: *"Make the bathroom luxurious and modern,"* you might return home to find they knocked down the bathroom wall, expanded into your master bedroom, installed a jacuzzi where your closet used to be, and replaced your central air conditioning unit with radiant floor heating. They made it luxurious—and destroyed your house.

A sane homeowner defines negative space:
- *"Do not touch the load-bearing north wall."*
- *"Do not replace the copper plumbing pipes behind the vanity."*
- *"Do not alter the electrical wiring in the hallway."*
- *"Budget is strictly limited to the interior 60 square feet of the guest bathroom."*

Negative space sets the physical boundary. Inside that boundary, the contractor has full autonomy to choose tile grout, vanity height, and mirror placement.

### P-GLL COMPRESSION
```text
# ILLUSTRATIVE_EXAMPLE
NEGATIVE_SPACE_SPECIFICATION:
  scope_target: "core/auth/token_exchange.py"
  positive_space:
    goal: "Implement RFC 8693 OAuth 2.0 Token Exchange grant type"
    deliverables: ["TokenExchangeHandler", "test_token_exchange.py"]
  negative_space:
    non_goals:
      - "Do NOT refactor legacy JWT verification logic in session.py"
      - "Do NOT migrate database schema to support refresh token rotation"
      - "Do NOT modernize crypto utility libraries"
    must_not_change:
      - "core/auth/session.py"
      - "core/crypto/**"
      - "schema/migrations/**"
    forbidden_actions:
      - RUN_GIT_PUSH
      - DELETE_EXISTING_TESTS
      - MODIFY_ENVIRONMENT_SECRETS
  maximum_allowable_status:
    verdicts: [IMPLEMENTATION_SELF_CHECK_PASSED, IMPLEMENTATION_PARTIAL, IMPLEMENTATION_FAILED]
    promotion_states: [READY_FOR_INDEPENDENT_REAUDIT, NOT_READY_FOR_REAUDIT]
```

### ORION ENGINEERING EXAMPLE
An `ILLUSTRATIVE_EXAMPLE` (the paths are invented): an Implementer station is tasked with optimizing state serialization in `core/example/serialization.ts`. The P-GLL packet defines:
```text
MUST_NOT_CHANGE:
  - "core/example/wire-format.ts"  # [External network protocol must remain frozen]
  - "core/example/invariants.ts"   # [System-wide invariants cannot be loosened]
WRITE_MASK:
  allowed: ["core/example/serialization.ts", "tests/unit/serialization.test.ts"]
  forbidden: ["**/*"]
```
When the Implementer runs tests, it finds that serializing timestamps as Unix epochs would be faster than ISO-8601 strings, but doing so would require altering `wire-format.ts`. Because that file is in the `MUST_NOT_CHANGE` mask, the model must stop that path. It records the finding and optimizes the string serialization internally instead.

### FAILURE MODE: THE VAGUE ORCHESTRATION VACUUM (`TOPIC-ANTI-10`)
An orchestration pipeline assigns tasks with vague instructions: *"Agent 1: Explore and fix bugs. Agent 2: Clean up the repository."*
Agent 1 modifies an internal API signature to fix a local edge case. Agent 2 simultaneously deletes "unused" classes that Agent 1 was planning to call. Both models report full local success.
When merged, the entire system crashes. Neither agent violated its instructions, because neither agent had boundaries.

### OPERATOR RULE
> **Always specify the negative space before describing the positive task. A model with an explicit write mask and a clear list of non-goals will tend to produce narrower, more reviewable changes than one without them.**

---

## 3. Aggressive in Depth, Conservative in Breadth

A fundamental principle of Orion engineering scope is:

```text
AGGRESSIVE IN DEPTH, CONSERVATIVE IN BREADTH   (TOPIC-GOV-06)
```

```
                   CONSERVATIVE IN BREADTH
                   (Narrow Blast Radius)
                  ┌───────────────────────┐
                  │ Target: 1 or 2 files  │
                  └───────────┬───────────┘
                              │
                              │
                              ▼
            ┌───────────────────────────────────┐
            │ • Deep AST & type inspection      │
            │ • Thorough edge-case analysis       │  AGGRESSIVE
            │ • Concurrency & race condition test│  IN DEPTH
            │ • Full invariant falsification    │  (Uncompromising
            │ • Precise byte-level diff audits  │   Rigor)
            │ • Complete provenance receipts    │
            └───────────────────────────────────┘
```

### What It Means
- **Conservative in Breadth:** Keep the horizontal blast radius as small as possible. Touch the absolute minimum number of subsystems, files, and architectural layers required to achieve the mission. Do not allow the mission to sprawl across the codebase.
- **Aggressive in Depth:** Within that narrow horizontal footprint, be thorough. Do not settle for surface-level "it compiles." Write rigorous boundary tests. Probe race conditions. Check null safety. Verify hash integrity. Audit the generated AST. Test the change under adversarial conditions and report what was and was not established.

Most failed AI workflows do the exact inverse: they are **broad and shallow**. They touch thirty files, add superficial comments, fix two typos, leave ten hidden edge cases unhandled, and skip writing any adversarial tests.

Orion mandates that models dig a deep, solid foundation under a single stone rather than scattering dust across the entire building site.

---

## 4. Expected vs. Source-Revealed Repair Surface

When an Architect/Denoiser or human operator plans an engineering change, they formulate an **Expected Repair Surface**:

```text
EXPECTED_REPAIR_SURFACE := the files we think we need to touch
```

However, software is an interconnected physical reality. When the Implementer opens the repository, compiles the code, and runs the test suite, reality pushes back:

```text
ACTUAL_REPAIR_SURFACE := the files the compiler, linker and tests show we must touch   (TOPIC-GOV-07)
```

### How Scope Legally Expands
Can an Implementer expand its scope beyond the original packet?

**Yes—but ONLY when forced by mechanical evidence (`TOPIC-GOV-05`), never by stylistic preference.**

```
SCENARIO A: STYLISTIC SCOPE EXPANSION (FORBIDDEN)
Implementer: "While editing parser.py, I noticed logger.py uses camelCase.
              I will expand scope to rename logger methods to snake_case."
VERDICT: CONSTITUTIONAL VIOLATION. REVERTED IMMEDIATELY.

SCENARIO B: EVIDENCE-DRIVEN SCOPE EXPANSION (PERMITTED WITH AUDIT)
Implementer: "I added the mandatory parameter 'tenant_id' to StorageEngine.read().
              Running 'pytest tests/' reveals that tests/integration/test_tenant.py
              instantiates StorageEngine directly and fails with TypeError.
              Expanding repair surface to include tests/integration/test_tenant.py."
VERDICT: LEGITIMATE MECHANICAL DEPENDENCY. EXPANSION DOCUMENTED IN RECEIPT.
```

### The Invariant of Scope Expansion
When mechanical evidence forces the actual repair surface to expand beyond the expected repair surface:

```text
SCOPE MAY EXPAND DUE TO EVIDENCE
EVIDENCE STANDARDS MAY NOT SHRINK MERELY BECAUSE SCOPE EXPANDED
```

If an unexpected compilation error forces you to touch an additional integration test, you do not get to lower your testing standards to save time. The newly touched file falls under the exact same depth, verification, and falsification rules as the primary target.

If the necessary expansion violates a `MUST_NOT_CHANGE` boundary, the model is **strictly forbidden from expanding scope unilaterally**. It must halt, preserve its work, and request expanded authority from the decision authority (for Pass 1C, the operator).

---

## 5. Authority Boundaries & Status Ceilings

A model station does not possess inherent authority. It possesses only the authority explicitly granted to it by its current P-GLL contract.

To prevent models from minting their own authority, Orion gives every seat a **status ceiling** (`TOPIC-GOV-08`) on three separate axes: `station_completion`, `verdict` and `promotion_state`. The single authoritative table is [Appendix C §1](#appendix-c-reference-station-templates). In outline:

```
SEAT                         MAY CLAIM                            CANNOT CLAIM
────────────────────────────────────────────────────────────────────────────────
Mapper, Architect,           its own verdicts and promotion       certification,
Implementer, Falsifier,      states (Appendix C §1)               adoption
Bounded Repair,
Clean Reconstruction
Certifier                    a scoped certification verdict       adoption
────────────────────────────────────────────────────────────────────────────────
GOVERNANCE AUTHORITY         adoption (an operator decision or an explicitly
                             ratified governed policy)
```

### No Later-Stage Authority Minted by Earlier Stages (`TOPIC-STAT-13`)
A critical constitutional law of the Orion assembly line is:

```text
NO STATION MAY MINT AUTHORITY FOR A SUBSEQUENT STATION
```

- Station 2 (Architect) cannot write in its handoff packet: *"Station 3 is hereby authorized to merge its code directly to main."*
- Station 3 (Implementer) cannot write in its receipt: *"I have self-certified this code; Station 4 may skip adversarial testing."*
- Station 7 (Certifier) cannot write: *"This candidate is hereby adopted as the baseline."*

Each station's contract explicitly specifies its **maximum allowable status** (`maximum_allowable_status`). Any attempt by a model to claim a status beyond its contractual ceiling is a structural defect that invalidates the receipt.

Only valid governance authority can grant adoption, merge to protected branches, or declare a milestone accepted (`TOPIC-GOV-11`): an operator decision or an explicitly ratified governed policy. For Pass 1C specifically, explicit operator authorization is required (Chapter 17 §12).

### Handoff Routing vs. Authority Transitions
In an automated pipeline, a handoff packet may recommend the next station through its `next_station_rule`. How does an orchestrator handle this?

```text
HANDOFF_ROUTING CAN BE DETERMINISTIC
AUTHORITY_TRANSITION MUST BE GOVERNED
```

An automated harness or orchestrator may use the `next_station_rule` field to route work deterministically when:
- System policy explicitly permits automated routing for that stage.
- The designated target station exists and its input prerequisites are fully satisfied.
- The transition remains strictly within the current preauthorized boundary (for example, advancing from Implementer to Falsifier within an isolated test sandbox).

However, **routing does not mint authority**. A station handoff recommendation can answer *"What should logically inspect this next?"* It can never answer *"What is now authorized to mutate protected state?"*

```text
GOVERNED != ALWAYS_MANUAL
```

A model cannot mint authority. However, a governed authority transition does not require a manual human click at every boundary; depending on system policy, it may be authorized by:
- Explicit operator approval.
- A valid, pre-granted execution lease.
- An established preauthorization policy.
- A valid, time-bounded authorization capability issued by the governance mechanism (signed grants are a target mechanism, not a current one).

The operator remains the ultimate source of authority, and human review is required whenever policy demands it. The governance model is flexible enough to support automated policy enforcement without bottlenecking routine execution.

---

## 6. Get to the Flag Before Asking the Operator to Jump

While Orion is uncompromising about authority boundaries, it is equally concerned with developer ergonomics:

```text
ORION SHOULD GET TO THE FLAG BEFORE ASKING THE OPERATOR TO JUMP   (TOPIC-GOV-09)
```

### HUMAN EXPLANATION
Imagine you ask an assistant to book an international flight. The needy assistant asks one trivial question every fifteen minutes and has consumed your morning by noon. The executive assistant researches the options, holds the seats without charging your card, and presents a decision package: *"Option A (nonstop, $850) and Option B (one stop, $620) both fit your schedule. Confirm payment for A or B."* The executive assistant did all the reversible, preauthorized work, reached "the flag", and asked the human only for the actual authority transition (spending money).

### The Orion Engineering Standard
When a multi-model workflow executes:
1. **Do not stop every five minutes to ask the user trivial questions** that can be answered by reading the codebase or running a grep search.
2. **Execute all reversible, isolated, preauthorized work autonomously (`TOPIC-GOV-10`):**
   - Perform repository mapping.
   - Run compilation and tests.
   - Inspect ASTs and git history.
   - Author draft code in an isolated workspace or branch.
   - Construct adversarial falsification test suites.
   - Run the full test harness.
   - Compile complete, verifiable receipts with exact command logs and hashes.
3. **Stop exactly at the authority boundary:**
   - Present the receipt, the exact diff, the test evidence, and the remaining open trade-offs to the decision authority (often the operator).
   - Request review and the authority transition.

```text
REVERSIBLE != AUTOMATICALLY_AUTHORIZED
```

A model does not decide for itself which actions are preauthorized. Preauthorization must be genuinely established by contract, policy, or harness permissions. The safe rule is: **Do all reversible work that is already authorized by contract, policy, or harness permissions. Then stop at the actual authority boundary.**

```
AUTONOMOUS PREAUTHORIZED WORK (Isolated & Reversible)
┌────────────────────────────────────────────────────────┐
│ Map ──► Plan ──► Draft Code ──► Run Tests ──► Falsify  │
└────────────────────────────────────────────────────────┘
                            │
                            │ "GET TO THE FLAG"
                            ▼
              ┌───────────────────────────┐
              │  AUTHORITY GATE           │ ◄─── Authority decides
              │  (e.g., operator review)  │
              └─────────────┬─────────────┘
                            │
                            ▼
             IRREVERSIBLE PROTECTED ACTIONS
┌────────────────────────────────────────────────────────┐
│ Merge to Main ──► Deploy Prod ──► Mutate Shared State  │
└────────────────────────────────────────────────────────┘
```

> [!WARNING]
> **Boundary Warning:** "Getting to the flag" is **NOT** permission to bypass the authority boundary. It does not permit pushing directly to production, dropping database tables, or silently modifying system contracts. It means doing all the preparation so that when the decision authority looks at the work, it has the complete mechanical evidence required to make an informed, low-friction decision.

---

## 7. Semantic Stop Conditions

An autonomous model must know when to stop typing (`TOPIC-GOV-04`).

In unconstrained conversational AI, models suffer from "infinite chatter syndrome": they answer the question, then explain why they answered the question, then offer three unsolicited suggestions, then apologize for talking too much, and then ask: *"Is there anything else I can help you with today?"*

In Orion, every station contract terminates with explicit **Semantic Stop Conditions**:

```text
STOP_CONDITIONS:
  halt_immediately_when:
    - TARGET_FILES_WRITTEN_AND_TESTS_PASSING
    - UNRECOVERABLE_COMPILATION_ERROR_OUTSIDE_WRITE_MASK
    - INVARIANT_VIOLATION_DETECTED
    - STATUS_CEILING_REACHED
  terminal_action:
    - EMIT_P_GLL_HANDOFF_RECEIPT
    - HALT
  prohibition:
    - "Do NOT suggest subsequent unprompted refactorings."
    - "Do NOT proceed to Station N+1."
```

When a model encounters a semantic stop condition, it emits its standardized receipt and yields the context. It does not begin the next task. It does not speculate on the future of the product. It stops.

---

## 8. Summary

- **Negative space first:** non-goals, must-not-change masks and forbidden actions before the positive task.
- **Aggressive in depth, conservative in breadth;** scope expands only on mechanical evidence.
- **Status ceilings:** seats claim only their own verdicts and promotion states; only valid governance authority grants adoption; `GOVERNED != ALWAYS_MANUAL`.
- **Get to the flag:** do all reversible, authorized, evidence-generating work, then stop at the authority boundary.
- **Semantic stop conditions:** halt when the contract is satisfied.

Laws: `LAW-GOV-02`, `LAW-GOV-03`, `LAW-GOV-04`, `LAW-GOV-05` ([Appendix A](#appendix-a-reference-orion-prompting-laws)).


---


# Chapter 9: Receipts and Handoffs: Surviving Model Death

> "A model session is ephemeral; it will be destroyed when the token window closes. But an engineering project must endure for months or years. Continuity is the discipline of making progress survive model death without carrying forward its conversational rot."

---

## 1. The Reality of Model Death

Every Large Language Model session is mortal.

Whether due to token context exhaustion, vendor rate limits, process timeouts, network disconnects, or simply the end of a work session, the conversational state of an AI agent will die. When you launch a fresh prompt tomorrow—or when an automated pipeline kicks off the next station in an assembly line—the new model starts with a clean slate of blank memory.

How does an engineering organization bridge this abyss?

The naive response is to preserve the transcript. Engineers copy the 40-page chat log, paste it into the new model's context window, and hope the newcomer can decipher the trajectory.

We already know why this fails:
- Transcripts are saturated with conversational pleasantries, discarded tangents, outdated debugging hypotheses, and token bloat.
- Transcripts obscure what actually happened behind thousands of tokens of how the model felt about what happened.
- Most dangerously, **transcripts encourage the incoming model to adopt unverified conversational claims as established facts**.

In Orion, we survive model death not through chat transcripts, but through **Durable Verified Receipts and Survivable Handoffs**.

---

## 2. Epistemic Law: A Receipt Is Not Proof

Before constructing a single receipt, we must establish the most critical epistemic law in the Orion architecture:

```text
RECEIPT != PROOF
CLAIM + RECONSTRUCTABLE_EVIDENCE + VALID_PROVENANCE + APPROPRIATE_VERIFICATION -> VERIFIED_CLAIM_WITH_DEFINED_SCOPE
VERIFIED_HERE != TRUE_EVERYWHERE
```

In the generative AI landscape, engineers routinely confuse a model writing down a claim with the claim being true. A model runs a task and emits a handsome Markdown table asserting:
```markdown
## Execution Summary (Unverified Model Claims)
- All unit tests passed: YES
- Security vulnerabilities found: 0
- Performance improvement: 35% faster [unverified claim]
- Status: PRODUCTION_READY
```

The operator looks at the Markdown document, sees the word "Receipt," and assumes the code has been proven correct.

**It has not.**

A model-authored Markdown file is just text. A model can hallucinate a passing test suite just as easily as it can hallucinate a poem about a butterfly. Writing down the words "All tests passed" in a receipt establishes only that the model generated those characters.

To engineer high-assurance systems, we must strictly distinguish three distinct layers of reality:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. MODEL-AUTHORED RECEIPT                                              │
│    Records: claims, hypotheses, commands invoked, declared outcomes.   │
│    Epistemic Status: UNVERIFIED CLAIM                                  │
├────────────────────────────────────────────────────────────────────────┤
│ 2. MECHANICAL EVIDENCE                                                 │
│    Establishes: command actually ran, exit code was 0, artifact        │
│    actually exists on disk, SHA-256 hash matches, state changed.       │
│    Epistemic Status: OBSERVABLE PHYSICAL FACT                          │
├────────────────────────────────────────────────────────────────────────┤
│ 3. VERIFIED RECEIPT                                                    │
│    Receipt + Reconstructable Mechanical Evidence + Appropriate         │
│    Provenance + Independent Verification Gate                          │
│    Epistemic Status: VERIFIED ENGINEERING STATE                        │
└────────────────────────────────────────────────────────────────────────┘
```

### The Three Layers Defined
1. **Model-Authored Receipt:** The structured document authored by the station (`TOPIC-RCPT-01`). It records what the model observed, what decisions it made, what baseline it started from, and what claims it makes about its deliverables.
2. **Mechanical Evidence:** The deterministic trail generated by the operating system, compiler, test harness, or version control system. It includes raw terminal stdout/stderr logs, exact tool execution exit codes, timestamped filesystem diffs, and cryptographic file hashes.
3. **Verified Receipt:** A receipt whose recorded claims are backed by reconstructable mechanical evidence, carry complete provenance, and have been verified by an independent auditor or the rightful verification gate.

A receipt does not magically establish truth. **A receipt organizes claims so that an auditor can mechanically verify them.**

---

## 3. Receipt != Transcript: Outcomes Over Cognitive Noise

A receipt is not a transcript (`TOPIC-RCPT-02`).

A mathematician publishes the distilled argument, not the wastebaskets of scratch work. Similarly, an Orion receipt preserves **what mattered**, not the cognitive noise of getting there:

```
WHAT TO PURGE (Transcript Noise)          WHAT TO PRESERVE (Receipt State)
────────────────────────────────────────────────────────────────────────
• Conversational greetings & apologies    • Contract ID & Station Role
• Chain-of-thought scratch reasoning      • Baseline Commit Hash
• Discarded debugging dead-ends           • Exact Shell Commands Executed
• Unprompted model speculations           • Generated Artifact Paths & Hashes
• Raw verbose output from passing linters • Concrete Reality Deltas Discovered
• Sycophantic conversational pleasantries • Unresolved Claims & Blockers
• Tentative intermediate code drafts      • Maximum Allowable Status
```

### Why We Exclude Chain-of-Thought
Modern frontier models often generate extensive internal reasoning or chain-of-thought tokens. Some developers make the mistake of serializing thousands of lines of raw chain-of-thought into handoff receipts.

This is an anti-pattern:
1. **Context Pollution:** The incoming model must read thousands of tokens of internal scratchpad monologue before seeing the code, diluting its attention.
2. **Anchoring on Discarded Biases:** If the previous model toyed with an incorrect hypothesis before abandoning it, serializing that scratchpad causes the next model to re-examine the same dead end.
3. **Epistemic Distraction:** An auditor should audit the **resulting code and test evidence**, not how the model felt while authoring them.

Receipts preserve **decisions, evidence, and deliverables**. Everything else is incinerated.

---

## 4. The Anatomy of an Orion Receipt

A receipt is a durable, structured record of claims, observations, outcomes, provenance and supporting evidence. It is tamper-evident only if a mechanism makes it so (Section 7). The reference field specification and template are in [Appendix D](#appendix-d-receipt-schema). This section shows the shape of the main blocks in an abridged `ILLUSTRATIVE_EXAMPLE` (invented paths and digests):

```text
station_receipt:
  header: { receipt_id, station_role, model_identity, execution_environment, artifact_author, created_at, contract_id }
  baseline:
    baseline_commit: "<commit>"
    expected_repair_surface: ["core/example/router.ts"]
    actual_repair_surface: ["core/example/router.ts", "tests/unit/router.test.ts"]
    scope_expansion_rationale: "Added unit tests to satisfy a declared invariant"
  mechanical_evidence:
    commands_executed:
      - command: "npm test -- tests/unit/router.test.ts"
        exit_code: 0
        stdout_sha256: "sha256:<64-hex-placeholder>"
        evidence_log_path: "logs/test_runs/router-run.log"
    artifacts_created_or_modified:
      - { path: "core/example/router.ts", sha256: "sha256:<64-hex-placeholder>", diff_stat: "+42 -8" }
  discovered_reality_delta:
    - { target: "core/example/router.ts:45", finding: "handler assumed synchronous", impact: "adapter added" }
  unresolved_claims_and_risks:
    - { claim: "concurrency behavior under load", status: UNTESTED, mitigation: "Falsifier seat" }
  terminal_assessment:
    station_completion: COMPLETE
    verdict: IMPLEMENTATION_SELF_CHECK_PASSED
    promotion_state: READY_FOR_INDEPENDENT_REAUDIT
    next_station_rule: FALSIFIER
```

---

## 5. Provenance: The Quad of Independent Identities

A receipt must never blur who did what and where it happened. In Orion, every receipt mandates the **Provenance Quad** (`TOPIC-RCPT-07`, `TOPIC-RCPT-08`, `TOPIC-RCPT-09`):

```
┌─────────────────────────────────────────────────────────────┐
│                      PROVENANCE QUAD                        │
├──────────────────────────┬──────────────────────────────────┤
│ 1. STATION_ROLE          │ The contractual seat             │
│    (e.g., IMPLEMENTER)   │ (governs authority & write mask) │
├──────────────────────────┼──────────────────────────────────┤
│ 2. MODEL_IDENTITY        │ The engine occupying the seat    │
│    (e.g., frontier-model) │ (ephemeral, swappable)          │
├──────────────────────────┼──────────────────────────────────┤
│ 3. EXECUTION_ENVIRONMENT │ Where commands actually ran      │
│    (e.g., linux-x64-ci)  │ (OS, shell, runtime versions)    │
├──────────────────────────┼──────────────────────────────────┤
│ 4. ARTIFACT_AUTHOR       │ Who directed the change          │
│    (e.g., operator-bob)  │ (human operator or agent system) │
└──────────────────────────┴──────────────────────────────────┘
```

### Why These Four Fields Must Be Independent
- **Role $\neq$ Model:** As established in Chapter 7, `STATION_ROLE` is the invariant contract; `MODEL_IDENTITY` is the swappable worker.
- **Model $\neq$ Environment:** A model running locally on an M3 MacBook generates different path separators, environment variables, and shell syntax than the same model running inside an isolated Linux Docker container. Recording `EXECUTION_ENVIRONMENT` ensures mechanical reproducibility.
- **Author $\neq$ Role:** A human operator might manually author a draft station packet while wearing the Architect role. An automated cron agent might trigger the Mapper station. `ARTIFACT_AUTHOR` preserves the chain of custody.

### Law of Provenance Continuity
```text
CONTINUITY MUST SURVIVE MODEL REPLACEMENT WITHOUT PROVENANCE LOSS   (TOPIC-RCPT-10)
```

If Station 1 was executed by Model A, Station 2 by Model B, and Station 3 by Model C, the final audit must be able to trace which model authored which change and which test run produced which hash. When a bug is discovered, we never want to ask: *"Which AI generated this unverified assumption?"* The provenance quad keeps accountability traceable.

---

## 6. The Survivable Handoff Contract

When a station finishes its work, it does not hand over a conversational chat. It emits a **Survivable Handoff Packet** (`TOPIC-RCPT-03`).

### What Makes a Handoff "Survivable"?
A handoff packet is independently survivable if a completely fresh model—instantiated in a new container with zero memory of the prior conversation—can read the packet and immediately know:
1. **Inherited Reality (`TOPIC-RCPT-04`):** The verified baseline commit, the state of the repository when the previous station began, and the established invariants.
2. **Newly Verified Delta (`TOPIC-RCPT-04`):** Exactly what files were modified, what tests were executed, and what physical diff was produced.
3. **Unresolved Claims (`TOPIC-RCPT-05`):** Explicit declarations of what was *not* verified, what risks remain unaddressed, and what edge cases were deferred.
4. **Known Limitations:** Compiler warnings, performance caveats, or environmental assumptions.
5. **Source References:** Precise file paths and line ranges where living code can be inspected.
6. **Maximum Allowable Status (`TOPIC-RCPT-06`):** The constitutional ceiling on what the prior station achieved.
7. **Next Station (`TOPIC-RCPT-05`):** The recommended next station in the assembly line.

```
                   SURVIVABLE HANDOFF PACKET
┌─────────────────────────────────────────────────────────────┐
│ • Inherited Reality Baseline (Git Hash, Invariants)         │
│ • Newly Verified Delta (Diff Stat, Hashes, Test Evidence)   │
│ • Explicit Unresolved Claims (What was NOT tested)          │
│ • Living Source Pointers (File paths, symbol anchors)       │
│ • Maximum Allowable Status Ceiling                          │
│ • Next Station Recommendation                               │
└─────────────────────────────────────────────────────────────┘
                               │
               BRIDGES THE GAP ACROSS MODEL DEATH
                               │
                               ▼
┌─────────────────────────────────────────────────────────────┐
│ FRESH MODEL INSTANCE (Zero Prior Context Memory)            │
│ Reads packet ──► Rehydrates State ──► Resumes Trajectory    │
└─────────────────────────────────────────────────────────────┘
```

### Handoff Routing vs. Execution Authority
A prior station may recommend the next station through its `next_station_rule`, and may even draft the next prompt. Chapter 8 §5 states the rule: `HANDOFF != AUTHORITY`. Routing can be deterministic; authority transitions must be governed, and `GOVERNED != ALWAYS_MANUAL`. A handoff note never expands the next station's write mask or grants it execution authority.

### Receipt Storage vs. Git Metadata
Where do receipts live?

In Orion, we establish a strict separation between the **Durable Receipt Store** and **Version Control Metadata**:

```text
LOGICAL_RECEIPT_LAYER != PHYSICAL_STORAGE_BACKEND
```

- **The Durable Receipt Store:** Owns the structured receipts, raw command logs, cryptographic hashes, and station lineage. Physically, this store may reside in a dedicated repository directory (e.g., `receipts/`), an immutable artifact store, or a content-addressed storage system.
- **Git Commits and Pull Requests:** Are **not** the receipt store. A git commit message or PR description should never be burdened with thousands of lines of raw receipt logs. Instead, commit messages and PR bodies *reference* the receipt:

  **ILLUSTRATIVE_EXAMPLE (not an actual receipt):**
  ```text
  Receipt-ID: RCPT-2026-10-01-SPINE-CONV-04
  Receipt-Root-SHA256: sha256:<64-hex-placeholder>
  Receipt-Link: receipts/2026-10-01-spine-conv-04.receipt.p-gll
  ```

Receipts must be durable, addressable, provenance-bound, and rehydratable across model generations.

---

## 7. Durability, Tamper-Evidence, Immutability and Freshness

Some AI frameworks claim their receipts are "cryptographically immutable." In Orion we keep three properties apart:

- **Durability:** the record survives crashes (sync barriers, committed storage).
- **Tamper-evidence:** alteration is detectable (digests, signatures, hash chains).
- **Immutability:** alteration is prevented by enforced storage (write-once media, enforced append-only stores, permissions).

> [!IMPORTANT]
> **Storage Realism:** Unless receipts are stored on write-once media or an enforced append-only ledger, a file on an ordinary disk filesystem is **not** physically immutable. It can be edited, deleted or overwritten. Describe receipts as **durable**, **versioned**, **hash-bound** and, where a mechanism supports it, **tamper-evident**. Content addressing alone gives tamper-evidence, not immutability. Receipt hash-chaining is `SPECIFIED_NOT_IMPLEMENTED` today (Appendix D §4).

### Stale != False
Consider a receipt generated on Monday asserting that `router.test.ts` passed all 12 tests against commit `a1b2c3d`. On Tuesday another engineer refactors the router in a later commit. On Wednesday an auditor reads Monday's receipt. Is it **false**?

Not by virtue of the later change. If it was properly verified, it remains a correct record of what was observed against that baseline. What it has become is **STALE**: its current applicability is void until re-verified.

```text
STALE != FALSE
HISTORICAL_VALIDITY != CURRENT_APPLICABILITY
IF the claim's dependency boundary has changed since the receipt baseline
  => CURRENT_APPLICABILITY := REVERIFICATION_REQUIRED
```

Before inheriting a historical receipt as evidence about current reality, run a **Freshness Check**:
1. Compare the receipt's baseline digests for the claim's dependency boundary against the current state.
2. If they match, the evidence is applicable to the current state.
3. If they diverge, current applicability is void and re-verification is required before the claim is promoted.

HEAD equality is neither necessary (unrelated commits do not stale a claim) nor sufficient (a dirty worktree can differ while HEAD matches); compare the dependency boundary, not the commit pointer (Chapter 16 §9).

---

## 8. High-Assurance Scoping: Calibrating Rigor to Risk

Throughout Chapters 7, 8 and 9 we have detailed a rigorous methodology: seven-station assembly lines, adversarial falsification, hash tracking, tamper-evident receipts and verification gates.

It is vital to close this foundation section with a practical engineering warning:

> [!CAUTION]
> **Ceremony Inflation:** Do not inflict the full high-assurance certification ceremony on every trivial edit in a codebase.

If an engineer needs to fix a misspelled word in a README file or adjust a margin in a CSS stylesheet, requiring a Mapper, an Architect, an Implementer, a Falsifier, a Bounded Repair station, and a formal cryptographically hashed receipt is absurd theater. It slows development to a crawl and breeds contempt for governance processes.

### The Assurance Calibration Matrix
Orion scales verification rigor directly with **risk, blast radius, and irreversibility**:

```
CHANGE PROFILE          EXAMPLE                      WORKFLOW CEREMONY
────────────────────────────────────────────────────────────────────────────
Low Risk                Doc fixes, CSS tweaks,       Single prompt, local
(Reversible, Isolated)  internal dev script edits    unit test, simple diff review.

Medium Risk             New feature in bounded       Two-station (Implementer ──►
(Bounded feature,       service, non-critical API    Reviewer), standard test
existing test harness)  addition                     suite execution receipt.

High Risk               Core runtime spine refactor, Full seven-station assembly
(Architectural change,  cryptographic update, wire   line, adversarial falsification,
cross-cutting, promo)   protocol migration, books    tamper-evident receipts, clean
                                                     reconstruction, operator gate.
```

Save the heavy machinery for the structures that hold up the roof. When you do need high assurance, the receipt-and-handoff protocol ensures that your system can maintain continuity across dozens of model generations without relying on fragile conversational memory.

---

## 9. Summary

Receipts and handoffs let work survive model death: record outcomes, not thoughts; keep the provenance quad; route deterministically but authorize by governance; keep tamper-evidence, immutability and durability apart; and treat a stale receipt as not-applicable, not false.

Laws: `LAW-EVD-04`, `LAW-EVD-05`, `LAW-GOV-05`. The formal receipt specification is [Appendix D: Receipt Schema](#appendix-d-receipt-schema).


---


# Chapter 10: Deterministic Intelligence: Stop Reasoning About Things You Already Know

> **"Intelligence should only be invoked where uncertainty exists. If a deterministic procedure already knows the answer, spending reasoning tokens to re-derive it is not engineering—it is cognitive waste."**  
> — *Orion Engineering Maxim*

---

## 1. The Trap of the Ubiquitous LLM

In the early exploration of modern generative AI, a pervasive design anti-pattern infected software engineering: the belief that because Large Language Models *can* reason about nearly anything, they *should* be asked to execute everything.

Engineers built agent loops where a reasoning model was placed in the middle of standard procedural code. The model was asked to iterate through lists, check whether an HTTP response was a 200 or a 503, decide how many milliseconds to wait before retrying, parse file paths, and sequentially call tools one item at a time.

Consider what occurs in such a system:

```text
[COGNITIVE BABYSITTING ANTI-PATTERN]

   Model: "Please read item 1 from the work queue."
   Tool:  "Item 1: user_id=101, status=pending."
   Model: "Please execute update on user_id=101."
   Tool:  "Update successful."
   Model: "Please read item 2 from the work queue."
   Tool:  "Item 2: user_id=102, status=pending."
   Model: "Please execute update on user_id=102."
   Tool:  "Update successful."
   Model: "Please read item 3 from the work queue..."
```

Notice what has occurred here. A complex neural network trained on broad cross-domain corpora is acting as a slow, expensive, nondeterministic `for` loop.

Every single hop across this loop incurs:
- **Severe Latency:** Unnecessary round-trip serialization and token generation delay.
- **Economic Waste:** Spending high-tier reasoning tokens to perform an iteration that procedural code executes in sub-millisecond time.
- **Attention Degradation:** Flooding the model's active context window with repetitive operational transcripts, pushing valuable high-level instructions out of effective attention range.
- **Compounding Failure Surface:** Every turn introduces a non-zero probability that the model will get distracted, lose count, re-interpret its instructions, or terminate prematurely.

In Orion, this behavior is recognized as an architectural failure. The fundamental axiom of deterministic intelligence is simple:

```text
UNCERTAINTY_PRESENT?
   NO  ──► Execute via Deterministic Mechanism (Zero Model Token Generation)
   YES ──► Bounded Cognition Justified
```

This is a design preference, not a prohibition. Whether a deterministic mechanism is worth building depends on its build cost, maintenance cost and coverage of the problem; the principle says to prefer the lowest *sufficient* deterministic mechanism, and to escalate when it is not sufficient.

---

## 2. What "Deterministic" Really Means

Before exploring the architecture, we must establish strict semantic discipline. In casual technical discussions, "deterministic" is frequently misapplied as a synonym for *simple*, *safe*, *correct*, or *infallible*. 

It is none of those things.

A deterministic system can be intricate. It can be unsafe. It can be completely wrong, and it can execute that wrongness with mechanical consistency.

```text
DETERMINISTIC
  := Under a defined initial state and defined inputs, the system produces 
     reproducible, governed state transitions according to fixed mechanical rules.

DETERMINISTIC != CORRECT
CORRECTNESS    := Requires a valid contract + thorough testing + runtime verification.
```

If a deterministic script contains an off-by-one bug, it will reliably and deterministically corrupt an array every time it runs under those inputs. Determinism does not guarantee truth or safety; it guarantees **reproducibility and predictability**. 

Why is this property so valuable in an AI architecture? Because when an error occurs in a deterministic mechanism, it is a **mechanical defect**. You can inspect the call stack, set a breakpoint, trace exact variables, write a regression test, fix the logic, and verify that the defect class is closed within the tested semantic neighborhood and current baseline. 

When an error occurs in an unconstrained reasoning model, you are dealing with a **stochastic failure mode**. While prompt adjustments, structured decoding, temperature tuning, model selection, and guardrails help shape the probability distribution, you cannot patch a neural weight distribution with a compiler check. 

Therefore, our goal in multi-model engineering is to push as much of the system's operational surface into deterministic machinery as possible, reserving stochastic intelligence strictly for problems characterized by genuine semantic ambiguity.

---

## 3. The Execution Ladder

How do we decide which mechanism should handle a given operational problem? Orion models this through the **Execution Ladder**.

It is important to understand that this ladder is not a rigid, universal implementation hierarchy that every software module must strictly construct. Rather, it is a practical **escalation model** for engineering design. When designing a capability, start at the lowest possible rung. Escalate to higher rungs only when the uncertainty of the environment or the problem domain demands it.

```text
           ▲   [HIGH UNCERTAINTY / OPEN SEMANTICS]
           │
           ├─► RUNG 6: REASONING AGENT (Frontier Model)
           │     Open semantic synthesis, ambiguous tradeoff arbitration, policy resolution
           │
           ├─► RUNG 5: MODEL-ASSISTED SELECTOR (Small / Bounded Classifier)
           │     Classifying intent into a closed taxonomy, selecting a known tool from a menu
           │
           ├─► RUNG 4: DETERMINISTIC PLANNER
           │     Rule-based or graph-based dependency resolution (DAG generation, topological sort)
           │
           ├─► RUNG 3: BEHAVIOR TREE
           │     Hierarchical reactive control (selectors, sequences, conditions, fallbacks)
           │
           ├─► RUNG 2: FINITE STATE MACHINE (FSM)
           │     Strict monotonic state transitions, validated predecessor gates, fail-closed guards
           │
           ├─► RUNG 1: STATIC ROUTINE
           │     Linear or looping procedural code with fixed error-handling policies
           │
           └─► RUNG 0: STATIC SCRIPT
                 Pure deterministic transformations, schema validation, hashing, parsing
           │
           ▼   [ZERO UNCERTAINTY / MECHANICAL EXECUTION]
```

### Rung 0: Static Scripts
*Mechanisms:* Pure functions, parsers, cryptographic hashers, regex engines, formatters.  
*When to use:* Any transformation where input A must always yield output B. Computing a SHA-256 digest, validating a JSON payload against a schema, or extracting file paths from a Git status string requires zero cognition.

### Rung 1: Static Routines
*Mechanisms:* Fixed procedural algorithms, HTTP client wrappers with exponential backoff, retry loops, database queries.  
*When to use:* Known operational sequences. Retrying an HTTP request on a 503 response with jittered backoff is a solved procedural problem. The model should not decide how many milliseconds to wait between network attempts.

### Rung 2: Finite State Machines (FSMs)
*Mechanisms:* Explicit transition tables, validated phase gates, monotonic progress counters.  
*When to use:* Systems with discrete, well-defined lifecycles where invalid state transitions must fail closed. In Orion, the turn lifecycle is governed by a state machine (Section 6). The Pass 1C candidate, which was uncommitted and uncertified at audit time, applies the same idea to process startup: a transition from `CONSTRUCTED` directly to `SERVING` without passing through `WRITER_AUTHORIZED` and `CORE_PERSISTENCE_READY` would halt the process.

### Rung 3: Behavior Trees
*Mechanisms:* Hierarchical trees of control nodes (Sequences, Selectors, Decorators) that evaluate blackboard state to execute reactive tasks.  
*When to use:* Dynamic operational workflows that require flexible execution paths without open-ended reasoning. If a file download fails due to disk space, a behavior tree can deterministically evaluate an alternative clean-up sequence before retrying, without invoking an LLM.

### Rung 4: Deterministic Planners
*Mechanisms:* Graph traversal, dependency solvers, topological sorting algorithms.  
*When to use:* When a task has multiple interdependent subtasks with known prerequisites. If you need to compile multiple packages in a monorepo, a deterministic planner builds the DAG and resolves the build order mathematically.

### Rung 5: Model-Assisted Selectors
*Mechanisms:* Small, fine-tuned, or quantized bounded models operating over constrained, typed classification grammars.  
*When to use:* Narrow semantic interpretation where the set of possible outcomes is closed. For example, classifying an incoming operator sentence into one of a dozen predeclared intent types, or matching an ambiguous natural language query to an installed capability seed.

### Rung 6: Reasoning Agents
*Mechanisms:* Frontier multi-modal reasoning models operating with broad context windows and structured tool surfaces.  
*When to use:* True semantic uncertainty. Designing an architectural refactoring, diagnosing a complex cross-subsystem race condition, synthesizing qualitative requirements from disparate human transcripts, or deciding how to reconcile conflicting system policies.

---

## 4. The Economic Law of Cognition

Frontier reasoning models are computationally intensive resources. Every generated token consumes electricity, high-bandwidth memory, specialized inference scheduling, and measurable latency.

To treat reasoning tokens as an unlimited commodity is poor software engineering. The economic principle of deterministic intelligence is governed by a strict rule:

```text
DO NOT SPEND REASONING TOKENS DECIDING:
- How to retry a known transient network timeout
- Which file to process next in an explicit directory manifest
- Whether an idempotency key has already been executed
- How to checkpoint an intermediate state to disk
- How to serialize a phase record into an append-only journal
- Which phase transition is legally permitted after INGRESS
```

When an engineer asks an LLM to manage these operations, they not only burn resources—they actively destabilize the system. An LLM instructed to "retry up to three times with exponential backoff" might retry twice and give up, retry four times, or unpredictably alter the payload on the third attempt. A deterministic retry routine executes the configured policy with mechanical precision every time.

> [!IMPORTANT]
> **What "Uncertainty" Means in Orion:**  
> When we state that intelligence should only be invoked where uncertainty exists, "uncertainty" refers strictly to **unresolved semantic or decision uncertainty relevant to the task**.  
> It does *not* mean that every environmental variance requires an LLM. A network socket closing unexpectedly is environmental variance, but its handling should be deterministic (reconnect or abort per policy). True semantic uncertainty occurs when the system cannot determine the *meaning* of an input, the *intent* of an operator, or the *optimal tradeoff* between competing architectural goals.

---

## 5. The Maturity Direction: Models Discover Roads; Orion Paves Them

In long-horizon engineering, the relationship between frontier models and deterministic code is dynamic. We do not view deterministic systems and AI models as competing paradigms. Instead, they form a continuous evolutionary lifecycle:

```text
                  ┌───────────────────────────────┐
                  │   FRONTIER MODEL DISCOVERY    │
                  │   Explores open solution space│
                  │   Identifies valid sequences  │
                  └──────────────┬────────────────┘
                                 │
                                 ▼
                  ┌───────────────────────────────┐
                  │   REPETITION & CONVERGENCE    │
                  │   Route repeats across tasks  │
                  │   Pattern becomes predictable │
                  └──────────────┬────────────────┘
                                 │
                                 ▼
                  ┌───────────────────────────────┐
                  │       PROCEDURALIZATION       │
                  │   Extract state machine/script│
                  │   Encode preconditions/tests  │
                  └──────────────┬────────────────┘
                                 │
                                 ▼
                  ┌───────────────────────────────┐
                  │         VERBIFICATION         │
                  │   Package as typed public Verb│
                  │   Deterministic execution     │
                  └──────────────┬────────────────┘
                                 │
                                 ▼
                  ┌───────────────────────────────┐
                  │      COGNITIVE EXCLUSION      │
                  │   LLM leaves the normal path  │
                  │   Returns only on escalation  │
                  └───────────────────────────────┘
```

We summarize this evolutionary trajectory in a core Orion maxim:

> **Models discover roads; Orion paves them.**

### How the Cycle Works in Practice

1. **Discovery:** When facing a novel problem—such as diagnosing an unfamiliar operating system error or integrating a newly released third-party API—a frontier reasoning model is valuable. The model explores the ambiguous environment, experiments with various CLI commands or API calls, inspects error payloads, synthesizes documentation, and discovers a working sequence of actions.
2. **Proceduralization:** Once that sequence has been executed successfully and its failure modes are understood, human engineers or harness builders extract the sequence. We do not leave the model in charge of executing that sequence on future routine runs. We write a static script, a state machine, or a deterministic routine that encodes the exact sequence, parameters, regex checks, and retry policies.
3. **Verbification:** (Note: *Verbification* is an established Orion engineering shorthand describing the packaging of procedural routines into high-level, typed semantic capability boundaries, detailed thoroughly in Chapter 11.) The routine is wrapped in a governed interface with explicit preconditions, postconditions, and structured receipts.
4. **Cognitive Exclusion:** Once a road is paved, the frontier model is evicted from the normal execution path. Future requests for that capability call the deterministic mechanism directly. 

The directional metric of architectural maturity in Orion is expressed simply:

```text
MATURITY_DIRECTION:
SAME_OR_BETTER_VERIFIED_OUTCOME
WITH
LESS_UNNECESSARY_UNCERTAIN_COGNITION
```

A mature system achieves the **same verified outcome with less uncertain cognition**.

---

## 6. What Orion Does Today vs. What We Are Designing

To maintain strict epistemic hygiene, we must distinguish between what Orion's codebase executes today, what has been experimentally demonstrated, and what is currently target architecture.

### Current Orion Production Reality
In Orion's active production and core runtime (`core/planning/planner-service.ts`):
- Orion implements an explicit split between **Deterministic Planning** and **Model Planning** modes.
- In `PlannerService.createPlan()`, callers select `mode: "deterministic" | "model"`.
- When called in `mode: "deterministic"` (which is the default in cascade runners), the planner executes completely through deterministic TypeScript methods. It matches installed capabilities via `dynamicTools.findMatchingDynamicTool(goal)` and `seedCatalog.suggestSeedForGoal(goal)`.
- If a dynamic tool matches, it produces a plan using `executor_kind: "deterministic_tool"`. If no dynamic tool matches, it constructs a bounded evidence-grounded recommendation plan (`executor_kind: "worker_chat"`).
- **Critical Runtime Verification:** In `PlannerService.ts`, there is **no automatic fallback** from a failed deterministic match to `createModelPlan()`. Mode selection is explicit. If `mode: "deterministic"` is passed, it executes `createDeterministicPlan()`; if `mode: "model"` is passed, it executes `createModelPlan()`. Higher-level orchestrators (`core/orchestration/cascade-service.ts`) explicitly configure `mode: "deterministic"`.
- Thus, while reasoning agents exist in the codebase as planners and chat workers, automatic runtime escalation from deterministic planning to model planning is an **architectural pattern**, not an automatic internal fallback inside `PlannerService`.

```typescript
// CURRENT ORION IMPLEMENTATION: core/planning/planner-service.ts
async createPlan(request: CreatePlanRequest): Promise<CreatePlanResult> {
  const mode = request.mode ?? "deterministic";
  
  // Deterministic catalog and tool matching
  const capabilityGap = this.analyzeCapabilityGap(request.goal);
  
  try {
    // Explicit mode dispatch — NO automatic fallback inside this method
    const plan = mode === "model"
      ? await this.createModelPlan(request)
      : this.createDeterministicPlan(request);

    return { ok: true, plan };
  } catch (error: any) {
    return { ok: false, error: error.message };
  }
}
```

### Experimental Runtime Reality
In the Turn Lifecycle architecture (`LIVE_ALPHA_M5_R2_CANONICAL_LIFECYCLE_DESIGN.md`; its W3 implementation was re-verified by a separate station, Chapter 3 §4; live-process evidence comes from the H0 proof harness `scripts/h0-live-os-process-proof.ts`):
- State progression through turn execution is governed by a **12-phase monotonic state machine** on the effectful path (legal shortened chains have 9 or 10 phases), enforced by `MindRuntime` and `CognitiveTurnJournal`.
- The transitions (for example `PLAN_CHALLENGE` to `COGNITIVE_COMMIT` to `AUTHORITY_DECISION`) are enforced deterministically. A model cannot "decide" to skip phase validation.
- The lifecycle protocol requires a filesystem flush barrier before any state transition is acknowledged as durably committed.
- The H0 script is a destructive pre-launch proof harness: it truncates the live `data/` journal, receipt and trace ledgers in its working directory before each run. It is evidence for H0, not a production routine.

### Target Architecture (Design in Progress)
In our experimental specifications (`ORION_EXPERIMENTAL_DETERMINISTIC_ENGINEERING_AND_SMALL_MODEL_CODING_SPEC.md`):
- We are designing automated **AST Transformation Verbs** and **Syntax-Guided Synthesis** engines. Under this target design, when a model needs to modify code, it will not write freeform string diffs. Instead, it will emit typed AST manipulation instructions (e.g., `AddExport`, `WrapFunction`) that a deterministic compiler validates against the syntax tree, rejecting syntactically invalid transformations before adoption.

---

## 7. Agency Taxonomy: Many Actions Do Not Equal Agency

A common source of confusion in modern software design is conflating the volume of work an automated system performs with its degree of "agency."

We frequently encounter claims that a system is an "autonomous cognitive agent" because it ran for an extended period and executed thousands of operations. When inspected under the hood, however, one finds that nearly all of those operations were static file reads, network calls, and database updates executing along a fixed procedural graph.

Orion enforces a clean semantic taxonomy:

```text
MANY_ACTIONS   != AGENCY
LONG_RUNNING   != COGNITIVE
AUTOMATION     != AGENT
```

```
┌────────────────────────────────────────────────────────────────────────┐
│                        ORION TAXONOMY SPECTRUM                         │
├───────────────────────────────────┬────────────────────────────────────┤
│ AUTOMATION / ENGINE               │ COGNITIVE SEAT / AGENT             │
├───────────────────────────────────┼────────────────────────────────────┤
│ • Executes deterministic loops    │ • Resolves semantic ambiguity      │
│ • Evaluates boolean conditions    │ • Arbitrates policy tradeoffs      │
│ • Enforces state machine rules    │ • Formulates novel hypotheses      │
│ • Retries network calls on policy │ • Synthesizes qualitative feedback │
│ • Can perform millions of actions │ • Operates temporarily where       │
│   without a single cognitive      │   uncertainty exists, then yields  │
│   decision                        │   control back to the harness      │
└───────────────────────────────────┴────────────────────────────────────┘
```

An engine that crawls a repository, compiles ASTs, and indexes symbol references is a **high-throughput deterministic engine**. Calling it an "agent" obscures its architecture and leads engineers to apply prompting techniques where standard systems programming is required.

In Orion, we reserve words like **Cognitive Seat** or **Agent** strictly for subsystems that must make bounded, policy-governed semantic judgments under uncertainty. And even then, the agent's job is to resolve that uncertainty, record its decisions in a durable receipt, and hand execution authority back to the deterministic harness.

---

## 8. Anti-Pattern: LLM Babysitting Deterministic Loops

Teams moving from chatbot wrappers to agent frameworks often reproduce the babysitting pattern from Section 1. Consider a hypothetical task: find every file that references a deprecated API (`legacyAuth`) and swap the import for `modernAuth`. In the naive version, the model gets `list_files` and `edit_file` tools and works one file per turn, spending a turn each on listing, grepping and editing:

```text
Turn 1: list_files("src/")   Turn 2: grep_file("src/a.ts", ...) no match   Turn 3: grep_file("src/b.ts", ...) match
Turn 4: edit_file("src/b.ts", ...)   ...  (dozens more turns)
```

The context saturates with file lists and status outputs, the model can lose its place or declare completion early, cost and latency balloon for a task with no semantic ambiguity, and no build check is guaranteed after an edit.

#### The Orion Deterministic Architecture
In Orion's design, this task is structured through the Execution Ladder (illustrative; `AST_REFACTOR_ROUTINE` is not an existing routine):

```text
[COGNITIVE SEAT (Reasoning Model)]
   │
   ▼ Synthesizes Migration Intent
Intent: "Migrate deprecated imports from 'legacyAuth' to 'modernAuth' across 'src/'"
   │
   ▼ Compiles into a Parameterized Managed Routine
Routine: AST_REFACTOR_ROUTINE {
   target_dir: "src/",
   pattern: "import { legacyAuth } from '@orion/auth'",
   replacement: "import { modernAuth } from '@orion/auth'",
   post_condition: "npm run typecheck"
}
   │
   ▼ Hands off to Deterministic Harness (Zero Model Token Generation)
   ├─ 1. ripgrep identifies exact matching files.
   ├─ 2. ast-grep performs structural replacements.
   ├─ 3. git status captures modified file set.
   ├─ 4. tsc validates TypeScript compilation.
   ├─ 5. Harness emits structured execution receipt.
   │
   ▼ Returns Single Evidence Summary to Cognitive Seat
Outcome: "SUCCESS: Matching files modified, 0 type errors. Receipt: rcpt_ast_982."
```

Notice the contrast: one model invocation to state the intent plus a review of the final receipt; no mechanical iteration logs in the context window; the iteration runs in compiled binaries; and the typecheck runs deterministically before the change is accepted.

---

## 9. Summary

Prefer the lowest sufficient deterministic mechanism (`LAW-DET-01`, a design principle, not a prohibition). `DETERMINISTIC != CORRECT` (`LAW-DET-03`). Models discover roads and Orion paves them (`LAW-DET-02`). A system performing thousands of actions along a fixed track is an engine, not an agent (`LAW-DET-04`), and no LLM should babysit a mechanical loop.

Next, Chapter 11 shows how deterministic routines are packaged behind **Managed Verbs**.


---


# Chapter 11: Managed Verbs: The Semantic Boundary Between Thought and Work

> **"A Verb is not a single procedural function call. A Verb is a semantic capability boundary. The cognitive seat declares the intent once; the managed runtime expands, executes, verifies, and receipts the entire operational cycle."**  
> — *Orion Verb Language Specification*

---

## 1. The Semantic Boundary: What Is a Verb?

In conventional software engineering, when a programmer hears the word "function" or "method," they picture a specific subroutine in memory: an entry point that takes arguments, executes a block of instructions on a thread, and returns a value.

When engineers first began wiring LLMs to tools, they inherited this low-level mental model. They exposed internal library methods directly to the model as individual JSON-RPC functions or tool definitions. If an application had a subsystem for managing files, the model was handed:
- `filesystem.open`
- `filesystem.read_chunk`
- `filesystem.seek`
- `filesystem.write_chunk`
- `filesystem.close`
- `filesystem.stat`

As we saw in Chapter 10, exposing raw operational primitives directly to a reasoning model is a recipe for context saturation and cognitive drift. A model tasked with "saving a report" should not be forced to manually manage file descriptors, buffer allocations, and write offsets.

In Orion, we resolve this through the architectural concept of the **Verb**.

A Verb is not a primitive procedural action. A Verb is a **public semantic capability boundary**.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        THE CORE VERB RELATION                          │
├────────────────────────────────────────────────────────────────────────┤
│                                                                        │
│   VERB_ATOMICITY  IS_SEMANTIC,  NOT_PROCEDURAL                         │
│                                                                        │
│   From the Cognitive Caller's Perspective:                             │
│       ONE COGNITIVE INTENT  ──►  ONE VERB CALL                         │
│                                                                        │
│   Inside the Governed Runtime:                                         │
│       ONE VERB CALL         ──►  N CONTROLLED PROCEDURAL OPERATIONS    │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

When a cognitive seat (an agent station or model) invokes a Verb, it is declaring **what** semantic outcome it desires within the governed world. The underlying runtime owns **how** that outcome is mechanically achieved, verified, and recorded.

---

## 2. The Execution Taxonomy: From Primitive to Model

To prevent conceptual confusion, Orion defines a strict execution taxonomy. We do not use the words *routine*, *tool*, *verb*, and *agent* interchangeably. Each term occupies an unambiguous position in the system:

```text
PRIMITIVE
  │  The smallest deterministic operation. Atomic at the machine level.
  │  Examples: Read a single file block, execute a regex match, compute a SHA-256 hash.
  ▼
ROUTINE
  │  An ordered sequence of known primitives executed under fixed procedural logic.
  │  Examples: HTTP request with exponential backoff, atomic file write with temporary rename.
  ▼
BEHAVIOR
  │  A stateful deterministic controller that dynamically reacts to environmental signals.
  │  Examples: Finite state machine, behavior tree evaluating job queue leases.
  ▼
VERB
  │  A public semantic capability boundary exposed to cognitive callers.
  │  Encapsulates primitives, routines, behaviors, planners, queues, checkpoints, retries, 
  │  validation, and receipts behind a typed contract.
  │  Examples: current/ad-hoc semantic service boundaries (e.g. system access/probers); target Verbs: `reality.verify`, `image.generate_batch`, `code.refactor_symbol`.
  ▼
QUEST
  │  A top-level goal accompanied by explicit success criteria, constraints, and write masks.
  │  Composed of one or more Verbs, decision points, and evidence gates.
  ▼
COGNITIVE SEAT / AGENT
  │  A temporary role or station granted bounded reasoning freedom to resolve 
  │  unresolved semantic uncertainty within a Quest.
  ▼
MODEL
     An inference resource (frontier model, small specialized model, local embedding model)
     utilized by a Cognitive Seat to perform bounded cognitive transformations.
```

Notice the critical distinction: **Verb describes the interface exposed to cognition, not the internal complexity of the implementation.** 

A Verb might be internally simple (such as a system health probe that executes a single socket check), or it might encapsulate an extensive distributed workflow (such as dataset ingestion and indexing, which spins up worker processes, partitions data, checks hashes, and generates hierarchical digest trees). To the cognitive model, both present the identical structural contract: **a typed intent, governed boundaries, and an evidence-bearing outcome receipt.**

---

## 3. The Anatomy of a Managed Verb

Within Orion's target architecture, we introduce a powerful specialization of this concept: the **Managed Verb**.

A Managed Verb is a Verb that encapsulates an entire multi-stage operational lifecycle. The calling model does not hover over execution, checking intermediate status flags or issuing micro-commands. The Managed Verb owns the cycle from beginning to end:

```text
                  ┌─────────────────────────────────────┐
                  │           COGNITIVE SEAT            │
                  │   Declares high-level intent        │
                  │   Passes typed input spec           │
                  └──────────────────┬──────────────────┘
                                     │
                                     │ (Single Verb Call)
                                     ▼
                  ┌─────────────────────────────────────┐
                  │       MANAGED VERB RUNTIME          │
                  │                                     │
                  │  1. REQUEST INGRESS                 │
                  │  2. CONTRACT VALIDATION             │
                  │  3. INPUT NORMALIZATION             │
                  │  4. WORK QUEUE SCHEDULING           │
                  │  5. DETERMINISTIC EXECUTION         │
                  │  6. OBSERVATION & TELEMETRY         │
                  │  7. RETRY / CONTINUE / STOP LOGIC   │
                  │  8. ATOMIC CHECKPOINTING            │
                  │  9. TECHNICAL VERIFICATION          │
                  │ 10. RESULT AGGREGATION              │
                  │ 11. EVIDENCE RECEIPT EMISSION       │
                  └──────────────────┬──────────────────┘
                                     │
                                     │ (Single Evidence-Bearing Outcome)
                                     ▼
                  ┌─────────────────────────────────────┐
                  │           COGNITIVE SEAT            │
                  │   Receives: COMPLETE | PARTIAL |    │
                  │             FAILED | ESCALATE       │
                  └─────────────────────────────────────┘
```

### Target Architecture Example: Image Generation Batch

To understand the architectural concept, let us contrast a naive micro-tool approach with the target Managed Verb design.

*(Epistemic Notice: The following scenario is an **Illustrative Target Architecture Example** drawn from Orion's experimental specifications (`ORION_EXPERIMENTAL_VERB_LANGUAGE_AND_SKILL_LOOP_SPEC.md`). Orion's active core runtime implements deterministic planners and primitive tool registries, while the generalized `image.generate_batch` Verb described below represents a target design pattern for high-volume batch capabilities.)*

#### The Micro-Tool Anti-Pattern
In a naive system, an engineer exposes raw diffusion API primitives (`diffusion.load_model`, `diffusion.set_seed`, `diffusion.generate_single_image`, `diffusion.check_status`, `filesystem.save_image`) to an agent. When tasked with a batch of dozens of variations, the model begins an extensive conversational loop: it sets seeds, initiates single generations, polls status and saves files. If an HTTP connection times out mid-batch, the model risks losing track of completed items, hallucinating completion status, or exhausting its context budget on mechanical status strings.

#### The Target Managed Verb Architecture
In the target architecture, an agent would instead be provided with a single semantic Verb: `image.generate_batch`.

The model would formulate its intent once as a typed specification:

```typescript
// TARGET ARCHITECTURE SPECIFICATION (ILLUSTRATIVE)
interface ImageGenerationBatchSpec {
  campaign_id: string;
  base_prompt: string;
  prompt_matrix: readonly {
    variant_id: string;
    style_modifiers: readonly string[];
    aspect_ratio: "1:1" | "16:9" | "9:16";
  }[];
  quality_preset: "draft" | "production";
  budget_cap_cents: number;
  output_directory: string;
}
```

The model issues a single call:

```text
image.generate_batch(spec)
```

From that moment, the model leaves the execution path. The Managed Verb controller takes ownership:
1. **Manifest Validation:** Validates that the output directory exists and is writable within the active write mask, that prompt matrix combinations are structurally sound, and that the budget cap is valid.
2. **Deterministic Queue Scheduling:** Partitions generation requests into worker queues, assigns deterministic seeds derived from a master hash, and orchestrates parallel execution across available workers.
3. **Execution Variance Handling:** If a worker encounters an HTTP 503 from an inference server, the Managed Verb catches the transient error, applies an exponential backoff with jitter, and retries up to the configured limit.
4. **Resumable Checkpointing:** After each successful generation, the controller computes the artifact SHA-256 hash, writes the file to disk, updates a checkpoint journal, and tracks remaining budget. If the host process is killed by an OS signal, upon restart the Managed Verb reads the journal, identifies verified completed items, and resumes at the next pending item.
5. **Receipt Emission:** Once the batch completes, the Verb compiles an evidence-bearing receipt containing the batch ID, execution duration, compute metrics, and a manifest of output paths with their respective content hashes.

Finally, the Managed Verb returns control to the Cognitive Seat:

```json
{
  "status": "COMPLETED",
  "batch_id": "batch_img_7749",
  "total_generated": 50,
  "failed_count": 0,
  "budget_spent_cents": 184,
  "receipt_ref": "rcpt_img_batch_7749_a8f9",
  "artifacts": [
    { "variant_id": "v01", "path": "assets/v01.png", "sha256": "sha256:<64-hex-placeholder>" },
    { "variant_id": "v02", "path": "assets/v02.png", "sha256": "sha256:<64-hex-placeholder>" }
  ]
}
```

The model expends tokens only to define the batch and inspect the final outcome. The hundreds or thousands of procedural operations required to coordinate workers, handle retries, manage memory, and write files execute with **zero model token generation**.

---

## 4. Execution Variance vs. Semantic Variance

The core dividing line between what belongs inside a Managed Verb and what belongs inside a reasoning model is the distinction between **Execution Variance** and **Semantic Variance**.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE VARIANCE ALLOCATION PRINCIPLE                    │
├───────────────────────────────────┬────────────────────────────────────┤
│ VERB HANDLES EXECUTION VARIANCE   │ LLM HANDLES SEMANTIC VARIANCE      │
├───────────────────────────────────┼────────────────────────────────────┤
│ • HTTP 503 / 504 network timeouts │ • Prompt misunderstood by provider │
│ • Provider rate limits (HTTP 429) │ • Output technically valid but     │
│ • Local port or socket contention │   semantically off-target          │
│ • File write checksum mismatches  │ • Unforeseen policy contradictions │
│ • Worker process crash / restart  │ • Novel failure class never seen   │
│ • Idempotency key de-duplication  │   in system history                │
│ • Bounded retry exhaustion        │ • Tradeoffs between cost and       │
│                                   │   qualitative nuances              │
│                                   │ • Ambiguous operator requirements  │
└───────────────────────────────────┴────────────────────────────────────┘
```

### The Boundary of Retry Exhaustion: Mechanical Fact vs. Semantic Policy
A crucial architectural subtlety concerns **Retry Exhaustion**.

It is tempting to assume that when all configured retries fail, "execution variance has ended and semantic uncertainty begins." 

This is inaccurate. **Retry exhaustion is still a mechanical execution fact.** 

In a well-designed system, the contract or system policy often specifies the exact deterministic next step when retries are exhausted:
- `RETRIES_EXHAUSTED ──► FAIL JOB (Fail-closed)`
- `RETRIES_EXHAUSTED ──► RETURN PARTIAL BATCH`
- `RETRIES_EXHAUSTED ──► USE PRE-APPROVED FALLBACK PROVIDER`
- `RETRIES_EXHAUSTED ──► RETURN TYPED EXCEPTION TO CALLER`

None of these outcomes require LLM reasoning if the policy is already established.

```text
RETRY_EXHAUSTION != SEMANTIC_UNCERTAINTY

IF_POLICY_DETERMINES_NEXT_STEP:
    EXECUTE_DETERMINISTICALLY (Fail, Fallback, Partial Return)

ELSE_IF_POLICY_OR_MEANING_IS_UNRESOLVED:
    ESCALATE_TO_COGNITIVE_CALLER

AND_ONLY_IF_AUTHORITY_BOUNDARY_CROSSED:
    APPLY_GOVERNANCE_OR_OPERATOR_GATE
```

Cognitive escalation is justified **only when the policy or semantic meaning of the failure is unresolved**. If the policy states that a 10-item batch must either succeed completely or be rejected, the Verb deterministically fails the job and emits an error receipt. If the policy permits returning a partial batch with an advisory note, it does so deterministically.

Cognition is reintroduced only when an open semantic decision remains: for example, whether to spend additional budget on a more expensive provider, or how to rephrase a prompt that triggered a provider safety filter.

---

## 5. Cognitive Compression: The Sibling of P-GLL

In Chapter 4, we studied P-GLL (Programming-GLL) as Orion's language for **cognitive serialization**—compressing vast architectural knowledge, memory graphs, and project invariants into typed, minimum-sufficient state representations so that fresh models can rehydrate without reading megabytes of conversational transcripts.

The Managed Verb is the execution-lane sibling of P-GLL.

```text
KNOWLEDGE LANE (P-GLL):
   Vast Repository History ──► P-GLL Compilation ──► Compact Cognitive Rehydration

EXECUTION LANE (MANAGED VERB):
   High-Level Model Intent ──► Deterministic Expansion ──► Governed Execution ──► Compact Evidence Receipt
```

Both mechanisms serve the same economic and architectural goal: **Cognitive Compression**.

By compressing execution into an outward-facing intent and compressing results into an evidence receipt, the model's active context window remains focused on high-level mission decisions rather than consumed by operational telemetry.

---

## 6. Resumability and Idempotency: Identity vs. Mechanism

A production AI system operates in an environment where processes can terminate unexpectedly. Operating systems run out of memory, network connections drop, and hosts restart.

In a naive agent architecture, process death often means restarting from zero. An agent re-generates tokens, re-invokes tools, and risks leaving duplicate or orphaned artifacts.

A robust Managed Verb design considers **Resumability and Idempotency**:

```text
PROCESS DEATH  !=  RESTART FROM ZERO
SAME REQUEST   !=  DUPLICATE EFFECTS
```

However, a critical distinction must be maintained:

```text
IDEMPOTENCY_KEY != IDEMPOTENCY

IDEMPOTENCY := IDENTITY + DURABLE_EFFECT_ACCOUNTING + GOVERNED_REPLAY_POLICY
```

Simply passing a string labeled `idempotency_key` does not prevent duplicate effects. An idempotency key is merely an identifier. Actual idempotency requires underlying runtime mechanisms:
- Atomic reservations or database unique constraints.
- Durable lookup stores to detect previously settled requests.
- Transactional compare-and-set semantics on state changes.
- Content-addressed artifact deduplication.

### Resumability Requirements Scale with Risk and Duration
Furthermore, resumability is not an all-or-nothing requirement for every Verb. The necessity of checkpointing and state tracking scales with the nature of the operation:

```text
RESUMABILITY_REQUIREMENTS SCALE WITH:
- Duration (sub-second query vs. multi-hour batch)
- Side Effects (read-only query vs. filesystem mutations)
- Financial Cost (zero-cost local check vs. high-cost external API calls)
- Restart Risk (ephemeral exploratory task vs. mission-critical data migration)
- Irreversibility (easily redone calculation vs. permanent database write)
```

A simple read-only query Verb (`system.status`) requires neither checkpointing nor idempotency keys. A single-step atomic file write may require idempotency protection to prevent corrupting concurrent writes, but requires no multi-stage checkpoint journal. Multi-stage checkpointing is primarily essential for **long-running, expensive, or partially-completable Managed Verbs**.

---

## 7. The Escalation Contract: Routing Failure to the Immediate Caller

When a Managed Verb encounters an unexpected situation that exceeds its deterministic policy, where does it escalate?

Orion enforces a strict routing discipline:

```text
MANAGED_VERB
    │
    ▼ (Emits typed terminal or exception outcome)
IMMEDIATE CALLING STATION / ORCHESTRATOR
    │
    ├─► Evaluates whether outcome is already final
    ├─► Checks if an approved deterministic fallback route exists
    ├─► Determines if bounded cognitive resolution is justified
    └─► Escalates to Operator ONLY if governance policy requires it
```

Do not wire retry exhaustion or tool failures directly to a human operator session.

A Managed Verb returns a **typed outcome** (e.g., `STATUS: RETRIES_EXHAUSTED`, `STATUS: INVALID_INPUT`, `STATUS: RESOURCE_EXHAUSTED`) back to its immediate caller—typically the orchestrator or cognitive station that invoked it. 

The caller evaluates the failure against its own governance policy:
1. **Deterministic Fallback:** Can another pre-authorized route fulfill the goal? If so, the orchestrator invokes it without human intervention.
2. **Cognitive Resolution:** Does the failure involve semantic ambiguity (such as an ambiguous input parameter)? If so, a cognitive station resolves the ambiguity.
3. **Operator Escalation:** Only when an established authority boundary is reached—such as exceeding an authorized budget limit, encountering an irreversible system state, or violating security policy—does the system escalate to the operator.

---

## 8. Tool Surface Compression: Managing Selection Ambiguity

We conclude this chapter with an essential architectural principle: **Tool Surface Compression**.

In the broader AI industry, benchmark leaderboards frequently evaluate models on selecting tools from massive catalogs containing hundreds of functions.

In long-horizon engineering, exposing hundreds of low-level tools directly to a reasoning model introduces significant failure modes:
- **Model Attention Degradation:** Large tool catalogs increase parameter confusion and tool selection ambiguity, particularly for smaller, specialized, or local open-weights models.
- **Context Overhead:** Serializing extensive tool schemas consumes substantial context tokens before the model even processes user instructions.
- **Surface Confusion:** Models are more likely to invent incorrect parameter combinations or call tools in disorganized sequences when presented with flat primitive lists.

Orion's principle of Tool Surface Compression states:

```text
THE MODEL'S TOOL SURFACE SHOULD EXPOSE 
ROLE-RELEVANT SEMANTIC CAPABILITIES,
NOT EVERY INTERNAL PRIMITIVE.
```

Instead of exposing dozens of individual Git, file, and patch primitives:

```text
[UNCOMPRESSED PRIMITIVE SURFACE (ILLUSTRATIVE)]
git.status, git.diff, git.log, git.checkout, git.add, git.commit,
git.branch, git.fetch, git.rebase, fs.readFile, fs.writeFile,
fs.mkdir, fs.stat, patch.apply, patch.revert...
```

The system compresses the surface into a small set of role-relevant semantic Verbs:

```text
[COMPRESSED SEMANTIC SURFACE (ILLUSTRATIVE)]
1. repo.inspect_reality_packet(scope)
2. code.apply_governed_patch(spec)
3. verification.run_test_suite(suite_id)
```

### Clarification: Compression Is Not Security
It is vital to understand that tool surface compression is a **cognitive optimization**, not an authorization mechanism:

```text
TOOL SURFACE COMPRESSION REDUCES:
- Selection ambiguity
- Context schema overhead
- Parameter confusion

SECURITY COMES FROM:
- Explicit dispatch authorization
- Parameter validation
- Write masks
- Governed execution boundaries
```

Hiding a dangerous primitive tool from a model's prompt does not make the runtime secure. A secure Managed Verb architecture must route execution through governed mechanisms that enforce write masks, capabilities, validation, and authority boundaries. (Orion's existing runtime enforces dispatch and write-mask security boundaries where shown in source; the generalized Verb runtime is target architecture designed to inherit these invariants).

---

## 9. Summary

A Verb is a semantic capability boundary: one intent, N controlled operations (`LAW-VRB-01`). Verbs handle execution variance; models handle semantic variance (`LAW-VRB-02`). Retry exhaustion is a mechanical fact, not semantic uncertainty. Verbs return typed outcomes to their immediate caller. Expose intent, not plumbing (`LAW-VRB-03`), and remember that compression is not security.

*(The conceptual schema and failure taxonomy are in [Appendix F: Managed Verb Contract](#appendix-f-managed-verb-contract); the unified Managed Verb runtime is `SPECIFIED_NOT_IMPLEMENTED`.)*


---


# Chapter 12: The Reality Spine: Making a Huge Repository Finite

> **"A large repository should not require every fresh model to rediscover the entire codebase before doing useful work. We do not prompt a model against the raw, unfiltered breadth of Git; we declare a finite boundary of relevant reality, verify its continuity with checksums, and escalate into the broader repository only when evidence demands it."**  
> — *Orion Repository Governance Doctrine*

---

## 1. The Rediscovery Tax: The Curse of Repository Scale

When a human software engineer joins an organization with a substantial codebase, how do they get work done on their first day?

Do they clone the repository and read every single source file from beginning to end? Do they open every directory, inspect every test suite, and trace every RPC call across the architecture?

Of course not. If they attempted to do so, their working memory would quickly saturate, and they would produce zero working code.

Instead, a senior engineer provides them with a **finite mental boundary**:
> *"You are working on the checkout service. Here are the files that define the payment gateway interface. Here is the configuration schema. Here is the test suite that verifies transactions. Everything else in this repository—the data pipelines, the UI components, the deployment manifests, the legacy scrapers—is outside your immediate scope. Focus here."*

In modern AI agent engineering, systems frequently subject reasoning models to the exact disorientation that human engineers avoid.

An engineer gives a model a prompt: *"Fix the bug in the shutdown signal handler."* The model starts with a blank context window. To find where shutdown is handled, it runs broad text searches across the entire repository. It receives hundreds of search results spanning test fixtures, deprecated scripts, documentation files, build output, and experimental prototypes.

The model is disoriented. It reads irrelevant files, consumes substantial context tokens before writing a single line of code, risks confusing legacy shutdown scripts with modern lifecycle managers, modifies the wrong file, and breaks the build.

This is the **Rediscovery Tax**: the waste of tokens, attention, and architectural coherence that occurs when every fresh AI station must independently rediscover repository architecture from scratch.

To solve this, Orion introduces the architectural pattern of the **Reality Spine**.

---

## 2. Discovered Repository vs. Declared Reality

The foundational conceptual breakthrough of the Reality Spine is the distinction between two fundamentally different views of a codebase:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        TWO VIEWS OF THE CODEBASE                       │
├───────────────────────────────────┬────────────────────────────────────┤
│ DISCOVERED_REPOSITORY(mode)       │ DECLARED_REALITY                   │
├───────────────────────────────────┼────────────────────────────────────┤
│ • Everything physically present   │ • The finite, curated subset of    │
│   within the selected Git mode.   │   files, interfaces, and contracts │
│ • Can be noisy, historically      │   that Orion explicitly declares   │
│   layered, and semantically       │   relevant to active system        │
│   ambiguous to search.            │   operation and verification.      │
│ • What an unguided broad grep     │ • Bounded, attributed, and         │
│   encounters.                     │   structured for deterministic     │
│                                   │   compilation.                     │
│                                   │ • What an oriented station sees.   │
└───────────────────────────────────┴────────────────────────────────────┘
```

### The Explicit Git Modes of `DISCOVERED_REPOSITORY`
A repository does not have a single, static physical meaning. Depending on the operational phase, "the repository" refers to distinct modes:

```text
DISCOVERED_REPOSITORY(HEAD):
   All committed files and trees reachable from the selected HEAD commit.
   (Committed source reality for the selected HEAD; 
    SELECTED_HEAD != UNIVERSAL_REALITY).

DISCOVERED_REPOSITORY(WORKTREE):
   HEAD plus active tracked modifications, staged/unstaged edits,
   and untracked working files.
   (Dirty proposal reality).

DISCOVERED_REPOSITORY(CERTIFIED_SNAPSHOT):
   An explicit frozen certification subject whose identity is bound to a
   baseline plus its declared payload/delta, manifest, and verification root.
   It may be materialized as a clean isolated worktree or equivalent frozen subject.
   (Certification subject reality — candidate delta does not require prior commit).
```

By parameterizing `DISCOVERED_REPOSITORY(mode)`, the architecture prevents "repository reality" from shifting meaning between drafting, implementation, and certification.

### The "Inverse .gitignore" Intuition
A helpful mental model for understanding the Reality Spine is to think of it as an **Inverse `.gitignore`**:

```text
.gitignore:
   Declares what NOT to consider.
   "Ignore `node_modules/`, ignore `dist/`, ignore `.env`."
   (Everything else is assumed relevant by default).

REALITY SPINE:
   Declares what CONSTITUTES relevant project reality for an operational scope.
   "These declared files are the active system focus. Everything else is cold storage."
   (Establishes a finite starting boundary for navigation).
```

In a small project with fifteen files, an ordinary ignorelist is sufficient. But in a complex engineering system that contains years of design specifications, experimental prototypes, donor worktrees, legacy harnesses, and active code, relying on `.gitignore` alone leaves a massive surface of ambiguous files.

The Reality Spine turns the repository inside out: it establishes a **finite, declared island of operational focus** within the broader Git tree.

---

## 3. Very Important Epistemic Rule: What Is Reality Spine Today?

In keeping with strict epistemic hygiene, we must pause and establish the exact implementation status of the Reality Spine in Orion today.

> [!WARNING]
> **DOCUMENT TITLE != RUNTIME MATURITY**  
> In the Orion documentation suite, you will find an extensive artifact titled:  
> `docs/P-GLL/experimental/ORION_PRODUCTION_SPINE_CONNECTIVITY_AUDIT_GEMINI.md`  
> Do not let this title mislead you into believing that Orion currently runs an automated, production-compiled "Reality Spine CLI" or database engine.

### The True Epistemic Status
- **What That Audit Actually Is:** The *Production Spine Connectivity Audit* was an independent, mechanical audit conducted by Gemini to trace the live dependency graph of services instantiated in `api/server.ts` versus `core/runtime/orion-fabric.ts`. It examined service connectivity, identified severed authority boundaries, and showed where production was failing closed. It used the word "spine" in the architectural sense of a **backbone of critical runtime services**.
- **What `core/reality/` Actually Contains:** If you inspect Orion's active codebase in `core/reality/`, you will find classes like `CurrentRealityContextBuilder`, `HostRealityAtlas`, `ExecutableProber`, and `PortProber`. These are production and experimental services that probe **system and hardware reality** (checking which local host ports are open, which GPU drivers are installed, which binary executables exist on the OS path). They do *not* compile repository file allowlists.
- **The Repository Reality Spine Status:** The repository-level Reality Spine—the finite row model of files, tests, owners, and hash trees described in this chapter—is currently an **Emerging Architectural Pattern and Working Practice** (`TOPIC-REPO-01: SPECIFIED_NOT_IMPLEMENTED`). In convergence milestones like Pass 1C (`CANONICAL_RUNTIME_CONVERGENCE_PASS_1C_PLAN.md`), human architects and models manually author finite file manifests (e.g., the 19 `MUST_CHANGE` files and 13 `TEST_CHANGE` files). Automated compilation and mechanical verification via CLI verbs (`reality.compile`, `reality.verify`) represent **Target Architecture**.

By understanding this truth, we study the Reality Spine as a **working engineering discipline currently evolving from manual governance into automated tooling**.

---

## 4. The Reality Spine Information Model (Target)

What does a declared Reality Spine look like under the hood? It is not merely a flat list of file paths. A list of paths tells a model where files live, but it tells the model nothing about **authority, status, ownership, or boundaries**.

Orion specifies a rich, relational **Row Model** for entities declared in the Reality Spine:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   REALITY SPINE ROW SCHEMA (TARGET)                    │
├───────────────────────┬────────────────────────────────────────────────┤
│ FIELD                 │ SEMANTIC PURPOSE                               │
├───────────────────────┼────────────────────────────────────────────────┤
│ PATH                  │ Normalized POSIX path relative to repo root    │
│ KIND                  │ SOURCE | CONTRACT | TEST | RECEIPT | DOC | SPEC│
│ SUBSYSTEM             │ Runtime | Cognition | Authority | Persistence  │
│ RIGHTFUL_OWNER        │ The singular class/service owning this state   │
│ ROLE                  │ Core Façade | Storage Adapter | Ingress Route  │
│ STATUS                │ PRODUCTION | EXPERIMENTAL | FROZEN | DEPRECATED│
│ AUTHORITY_CLASS       │ HIGH_ASSURANCE | OPERATOR_ONLY | GOVERNED_EXEC │
│ SOT_LEVEL             │ LIVING_CODE | BINDING_CONTRACT | PROJECTION     │
│ READ_WRITE_CLASS      │ READ_ONLY | APPEND_ONLY | EXCLUSIVE_WRITER     │
│ LIVE_REACHABLE        │ ESTABLISHED | NOT_ESTABLISHED | TEST_ONLY      │
│ ENTRYPOINTS           │ Ingress routes or bootstrap scripts reaching it│
│ IMPORTS               │ Declared dependencies it consumes              │
│ IMPORTED_BY           │ Upstream consumers within the declared spine   │
│ TESTS                 │ Test files providing behavioral evidence       │
│ RECEIPTS              │ References to receipts/evidence of baseline    │
│ DECISIONS             │ Architecture decisions governing its design    │
│ CURRENT_HASH          │ SHA-256 digest of current on-disk content      │
│ VERIFIED_HASH         │ SHA-256 digest recorded at last approved freeze│
│ NOTES                 │ Known defects, invariants, or non-goals        │
└───────────────────────┴────────────────────────────────────────────────┘
```

### Reality Spine Reduces Navigational Uncertainty
When a prompt compiler injects a Reality Spine row into a model's context packet, it substantially **reduces navigational uncertainty**:
- The model sees who is designated as the state owner.
- It sees whether the file is considered `EXPERIMENTAL` or `PRODUCTION`.
- It identifies associated test files and design decisions.
- It understands the intended write boundary.

However, a crucial epistemic law must be maintained:

```text
REALITY_SPINE REDUCES NAVIGATIONAL UNCERTAINTY.
REALITY_SPINE DOES NOT ELIMINATE SEMANTIC OR FRESHNESS UNCERTAINTY.
```

Injecting a Reality Spine row does not magically make a stale declaration true, nor does it replace the need to verify living code. It provides structured orientation, not absolute infallibility.

---

## 5. Operational Context Views

[Chapter 5 §3](#chapter-5-context-metabolism-how-context-breathes) defines the HOT, WARM and COLD tiers. The Reality Spine plays a specific role among them: the declared spine rows are the **WARM index of declared reality** (owners, interfaces, hashes, relational edges). They live on disk and are exposed to a prompt only as a compact index when needed. HOT is the mission view (the files being edited, the write mask, the targeted tests). COLD is the broader repository and its history, reached only by explicit escalation (Section 9). File counts vary by mission scale.

### Subsystem Projections
Depending on the mission of a specific station, specialized slices of the Warm Reality Spine can be compiled:
- **Authority View:** Exposes security boundaries, capability issuers, dispatch authorization services, and writer locks. (Used by Falsifiers and Security Auditors).
- **Persistence View:** Exposes database adapters, journal streams, flush barriers, and filesystem schemas. (Used by Storage and Lifecycle Engineers).
- **Current Wave View:** Exposes files designated as `MUST_CHANGE` and `TEST_CHANGE` for the active development sprint.

---

## 6. Declared Reality != Canonical Reality

A critical governance distinction must be maintained when discussing declared reality:

```text
DECLARED_REALITY  !=  CANONICAL_REALITY
```

A declaration authored by a human engineer or an AI Copilot station is an **assertion**. Its status depends entirely on its governance phase:

```text
PROPOSED_DECLARATION   ──► (Authored by Copilot or Architect)
REVIEWED_DECLARATION   ──► (Audited by Falsifier or Peer Station)
ACCEPTED_DECLARATION   ──► (Ratified by Operator or Governance Policy)
CERTIFIED_DECLARATION  ──► (Verified against exact clean checkout hash)
CANONICAL_DECLARATION  ──► (Merged into repository baseline)
```

A model station proposing a Reality Spine does not make that spine canonical. The declaration becomes canonical only when the applicable governance process formally accepts it.

---

## 7. Protected Coverage: Finite Does Not Mean Undeclared Is Irrelevant

A dangerous misinterpretation of the Reality Spine pattern is to assume that because the spine is finite, anything outside it can be ignored.

If an engineer constructs a Reality Spine for an authentication subsystem, but a live code path imports an undeclared module (`core/security/token-validator.ts`), treating the undeclared module as "irrelevant" creates a critical blind spot.

In Orion, we enforce the **Law of Protected Coverage**:

```text
FINITE  DOES_NOT_MEAN  BLIND
UNDECLARED  !=  IRRELEVANT
```

The system classifies repository space across four explicit quadrants:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                     COVERAGE CLASSIFICATION MATRIX                     │
├──────────────────────────────┬─────────────────────────────────────────┤
│ CONDITION                    │ SYSTEM CLASSIFICATION                   │
├──────────────────────────────┼─────────────────────────────────────────┤
│ DECLARED + EXISTS ON DISK    │ EXPECTED REALITY                        │
│                              │ Normal declared state. Verified by      │
│                              │ hash matching.                          │
├──────────────────────────────┼─────────────────────────────────────────┤
│ DECLARED + MISSING ON DISK   │ MANIFEST DEFECT                         │
│                              │ A file promised by the spine does not   │
│                              │ physically exist. The manifest is stale.│
├──────────────────────────────┼─────────────────────────────────────────┤
│ UNDECLARED + LIVE REACHABLE  │ REALITY_SPINE_GAP                       │
│                              │ A live, reachable code path touches an  │
│                              │ undeclared file. Navigation failure!    │
├──────────────────────────────┼─────────────────────────────────────────┤
│ UNDECLARED + REACHABLE = NO  │ EXPLICIT NEGATIVE SPACE                 │
│                              │ Dormant code, donor files, scratch logs │
│                              │ intentionally excluded from scope.      │
└──────────────────────────────┴─────────────────────────────────────────┘
```

### The `REALITY_SPINE_GAP` Event
If static analysis or test execution reveals that a live component depends on an undeclared file, the system does not silently ignore it. It registers a **`REALITY_SPINE_GAP`**. 

This event indicates that the map does not match the territory. The navigation declaration itself must be updated before work in that subsystem can be certified.

---

## 8. Relational Edges: The Graph Behind the List

A flat manifest of files provides basic boundaries, but high-assurance engineering requires understanding **relationships**. 

When an engineer asks: *"What must I understand before I can safely modify the shutdown logic?"*, an unguided model greps for the word "shutdown." 

A Reality Spine equipped with relational edges provides structural navigation (illustrative edges):

```text
                   ┌───────────────────────────────┐
                   │        TARGET SOURCE:         │
                   │ core/runtime/lifecycle-mgr.ts │
                   └───────────────┬───────────────┘
                                   │
         ┌─────────────────────────┼─────────────────────────┐
         │                         │                         │
         ▼ (Owner Edge)            ▼ (Test Edge)             ▼ (Decision Edge)
┌─────────────────┐       ┌─────────────────┐       ┌─────────────────┐
│  RIGHTFUL OWNER │       │ VERIFYING TESTS │       │ DESIGN DECISION │
│ OrionComposition│       │ tests/lifecycle-│       │ Pass 1C Plan    │
│ Root            │       │ shutdown.test.ts│       │ Section 11      │
│ (Shutdown owner)│       │ (illustrative)  │       │ (Graceful drain)│
└─────────────────┘       └─────────────────┘       └─────────────────┘
```

By following these typed edges:
- `SOURCE ──► OWNER`: Identifies who holds authority over the state.
- `SOURCE ──► TEST`: Identifies which test suite validates behavior.
- `SOURCE ──► DECISION`: Identifies the architectural rationale and constraints.
- `SOURCE ──► RECEIPT`: Identifies historical evidence associated with earlier baselines.

---

## 9. Search Escalation: Evidence-Driven Expansion

Does a Reality Spine prevent an AI station from ever inspecting code outside the declared set?

No. That would make the system brittle. Novel defects and cross-cutting interactions sometimes require looking beyond the active boundary.

However, Orion governs this through **Search Escalation**:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                      SEARCH ESCALATION PROTOCOL                        │
├────────────────────────────────────────────────────────────────────────┤
│                                                                        │
│   STEP 1: Search the current HOT Mission View (Active files)           │
│           ▼ (If unresolved)                                            │
│   STEP 2: Search the WARM Reality Spine (Declared subsystem)           │
│           ▼ (If unresolved)                                            │
│   STEP 3: Traverse Relational Edges (Tests, Owners, Decisions)         │
│           ▼ (If unresolved)                                            │
│   STEP 4: Query Evidence & Receipt Indexes (Prior verification records)│
│           ▼ (If unresolved)                                            │
│   STEP 5: Search the Broader HEAD Tree (Outside declared spine)        │
│           ▼ (If unresolved)                                            │
│   STEP 6: Search Git History / Other Branches (Historical provenance)  │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

### The Law of Search Escalation
```text
SEARCH EXPANDS BECAUSE EVIDENCE DEMANDS IT,
NOT BECAUSE THE MODEL IS DISORIENTED.
```

In a naive agent system, models perform repository-wide searches by reflex because they lack structured orientation. 

In Orion, search begins within the tightest declared boundary. A model expands outward only when concrete evidence (such as a stack trace or an import statement) points outside the declared boundary. And when an external dependency is confirmed, the system logs a `REALITY_SPINE_GAP` to ensure the declaration is repaired.

---

## 10. Architectural Resolution: Reality Spine Storage Model

How should a Reality Spine be stored and materialized?

Orion's target design separates the **source semantic declaration** from the **compiled machine representation**:

```text
SEMANTIC DECLARATION (SOURCE FORM):
   A version-controlled, human-readable manifest (e.g., `reality-spine.yaml`).
   Maintained under version control alongside source code.
   Authored and audited by human engineers and Copilot stations.

COMPILED MACHINE REPRESENTATION:
   Deterministically generated JSON/JSONL indexes, relational edge graphs,
   and root checksum manifests derived directly from the semantic declaration.

TRIGGER:
   CLI commands, CI pipelines, pre-commit hooks, or runtime orchestrators
   may invoke compilation.
   The trigger does NOT own truth; the version-controlled manifest is the 
   authoritative declaration (owning the declared state, not metaphysical truth).
```

```text
MANIFEST_PROVIDES_DECLARED_STATE
MANIFEST_DOES_NOT_OVERRIDE_LIVING_REALITY
TRIGGER != SOURCE_OF_TRUTH
```

```text
DECLARATION  ──►  COMPILER  ──►  COMPILED INDEX + HASH ROOTS
TRIGGER      !=   SOURCE_OF_TRUTH
```

This clean separation ensures that Git hooks or build scripts act as execution triggers, while authority remains anchored in version-controlled semantic declarations.

---

## 11. Summary

Declare a finite focus instead of rediscovering the repository on every task. A document title is not runtime maturity. Parameterize repository reality by mode (`HEAD`, `WORKTREE`, `CERTIFIED_SNAPSHOT`). Finite does not mean blind: reachable undeclared code is a `REALITY_SPINE_GAP` (`LAW-REAL-04`). The spine reduces navigational uncertainty but not semantic or freshness uncertainty. Triggers are not sources of truth.

*(The conceptual schema, Merkle roots and verification modes are in [Appendix E: Reality Spine / reality.verify Conceptual Schema](#appendix-e-reality-spine--realityverify-conceptual-schema).)*


---


# Chapter 13: Copilot vs. Verb: Establishing Meaning and Verifying Sameness

> **"A reasoning copilot establishes what reality ought to mean. A deterministic verb verifies whether physical bytes match. Never ask a model to rediscover what a checksum can verify; never trust a checksum to decide whether an architecture makes sense."**  
> — *Orion Verification Doctrine*

---

## 1. Two Fundamentally Different Questions

When an engineering system orients itself within a complex, evolving repository, it is constantly confronted with two questions. To the untrained eye, these questions appear related:

```text
QUESTION A: "What constitutes the reality of this system?"

QUESTION B: "Does the current repository state match our established reality?"
```

Because both questions involve the word "reality," naive AI architectures attempt to answer both using the same tool: an open-ended LLM reasoning prompt.

They ask a model to re-scan the codebase on every task, re-read configuration files, re-verify dependencies, re-check whether files have drifted, and re-interpret the architecture.

This is a fundamental category error.

Question A and Question B belong to entirely different computational domains:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        THE CORE JURISDICTION SPLIT                     │
├───────────────────────────────────┬────────────────────────────────────┤
│ QUESTION A: ESTABLISHING MEANING  │ QUESTION B: VERIFYING SAMENESS     │
├───────────────────────────────────┼────────────────────────────────────┤
│ • "What is the rightful owner of  │ • "Are the bytes in `api/server.ts`│
│   this new lifecycle state?"      │   identical to the commit baseline │
│ • "Does this module belong in the │   we verified yesterday?"          │
│   Authority or Persistence view?" │ • "Has any file in the declared    │
│ • "Is this legacy interface safe  │   write mask been modified?"       │
│   to deprecate?"                  │ • "Does the on-disk SHA-256 digest │
│ • "How should we resolve this     │   match the recorded hash?"        │
│   policy contradiction?"          │                                    │
│                                   │                                    │
│ JURISDICTION: COGNITIVE SEAT      │ JURISDICTION: DETERMINISTIC VERB   │
│ (Human Architect / Copilot Model) │ (Compiled Script / Checksum Tool)  │
│ Tool: Semantic Reasoning          │ Tool: Cryptographic Hashing        │
└───────────────────────────────────┴────────────────────────────────────┘
```

The foundational law of Orion's verification architecture is expressed in six words:

```text
COPILOT  ESTABLISHES  MEANING.
VERB     ESTABLISHES  SAMENESS.
```

---

## 2. The Copilot Responsibility: Resolving Semantic Uncertainty

What does a **Reality Re-establishment Copilot** actually do?

When a repository undergoes structural evolution—when new subsystems are introduced, directories are refactored, or legacy code is retired—the system's navigation map becomes stale. Mechanical tools cannot fix this on their own, because a mechanical tool has no conception of design intent. A checksum can identify that a file was renamed from `auth.ts` to `security.ts`, but it cannot determine *why*, or whether the new file properly preserves the security invariants of the old one.

The Copilot station enters the loop specifically to resolve this **semantic uncertainty**:
- **Discovers and Interprets:** Searches the living repository to identify newly emerged architectural components, orphaned modules, and undocumented seams.
- **Resolves Ownership:** Evaluates competing service boundaries and assigns rightful owners according to system invariants (e.g., determining that `CognitiveTurnJournal`, not `MindRuntime`, must own durable sequence allocation).
- **Proposes Declarations:** Synthesizes its findings into a formal, machine-readable declaration—such as a proposed Reality Spine manifest, an Extension Contract, or an update to the topic ledger.
- **Identifies Stale Indexes:** Spots discrepancies between historical documentation and living code (for example, identifying that a specification claimed a feature was in production when live source demonstrates it was never implemented).

### The Boundary of Copilot Authority
Notice the explicit output status of the Copilot:

```text
COPILOT OUTPUT  :=  PROPOSED_REALITY
COPILOT OUTPUT  !=  CERTIFIED_TRUTH
```

A reasoning model—regardless of capability or confidence—**cannot certify its own proposals as ratified truth**. 

Its output is an unratified candidate hypothesis. It says: *"Based on my bounded analysis of the repository, I propose that these files constitute the runtime owners, and here is my architectural rationale."* 

That proposed reality must pass through operator review or formal verification gates before it can be adopted into the approved baseline.

---

## 3. The Verb Responsibility: Mechanical Sameness Verification

Once a declared reality has been established and approved, the reasoning model leaves the room.

To answer Question B—*"Does the current repository state match our established reality?"*—we invoke a deterministic **Verification Verb**.

The Verification Verb requires zero cognitive capability. It operates through deterministic computation:
- **Git Identity Check:** Verifies that the current repository HEAD matches the declared commit SHA.
- **Path Existence Check:** Verifies that every path promised in the declared Reality Spine physically exists on disk.
- **Content Hash Verification:** Computes the SHA-256 digest of each file's bytes and compares it against the declared `VERIFIED_HASH`.
- **Coverage Validation:** Checks whether files matching an active write mask have been modified.
- **Hierarchical Hash Aggregation:** Combines leaf digests into a deterministic root hash.

The Verification Verb does not infer, interpret, or guess. It returns an exact, mechanical status:

```text
VERB OUTPUT  :=  VERIFIED | STALE | SOURCE_MISMATCH |
                 REALITY_SPINE_GAP | INVALID_MANIFEST
```

If a single byte has changed in an audited file, the Verification Verb detects the mismatch and reports:

```text
STATUS: SOURCE_MISMATCH
FAILED_PATH: core/runtime/orion-composition-root.ts
EXPECTED_HASH: a1b2c3...
ACTUAL_HASH:   f9e8d7...
```

It does not attempt to "reason" about whether the change was harmless. It reports the objective mechanical fact: **the state is no longer the same**.

---

## 4. Target Architecture: `reality.compile` and `reality.verify`

*(Epistemic Notice: The following interface definitions represent **Target Architecture / Specified Not Implemented** (`TOPIC-COPV-02`). In current Orion practice, as demonstrated in Pass 1C and H0 milestones, these verifications are executed via targeted TypeScript scripts, Git commands, and manual inspection. The interfaces below describe standardized Verb contracts specified for future automated runtime implementation.)*

In Orion's target architecture (`ORION_EXPERIMENTAL_VERB_LANGUAGE_AND_SKILL_LOOP_SPEC.md`), this separation of concerns is embodied in two complementary interfaces:

```typescript
// TARGET ARCHITECTURE SPECIFICATION: REALITY VERB INTERFACES (ILLUSTRATIVE)

export interface RealityCompileInput {
  // The semantic declaration produced by Copilot/Architect
  readonly declaration_manifest_path: string;
  readonly target_commit_sha: string;
  readonly coverage_rules_path: string;
}

export interface RealityCompileResult {
  readonly ok: boolean;
  // The deterministic, canonicalized index
  readonly compiled_spine_path: string;
  // Master hierarchical root digest representing the declared reality
  readonly reality_root_hash: string;
  readonly leaf_count: number;
}

export interface RealityVerifyInput {
  readonly compiled_spine_path: string;
  // Repository mode (see Chapter 12 §2) and verification depth (hashes only, or transitive import coverage)
  readonly repository_mode: "HEAD" | "WORKTREE" | "CERTIFIED_SNAPSHOT";
  readonly depth: "FAST_HASH" | "DEEP_COVERAGE";
}

export interface RealityVerifyResult {
  readonly status: 
    | "VERIFIED"          // All declared files match verified hashes
    | "STALE"             // Repository commit has advanced past compiled baseline
    | "SOURCE_MISMATCH"   // One or more declared files have mutated on disk
    | "REALITY_SPINE_GAP" // Undeclared live code detected in static reachability check
    | "INVALID_MANIFEST"; // Declared file missing from disk
  readonly mismatch_details?: readonly {
    readonly kind: "MUTATED" | "UNATTRIBUTED_FILE";
    readonly path: string;
    readonly expected_sha256: string;
    readonly actual_sha256: string;
  }[];
  readonly execution_receipt_id: string;
}
```

Notice the distinction between **Path/Membership Verification** and **Static Reachability Coverage**:
- A basic hash check verifies that declared files on disk match their declared hashes.
- Detecting a `REALITY_SPINE_GAP` (where a live entry point imports an undeclared file) requires a deterministic source graph compiler or static analysis pass to evaluate the import graph.

---

## 5. The Root Hash Model: A Hierarchical Hash Taxonomy

How can a single digest represent the declared reality of an engineering subsystem?

Orion specifies a **Hierarchical Hash Taxonomy** over declared reality. Instead of hashing the entire repository into an undifferentiated string, the target design partitions reality into distinct structural roots:

```text
                                  REALITY_ROOT
                                       │
        ┌──────────────┬───────────────┼───────────────┬──────────────┐
        │              │               │               │              │
        ▼              ▼               ▼               ▼              ▼
   SOURCE_ROOT   RECEIPT_ROOT    DECISION_ROOT   OWNERSHIP_ROOT COVERAGE_ROOT
        │              │               │               │              │
   (Code Files)   (Prior Evidence)  (Architecture   (Assigned      (Explicit
                                   Records)        Boundaries)    Negative Space)
```

*(Epistemic Notice: Per-file hashing is standard in Orion freeze certificates; the hierarchical Merkle structure above is a **Target Specification** (`TOPIC-COPV-04`).)*

### The File Leaf Digest (Target Model)
In the target specification, a leaf node in the `SOURCE_ROOT` binds code content to its architectural metadata:

```text
FILE_LEAF_DIGEST := SHA256(
    normalized_relative_path  + "\n" +
    git_blob_sha              + "\n" +
    raw_content_sha256        + "\n" +
    declared_role             + "\n" +
    rightful_owner            + "\n" +
    authority_class           + "\n" +
    read_write_class
)
```

If code is modified, `raw_content_sha256` changes, breaking the leaf digest.  
If code remains untouched but its designated ownership is changed in the manifest, `rightful_owner` changes, altering the leaf digest.

Under this target model, the `REALITY_ROOT` reflects both **physical content** and **declared governance**.

---

## 6. The Danger of False Conflation: Sameness vs. Correctness

We now arrive at a critical epistemic warning:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        THE SUPREME EPISTEMIC LAW                       │
├────────────────────────────────────────────────────────────────────────┤
│                                                                        │
│   REALITY_ROOT_MATCH  !=  ARCHITECTURE_CORRECT                         │
│                                                                        │
│   ROOT_MATCH                                                           │
│   = STRONG MECHANICAL EVIDENCE THAT THE DECLARED BYTES AND METADATA    │
│     MATCH WITHIN THE VERIFIED BOUNDARY UNDER CHOSEN CANONICALIZATION   │
│                                                                        │
│   CHECKSUM CONTINUITY !=  SEMANTIC TRUTH                               │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

Consider what occurs if an architect creates a Reality Spine containing an architectural defect—for example, granting write access over a lock file to an unauthenticated endpoint.

The Reality Spine is compiled, and a `REALITY_ROOT` is generated. 

When `reality.verify` runs, it reports: `STATUS: VERIFIED (ROOT MATCH)`.

What does that match establish?  
Strong mechanical evidence, under the chosen canonicalization boundary, that **the declared files have not changed since the baseline was recorded**. It demonstrates boundary-scoped mechanical sameness. It does **not** establish that the architecture is safe, correct, or free of design flaws.

A checksum cannot evaluate whether an interface is sound, whether a security model holds, or whether code satisfies requirements. 

**Checksums verify continuity, not quality. They verify sameness, not correctness.**

Therefore, two orderings coexist in the Orion lifecycle, for different purposes:
1. **Baseline adoption: semantic approval first.** Qualified Copilot stations and the rightful reviewers audit the soundness of a proposed reality. Only after it is approved is its root locked in as the approved baseline, which then acts as a sentry against silent drift.
2. **Subject freezing: hash first.** When an audit or certification begins, the subject's identity is hash-frozen *before* the semantic audit, so the audit is about a fixed subject (Chapter 17 §9). Freezing a subject asserts identity, not approval.

---

## 7. The Copilot / Verb Cooperative Loop

In daily engineering operations, Copilot and Verb do not operate in isolation. They form a continuous, cooperative loop:

```text
               ┌──────────────────────────────────────────────┐
               │ 1. REALITY UNKNOWN OR STALE                  │
               │    (New wave begins, or drift detected)      │
               └──────────────────────┬───────────────────────┘
                                      │
                                      ▼
               ┌──────────────────────────────────────────────┐
               │ 2. COPILOT RE-ESTABLISHES MEANING            │
               │    (Explores source, resolves owners,        │
               │     drafts proposed Reality Spine)           │
               └──────────────────────┬───────────────────────┘
                                      │
                                      ▼
               ┌──────────────────────────────────────────────┐
               │ 3. REVIEW / GOVERNANCE GATE                  │
               │    (Audits proposal, accepts baseline)       │
               └──────────────────────┬───────────────────────┘
                                      │
                                      ▼
               ┌──────────────────────────────────────────────┐
               │ 4. COMPILER MATERIALIZES INDEX               │
               │    (Computes leaf digests & REALITY_ROOT)    │
               └──────────────────────┬───────────────────────┘
                                      │
                                      ▼
               ┌──────────────────────────────────────────────┐
               │ 5. VERB LOCKS IN MECHANICAL SAMENESS         │
               │    (Root digest stored in freeze record)     │
               └──────────────────────┬───────────────────────┘
                                      │
                                      ▼
               ┌──────────────────────────────────────────────┐
               │ 6. PRODUCTION WORK WAVE                      │
               │    (Stations verify root mechanically;       │
               │     reuse established orientation;           │
               │     zero rediscovery token overhead)         │
               └──────────────────────┬───────────────────────┘
                                      │
                                      ▼
                      [IF ANY DRIFT OR GAP OCCURS]
                                      │
                                      ▼
               ┌──────────────────────────────────────────────┐
               │ 7. VERB FAILS CLOSED                         │
               │    (Emits REESTABLISHMENT_REQUIRED signal;   │
               │     loop returns to Step 2)                  │
               └──────────────────────────────────────────────┘
```

Notice the division of labor:
- **Step 2 (The Cognitive Step):** Runs when a project begins a major wave or when legitimate architectural drift occurs. It expends reasoning tokens deliberately where uncertainty exists.
- **Step 6 (The Production Work Wave):** Runs repeatedly. Automated routines, test runners, and specialized coding stations verify the root mechanically. When the root matches within the declared boundary, the station can proceed without re-parsing documentation or re-grepping the repository.

---

## 8. Real-World Case Study: Pass 1C and H0 Clean Reconstruction

To see how this distinction operates in practice, let us examine two actual engineering milestones in the Orion repository: the **H0 Minimum Viable Orion Independent Verification** and the **Pass 1C Clean Reconstruction Strategy**.

### The H0 Independent Verification Receipt
On September 18, 2026, an independent Claude verifier station (`INDEPENDENT_H0_VERIFIER`, recorded in receipt metadata as `Claude Sonnet 5`) evaluated Gemini's claim that a minimal runnable Orion process (`H0`) had successfully executed live OS-level process restarts without losing state (`LIVE_ALPHA_H0_INDEPENDENT_VERIFICATION_RECEIPT.md`).

Notice the verification method:
1. **Did Not Rely on Receipt Prose:** The verifier did not treat Gemini's markdown summary as proof.
2. **Mechanical Re-Execution:** The verifier spawned live OS child processes via `tsx api/server.ts`, executed HTTP requests, issued OS-level termination signals, spawned a subsequent child process, and observed journal rehydration with fresh Process IDs (`PIDs 43228/44164` vs. Gemini's reported `30196/20680`).
3. **Byte-Level Hash Verification:** The verifier diffed content hashes of frozen M5 R2 W0-W3 files against hashes recorded in the freeze certificate from 2026-09-17, confirming byte-identity across audited implementation files.
4. **Falsification of Overclaims:** The verifier discovered that Claim D ("removed a duplicate partial systemAccessRoute mount") was unsupported by Git diff history, flagging the descriptive inaccuracy while confirming core functional properties.

### The Payload vs. Evidence Distinction
Clean verification (Pass 1C plan §16) rests on a distinction developed in [Chapter 17 §5](#chapter-17-repair-clean-reconstruction-certification-and-adoption): `PAYLOAD_IDENTITY != EVIDENCE_ABOUT_PAYLOAD_IDENTITY`. The payload is the set of files proposed; the evidence (logs, receipts, audit notes) is produced during verification and stays outside the payload's byte root. Pass 1C was in progress at audit time; see Chapter 17 §10.

---

## 9. Summary

Copilots establish meaning; Verbs establish sameness. Never ask an LLM to rediscover what a checksum can verify, and never let a matching checksum convince you that a flawed architecture is correct (`LAW-REC-03`).

Part VI turns to defect lifecycles and control identity (Chapters 14–15). Part VII covers adversarial verification, clean reconstruction and certification (Chapters 16–17).


---


# Chapter 14: Defect Instances, Defect Classes, and Semantic Neighborhoods

> *"Fixing the observed failure is not the same as closing the failure class."*

---

## 1. The Whack-a-Mole Trap

In naive AI-assisted software engineering, defect repair follows an expensive, circular rhythm:

1. A test fails or an operator reports an error.
2. The model inspects the immediate stack trace.
3. The model patches the exact line of code where the exception occurred.
4. The test turns green.
5. The model declares victory: *"The bug is fixed."*
6. Three days later, an adjacent component fails under the identical underlying condition, or the original component fails when provided with a slightly different input.

This pattern is known in Orion engineering as **Symptom Patching** or the **Whack-a-Mole Trap**.

The failure stems from a fundamental epistemic confusion: the model treated the **defect instance** (the single observed manifestation of an error) as if it were the **defect class** (the underlying causal mechanism capable of producing that entire family of failures).

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE DEFECT DEPTH PYRAMID                             │
├───────────────────────────────────┬────────────────────────────────────┤
│ LEVEL                             │ WHAT IT REPRESENTS                 │
├───────────────────────────────────┼────────────────────────────────────┤
│ 1. ERROR SYMPTOM                  │ The stack trace or exception text. │
│                                   │ "TypeError: cannot read null"      │
├───────────────────────────────────┼────────────────────────────────────┤
│ 2. DEFECT INSTANCE                │ The concrete line of code that     │
│                                   │ crashed under specific input.      │
├───────────────────────────────────┼────────────────────────────────────┤
│ 3. ROOT CAUSE MECHANISM           │ The architectural invariant that   │
│                                   │ was violated.                      │
├───────────────────────────────────┼────────────────────────────────────┤
│ 4. DEFECT CLASS                   │ All sibling paths and services     │
│                                   │ sharing that flawed mechanism.     │
└───────────────────────────────────┴────────────────────────────────────┘
```

When an engineering system delegates repair tasks to cognitive models, the prompt must explicitly forbid symptom-level patching. The goal of repair is not merely to produce a passing test; it is to eliminate the mechanism that permits the defect class to exist within the bounded semantic neighborhood.

---

## 2. Defect Instance vs. Defect Class

To reason about defects rigorously, we must separate the instance from the class:

```text
DEFECT_INSTANCE:
  The concrete, localized failure observed during execution.
  A point in space and time.

DEFECT_CLASS:
  The architectural vulnerability, missing invariant, or semantic flaw
  capable of generating a family of related failure instances.
```

### An Orion Case Study: The Ambient Storage Root
In the evolution of Orion's test harnesses (documented in `TEST_HARNESS_DESIGN_CLOSURE_SPOT_CHECK.md`), a recurring vulnerability was identified where test execution polluted ambient workspace state.

- **The Instance:** A persistence ledger was writing records relative to the current working directory (`process.cwd()`), instead of writing to an isolated temporary sandbox provided by the test runner.
- **The Naive Patch:** An LLM prompted with *"fix the test"* might simply change the test to `chdir` into a temporary folder before running, or add an ad-hoc `if (process.env.NODE_ENV === "test")` branch inside the service.
- **The Defect Class (`StorageRootAmbientDefault`):** Multiple stateful services—such as quest services defaulting to unrooted ledgers (`?? new PhaseXLedger()`)—fell back to ambient process state (`process.cwd()`) when no explicit storage root configuration was injected:
  ```typescript
  // THE FLAWED MECHANISM:
  this.storageRoot = config.storageRoot ?? path.resolve(process.cwd(), "data");
  ```
- **The Class Repair:** Searching the semantic neighborhood revealed that several sibling services in the quest cluster shared similar ambient fallbacks. The defect class was addressed across the service neighborhood by requiring explicit configuration injection (e.g. `createSandboxQuestRoots` passing all required storage roots), sandboxing direct ledger/service instantiations, and backing the invariant with a mechanical test write-guard (`TrackedWriteGuard`) configured with `ORION_TEST_PROTECTED_ROOT` to fail closed whenever an unrooted write was attempted.

```text
LAW:
FIXING_THE_OBSERVED_FAILURE  !=  CLOSING_THE_FAILURE_CLASS
```

---

## 3. The Bounded Defect Packet

When Orion's multi-model assembly line encounters an architectural defect, the diagnostic station does not output an informal paragraph of prose. It compiles a **Bounded Defect Packet**.

This structured packet defines the complete engineering boundary of the problem:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   BOUNDED DEFECT PACKET                                │
├──────────────────────────────┬─────────────────────────────────────────┤
│ FIELD                        │ PURPOSE                                 │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 1. DEFECT                    │ Concise semantic definition of the flaw.│
│ 2. REPRODUCTION_OR_FAILURE_  │ Strongest mechanically inspectable      │
│    EVIDENCE                  │ evidence establishing defect boundary   │
│                              │ (replay, stochastic contract, crash     │
│                              │ trace, corruption, static analysis).    │
│ 3. ROOT_CAUSE                │ Invariant violation that causes it.     │
│ 4. RIGHTFUL_OWNER            │ Owner of the violated invariant         │
│                              │ (component responsible for truthful     │
│                              │ state or contract normalization).       │
│ 5. REPAIR_INVARIANT          │ Exact truth condition that must hold    │
│                              │ after repair.                           │
│ 6. ADVERSARIAL_TEST          │ Test designed to actively attack the    │
│                              │ proposed repair.                        │
│ 7. MUST_NOT_CHANGE           │ Protected surfaces that the repair is   │
│                              │ strictly forbidden from touching.       │
│ 8. BOUNDED_SIBLING_SEARCH    │ Rules for identifying adjacent instances│
│                              │ of the same defect class.               │
└──────────────────────────────┴─────────────────────────────────────────┘
```

### P-GLL Representation (ILLUSTRATIVE_NONHISTORICAL_EXAMPLE)

```text
DEFECT_PACKET:
  # ILLUSTRATIVE_NONHISTORICAL_EXAMPLE - Conceptual defect contract demonstrating schema
  defect_id: "DFCT-LIFE-004-EXAMPLE"
  defect_class: "ApplicationDataImpersonatingControlState"
  instance: "example/routes/mock-task-execution.ts:114"
  reproduction_or_failure_evidence:
    command: "npx tsx scripts/reproduce-task-timeout-example.ts"
    input_payload: { task_id: "task-99", simulate_user_error: "TIMED_OUT" }
    observed_state: "STATUS: ORCHESTRATOR_ABORTED (False Timeout Promotion)"
  root_cause: "Orchestrator inferred control timeout by checking err.message === 'TIMED_OUT'"
  rightful_owner: "example/orchestration/mock-task-supervisor.ts"
  repair_invariant: "Control timeouts require tagged union identity originating from timer signal"
  adversarial_test: "tests/mock-task-timeout-control-identity.test.ts"
  must_not_change:
    - "example/protocol/mock-lifecycle-messages.ts"
    - "example/routes/mock-system-access.ts"
  bounded_sibling_search:
    axis: "String-equality error checks in orchestration runners"
    scope: "example/orchestration/*.ts"
```

This packet acts as a binding contract. An implementer station receiving this packet cannot wander off into unrelated refactoring, must satisfy the applicable repair-verification contract (replaying historical failures when available, or employing the strongest available falsifier/evidence while explicitly bounding verification confidence when replay is infeasible), and cannot ignore sibling components that share the flaw. Preserving: `REPAIR_CONFIDENCE MUST_NOT EXCEED_AVAILABLE_EVIDENCE`.

---

## 4. Defect Reproduction Epistemology: Evidence Beyond Aesthetic Intuition

In software engineering debates, cognitive models frequently fall into subjective rhetoric:
- *"This code looks inefficient."*
- *"This error handling seems fragile."*
- *"We should probably refactor this promise chain."*

In Orion, **subjective aesthetic critiques do not constitute defect reports**. An unproven suspicion is merely a candidate hypothesis.

However, we must avoid the opposite error: asserting that if you cannot deterministically replay an issue on demand, no defect exists. A defect may be established with strong evidence through:
- Production crash traces and diagnostic dumps
- Corrupted durable state or cryptographic digest contradictions
- Static invariant contradictions or unreachable-state analyses
- Formal verification or model-checking counterexamples
- Probabilistic race reproduction under stress
- Historical telemetry and monotonic sequence gaps
- Destructive conditions that cannot safely or ethically be replayed in production

Therefore, Orion's governing epistemic law is:

```text
LAW:
REPRODUCTION_STRENGTHENS_DEFECT_BOUNDARY_KNOWLEDGE

BUT:
NOT_REPRODUCED  !=  NO_DEFECT

AND:
WHEN_HISTORICAL_FAILURE_CANNOT_BE_REPLAYED
REPAIR_VERIFICATION_REMAINS_PARTIAL_OR_SCOPE_LIMITED
```

A suspected issue with insufficient evidence should be classified as `NOT_DETERMINABLE`, requiring targeted probes. We do not erase or deny real defects simply because deterministic replay is difficult or unavailable.

### Mechanical Reproduction May Be Stochastic
Furthermore, not every valid reproduction is a single deterministic command. Concurrency races, socket timeouts, and scheduling hazards are frequently probabilistic.

A rigorous reproduction contract for stochastic defects defines **Reproducible Evidence** over an experimental trial space:

```text
STOCHASTIC_REPRODUCTION_CONTRACT:
  input_stimulus:       Specific payload or command sequence
  environment:          Hardware constraints, Node runtime, thread count
  stress_conditions:    Concurrency factor (e.g. 50 parallel workers)
  observation_window:   Temporal duration or event cycle bound
  trial_count:          Number of iterations (e.g. 1,000 trials)
  observed_frequency:   Failure occurs in >= N% of trials
  failure_identity:     Exact signature or invariant violation
```

### The Anatomy of Truthful Reproduction
Where reproducible evidence can be established, it typically contains six concrete elements:

1. **Baseline Commit:** The exact Git commit SHA or snapshot digest against which the failure occurs.
2. **Execution Command:** The verbatim shell or test command.
3. **Exact Input Stimulus:** The parameters, payload, or schedule stress passed to the system.
4. **Environment Constraints:** Pertinent host details (Node version, OS signal behavior, path bounds).
5. **Expected State:** The invariant required by the system contract.
6. **Observed Invalid State:** The physical failure observed (e.g., `FATAL: journal sequence gap at index 22`).

```text
WEAK EVIDENCE:
  "I reviewed the code and think the restart logic has a race condition."

STRONG REPRODUCIBLE EVIDENCE:
  INPUT: 50 parallel workers executing concurrent acquire-release loops.
  COMMAND: npx tsx tests/concurrency-race-stress.test.ts
  OBSERVED: Lease acquired by 2 PIDs simultaneously in 4 out of 100 runs.
  FAILURE_IDENTITY: ERR_CONCURRENT_LEASE_COLLISION
```

Reproduction provides an empirical falsification target for repair verification. When historical failure cannot be mechanically replayed, repair verification must be explicitly recognized as bounded and scope-limited.

---

## 5. Root Cause vs. Symptom

A common failure mode in LLM coding is conflating the **error message** with the **root cause**.

```text
ERROR_MESSAGE   !=  ROOT_CAUSE
TEST_FAILURE    !=  ROOT_CAUSE
```

### The Symptom Mask (Illustrative Scenario)
Suppose an execution process crashes during reboot with the following error:
```text
Uncaught Error: AutonomyLeaseRevoked: writer lease held by PID 4412
    at AutonomyLeaseManager.acquire (core/autonomy/lease-manager.ts:89)
    at MindRuntime.initialize (core/runtime/mind-runtime.ts:42)
```

- **The Symptom:** `AutonomyLeaseRevoked`.
- **The Naive LLM Reflex:** Modify `AutonomyLeaseManager.acquire()` to bypass the lease check if the process is starting up, or add a try/catch block around `leaseManager.acquire()` to swallow the error.
- **The Disaster:** Swallowing the lease error allows two processes to simultaneously write to the same event log, permanently corrupting the cognitive turn journal!

To find the **Root Cause**, the diagnostic station must trace backward through the causal chain of invariants:
1. *Why was the lease still held?* Because the previous process was killed abruptly by an OS signal (`SIGKILL`).
2. *Why didn't the new process claim the lease?* Because the lease had an expiration timeout of 30 seconds that had not yet elapsed.
3. *Why didn't the new process detect that the previous PID was dead?* Because the lease manager checked only timestamp expiration, not operating system process liveness (e.g., an OS-level liveness check `isPidAlive()`).
4. **The True Root Cause:** The lease reclamation policy lacked an OS-level liveness verification step for local process boundaries.

A root cause identifies the **specific mechanism that violated an architectural invariant**. Repairing the root cause preserves all system invariants; patching the symptom compromises them.

---

## 6. The Law of the Rightful Owner

Where in the codebase should a defect be repaired?

A naive model will repair a defect wherever it happens to crash. If Component C crashes because it received bad data from Component B, which received it from Component A, the model will typically add a defensive `if (!data) return;` check inside Component C.

This creates **Architectural Sclerosis**: defensive guards accumulate deep in the consumer layer, while the producer continues emitting invalid data.

Orion enforces the **Law of the Rightful Owner**:

```text
END_TO_END_CONTRACT_TRUTH  =  TRUTHFUL_PRODUCTION  +  CORRECT_CONSUMPTION

A CORRECT CONSUMER CANNOT REPAIR A DISHONEST PRODUCER.
```

*(Note: In technical architecture, "dishonest" denotes a component that mechanically emits inaccurate, incomplete, or out-of-spec state, not intentional human deception).*

```text
[PRODUCER A] ──────► [CONSUMER B] ──────► [CONSUMER C]
  Emits invalid       Passes along         Crashes on
  null timestamp      malformed record     null pointer
       ▲
       │
RIGHTFUL OWNER:
Repair MUST happen here!
Do NOT patch Consumer C to silently accept corrupt records.
```

### Consumer Validation vs. Producer Repair
We must draw an essential boundary between **Consumer Validation** and **Producer Repair**:

```text
CONSUMER_VALIDATION  !=  PRODUCER_REPAIR

RIGHTFUL_OWNER  :=  OWNER_OF_THE_VIOLATED_INVARIANT
```

1. **Consumer Validation Is Obligatory:** A consumer MAY and often SHOULD validate its input contracts, reject invalid producer output, fail closed, or quarantine malformed records. A consumer that validates incoming data is upholding its own contract.
2. **Producer Repair Is Forbidden in Consumers:** What a consumer must **never** do is silently invent replacement truth (such as forging default timestamps or synthesizing surrogate identity IDs) to mask an upstream invariant failure.
3. **Rightful Owner Defined by Invariant, Not Call Stack Position:** The rightful owner is the component responsible for the violated invariant. In layered architectures, an adapter or normalization boundary legitimately owns translation between external formats and internal types. Rightful ownership does not mean every edit must occur at the physically earliest utility function in the stack, but rather at the architectural boundary governing that invariant.

---

## 7. The Bounded Semantic Neighborhood

Once a defect instance is understood and its root cause mechanism is identified, the repair station must not stop. It must explore the **Bounded Semantic Neighborhood**.

```text
INSTANCE FOUND
      │
      ▼
ROOT CAUSE MECHANISM IDENTIFIED
      │
      ▼
BOUNDED SEMANTIC NEIGHBORHOOD DEFINED
      │
      ▼
SIBLING SEARCH EXECUTED
      │
      ▼
CONVERGENCE ASSESSMENT REACHED
```

### What Is a Semantic Neighborhood?
A semantic neighborhood is not a random collection of nearby files, nor is it an entire repository. It is the bounded set of components that share **architectural characteristics** with the flawed component:

```text
A SEMANTIC NEIGHBORHOOD IS DEFINED BY:
- The same component owner or subsystem family
- The same state dimension or enum classification
- The same serialization or parsing pathway
- The same authority boundary or lease controller
- The same lifecycle transition or event hook
- The same ambient environmental assumption
```

### Bounded Does Not Mean Arbitrary File Counts
Many prompting guides suggest arbitrary rules like *"search the top 5 files"* or *"read 10 search results."* 

In Orion, bounded searches are defined by **semantic stop conditions**, not arbitrary integers:

```text
THE SEARCH EXPANDS WHEN EVIDENCE DEMANDS IT,
NOT BECAUSE THE MODEL'S CONTEXT FEELS INCOMPLETE.
```

A sibling search terminates when:
1. The rightful owner of the mechanism is established.
2. All active call sites or sibling implementations sharing the flawed mechanism within the declared boundary have been inspected and classified.
3. Every identified sibling is categorized into a defined action state.
4. No unresolved evidence (such as unclassified references or broken type signatures) points to further propagation.

---

## 8. Sibling Defect Classification

When searching a semantic neighborhood for siblings of a defect class, not every match has identical severity. Orion classifies sibling discoveries into five explicit categories:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   SIBLING DEFECT CLASSIFICATION                        │
├──────────────────────────────┬─────────────────────────────────────────┤
│ STATUS                       │ MEANING & REQUIRED ACTION               │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 1. LIVE_MATERIAL_DEFECT      │ An active, reachable component actively │
│                              │ exhibiting the flawed mechanism. Must   │
│                              │ be repaired in the current wave.        │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 2. DORMANT_DEFECT            │ The flawed mechanism is present, but    │
│                              │ currently unreachable due to upstream   │
│                              │ guards or configuration. Documented and │
│                              │ scheduled for hardening.                │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 3. DEFERRED_ACTIVATION_GUARD │ A path that would fail under future     │
│                              │ expansion, but is protected by active   │
│                              │ write masks. Explicitly logged as gap.  │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 4. NOT_APPLICABLE            │ Code matches the text pattern (e.g. has │
│                              │ similar variable names) but uses a      │
│                              │ safe, independent mechanism.            │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 5. NOT_DETERMINABLE          │ Reachability or authority cannot be     │
│                              │ established with current evidence.      │
│                              │ Requires targeted probe before action.  │
└──────────────────────────────┴─────────────────────────────────────────┘
```

### Historical Case Study: Pass 1C R4 Timeout Classification and the Dormant Supervisor
During the Pass 1C convergence campaign (in progress and uncommitted at audit time; the files named below exist in the Pass 1C worktree, not in the main tree), an audit investigated timeout handling and authority retention during shutdown.

The active defect centered on orchestrator timeout classification:
- **Active Defect (`LIVE_MATERIAL_DEFECT`):** The orchestrator inspected an error from a detached promise. When an application-level operation rejected with an error whose message happened to be `"TIMED_OUT"` (or an error labeled as a timeout), the orchestrator erroneously treated it as an un-settled, still-running background mutator (`TIMED_OUT_STILL_LIVE`). Consequently, shutdown retained writer authority indefinitely and blocked clean restarts on the same root, even though the task had fully settled (failed).
- **The Active R4 Repair:** As exercised by test `PASS1C-R4-ORCHESTRATOR-TIMEOUT-COLLISION-SETTLED-1`, the classification mechanism was repaired to distinguish settled application failures from true un-settled timer expirations. When the promise settles with failure, shutdown reports the step as `FAILED` (not `TIMED_OUT_STILL_LIVE`), releases writer authority safely, and permits immediate same-root restart.

When searching the semantic neighborhood for sibling implementations of timeout string-classification, the audit uncovered an adjacent finding:
- **Adjacent Sibling Finding:** `core/runtime/runtime-task-supervisor.ts` contained a magic-string timeout classifier matching the flawed pattern.
- **Classification (`DORMANT_DEFECT`):** Source analysis revealed that `runtime-task-supervisor.ts` had zero active production registrations in the live server startup path and did not participate in writer-authority retention decisions. It was categorized as nonblocking and dormant, preventing scope explosion while preserving the finding in the technical debt ledger.

This distinction between active blocking repairs and dormant sibling discoveries allowed the station to proceed without stalling on dead code.

---

## 9. Convergence: Stopping Defect Class Propagation

What does it mean for a defect repair campaign to "converge"?

In naive engineering, teams chase the illusion of "perfection"—believing that a repair campaign is finished only when every theoretical issue in the repository has been explored. This leads to **Scope Explosion**, where a simple bug fix turns into an endless multi-month rewrite.

In Orion, we define **Bounded Convergence**:

```text
CONVERGENCE  !=  "ALL CODE IS PERFECT"

CONVERGENCE  :=  THE DEFECT CLASS NO LONGER PROPAGATES 
                 THROUGH THE VERIFIED SEMANTIC NEIGHBORHOOD 
                 AT THE CURRENT BASELINE.
```

Notice the critical qualifications:
- **No Longer Propagates:** Every live sibling in the neighborhood has been repaired or verified safe.
- **Through the Verified Semantic Neighborhood:** The boundary of investigation was explicit and respected.
- **At the Current Baseline:** The claim is strictly scoped to the tested commit and environment. Future source mutations may reopen the defect class, which is why automated adversarial regression tests are committed alongside the repair.

We never claim a defect is "permanently fixed forever." We claim that **its causal mechanism has been mechanically eliminated from the declared boundary under current regression evidence.**

---

## 10. Anti-Pattern: Full Architecture Redesign on Every Failure

`TOPIC-ANTI-13`: handed an error log, an unguided model often reaches for radical overreach (*"the entire StateMachine pattern is flawed; replace it with an actor framework"*, or *"because this relative path failed, rewrite all storage layers to use SQLite"*). A null pointer on an uninitialized configuration object becomes a proposal to refactor the schema, rewrite the composition root and replace the build system. Orion's governance suppresses this: the defect packet lists must-not-change surfaces; the repair station drills deep into the root-cause mechanism but is forbidden from widening breadth across unproven subsystems (Chapter 8 §3); and an architecture that satisfies its requirements is not discarded because of a localized implementation defect. Repair the mechanism; do not replace the subsystem.

## 11. Summary

Fixing the instance is not closing the class (`LAW-DFC-02`). Reproduction strengthens boundary knowledge; not reproduced is not no defect (`LAW-DFC-03`). An error message is not a root cause. A correct consumer cannot repair a dishonest producer (`LAW-DFC-01`). Search expands because evidence demands it, and convergence means class elimination within a verified neighborhood at the current baseline.


---


# Chapter 15: Truth Tables, Lifecycle Dimensions, and Control Identity

> *"Different state dimensions must remain orthogonal. Never collapse outcome, lifetime, and authority into a single enum."*

---

## 1. The Multi-Dimensional State Trap

When software systems fail in complex, unrepeatable ways, engineers often blame "concurrency bugs" or "distributed systems mysteries." 

In many recurring failure cases, the true culprit is much simpler: **State Dimension Collapse**.

State Dimension Collapse occurs when an engineer or AI model attempts to compress multiple independent physical questions into a single variable, enum, or status string.

Consider a naive asynchronous task system that defines a single status enum:
```typescript
type TaskStatus = "PENDING" | "RUNNING" | "SUCCESS" | "FAILED" | "TIMEOUT";
```

At first glance, this looks clean and standard. But consider what happens when a task exceeds its allocated duration:
- The orchestrator sets `status = "TIMEOUT"`.
- Does the background worker actually stop executing?
- If the worker makes a database write five seconds later, is it permitted?
- Did the work succeed partially before timing out?
- Is the execution thread dead, paused, or still running?

The single enum cannot answer these questions because it collapses at least three independent physical dimensions:
1. **The Outcome Dimension:** Did the operation achieve its functional goal?
2. **The Settlement Dimension:** Can this asynchronous work still execute instructions or mutate state?
3. **The Authority Dimension:** Does this task hold the legal right to write to system storage?

When these dimensions are collapsed into one label, the system inevitably introduces critical race conditions, ghost writes, and security leaks.

In Orion, we enforce the **First Law of Lifecycle Engineering**:
```text
DIFFERENT_STATE_DIMENSIONS  MUST_REMAIN_ORTHOGONAL.
```

---

## 2. Success != Settlement

The most common dimensional collapse in modern engineering is confusing **Success** with **Settlement**.

```text
SUCCESS:
  Answers the business question:
  "Did the operation achieve its desired functional goal?"
  (Values: SUCCESS | FAILURE | PARTIAL)

SETTLEMENT:
  Answers the physical lifecycle question:
  "Can this asynchronous work still execute, allocate, or mutate?"
  (Values: SETTLED | LIVE)
```

These two questions are completely orthogonal. Neither implies the other.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   SUCCESS VS. SETTLEMENT MATRIX                        │
├─────────────────────┬──────────────────┬───────────────────────────────┤
│ STATE COMBINATION   │ PHYSICAL STATE   │ PRACTICAL EXAMPLE             │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ SUCCESS + SETTLED   │ Goal achieved,   │ File write completed and      │
│                     │ execution dead.  │ flushed to disk successfully. │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ FAILED + SETTLED    │ Goal missed,     │ Input validation failed;      │
│                     │ execution dead.  │ rejected before any I/O began.│
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ FAILED + STILL_LIVE │ Goal missed,     │ Worker threw an error, but    │
│                     │ execution alive. │ background cleanup thread is  │
│                     │                  │ still flushing buffer to disk.│
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ TIMED_OUT + LIVE    │ Deadline passed, │ Network call timed out at the │
│                     │ execution alive. │ client, but remote server is  │
│                     │                  │ still executing the payload.  │
└─────────────────────┴──────────────────┴───────────────────────────────┘
```

Notice the dangerous combinations:
- **`FAILED + STILL_LIVE`:** If the control plane assumes that because an operation returned an error it is completely finished, it might immediately schedule a new task to write to the same file. The still-live failed task then emits an asynchronous write, corrupting the new task's data!
- **`TIMED_OUT + STILL_LIVE`:** Timing out on a client timer does not mechanically terminate the remote process. The remote worker remains live until explicitly cancelled or fenced.

```text
LAW:
SUCCESS_IS_FUNCTIONAL;  SETTLEMENT_IS_PHYSICAL.
NEVER_INFER_SETTLEMENT_FROM_FAILURE.
```

---

## 3. Failed != Live

Let us examine the inverse error: **Assuming that a failure means the system is still live**, or conversely, **assuming that a failure means the system is dead**.

The two laws below are book doctrine, motivated by Orion's lifecycle work (the Pass 1C R4 timeout-classification repair and the M5 R2 design's care about what a failure leaves running). They are not quoted from the M5 R2 design:

```text
FAILED  DOES_NOT_IMPLY  MUTATOR_STILL_RUNNING
TIMED_OUT  DOES_NOT_IMPLY  MUTATOR_TERMINATED
```

### The Zombie Worker Disaster
Suppose an agent is assigned a coding task. It spins up a background TypeScript compilation process. After 60 seconds, the parent orchestrator logs `TASK_FAILED: Execution deadline exceeded` and returns control to the user.

If the orchestrator did not send an OS-level `SIGKILL` or verify process termination, that TypeScript process is now a **Zombie Mutator**. 

Ten seconds later, the user gives the agent a new command: *"Switch to the release branch and run tests."* The agent switches branches. Suddenly, the background zombie compiler finishes writing its compiled artifacts, dropping outdated `.js` files from the *previous* branch directly into the *new* branch!

Tests fail unpredictably. The agent becomes disoriented. It hallucinates that Git is broken.

### The Orion Invariant: Scoped Settlement
In Orion, a task is never marked completed or cleaned up until its **Settlement State** is mechanically confirmed within its authority scope:

```text
SETTLED_FOR_AUTHORITY_SCOPE  :=  NO OPERATION-OWNED EXECUTION CAN STILL PRODUCE
                                 EFFECTS INSIDE THE PROTECTED AUTHORITY OR
                                 RESOURCE BOUNDARY.
```

Notice the critical boundary: **Settled for Authority Scope**. A host process or runtime daemon may remain alive to perform unrelated work, serve health checks, or manage subsequent tasks. Settlement does not demand that every thread or child process in the host operating system be dead; it asks specifically whether any residual mutator owned by the governed operation can still execute mutations within the protected resource boundary.

If settlement cannot be verified, the runtime must enter a governed fence state rather than pretending the failure cleanly terminated the mutator.

---

## 4. Truth Tables Before Lifecycle Implementation

How do high-assurance systems prevent state collapse?

In Orion, we follow an explicit engineering principle: **author a multi-dimensional truth table for high-assurance, lifecycle-sensitive state machines.**

```text
RULE:
ASSURANCE_DEPTH_SCALES_WITH_STATE_RISK.
DEFINE ORTHOGONAL DIMENSIONS FIRST FOR LIFECYCLE-SENSITIVE MACHINES.
CONSTRUCT THE TRUTH TABLE SECOND.
WRITE THE CODE THIRD.
```

Authoring a comprehensive truth table is not a mandatory prerequisite for every trivial one-line UI transition. But for state machines that govern **exclusive writer leases, process lifecycles, concurrency barriers, or data-loss risks**, a truth table is an essential design discipline.

### Defining the Independent Dimensions
For any stateful subsystem, identify the independent physical axes. A standard Orion execution station typically tracks four conceptual axes:

1. **`OUTCOME`:** `[PENDING, SUCCESS, FAILURE, ABORTED]`
2. **`SETTLEMENT`:** `[LIVE, SETTLED]`
3. **`RUNTIME_STATE`:** `[INITIALIZING, RUNNING, DRAINING, STOPPED, ERROR]`
4. **`AUTHORITY`:** `[RESERVED, ACTIVE, SUSPENDED, RELEASED, RETAINED_FENCE]`

### Illustrative High-Assurance Truth Table (Conceptual Model)
Once the dimensions are declared, map the legal combinations in a truth table. Any combination not explicitly allowed is forbidden by default (`FAIL_CLOSED`):

```text
┌────────────────────────────────────────────────────────────────────────┐
│             ILLUSTRATIVE HIGH-ASSURANCE LIFECYCLE TRUTH TABLE          │
├───────────┬────────────┬──────────────┬────────────────┬───────────────┤
│ OUTCOME   │ SETTLEMENT │ RUNTIME      │ AUTHORITY      │ STATUS        │
├───────────┼────────────┼──────────────┼────────────────┼───────────────┤
│ PENDING   │ LIVE       │ INITIALIZING │ RESERVED       │ Admitted.     │
├───────────┼────────────┼──────────────┼────────────────┼───────────────┤
│ PENDING   │ LIVE       │ RUNNING      │ ACTIVE         │ Executing.    │
├───────────┼────────────┼──────────────┼────────────────┼───────────────┤
│ ABORTED   │ LIVE       │ DRAINING     │ SUSPENDED      │ Draining.     │
├───────────┼────────────┼──────────────┼────────────────┼───────────────┤
│ ABORTED   │ SETTLED    │ STOPPED      │ RELEASED       │ Safe restart. │
├───────────┼────────────┼──────────────┼────────────────┼───────────────┤
│ FAILURE   │ SETTLED    │ STOPPED      │ RELEASED       │ Clean fail.   │
├───────────┼────────────┼──────────────┼────────────────┼───────────────┤
│ SUCCESS   │ SETTLED    │ STOPPED      │ RELEASED       │ Clean pass.   │
├───────────┼────────────┼──────────────┼────────────────┼───────────────┤
│ FAILURE   │ LIVE       │ ERROR        │ RETAINED_FENCE │ VALID SAFETY: │
│           │            │              │                │ Mutator live, │
│           │            │              │                │ authority held│
├───────────┼────────────┼──────────────┼────────────────┼───────────────┤
│ FAILURE   │ LIVE       │ ERROR        │ RELEASED       │ UNSAFE HAZARD:│
│           │            │              │                │ Authority free│
│           │            │              │                │ while mutator │
│           │            │              │                │ is still live!│
└───────────┴────────────┴──────────────┴────────────────┴───────────────┘
```

Notice the critical distinction in the final two rows:
- **`FAILURE + LIVE + ERROR + RETAINED_FENCE` IS A VALID SAFETY STATE:** If an operation experiences an internal failure or timeout while its mutator is still alive (or settlement is unconfirmed), retaining or fencing authority is **the safe, correct action**. Releasing authority while the mutator remains live is the actual hazard!
- **`FAILURE + LIVE + ERROR + RELEASED` IS THE HAZARD:** Releasing authority while a failed mutator is still executing opens the system to ghost writes and concurrent resource corruption.

```text
EPISTEMIC LAW:
FAILURE + LIVE  !=  ILLEGAL
FAILURE + LIVE + AUTHORITY_RELEASED  =  UNSAFE
FAILURE + LIVE + AUTHORITY_RETAINED_OR_FENCED  =  VALID SAFETY STATE UNTIL SETTLEMENT
```

---

## 5. Present != Valid

A related failure mode in cognitive reasoning is confusing **Physical Existence** with **Semantic Validity**.

```text
PRESENT     !=  VALID
REGISTERED  !=  EXECUTABLE
TESTED      !=  AUTHORIZED
```

### The Existence Fallacy
When an unguided model writes validation logic, it frequently writes presence checks:
```typescript
if (config.apiKey && config.endpoint) {
  // Model assumes: Configuration is completely valid!
  proceedWithDeployment();
}
```

This is the **Existence Fallacy**.
- An API key may be present, but revoked.
- An endpoint may be configured, but unreachable or pointing to a deprecated staging server.
- A lease token may exist in memory, but have expired three seconds ago.
- A test file may exist in `tests/`, but test an obsolete, bypassed prototype harness.

### Grounding in Orion Architecture
In Orion's provider and capability registration layers:
- **`PRESENT != VALID`:** An encryption key file may exist on disk with 256 bytes (`PRESENT`), but have corrupted checksums or invalid padding (`INVALID`).
- **`REGISTERED != EXECUTABLE`:** A tool or provider may be registered in the capability catalog (`core/skills/primitive-skill-registry.ts`), but its local binary dependencies may not exist on the host OS path. (This is why `ExecutableProber` mechanically verifies OS executables rather than trusting registry entries).
- **`TESTED != AUTHORIZED`:** A patch may have passing unit tests in a developer sandbox, but lack the operator-issued authority grant required to touch protected composition root files. (Today such grants are registry-issued, time-bounded capabilities; signed grants are a target mechanism.)

Never write a prompt or contract that treats existence as evidence of validity. **Validity must be verified through semantic evaluation and mechanical evidence, not null checks.**

---

## 6. Control Signals Require Control Identity

Now we arrive at one of the most critical security and stability lessons discovered during Orion's R4 convergence audits: **Control Identity**.

```text
LAW:
APPLICATION_DATA  MUST_NOT  MASQUERADE_AS  CONTROL_STATE.
```

### The Dangerous Anti-Pattern: Magic String Control
Consider a standard task supervisor designed to enforce execution timeouts:
```typescript
// THE DANGEROUS IMPLEMENTATION:
try {
  await runUserSuppliedTask(task);
} catch (err: any) {
  if (err.message === "TIMED_OUT") {
    // Orchestrator assumes: The system timer expired!
    triggerSystemTimeoutPolicy();
  } else {
    triggerStandardErrorPolicy();
  }
}
```

Do you see the critical vulnerability?
What happens if the user-supplied task executes application code that deliberately or accidentally throws an error with that exact message?

```typescript
// Inside a user-authored tool or untrusted script:
throw new Error("TIMED_OUT");
```

The application error bubbles up. The orchestrator inspects `err.message`, sees `"TIMED_OUT"`, and concludes: *"Our internal system timer expired! We must abort the entire pipeline and invalidate the lease."*

The application data has successfully **impersonated control-plane state**. An untrusted application script has usurped the authority of the system clock!

### Why Magic Strings Are an Anti-Pattern (`TOPIC-ANTI-08`)
Magic strings (`"TIMED_OUT"`, `"CANCELLED"`, `"LEASE_EXPIRED"`, `"AUTHORIZED"`) are harmless when used as human-readable log messages. 

They become toxic when **identity-sensitive control decisions infer authority solely from string equality**.

```text
MAGIC STRING TRAP:
String Equality ("TIMED_OUT" === "TIMED_OUT")
shows ONLY that two byte sequences match.
It says NOTHING about WHO emitted the signal!
```

---

## 7. The Tagged Race Pattern: Enforcing Control Identity

How do we prevent application data from impersonating control signals?

We enforce **Control Identity**. Control signals must carry structural evidence of their origin that application data cannot produce.

In JavaScript and TypeScript runtimes, Orion achieves this through the **Tagged Race Pattern**:

```typescript
// THE ORION TAGGED RACE PATTERN (CONCEPTUAL FORM)
type ExecutionResult<T> = 
  | { kind: "SETTLED"; value: T }
  | { kind: "FAILED"; error: unknown };

type TimerSignal = { readonly kind: "CONTROL_TIMEOUT"; timerId: symbol };

const timerSignal: TimerSignal = {
  kind: "CONTROL_TIMEOUT",
  timerId: Symbol("ORION_CONTROL_TIMER")
};

// Race the application promise against the trusted control timer
let timerHandle: ReturnType<typeof setTimeout> | undefined;
const raceOutcome = await Promise.race([
  // Branch A: The Application Execution Branch
  taskPromise.then(
    (value): ExecutionResult<T> => ({ kind: "SETTLED", value }),
    (error): ExecutionResult<T> => ({ kind: "FAILED", error })
  ),

  // Branch B: The Trusted Control Timer Branch
  new Promise<TimerSignal>((resolve) => {
    timerHandle = setTimeout(() => resolve(timerSignal), timeoutMs);
  })
]).finally(() => clearTimeout(timerHandle)); // do not leak the timer

// Mechanical Verification of Origin:
if (raceOutcome.kind === "CONTROL_TIMEOUT") {
  // ESTABLISHED: This signal originated ONLY from the trusted timer closure.
  // No error thrown by taskPromise could ever emit this branch.
  // Classification is not settlement: the task may still be running (Section 8).
  handleSystemTimeout();
} else if (raceOutcome.kind === "FAILED") {
  // ESTABLISHED: An application-level error occurred. Even if error.message
  // happens to be "TIMED_OUT", it is classified as application failure,
  // NOT a system timer expiration.
  handleApplicationFailure(raceOutcome.error);
} else {
  handleSuccess(raceOutcome.value);
}
```

### Trusted Branch Provenance and Outer Result Wrapping
The protection of the Tagged Race comes from two mechanical properties, not magical language features:

1. **Trusted Branch Provenance:** The timeout signal is instantiated exclusively inside the timer branch callback closure. It cannot be returned or resolved by the task branch unless the task is explicitly handed the private timer capability.
2. **Outer Result Wrapping:** Branch A *always* wraps application outcomes into a typed envelope:
   - If the task resolves with `val`, Branch A emits `{ kind: "SETTLED", value: val }`.
   - If the task throws/rejects with `err`, Branch A emits `{ kind: "FAILED", error: err }`.
   Even if the untrusted application payload throws an object containing `{ kind: "CONTROL_TIMEOUT" }`, Branch A captures it inside `{ kind: "FAILED", error: { kind: "CONTROL_TIMEOUT" } }`. 

```text
APPLICATION_DATA_CANNOT_ESCAPE_ITS_WRAPPER
WITHIN_THIS_DEFINED_BOUNDARY.
```

A JavaScript `Symbol` or unique object reference can strengthen local identity within a single process memory space, but:
```text
Symbol(...)  !=  GENERAL_AUTHENTICATION_PRIMITIVE
```
Symbols do not protect across serialization boundaries, IPC channels, or process restarts. The security derives from **provenance and structural wrapping**.

*(Note: In the Pass 1C R4 repair (in progress and uncommitted at audit time), orchestrator timeout classification was corrected so that an application promise rejecting with an error labeled "TIMED_OUT" is recognized as a settled failure rather than a still-live background mutator. Hardened variants add private symbols or capabilities when crossing untrusted code boundaries.)*

```text
P-GLL LAW:
CONTROL_SIGNALS_REQUIRE_TRUSTED_PROVENANCE.
NEVER_BRANCH_ON_UNTYPED_STRINGS_FOR_AUTHORITY_DECISIONS.
```

---

## 8. Authority Release as a Proof Obligation

In naive systems, releasing authority (such as unlocking a file, releasing a distributed mutex, or relinquishing a database lease) is treated as a trivial cleanup step:
```typescript
try {
  await doWork();
} finally {
  releaseLock(); // DANGEROUS!
}
```

In high-assurance engineering, **Authority Release is a Proof Obligation**:

```text
LAW:
ABORT_REQUESTED  !=  TERMINATED
TIMED_OUT        !=  SAFE_TO_RELEASE_AUTHORITY
```

### The Invariant: Authority Release Is Claim-Sensitive
You may not release an exclusive writer lease or capability grant until you have **mechanically verified that no still-authorized mutator can produce protected effects**.

The specific evidence required for authority release is **claim-sensitive and subsystem-dependent**:

```text
AUTHORITY_RELEASE_EVIDENCE_DEPENDS_ON_SUBSYSTEM:
- In asynchronous Promise orchestrations: tracked promise settlement or rejection.
- In local OS child processes: OS-level process termination verification (PID dead).
- In distributed storage leases: fencing token expiration or explicit lease revocation.
- In model provider sessions: provider cancellation acknowledgement or socket close.
- In append journals: verified completion of disk sync flush barriers.
- In distributed workers: explicit job ownership transfer or fencing barrier.
```

It is not necessary for every unrelated host process or memory buffer to terminate. The invariant requires only that **no residual execution within the governed authority scope can produce persistent protected writes**.

If an operation times out, releasing authority while background writes are still in flight creates a race condition: another station acquires authority while the first station's writes are still completing. Authority must remain held or fenced until physical settlement for the authority scope is established.

---

## 9. Runtime Error vs. Authority Decision

We conclude with a vital operational distinction: **Separating Runtime Errors from Authority Decisions.**

```text
RUNTIME_ERROR       :=  A physical execution failure 
                        (e.g., connection reset, out of disk space, syntax error).

AUTHORITY_DECISION  :=  A governance determination 
                        (e.g., grant access, revoke lease, fail closed, quarantine).
```

A common bug in cognitive models is assuming that whenever a `RUNTIME_ERROR` occurs, authority is automatically revoked:

```text
[FALSE CONFLATION]
Runtime error occurs ──► System immediately marks authority = REVOKED.
```

### Why This Fails
Suppose a storage engine hits a temporary disk I/O timeout while writing a cognitive turn envelope. Releasing the writer lease immediately would let a new process write to the journal while the old one may still be flushing dirty pages, interleaving corrupted frames. Orion instead separates the axes: the **runtime state** moves to `ERROR`, and the **authority state** moves to `RETAINED_FENCE`. No new operations are scheduled, and no other station can claim the resource until the flush barrier completes or the process is hard-killed. The valid and hazardous combinations are the ones in the truth table of Section 4.

By keeping runtime errors and authority decisions on separate axes, Orion reduces a major class of lifecycle ambiguity. Concurrency races may still occur for other reasons, but the system prevents premature authority release while mutators remain live.

---

## 10. Summary

Keep outcome, settlement, runtime state and authority orthogonal; `SUCCESS != SETTLEMENT` (`LAW-CTL-01`). Settlement is scoped to the authority boundary; a failed-but-live mutator under retained or fenced authority is a valid safety state (`LAW-CTL-02`). `PRESENT != VALID` (`LAW-CTL-04`). Application data must not masquerade as control state (`LAW-CTL-03`). Releasing authority is a proof obligation: verify settlement first.


---


# Chapter 16: Evidence, Falsification, and Why Green Is Not Proven

> *"A green test proves only that your test passed under your chosen preconditions. It does not prove your system is correct."*

---

## 1. The Myth of the Green Checkmark

In standard software engineering culture, a green test suite is treated as holy writ. Continuous integration dashboards display bright green checkmarks; developers see `All 42 tests passed`, assume the work is flawless, and merge to production.

In AI-assisted engineering, this naive faith in green test suites becomes a primary vector of systemic failure.

Consider how an unguided LLM creates a passing test:
1. It writes an algorithm with an undetected edge-case bug.
2. It writes a test suite to verify the algorithm.
3. Because the model harbors the same blind spots when authoring the test as it did when authoring the code, the test exercises only the happy paths that the model already knows how to handle.
4. The test passes with a 100% success rate.
5. The model outputs: *"I have thoroughly tested this code and proven it is 100% bug-free."*

In Orion, we reject this complacency. We enforce the **Core Promotion Ladder of Verification**:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE VERIFICATION PROMOTION LADDER                    │
├──────────────────────────────┬─────────────────────────────────────────┤
│ PROMOTION STEP               │ MEANING & BOUNDARY                      │
├──────────────────────────────┼─────────────────────────────────────────┤
│ GREEN  !=  PROVEN            │ A passing test shows only that the      │
│                              │ exact assertions executed succeeded.    │
├──────────────────────────────┼─────────────────────────────────────────┤
│ TESTED  !=  VERIFIED         │ Running an ad-hoc test is not the same  │
│                              │ as evaluating a claim against a formal  │
│                              │ verification contract.                  │
├──────────────────────────────┼─────────────────────────────────────────┤
│ VERIFIED  !=  AUTHORIZED     │ An independent verification receipt is  │
│                              │ an observation; it does not grant legal │
│                              │ authority to merge or deploy.           │
├──────────────────────────────┼─────────────────────────────────────────┤
│ AUTHORIZED  !=  EXECUTED     │ Approving an architectural promotion    │
│                              │ does not mean the physical state change │
│                              │ has successfully settled on disk.       │
└──────────────────────────────┴─────────────────────────────────────────┘
```

Testing is not an exercise in confirmation; **testing is an adversarial search for falsification**. 

---

## 2. Claim-First Verification: Beginning with Falsification

When a verification station or human operator evaluates a proposed code change, they must not begin by asking: *"What tests can I run to see if this works?"*

That question invites confirmation bias.

Instead, Orion enforces **Claim-First Verification**:

```text
1. WHAT EXACTLY IS THE CLAIM?
2. WHAT OBSERVATION WOULD FALSIFY IT?
3. WHAT MECHANICAL TEST CAN FORCE THAT OBSERVATION?
```

```text
CLAIM
  │
  ▼
FALSIFIER (Hypothesis of failure)
  │
  ▼
MECHANICAL TEST (Adversarial stimulus)
  │
  ▼
EVIDENCE (Observed outputs and receipts)
  │
  ▼
SCOPED VERDICT (PASS / FAIL / NOT_DETERMINABLE)
```

### The Structure of an Exact Claim
A claim must never be vague or sweeping.
- **Weak Claim:** *"The database is now reliable."*
- **Exact Claim:** *"Under an unexpected OS termination (`SIGKILL`) during an active append transaction, the journal scanner rehydrates the last valid frame offset, quarantines any trailing partial frame, and rejects subsequent out-of-order sequence appends."*

Notice the precision:
- The exact operational condition is specified (`SIGKILL` during active append).
- The exact survival boundary is defined (rehydrate last valid offset).
- The exact failure condition that would falsify the claim is obvious (if the scanner crashes on partial headers, or if out-of-order frames are accepted, the claim is instantly falsified).

Once the claim is framed, the verification station's entire duty is to **attempt to break it**. If the station tries aggressively to falsify the claim and fails, our confidence in the system increases.

---

## 3. Reproducing the Old Defect

When repairing a previously identified defect (such as the defect classes examined in Chapter 14), what constitutes sufficient evidence of repair?

In naive engineering, an implementer writes a new happy-path test:
```typescript
// WEAK REPAIR TEST:
test("task runs to completion", async () => {
  const result = await supervisor.runTask(validTask);
  expect(result.status).toBe("SUCCESS");
});
```

This test establishes nothing about the defect. The system may pass it while remaining completely vulnerable to the original failure.

When historical replay is feasible, a strong repair verification should **replay the original failure stimulus**. When exact replay is impossible, unsafe, stochastic, or unavailable, use the strongest claim-relevant falsifier available and explicitly bound the resulting verdict:

```text
LEVEL 1 (WEAK):
  The new happy path passes.

LEVEL 2 (STRONG):
  Historical replay when feasible, or the strongest equivalent falsifier/evidence 
  when exact replay is impossible, unsafe, stochastic, or unavailable (with the 
  resulting verdict explicitly bounded).

LEVEL 3 (STRONGEST — ADVERSARIAL SIBLING ATTACK):
  Adversarial variants and corrupted inputs representing the broader 
  defect class are thrown at the component, and all fail closed.
```

### Case Study: What Design Review Can and Cannot Show
The M5 R2 V1.5 certification (the sourced account is in Chapter 3 §4, `LIVE_ALPHA_M5_R2_DESIGN_V1_5_FINAL_CERTIFICATION_RECEIPT.md`) was a read-only design review. The certifier read the design line by line and re-ran the R1 regression suite, `tsc --noEmit` and the build, with `IMPLEMENTATION_AUTHORIZED := FALSE`. It falsified a *design* claim about restart recovery. It did not inject bytes into a journal or spawn a child process, because there was no implementation under review yet.

Live-process evidence belongs to later stations: the W3 independent verification re-ran the restart-reconstruction suites fresh (`LIVE_ALPHA_M5_R2_W3_INDEPENDENT_FREEZE_CERTIFICATE.md`), and the H0 verification described in Section 10 restarted real processes. The distinction is the point. A design review can show that a design is internally coherent; a claim that running code recovers from a crash needs live-process tests.

---

## 4. Fixture Masking: When Tests Lie

One of the most dangerous illusions in modern software engineering is **Fixture Masking**.

```text
FIXTURE MASKING:
  When a test passes because the test harness, mock, or fixture 
  artificially bypasses the physical failure mechanism present in production.
```

```text
[PRODUCTION EXECUTION PATH]
User Request ──► Network Ingress ──► Auth Seam ──► Runtime Engine ──► Disk I/O
                         ▲
                         │ (Real failure occurs here: auth token malformed)

[MASKED TEST EXECUTION PATH]
Test Harness ────────────────────────────────────► Runtime Engine (Mocked Disk)
  (Bypasses Ingress and Auth Seam entirely! Test passes 100% green!)
```

### The Common Vectors of Fixture Masking
1. **Mocking the Real Owner:** A test mocks out the `DatabaseAdapter` with an in-memory dictionary. The in-memory dictionary does not enforce foreign keys, write serialization, or connection pool timeouts. The test passes; production deadlocks under real concurrency.
2. **Injecting Already-Correct State:** A test directly injects a pre-validated, pre-sanitized configuration object into a constructor, bypassing the JSON parsing and environment variable resolution where real production errors happen.
3. **Synthetic Construction Paths:** The test instantiates a class using internal helper methods (`createTestInstance()`) that initialize dependencies in an order different from the real composition root (`api/server.ts`).
4. **Stubbing the Authority Seam:** A test stubs out the authorization check with `() => true`. The test shows that the business logic works, but masks the fact that the production caller lacks the security grant required to invoke it.

### The Litmus Test for Honest Testing
Whenever you audit a test suite, apply the **Four-Part Reality Check**:
```text
DID THE TEST TOUCH:
1. THE REAL OWNER (not an unverified mock)?
2. THROUGH THE REAL PATH (traversing real ingress boundaries)?
3. UNDER THE REAL PRECONDITIONS (with genuine uninitialized state)?
4. WITH REAL PHYSICAL EFFECTS (testing real files or child processes)?
```

### Proportionality Notice
This does not mean every unit test must spin up a multi-node cluster. Fast, isolated unit tests with mock interfaces are valuable for algorithmic validation.

However, **a unit test with mocked I/O cannot verify an integration or durability claim**. If your claim asserts that data survives an OS process crash, your test must spawn and kill real OS processes.

---

## 5. Test Diversity: The Triangulation of Evidence

Evidence derives its strength not from running the same test a thousand times, but from **triangulating truth across diverse, complementary testing methodologies**.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        THE SPECTRUM OF TEST DIVERSITY                  │
├─────────────────────┬──────────────────┬───────────────────────────────┤
│ TEST FORM           │ WHAT IT ATTACKS  │ ORION APPLICATION             │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ UNIT TESTS          │ Pure algorithmic │ Abstract state machine rules, │
│                     │ transformation   │ hash computations, schemas.   │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ INTEGRATION TESTS   │ Seams between    │ Composition root wiring,      │
│                     │ truthful owners  │ service-to-service contracts. │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ ADVERSARIAL TESTS   │ Invariant limits │ Malformed JSON, corrupted     │
│                     │ and boundary edge│ byte offsets, illegal frames. │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ LIVE PROCESS TESTS  │ OS reality and   │ Spawning real Node child      │
│                     │ physical hosting │ processes, testing SIGKILL.   │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ FILESYSTEM PROBES   │ Physical storage │ Probing real disk writes,     │
│                     │ and sync barriers│ verifying flush durability.   │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ INDEPENDENT AUDIT   │ Human / model    │ Cross-model verification      │
│                     │ cognitive bias   │ (one family audits another).  │
└─────────────────────┴──────────────────┴───────────────────────────────┘
```

A high-assurance milestone in Orion (such as an Alpha freeze certificate) is never granted based solely on unit tests. It requires evidence drawn from across the spectrum.

---

## 6. Counts vs. Identities: Why Numbers Conceal Regressions

Here we arrive at a critical practical lesson in test reporting: **`TOPIC-ANTI-07`: Test Counts Without Identities**.

Imagine the following scenario during a major code migration:
- **Baseline Run:** `Tests: 384 passed, 22 failed.`
- The implementer refactors three core services.
- **New Run:** `Tests: 384 passed, 22 failed.`

The implementer reports to the operator: *"No regressions introduced! We still have exactly 22 failing tests, matching our baseline."*

Is the no-regression claim established?
**No. Equal aggregate counts are insufficient.**

The two failure sets can differ even when the counts match: the refactoring may have fixed two baseline failures while introducing two new ones, leaving the total at 22 and concealing a regression.

```text
LAW:
COUNTS_ARE_SUPPORTING_EVIDENCE
NOT_IDENTITY_EVIDENCE

NO_NEW_REGRESSION_CLAIMS
SHOULD_COMPARE_FAILURE_IDENTITIES
WHEN_STABLE_IDENTITIES_EXIST

COUNTS_DO_NOT_SUBSTITUTE_FOR_IDENTITIES
```

### The Complementary Role of Counts and Identities
Counts are a valuable aggregate signal. Receipts should always record total, passing, and failing test counts to provide high-level sanity checks and identify massive pipeline drops.

However, counts alone cannot substantiate a claim of "no new regressions." Where stable, fully qualified test identities exist, high-assurance regression checks compute set differences over identities:

```text
FAILURE_SET_BASELINE  := { suite_id::test_name }
FAILURE_SET_CANDIDATE := { suite_id::test_name }

NEW_FAILURES := FAILURE_SET_CANDIDATE  \  FAILURE_SET_BASELINE
RESOLVED     := FAILURE_SET_BASELINE   \  FAILURE_SET_CANDIDATE
PERSISTENT   := FAILURE_SET_BASELINE   ∩  FAILURE_SET_CANDIDATE
```

### New Failure Identity = Regression Candidate
If `NEW_FAILURES` is non-empty, the system has discovered **Regression Candidates**, not necessarily an automatic defect:

```text
NEW_FAILURE_IDENTITY  =  REGRESSION_CANDIDATE
NEW_FAILURES  MUST_BE_EXPLAINED
```

A new failure identity may arise from:
1. **Newly Added Test Coverage:** A new test introduced in the candidate is exercising an edge case that previously had zero coverage.
2. **Intentional Behavior Change:** An approved feature or contract redesign intentionally altered an interface or output format.
3. **Renamed or Reorganized Tests:** A test was moved or renamed, causing the old identity to vanish and a new identity to appear.
4. **Environmental Differences:** Missing host dependencies, platform socket differences, or differing file-path separators.
5. **Flakiness:** An unstable test failing intermittently due to timing or race conditions.
6. **Actual Regression:** An unintended code breakage introduced by the repair.

Therefore, new failure identities must be **classified and explained** against the baseline contract, rather than reflexively declared regressions.

Furthermore, reporting `384/384 passed` without a reconstructable test inventory is **weak and incomplete evidence**. It supports the narrow claim that the runner reported 384 passes, but does not adequately substantiate that the intended test inventory executed. If a test file was renamed, skipped, or omitted from the test runner's glob pattern, the count may drop without triggering a failure.

---

## 7. Reconstructable Evidence

What separates an informal conversational claim from durable engineering evidence?

The answer is **Reconstructability**:

```text
RECONSTRUCTABLE_EVIDENCE:
  An evidentiary record containing sufficient operational metadata 
  that an independent auditor can reconstruct an equivalent verification 
  pass under the materially relevant declared environment.
```

### The Required Evidence Metadata: Claim-Sensitive
Every durable test receipt in Orion captures operational metadata relevant to the claim being evaluated. The minimum required fields depend on the claim; irrelevant machine trivia can and should be omitted:

```text
# ILLUSTRATIVE_EXAMPLE (invented identifiers)
EVIDENCE_BLOCK:
  command: "npm test -- tests/unified-mind-slice-a-contracts.test.ts"
  working_directory: "C:/orion-next"
  baseline_commit: "<commit-sha>"
  environment_snapshot:
    node_version: "v20.18.0"
    os_platform: "win32"
    runtime_flags: "--no-warnings"
  execution_metrics:
    exit_code: 0
    duration_ms: 4120
    test_count_total: 38
    test_count_passed: 38
    test_count_failed: 0
  failure_identities: []
  output_artifact_references:
    - "reports/runtime/slice-a-test.log"
    - "reports/runtime/slice-a-receipt.jsonl"
```

Notice what is captured: the command, working directory, baseline, relevant environment, exit code, aggregate counts, failure identities, and artifact references. The required fields scale with the assurance level of the claim.

---

## 8. Receipt vs. Evidence

In Chapter 9, we introduced the concept of the durable receipt. Now, in the context of verification, we must establish the precise relationship between **Receipts**, **Evidence**, **Verification** and **Certification**:

```text
RECEIPT       :=  A durable structured record capturing claims, metadata, 
                  provenance, and artifact references at an exact point in time.

EVIDENCE      :=  The concrete physical artifacts (logs, process outputs, 
                  hash diffs, exit codes) supporting an observation.

VERIFICATION  :=  The evaluation process that compares an exact claim 
                  against mechanical evidence within a declared boundary.

CERTIFICATION :=  A formal assessment by an independent station, verifying that a
                  candidate satisfies an explicit contract (it does not confer adoption).
```

### Receipts Are Not Automatically Immutable
Earlier in this volume, we established that a receipt is not magically immutable merely because it is called a "receipt."

```text
IMMUTABILITY  REQUIRES  AN IMMUTABILITY MECHANISM.
```

Three properties are easily conflated (Chapter 9 §7):
- **Tamper-evidence** comes from digests, signatures or hash chains.
- **Immutability** comes from enforced write-once or append-only storage and permissions.
- **Durability** comes from sync barriers.

```text
CRITICAL DISTINCTION:
RECEIPT  !=  PROOF
RECEIPT  :=  DURABLE_RECORD_OF_AN_OBSERVATION
```

A receipt does not certify its own truth. If a receipt claims: *"All 386 tests passed"*, the receipt is not self-authenticating proof that the tests passed. The receipt is a structured statement that an observer executed a command and observed that outcome. 

An independent verifier validates the claim by **re-executing the command or verifying the evidence digests** linked in the receipt.

---

## 9. The Four-Part Verification Lens: Claim, Evidence, Scope, Freshness

Whenever you evaluate any engineering proposal or receipt, examine it through the **Four-Part Verification Lens**:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE FOUR-PART VERIFICATION LENS                      │
├──────────────────────────────┬─────────────────────────────────────────┤
│ DIMENSION                    │ CORE QUESTION                           │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 1. CLAIM                     │ What exact functional or invariant      │
│                              │ property is being asserted?             │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 2. EVIDENCE                  │ What mechanical output (hashes, logs,   │
│                              │ PIDs) supports that assertion?          │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 3. SCOPE                     │ Within what exact boundary (files,      │
│                              │ services, test suite) does this hold?   │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 4. FRESHNESS                 │ Does this evidence apply to the CURRENT │
│                              │ baseline, or has source mutated since?  │
└──────────────────────────────┴─────────────────────────────────────────┘
```

### Truth Status vs. Freshness Status
Notice the separation between **Truth** and **Freshness**:

```text
TRUTH_STATUS:      [PASS, FAIL, NOT_DETERMINABLE]
FRESHNESS_STATUS:  [FRESH, STALE]
```

A verification receipt may have:
```text
TRUTH_STATUS:      PASS
FRESHNESS_STATUS:  STALE
```

This is not a contradiction! It means:
*"This claim was verified within its declared scope against commit `a1b2c3`. However, three files within that scope have since been modified. The evidence is now stale. The claim is not known to be false, but it requires re-verification before adoption."*

```text
LAW:
STALE  !=  FALSE
STALE  :=  REQUIRES_REVERIFICATION_AGAINST_CURRENT_BASELINE
```

### Mutation Invalidates Evidence Where Relevant
Whenever code within a verified boundary undergoes mutation, all prior evidence touching that boundary transitions from `FRESH` to `STALE`:

```text
EVIDENCE_AFTER_RELEVANT_MUTATION  ──►  REVERIFY
```

Notice the word **Relevant**. If an engineer updates a markdown documentation file in `docs/P-GLL/`, this does not invalidate the OS process restart evidence in `scripts/h0-live-os-process-proof.ts`. Freshness tracking must be **claim-sensitive and boundary-aware**.

---

## 10. Independence: Why Implementers Cannot Self-Certify

We conclude this chapter with a fundamental law of cognitive governance: **The Law of Verification Independence**.

```text
IMPLEMENTERS MAY SELF-TEST.
IMPLEMENTERS MAY NOT SELF-CERTIFY.
```

### Why Implementers Suffer from Momentum Bias
When a human engineer or an AI model spends three hours writing a complex patch, it develops **Implementation Momentum**:
- It wants the code to work.
- It subconsciously avoids running the specific test input that might destroy its elegant design.
- It interprets ambiguous warning messages charitably: *"Oh, that timeout warning is probably just an artifact of my local machine."*

An independent station has zero implementation momentum:
- It does not care how long the implementer spent writing the patch.
- It does not care how beautiful the code looks.
- Its sole mandate is to verify claims against evidence and attempt to falsify them.

### Different Model Name != Independent Evidence
A dangerous trend in LLM agent pipelines is asking Model A to write code, and then prompting Model B: *"Model A wrote this code. Do you agree it looks good?"*

Model B reads Model A's explanation, nods along, and replies: *"Yes, Model A's architecture is excellent and I see no flaws."*

This is **Synchronized Hallucination**, not independent verification!

```text
DIFFERENT_MODEL_NAME  !=  INDEPENDENT_EVIDENCE

INDEPENDENCE REQUIRES:
1. Re-executing tests from scratch on a clean baseline.
2. Independently deriving assertions from the specification.
3. Checking actual file diffs, not trusting the author's summary.
4. Attempting adversarial falsification.
```

In the H0 independent verification receipt (`LIVE_ALPHA_H0_INDEPENDENT_VERIFICATION_RECEIPT.md`), the independent Claude verifier did not read Gemini's report and say "looks good." 
The verifier:
1. Refused to trust Gemini's summary text.
2. Read the raw diff of `api/server.ts`.
3. Backed up the original journal logs.
4. Re-ran the live child-process run with fresh PIDs (`43228/44164`).
5. Falsified Gemini's Claim D ("removed duplicate partial route mount"), catching an overclaim in the receipt.

That is genuine verification.

---

## 11. Anti-Pattern: Vague "Review This" Prompts

`TOPIC-ANTI-05`: *"Please review this file and tell me what you think"* specifies no claim, no invariant and no falsification target, and invites aesthetic commentary, style nitpicks or sycophantic praise (Chapter 3 §1). Compile a bounded **Adversarial Falsification Contract** instead:

```text
ADVERSARIAL_CHALLENGE_PROMPT:
  role: "INDEPENDENT_FALSIFIER"
  subject: "core/runtime/mind-runtime.ts (lines 120-185)"
  claim: "initializeFromJournal() will fail closed without mounting routes
          if the journal file contains an unclosed JSON frame."
  instructions:
    1. Do not praise the code or suggest stylistic cleanups.
    2. Identify the exact execution path where an unclosed JSON frame is parsed.
    3. Construct a mechanical test fixture that feeds an unclosed frame.
    4. Determine whether the runtime throws, silently skips the line, or fails closed.
    5. Report verdict as: FALSIFIED (with failure trace) or HARDENED (with evidence).
```

When you prompt for falsification, you get engineering evidence. When you prompt for review, you get polite conversation.

---

## 12. Summary

Green is not proven (`LAW-EVD-01`). Start from the falsifier, not the test. Replay the old stimulus when feasible, otherwise bound your verdict. Test the real owner through the real path. Compare failure identities, not counts (`LAW-EVD-02`, `LAW-EVD-03`). Truth status is orthogonal to freshness status (`LAW-EVD-05`). Independence requires mechanical re-derivation, not a different model name.

*(The diagnostic matrix of anti-patterns is [Appendix G](#appendix-g-prompt-anti-patterns-catalog); the pre-flight checklist is [Appendix H](#appendix-h-operator-checklist-before-you-send-a-serious-prompt).)*


---


# Chapter 17: Repair, Clean Reconstruction, Certification, and Adoption

> *"A dirty proposal that passes all tests is not a certification candidate. A certified candidate is not an adopted baseline. Never confuse fixing code with establishing adopted production reality."*

---

## 1. The Four Distinct Stations of Promotion

In small, individual programming projects, changing software is often treated as a single, continuous act: you edit a file, run the compiler, commit to Git, and push to production.

In high-assurance engineering, conflating these phases is the single most common cause of repository corruption.

When an AI agent or human team undertakes an extensive refactoring or defect repair campaign, they must navigate four distinct promotion stations. These are the late stations of the seven-seat line in [Chapter 7](#chapter-7-the-multi-model-assembly-line); the earlier seats (Mapper, Architect, Implementer, Falsifier) produce and test the proposal. Each seat's ceiling is stated on three axes in [Appendix C §1](#appendix-c-reference-station-templates).

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE FOUR PROMOTION STATIONS                          │
├─────────────────────┬──────────────────┬───────────────────────────────┤
│ STATION             │ PRIMARY MISSION  │ CEILING (verdict / promotion) │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ 1. REPAIR           │ Make the proposed│ REPAIR_SELF_CHECK_PASSED /    │
│                     │ code correct.    │ READY_FOR_INDEPENDENT_REAUDIT │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ 2. RECONSTRUCTION   │ Isolate the clean│ CLEAN_RECONSTRUCTION_         │
│                     │ finite delta.    │ ESTABLISHED / READY_FOR_      │
│                     │                  │ INDEPENDENT_CERTIFICATION     │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ 3. CERTIFICATION    │ Independently    │ CERTIFIED_WITHIN_DECLARED_    │
│                     │ audit contract.  │ SCOPE / READY_FOR_GOVERNED_   │
│                     │                  │ ADOPTION_DECISION             │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ 4. ADOPTION         │ Promote to the   │ ADOPTED (a governance act,    │
│                     │ baseline.        │ not a station verdict).       │
└─────────────────────┴──────────────────┴───────────────────────────────┘
```

```text
LAW:
REPAIR  !=  RECONSTRUCTION  !=  CERTIFICATION  !=  ADOPTION
```

Each station has its own authority boundary, its own operational invariants, and its own definition of done. Conflating any two of these stations introduces critical vulnerabilities into the software supply chain.

---

## 2. Promotion Station 1: Repair (Making the Proposal Correct)

The **Repair Station** is where engineering changes are born.

An Implementer station takes a defect packet or feature specification, enters a working tree or sandbox, and writes code.

During an active repair campaign—such as resolving a concurrency race condition or converging two divergent service registries—the working tree frequently becomes **dirty**:
- Scratch scripts are written to inspect internal state (`scripts/probe-ports.ts`).
- Temporary test fixtures and mock journals are generated.
- Debug log statements are inserted and commented out.
- Experimental configuration files and build artifacts accumulate.
- Exploratory edits may touch adjacent files.

While a repair sandbox may become dirty during exploratory iteration, unattributed mutations remain contamination and should be minimized:

```text
DIRTY_CAN_BE_EXPECTED
UNATTRIBUTED_DIRTY_IS_NOT_DESIRED
```

The mission of the Repair Station is:
```text
MISSION(REPAIR):
  MAKE THE PROPOSAL ARCHITECTURALLY AND FUNCTIONALLY CORRECT.
```

### The Terminal Authority Boundary of Repair
Here is the iron rule of the Repair Station:
```text
AN IMPLEMENTER CAN NEVER CERTIFY ITS OWN WORK.
MAXIMUM IMPLEMENTER/REPAIR PROMOTION_STATE := READY_FOR_INDEPENDENT_REAUDIT.
IMPLEMENTER AND REPAIR MAY NEVER ISSUE A CERTIFICATION VERDICT.
```

When all tests pass in the dirty working tree, the implementer does **not** declare: *"The candidate is certified and ready to merge."* 

The implementer declares: *"The proposed changes are functionally verified in my dirty sandbox and ready for clean reconstruction and independent re-audit."*

---

## 3. Promotion Station 2: Clean Reconstruction (The Finite Intended Delta)

Now we arrive at the station that naive development pipelines completely omit: **Clean Reconstruction**.

```text
LAW:
DIRTY_VERIFIED_PROPOSAL  !=  CLEAN_CERTIFICATION_CANDIDATE
```

Why can't we simply take the dirty sandbox, run `git add .`, and hand it to a certifier?

Because a dirty working tree contains **Epistemic Pollution**:
1. **Accidental Artifacts:** Temporary logs, compiled `.js` caches, and scratch files that were never intended to become part of the production codebase.
2. **Hidden Preconditions:** The tests in the dirty tree might be passing only because an untracked temporary file exists in `./data/`, or because an ambient environment variable was set in that specific shell session.
3. **Mixed-Wave Drift:** Edits to files that belong to a future development sprint or an earlier experimental pass may be mixed into the working tree.

### The Question of Reconstruction
The Reconstruction Station asks a precise question:
> *"Starting from a clean checkout of the declared baseline commit, what is the smallest coherent attributed delta of file mutations that represents the intended architectural change?"*

Notice the phrasing: **smallest coherent attributed delta**. A mathematically minimal byte edit is not always the most truthful architecture. The delta must be coherent, complete, and fully attributed to the declared contract.

```text
[DIRTY WORKSPACE]
- 19 modified source files (intended)
- 4 scratch scripts (unintended)
- 2 temporary log files (unintended)
- 1 unrelated config tweak (unintended)

          │
          ▼ CLEAN RECONSTRUCTION PASS
          │ (Explicit Manifest Filtering & Attribution)

[CLEAN CERTIFICATION CANDIDATE]
- Exactly 19 modified source files.
- Zero untracked files.
- Zero scratch scripts.
- Verified against pristine baseline.
```

---

## 4. Attribution and the Finite Attributed File Set

To perform clean reconstruction, Orion requires a **Finite Attributed File Set**.

Every single file included in the clean candidate must have an explicit ledger entry accounting for its presence, its origin, and its necessity:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   FINITE ATTRIBUTED FILE SET SCHEMA                    │
├───────────────────┬────────────────────────────────────────────────────┤
│ ATTRIBUTE         │ ENGINEERING MEANING                                │
├───────────────────┼────────────────────────────────────────────────────┤
│ PATH              │ Normalized repository path relative to root.       │
│ CATEGORY          │ MUST_CHANGE (Source) | TEST_CHANGE (Verification)  │
│ ACTION            │ MODIFIED | ADDED | DELETED                         │
│ BASELINE_DIGEST   │ SHA-256 content hash at the pristine baseline.     │
│ CANDIDATE_DIGEST  │ SHA-256 content hash of the proposed new bytes.    │
│ JUSTIFICATION     │ Exact defect or invariant requiring this change.   │
│ RIGHTFUL_OWNER    │ Subsystem owner ratifying the inclusion.           │
└───────────────────┴────────────────────────────────────────────────────┘
```

```text
LAW:
DIRTY  !=  INTENDED
```

If a file cannot provide an attributed justification tied to the mission contract, it is rejected from the reconstruction manifest. It does not matter that the file exists in the dirty sandbox; if it is not in the declared manifest, it is left behind.

---

## 5. Payload vs. Control Evidence

Clean-reconstruction work such as Pass 1C's (`CANONICAL_RUNTIME_CONVERGENCE_PASS_1C_PLAN.md`) motivates a distinction. It is book doctrine, not a quoted Pass 1C law:

```text
PAYLOAD_IDENTITY  !=  EVIDENCE_ABOUT_PAYLOAD_IDENTITY
```

Consider what occurs when a reconstruction pipeline runs:
- The pipeline copies the clean source files into a candidate workspace.
- The pipeline executes test suites, audit linters, and verification scripts.
- These tools produce verification logs, audit summaries, and receipt markdown files.

A naive pipeline might bundle the verification logs and receipts directly into the candidate payload folder.

### Subject Contamination vs. Self-Referential Roots
When managing evidence during reconstruction, we must distinguish between two separate hazards:

```text
HAZARD A: SUBJECT CONTAMINATION
  Certification or test actions mutate files inside the candidate subject 
  after its identity was frozen, invalidating prior hashes.

HAZARD B: SELF-REFERENTIAL ROOT
  A manifest or receipt attempts to record a cryptographic digest that 
  directly includes the manifest's or receipt's own bytes.
```

Evidence MAY physically coexist in a broader repository or workspace directory provided:
1. The implementation payload boundary explicitly excludes evidence directories.
2. Hash roots are defined non-self-referentially (e.g. hashing the payload directory, not the outer enclosing workspace).
3. The certification subject identity is explicit.

For example, a certification contract can establish the subject identity via the **Payload Root Hash** combined with **Control Artifact Hashes**, while evidence logs and test recordings are written out-of-band:

```text
LAW:
EVIDENCE_MUST_NOT_MUTATE_THE_FROZEN_SUBJECT_IT_IS_CLAIMED_TO_VERIFY.
```

### The Multi-Layer Separation of Concerns
To enforce this separation, Orion defines five structural layers:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE FIVE LAYERS OF RECONSTRUCTION                    │
├─────────────────────┬──────────────────────────────────────────────────┤
│ LAYER               │ CONTENTS & ROLE                                  │
├─────────────────────┼──────────────────────────────────────────────────┤
│ 1. IMPLEMENTATION   │ Pure source and test files that execute in       │
│    PAYLOAD          │ production. (Forms the byte root.)               │
├─────────────────────┼──────────────────────────────────────────────────┤
│ 2. RECONSTRUCTION   │ Manifest allowlist, copy scripts, and audit      │
│    CONTROL          │ tools used to assemble the payload.              │
├─────────────────────┼──────────────────────────────────────────────────┤
│ 3. CERTIFICATION    │ Test logs, execution receipts, and evidence      │
│    EVIDENCE         │ recordings produced by the certifier. (Sidecar). │
├─────────────────────┼──────────────────────────────────────────────────┤
│ 4. GENERATED        │ Build artifacts (e.g. `dist/**`) compiled from   │
│    OUTPUT           │ the implementation payload.                      │
├─────────────────────┼──────────────────────────────────────────────────┤
│ 5. ADOPTION         │ The exact subset of material promoted into the   │
│    SUBJECT          │ baseline commit by governance authority.         │
└─────────────────────┴──────────────────────────────────────────────────┘
```

Evidence is maintained as a **Sidecar**. It points *at* the payload's immutable digest; it is never placed *inside* the payload's byte root.

---

## 6. Byte Identity and Hierarchical Hash Roots

Once the implementation payload is assembled in a clean directory, how do we verify that its contents match the intended design?

We invoke deterministic **Byte Identity**:

```text
BYTE_IDENTITY:
  Computing cryptographic digests (SHA-256) of every file in the 
  payload and comparing them against the declared candidate hashes.
```

Building on the principles established in Chapter 13, the reconstruction engine aggregates individual file digests into a deterministic **Payload Root Hash**:

```text
LEAF HASHES (Deterministic Alphabetical Sort):
  SHA256(api/server.ts)                                 := 4f3a...
  SHA256(core/runtime/orion-composition-root.ts)        := 8b1c...
  SHA256(tests/composition-boundary-contract.test.ts)   := c9e2...
                           │
                           ▼ DETERMINISTIC CONCATENATION & HASH
  PAYLOAD_ROOT_HASH                                     := e4b7...
```

### The Epistemic Boundary of Byte Identity
As Chapter 13 §6 established:
```text
BYTE_IDENTITY := STRONG_MECHANICAL_EVIDENCE_OF_SAMENESS_UNDER_DECLARED_CANONICALIZATION
BYTE_IDENTITY != CORRECTNESS_OF_ARCHITECTURE
```
A matching digest shows that no files were lost in transit, no rogue edits were slipped in, and no blocks were corrupted, under the chosen hashing and canonicalization boundary. It does not establish that the code compiles, that the tests pass, or that the system meets requirements; that evaluation belongs to the next station: **Certification**.

---

## 7. The Clean Fixed-Point Rule: Contract-Scoped
Where the certification contract demands deterministic reconstruction, the pipeline must satisfy the **Clean Fixed-Point Rule**:

```text
THE CLEAN FIXED-POINT RULE:
  Given an identical baseline commit and an identical declared manifest, 
  running the reconstruction procedure twice from scratch 
  produces byte-identical candidate trees with zero diff.
```

```text
CLEAN BASELINE + MANIFEST ──► RECONSTRUCT PASS 1 ──► CANDIDATE TREE A (Hash X)
CLEAN BASELINE + MANIFEST ──► RECONSTRUCT PASS 2 ──► CANDIDATE TREE B (Hash Y)

FIXED-POINT ASSERTION: Hash X === Hash Y
```

```text
LAW:
FIXED_POINT_REQUIRED_WHERE
SUBJECT_IDENTITY_CONTRACT_REQUIRES_DETERMINISTIC_RECONSTRUCTION
```

If non-deterministic drift occurs (e.g. unseeded timestamps, ambient environment variables, or unordered filesystem traversals), the pipeline must eliminate or normalize that drift where deterministic reconstruction is an explicit contract requirement. Derivative outputs that are inherently non-deterministic may be excluded from the frozen subject or separately classified under policy.

---

## 8. Promotion Station 3: Certification (The Independent Adversary)

Now the clean candidate enters **Promotion Station 3: Certification**.

The Certification Station is occupied by an **Independent Certifier**—a dedicated human auditor or an independent AI model station that had zero involvement in writing the code.

```text
MISSION(CERTIFICATION):
  INDEPENDENTLY ATTACK AND VERIFY THE FROZEN CANDIDATE 
  AGAINST THE CERTIFICATION CONTRACT.
```

### What a Certifier Actually Does
A certifier does not repair code. When a certification check fails, the certifier emits an explicit finding and routes the defect packet to its **rightful owner station**:

```text
CERTIFICATION_FAIL  !=  AUTOMATIC_STATION_1_REPAIR_ROUTE

DEFECT CLASSIFICATION           ──► RIGHTFUL OWNER ROUTING:
IMPLEMENTATION_DEFECT           ──► Station 1: Repair
RECONSTRUCTION_DEFECT           ──► Station 2: Clean Reconstruction
CERTIFICATION_HARNESS_DEFECT    ──► Verification Tooling Owner
STALE_BASELINE                  ──► Baseline Re-establishment / Reconstruction
PACKAGING_POLICY_GAP            ──► Packaging / Governance Station
NOT_DETERMINABLE                ──► Targeted Probe / Evidence Acquisition
```

Routing every failure blindly back to Station 1 is an anti-pattern. If a failure occurred because the reconstruction manifest omitted a test fixture, the repair station cannot fix it—it is a Station 2 reconstruction defect. If a failure occurred because the certifier's own harness had an environment bug, that belongs to the tooling owner.

### The Certification Battery Is Contract-Calibrated
The certification battery executed by the certifier is calibrated to the assurance requirements of the contract:
1. **Subject Identity Verification:** Confirms candidate files match declared digests.
2. **Manifest Integrity:** Verifies no tracked files exist outside the declared allowlist.
3. **Pristine Build Verification:** Executes compilation in an isolated clean environment.
4. **Regression Battery:** Runs contract-specified test suites, comparing failure identities against the baseline set.
5. **Adversarial / Lifecycle Probing:** For high-assurance candidates (such as Pass 1C runtime convergence), runs process-kill tests, timeout races, and corrupt-state recovery tests.
6. **Packaging Policy Audit:** Verifies generated output compliance.

---

## 9. Subject Immutability: The Tripartite Sandbox Pattern

How does a certifier prevent its audit actions from contaminating the candidate?

In high-assurance certification, Orion employs the **Tripartite Certification Sandbox Pattern**:

```text
┌────────────────────────────────────────────────────────────────────────┐
│             TRIPARTITE CERTIFICATION SANDBOX (HIGH-ASSURANCE)          │
├─────────────────────┬──────────────────┬───────────────────────────────┤
│ COMPONENT           │ MUTABILITY       │ PURPOSE                       │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ 1. FROZEN CANDIDATE │ STRICTLY         │ Pristine, read-only subject   │
│                     │ IMMUTABLE        │ under audit.                  │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ 2. DISPOSABLE       │ READ/WRITE       │ Isolated copy where tests,    │
│    EXECUTION COPY   │ (EPHEMERAL)      │ builds, and probes run.       │
├─────────────────────┼──────────────────┼───────────────────────────────┤
│ 3. SIDECAR EVIDENCE │ APPEND-ONLY      │ Out-of-band directory where   │
│    DIRECTORY        │                  │ logs and receipts are written.│
└─────────────────────┴──────────────────┴───────────────────────────────┘
```

```text
LAW:
CERTIFICATION_SUBJECT  !=  EXECUTION_ENVIRONMENT  !=  EVIDENCE_DIRECTORY
```

This tripartite topology represents a high-assurance structural pattern rather than the only possible physical arrangement. Its fundamental invariant is **candidate immutability and evidence separation**: test execution must not mutate the frozen candidate, and recorded evidence must not alter the subject's digest.

When tests run, they execute inside the **Disposable Execution Copy**. If a test writes a temporary file or crashes a process, it affects only that disposable copy. Once testing concludes, the certifier re-computes the hash of the **Frozen Candidate** to mechanically verify that zero subject contamination occurred.

---

## 10. Active Case Study: Pass 1C Clean Certification

To ground these principles in living reality, let us examine the active engineering campaign in the Orion repository today: **Pass 1C Clean-Candidate Certification**.

### The Living Engineering Context
Pass 1C was initiated to resolve a foundational dual-runtime split: the production HTTP server in `api/server.ts` was operating on a legacy service spine, while experimental capabilities were being developed in `core/runtime/orion-fabric.ts`.

To unite these realities into a single `OrionCompositionRoot`, the engineering team planned Pass 1C (`CANONICAL_RUNTIME_CONVERGENCE_PASS_1C_PLAN.md`).

Pass 1C has progressed through:
- Initial implementation of the unified composition root.
- Revision waves R1, R2, R3, and R4, repairing route mounting, task supervisor leases, and timeout classifications.
- Independent whole-repo audits and clean reconstruction hygiene passes.

### Living Status Audit (Audit-Time Snapshots)
In accordance with our strict freshness rules, we audited the active certification target in `C:\orion-next-pass1c-certification` at two points on 2026-10-01 (the snapshots below, taken at audit time):

```text
PHYSICAL AUDIT OF C:\orion-next-pass1c-certification:
  error-shape-probe.json    (2,255 bytes)
  f005.log                 (11,256 bytes)
  focused-background.log   (16,407 bytes)
  full-suite.log           (1,986,118 bytes)
  pass1c-focused-union.log (136,711 bytes)

SNAPSHOT 1 STATUS (2026-10-01 10:08):    IN_PROGRESS | VERDICT: NONE_YET
SNAPSHOT 2 STATUS (2026-10-01 14:24):    IN_PROGRESS | VERDICT: NONE_YET
FINAL CERTIFICATION RECEIPT:              NOT PRESENT
```

Notice what the living evidence tells us:
- **Active Probing Is Underway:** The logs confirm execution of focused unions, background timeout probes, and full-suite runs.
- **The Verdict Is Not Yet Issued:** No final certification receipt exists.

```text
EPISTEMIC RULE:
DO NOT INVENT A FINAL VERDICT BEFORE ONE EXISTS.
PASS1C_CERTIFICATION_STATUS  :=  IN_PROGRESS
PASS1C_FINAL_VERDICT         :=  NONE_YET
```

We do not pretend that Pass 1C is already certified and historically closed. We teach it as it physically exists: an **active demonstration of the clean candidate certification pipeline in progress**.

---

## 11. Generated Output Policy: The `dist/**` Dilemma

During clean reconstruction and certification, an essential policy question arises: **What do we do with generated build artifacts (such as compiled JavaScript in `dist/**`)?**

```text
LAW:
SOURCE_PAYLOAD  !=  GENERATED_OUTPUT
```

In many TypeScript and Web projects, `dist/` is listed in `.gitignore`. But in some release branches, compiled bundles are tracked in Git to allow deployment without requiring Node build toolchains on production host servers.

This creates a critical certification fork:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   GENERATED OUTPUT CERTIFICATION POLICIES              │
├──────────────────────────────┬─────────────────────────────────────────┤
│ POLICY                       │ MEANING & OBLIGATION                    │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 1. SOURCE_ONLY_FREEZE_VALID  │ Only declared source/test payload is    │
│                              │ frozen; derivative output is excluded.  │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 2. SOURCE_PLUS_GENERATED_    │ Both source and compiled bundles are    │
│    OUTPUT_REQUIRED           │ frozen. Build must be shown             │
│                              │ deterministic from certified source.    │
├──────────────────────────────┼─────────────────────────────────────────┤
│ 3. NOT_YET_RESOLVED          │ Repository policy has not formally      │
│                              │ ratified whether `dist/` is canonical.  │
└──────────────────────────────┴─────────────────────────────────────────┘
```

Notice the definition of `SOURCE_ONLY_FREEZE_VALID`: it means the **declared source and test payload** constitutes the frozen subject, while generated derivative output is treated as build cache. Machine-generated source may still count as the source of record if declared as such; `AUTHOR_IDENTITY != SOURCE_CLASS`.

### Generated Output Policy May Block Certification or Packaging
How should a certifier handle an unresolved generated-output policy?

```text
POLICY SEMANTICS:
IF GENERATED_OUTPUT_POLICY DOES_NOT AFFECT SUBJECT IDENTITY:
  MAY_BE_NONBLOCKING_POLICY_NOTE

IF GENERATED_OUTPUT_POLICY DETERMINES SUBJECT / ADOPTION PAYLOAD:
  BLOCK_CERTIFICATION_OR_ADOPTION_UNTIL_RESOLVED
```

If the unresolved policy determines what the certification or adoption subject actually is (e.g. whether `dist/**` is included in the frozen payload root hash and promoted to production), the certifier cannot define the adoption subject and must **block certification or adoption packaging until the operator resolves the policy**. 

In Pass 1C, the generated output policy for `dist/**` remains `NOT_YET_RESOLVED`, and whether it blocks final certification packaging is an active determination being resolved by the certifier and operator.

---

## 12. Promotion Station 4: Adoption (Certification != Adoption)

We now reach the ultimate governing law of the promotion pipeline:

```text
LAW:
CERTIFICATION  !=  ADOPTION
CERTIFIED_WITHIN_DECLARED_SCOPE  !=  AUTHORIZED_FOR_ADOPTION
```

### Governed Adoption Requires Valid Governance Authority
Technical certification and governed adoption represent two distinct authority domains:

- **Certification** is an **Epistemic Evaluation**. It answers: *"Does this frozen subject satisfy the technical requirements of the certification contract?"*
- **Adoption** is a **Governance Decision**. It answers: *"Is this certified candidate promoted to become the adopted baseline of the repository?"*

```text
LAW:
ADOPTION_REQUIRES_VALID_GOVERNANCE_AUTHORITY.
THE_MODEL_OR_CERTIFIER_CANNOT_MINT_IT.
```

Governed adoption may proceed through an operator-approved authority mechanism where repository policy allows (such as automated promotion gates under ratified policy; signed policy tokens are a target mechanism, not a current one). However, the certification station itself cannot mint adoption authority. For Pass 1C specifically, explicit human operator authorization is required before promoting the converged composition root into production `main`.

### The Adoption Subject != The Workspace
When adoption is authorized, what actually gets committed to Git?

```text
LAW:
WORKSPACE  !=  ADOPTION_PAYLOAD
```

The adoption engine does not run `git commit -a` inside the certification directory. 

The adoption engine copies **only the certified Implementation Payload** (plus any required generated artifacts) into the production branch.

The disposable test copies, error shape probes, full-suite execution logs, and temporary sidecar receipts remain in the evidentiary archive. They do not pollute the clean Git commit history of the production baseline.

### The Certifier's Terminal Boundary
The certifier's job ends with an evaluation:
```text
TERMINAL CERTIFIER STATUS:
  verdict:         CERTIFIED_WITHIN_DECLARED_SCOPE | CERTIFIED_WITH_NONBLOCKING_LIMITATIONS
                   | CERTIFICATION_BLOCKED | CERTIFICATION_FAILED
  promotion_state: READY_FOR_GOVERNED_ADOPTION_DECISION | NOT_READY_FOR_ADOPTION
```

The certifier halts, presents the receipt, and leaves the promotion decision to rightful governance authority.

---

## 13. Summary

Four stations, four authority domains (`LAW-REC-01`). Implementers and repair stations cannot certify. A clean candidate is a finite attributed delta (`LAW-REC-04`, `LAW-REC-02`). Evidence must not mutate the frozen subject. Byte identity is strong evidence of sameness, not correctness (`LAW-REC-03`). The tripartite sandbox is a preferred pattern; the invariant is subject immutability and evidence separation. Route certification failures to their rightful owner. Certification is not adoption (`LAW-GOV-03`, `LAW-GOV-04`).

Chapters 14–17 (Parts VI and VII) close the loop from defect to adoption. Part VIII synthesizes everything in **Chapter 18: The Prompt Compiler**, and Part IX collects the reference appendices.


---


# Chapter 18: The Prompt Compiler: Synthesizing the Complete Contract

> *"A prompt is not an essay, a wish, or a pep talk. A prompt is a compiled, policy-bounded job contract that instantiates a transient reasoning engine over a declared slice of reality."*

---

## 1. The Core Realization: Compilation vs. Prompt Writing

Chapters 1–17 built the parts: prompts as contracts (Ch 1), reality precedence (Ch 2), process convergence (Ch 3), P-GLL serialization (Ch 4), context metabolism and memory navigation (Ch 5–6), the assembly line, governance and receipts (Ch 7–9), deterministic intelligence, Managed Verbs and the Reality Spine (Ch 10–13), and defects, falsification and certification (Ch 14–17). This chapter assembles them into one operational question: **how do we actually construct a serious Orion prompt?**

In conventional AI engineering, people **write** prompts: they stare at an empty text box, paste snippets, add polite adjectives, type *"think step by step,"* and press run. When the output breaks, they add more adjectives. In Orion engineering we **compile** them:

```text
PROMPT_WRITING     asks: "What should I say?"
PROMPT_COMPILATION asks: "What declared semantic state must this station receive, under what authority, in what representation, to advance the trajectory safely?"
```

```text
CONVENTIONAL PROMPT WRITING:
  HUMAN INTENT ──► AD-HOC PROSE ──► CHAT WINDOW ──► HOPE

ORION PROMPT COMPILATION:
  SEMANTIC INTENT
        │
  [MISSION NORMALIZATION] → [REALITY REHYDRATION] → [INVARIANT CONTRACT ASSEMBLY]
        │
  [STATION POLICY BINDING] → [MODEL PACKAGING PROFILE] → [STATIC VALIDATION]
        │
        ▼
  COMPILED STATION CONTRACT (PROMPT)
        │
        ▼
  EXECUTION ──► RECEIPT ──► VERIFIED DELTA ──► NEXT COMPILATION
```

---

## 2. Maturity Boundary: Current Practice vs. Target Architecture

- **Current working practice (manual).** Orion prompts are synthesized by **manual and semi-structured compilation**. The operator or an orchestration script gathers verified reality fragments, binds station policies, checks write masks, sets evidence standards, and serializes the packet into P-GLL. The validation mechanism today is the pre-flight checklist in [Appendix H](#appendix-h-operator-checklist-before-you-send-a-serious-prompt). No prompt-contract validator or compiler software exists in the repository at audit time.
- **Target architecture (`PROPOSED` / `SPECIFIED_NOT_IMPLEMENTED`).** The **Automated Prompt Compiler** is a target service that would accept mission state, query the Reality Spine compiler (`reality.compile`), bind machine-readable station policies, select qualified packaging profiles, run static validation, and dispatch compiled payloads.

We teach the architecture from first principles so that a contract assembled by hand today and one generated by software tomorrow honor the same invariants.

---

## 3. The Master Formula

Every compiled Orion prompt is synthesized from three orthogonal layers (`LAW-CMP-01`):

```text
PROMPT = INVARIANT_JOB_CONTRACT + STATION_POLICY + MODEL_PACKAGING_PROFILE
```

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        COMPILED STATION PROMPT                         │
│  1. INVARIANT JOB CONTRACT   (the declared picture of the work)        │
│     mission, done state, precedence rules, current reality, owners,    │
│     invariants, known facts and unknowns, negative space, evidence,    │
│     ambiguity rules, output contract                                   │
│                                   +                                    │
│  2. STATION POLICY           (what this seat may do)                   │
│     role, read scope, write mask, authority context, actions,          │
│     stop conditions, status ceiling, next-station rule                 │
│                                   +                                    │
│  3. MODEL PACKAGING PROFILE  (how this model ingests it)               │
│     encoding, context budget, recall placement, tool-call syntax       │
└────────────────────────────────────────────────────────────────────────┘
```

The field-level specification is [Appendix B §2](#appendix-b-p-gll-prompt-contract-schema); Chapter 4 §4 gives the conceptual blocks. This chapter does not repeat the field list.

### Layer 1: The Invariant Job Contract (`TOPIC-COMP-01`)

The Job Contract is the **declared picture of the work**: the problem, the baseline reality, the rules that must hold, and the evidence required to support a completion claim. It is a hypothesis about reality, not reality itself, and living source can invalidate it (Section 11).

It is **invariant across models in meaning**. If you swap one model for another, or a frontier model for a local one, the mission, invariants and evidence requirements do not change; only the packaging does (Section 7). The contract binds the claim-sensitive precedence rules (`LAW-REAL-02`), the rightful owners of the target invariants (`LAW-DFC-01`), the separation of known facts from unknowns (`TOPIC-PGLL-11`), the negative space (`TOPIC-GOV-01`), the evidence requirements (`LAW-EVD-01`, `TOPIC-EVID-12`) and the ambiguity rules (`TOPIC-ANTI-14`).

### Layer 2: Station Policy (`TOPIC-COMP-02`)

The Job Contract specifies the problem; the Station Policy specifies **who is allowed to do what**. An Implementer may write code within a tight mask but cannot certify it. A Falsifier may write adversarial test fixtures but must not repair production code. A Certifier may run non-mutating validation batteries but cannot modify the candidate or mint adoption authority.

The role set is the seven seats of Chapter 7: `MAPPER`, `ARCHITECT_DENOISER`, `IMPLEMENTER`, `FALSIFIER`, `BOUNDED_REPAIR`, `CLEAN_RECONSTRUCTION`, `CERTIFIER`. Each carries a three-axis status ceiling (`station_completion`, `verdict`, `promotion_state`), defined once in [Appendix C §1](#appendix-c-reference-station-templates). An Implementer's promotion state is capped at `READY_FOR_INDEPENDENT_REAUDIT`; only a Certifier may emit a certification verdict, and that verdict is not adoption.

```text
STATION_POLICY CONSTRAINS AUTHORITY, MUTATION AND PROMOTION.
STATION_POLICY DOES_NOT ARTIFICIALLY BLIND REASONING
               WITHIN THE AUTHORIZED OBSERVATION SCOPE.
```

A common failure in amateur multi-agent design is the "role-play prompt": *"You are an implementer, so do not think about architecture."* This is a design error (`LAW-FND-05`):

```text
PRIMARY_ROLE != EPISTEMIC_BLINDNESS
```

An Implementer must be free to observe, within its authorized scope: *"While implementing this repair, I discovered that the underlying architecture violates the durability invariant."* Station policy forbids redesigning the system on the fly, but requires the discovery to be reported in the receipt. Authority is restricted; reasoning is not artificially blinded.

### Layer 3: Model Packaging Profile (`TOPIC-COMP-03`)

The third layer is the transport adapter. Models differ in context capacity, attention behavior and format affinities. The profile translates the invariant P-GLL contract into the surface form that is most reliable *for the target model, as measured* (Chapter 5 §4):

```text
MEANING_IS_CANONICAL; PACKAGING_IS_ADAPTIVE
```

(`LAW-CNT-03`: this is a packaging-invariance law; it does not claim the contract itself is true.) Profile dimensions include context budget and working-set size, placement of high-priority invariants, structural syntax (XML envelopes, indented YAML, Markdown, strict JSON), tool-call encapsulation, and few-shot calibration. Small local models may need tighter chunking and one worked example; some frontier models need none. These are hypotheses to qualify, not facts to assume.

**The compiler adjusts formatting and chunking, never meaning.** You never weaken an invariant because a model is smaller. If a model cannot safely honor the contract within its packaging envelope, it is not qualified for the seat, and the compiler rejects it.

---

## 4. The Prompt Compilation Pipeline

The conceptual pipeline has nine phases:

```text
1. HUMAN / ORION INTENT      Operator or system initiates a mission
2. MISSION NORMALIZATION     Concrete mission, goal and done state
3. REALITY REHYDRATION       HEAD commit, active hashes, Reality Spine boundaries
4. CONTRACT ASSEMBLY         Invariant job contract (invariants, negative space, rules)
5. STATION POLICY BINDING    Role, write mask, authority context, stop conditions
6. MODEL PROFILE PACKAGING   Target model's syntax and context envelope
7. STATIC VALIDATION         Pre-flight rules; reject malformed contracts before the API
8. COMPILED STATION PROMPT   Dispatch the validated, self-contained contract
9. EXECUTION & RECEIPT       Station runs; the delta updates state for the next station
```

### Static Contract Validation: Catching Bugs Before Inference

A compiler catches type errors before machine code is emitted. A static validator for prompt contracts would do the same for contracts: deterministic checks before a single token is sent. None exists today; Appendix H is its manual equivalent.

```text
STATIC_CONTRACT_VALIDATION_RULES:
  1. MISSION_EXISTS              mission is defined and non-empty.
  2. DONE_STATE_DEFINED          verifiable success conditions are present.
  3. WRITE_MASK_SANITY           write_mask does not exceed the seat's authority
                                 (FAIL if FALSIFIER mask includes production source).
  4. CERTIFIER_CANNOT_REPAIR     CERTIFIER has write_mask == [].
  5. STATUS_CEILING_HONORED      no non-CERTIFIER seat lists a certification verdict.
  6. STOP_CONDITIONS_PRESENT     explicit semantic stop conditions exist.
  7. PRECEDENCE_RULES_INCLUDED   claim-sensitive precedence rules are attached.
  8. CONTRADICTIONS_PRESERVED    unresolved conflicts are marked, not silently dropped.
  9. CONTEXT_BUDGET_HONORED      assembled token weight <= the profile's budget.
```

If any check fails, compilation aborts, so you do not spend tokens on a contract that violates your own invariants. But a validator checks *declared structural rules*:

```text
WELL_FORMED != CORRECT
VALID_CONTRACT != SUCCESSFUL_EXECUTION
```

Passing validation shows that required fields are present and the declared structural constraints hold. It does not show that the contract is wise or complete, nor that the model will solve the problem. Correctness requires execution, mechanical evidence and independent falsification.

---

## 5. Packet Anatomy: One Schema

There is one authoritative field list: **15 job-contract fields, 10 station-policy fields and 4 optional profile fields**, in [Appendix B §2](#appendix-b-p-gll-prompt-contract-schema). Chapter 4 §4 is its conceptual summary. Earlier drafts of this book listed the fields several times with drifting names (`packet_id`/`contract_id`, `ambiguity_policy`/`ambiguity_rules`, `defects_under_investigation`/`defects`, `next_logical_station`/`next_station_rule`); the Appendix B names are the only ones used.

---

## 6. Worked Example: An Illustrative Compiled Packet

Consider repairing a timeout collision in which an orchestrator task failure is misclassified as an un-settled background timer. The operator says:

> *"Fix the timeout race in the orchestrator shutdown path where a settled promise is marked as a live background leak. Don't touch the public API, reproduce the failure first, and keep your changes inside the orchestrator module."*

The compiler normalizes this, finds the rightful owner, locates the falsifier test, and binds the `BOUNDED_REPAIR` policy. This abridged excerpt shows the fields that carry the doctrine (`ILLUSTRATIVE_EXAMPLE`; the file paths are illustrative, and the test identity and the dormant supervisor exist only in the uncommitted Pass 1C worktree). The complete schema-valid template is in Appendix B.

```yaml
contract_id: "ILLUSTRATIVE-CONTRACT-001"
invariant_job_contract:
  mission: >
    Repair orchestrator timeout classification so that settled task failures
    are reported as FAILED with writer authority released, rather than
    collapsing into TIMED_OUT_STILL_LIVE.
  done_state:
    - "Test PASS1C-R4-ORCHESTRATOR-TIMEOUT-COLLISION-SETTLED-1 passes."
    - "Authority release on task settlement is verified by the declared test."
    - "No regressions in the existing orchestrator test identities."
  source_precedence_rules:
    - claim_class: CURRENT_BEHAVIOR_AND_EXISTENCE
      authoritative_sources: [living_source, execution_evidence]
    - claim_class: INTENT
      authoritative_sources: [approved_specification]
  negative_space:
    - "Do not alter the public CascadeService interface."
    - "Do not touch the dormant supervisor classifier."
    - "Do not relax timeout durations in fixtures to mask the race."
  known_facts:
    - fact: "A task promise that rejects before the timer expires yields an application-level error."
      basis: living_source
      scope: "core/orchestration/cascade-service.ts at the declared baseline"
  unknowns:
    - "Whether cascade child fibers require separate cancellation tokens."
    - "Whether application errors can leave residual background mutators running (see Chapter 15 §2-3)."
  ambiguity_rules:
    on_contradiction: [investigate_within_read_scope, update_local_reality, emit_reality_delta]
    stop_when: [authority_boundary, write_mask_violation, must_not_change_conflict, safety, unresolved_decision_authority]
station_policy:
  station_role: BOUNDED_REPAIR
  write_mask: ["core/orchestration/cascade-service.ts"]
  maximum_allowable_status:
    verdicts: [REPAIR_SELF_CHECK_PASSED, REPAIR_PARTIAL, REPAIR_FAILED]
    promotion_states: [READY_FOR_INDEPENDENT_REAUDIT, NOT_READY_FOR_REAUDIT]
  next_station_rule: FALSIFIER
```

Note what this excerpt does *not* say. The earlier `known_fact` that "application errors do not leave residual background mutators running" is moved to `unknowns`, because Chapter 15 shows exactly such a state (`FAILED + STILL_LIVE`) is possible.

---

## 7. Model-Specific Packaging Profiles (`TOPIC-COMP-03`)

The mission, invariants, write mask and evidence requirements above are fixed. How the compiler presents them varies. The profiles below are **illustrative and unqualified**; measure each model family before relying on any of them (Chapter 5 §4).

- **Family A (strong tag adherence, hypothetical):** wrap the packet in XML semantic blocks, such as `<station_contract role="BOUNDED_REPAIR">` containing `<invariant_job_contract>` and `<execution_boundary>`.
- **Family B (strong structured-text handling, hypothetical):** emit the YAML/Markdown form of Section 6 with explicit stop-condition headers.
- **Family C (placement-sensitive, hypothetical):** repeat the `write_mask`, `forbidden_actions` and `output_contract` in a closing boundary block right before the response trigger.
- **Family D (small local model, hypothetical):** chunk the work. Rehydrate only the immediate function signature, format the packet as a compact JSON schema, and add one worked input/output example. Chunking this aggressively changes how much context the model sees, never the invariants it must satisfy.

```text
THE MEANING REMAINED IDENTICAL.
ONLY THE PACKAGING AND CHUNKING ADAPTED.
```

---

## 8. Minimum Sufficient Verified State

A central pathology of modern prompting is the **Giant Context Dump** (`TOPIC-ANTI-01`): with a million-token window, paste most of it full. Chapters 5 and 6 argued that large windows are capacity budgets, not optimization targets, and that attention can degrade as competing text accumulates. The compiler optimizes for (`LAW-CMP-02`):

```text
MINIMUM_SUFFICIENT_VERIFIED_STATE FOR MAXIMUM_USEFUL_REASONING
```

It partitions state using the tiers of [Chapter 5 §3](#chapter-5-context-metabolism-how-context-breathes):

- **HOT:** in the compiled contract: mission, active write mask, immediate signatures, failure identities, hard invariants.
- **WARM:** summarized into the prompt only as a compact **index** (spine rows, adjacent test names); the underlying material stays on disk.
- **COLD:** left on disk. The prompt carries navigational coordinates (paths, commit hashes, receipt IDs) so the model can issue targeted reads if its reasoning requires them.

```text
ILLUSTRATIVE BUDGET (not measured):
  [HOT: mission + invariants + mask]  ~2,000 tokens
  [WARM: spine index + hashes]        ~1,500 tokens
  [COLD: navigation pointers]         ~  500 tokens
```

---

## 9. Long-Horizon Compilation Across Days and Weeks

A project advances across days and model generations not by preserving a 200-message chat, but by **iterative contract compilation**:

```text
STATE_n + VERIFIED_DELTA_(n+1) = STATE_(n+1)

DAY 1 Mapper      STATE_0 ──► compiled prompt ──► Mapper      ──► Receipt_1 (reality graph)
DAY 2 Architect   STATE_1 ──► compiled prompt ──► Architect   ──► Receipt_2 (design spec)
DAY 3 Implementer STATE_2 ──► compiled prompt ──► Implementer ──► Receipt_3 (patch)
DAY 4 Falsifier   STATE_3 ──► compiled prompt ──► Falsifier   ──► Receipt_4 (evidence)
```

At every step the previous station's context is discarded; the durable receipt records the verified delta; the compiler reads the receipt, checks its freshness by comparing the receipt's baseline digests for the claim's dependency boundary against current state (Chapter 9 §7), binds the next seat's policy, and compiles a fresh prompt. The next station may run on a different model family, with continuity carried by the receipt:

```text
CONTINUITY != SAME_MODEL
CONTINUITY != SAME_CONTEXT_WINDOW
CONTINUITY := RECOVERABLE_STATE + RULES + EVIDENCE + TRAJECTORY
```

---

## 10. The Compiler Must Not Mint Authority

```text
A PROMPT DESCRIBES AUTHORITY.
A PROMPT DOES NOT CREATE AUTHORITY.
```

A compiler serializes **authority context** (`LAW-GOV-01`): it places lease identifiers, capability references and policy grants into the packet so the station knows its limits. It cannot invent authority that does not exist in governed system state.

- A compiled prompt cannot resurrect an expired execution lease.
- A compiled prompt cannot turn an implementer into a certifier by writing *"You are authorized to certify."*
- A saved prompt file cannot substitute for operator presence when repository policy requires it.
- An LLM cannot escalate its own status by arguing in prose that it deserves more.

If a prompt claims an authority grant that cannot be verified against the host's capability manager or authority registry, the execution harness must fail closed.

---

## 11. Living Source Can Invalidate Compilation

A compiled prompt is a hypothesis about reality at one instant. While reading the files in its read scope, the station may find that a signature changed in an unrecorded commit, that the rightful owner is a different service, that a prerequisite is missing, or that the defect class is far broader than the packet says.

```text
PACKET_PROVIDES_ORIENTATION; PACKET_DOES_NOT_OVERRIDE_REALITY
```

The station must not force reality to fit the prompt, and must not pretend the file matches the packet. Instead:

```text
CONTRADICTION_DISCOVERED != CONTRADICTION_REQUIRES_STOP
```

1. **Investigate** within the authorized read scope and **update** its local picture of reality from living source.
2. **Emit a reality delta** in its receipt, for example:
   ```yaml
   station_completion: PARTIAL
   reality_delta:
     expected_baseline: "<commit-sha>"
     discovered_source_digest: "sha256:<64-hex-placeholder>"
     finding: "cascade-service.ts delegates fiber management to child-pool.ts"
   promotion_state: NOT_READY_FOR_REAUDIT
   next_station_rule: ARCHITECT_DENOISER
   ```
3. **Continue within its mask where that is safe.** Halt only when an authority boundary, the write mask, a must-not-change invariant, a safety issue, an unresolved decision authority, or evidence it cannot acquire within scope prevents safe continuation.
4. **Hand the receipt back** so the contract can be recompiled against actual reality.

---

## 12. Compiler Anti-Patterns

The full catalog is [Appendix G](#appendix-g-prompt-anti-patterns-catalog). These compiler-specific failure modes are worth naming here:

| Anti-Pattern | Description | Mechanical Remedy |
| :--- | :--- | :--- |
| **GIANT_CONTEXT_COMPILER** | Dumping codebases into the prompt "because the window is big enough." | Compile minimum sufficient verified state; use the Chapter 5 tiers (`TOPIC-ANTI-01`). |
| **STATUS_ESCALATION_BY_PROSE** | An implementer marks its own work "certified" in chat text. | Enforce the per-seat status ceiling; reject self-certification (`TOPIC-ANTI-06`). |
| **MODEL_NAME_AS_AUTHORITY** | Trusting an audit because an expensive frontier model produced it. | Base trust on reconstructable commands and failure identities (`LAW-EVD-01`). |
| **ONE_PROMPT_FOR_ALL_MODELS** | Sending identical raw text to every model. | Separate the invariant contract from packaging profiles (`LAW-CNT-03`). |
| **CERTIFIER_WITH_WRITE_ACCESS** | Giving a certifier write permission to "fix small typos during testing." | Certifier `write_mask: []`; Falsifier write mask limited to adversarial fixtures (`TOPIC-STAT-09`). |

---

## 13. Summary: The Prompt as a Compiled Contract

Prompt engineering in this book is the discipline of **compiling bounded, auditable contracts for transient neural processors**. When you compile a prompt this way:

- You do not ask the model to remember who it was yesterday; you provide a rehydrated **Continuity Kernel**.
- You do not ask the model to be good; you bind an **Invariant Job Contract**.
- You do not ask the model to stay in its lane; you bind a **Station Policy**.
- You do not fight model quirks; you adapt the **Model Packaging Profile**.
- You do not accept claims of success; you demand **reconstructable evidence receipts**.

These contracts are intended to support long-horizon software engineering without depending on any one model or conversation. The reference appendices that follow collect the laws, reference templates, schemas, anti-patterns and checklists for applying the method by hand today and for specifying an automated compiler tomorrow.


---


# Appendix A: Reference Orion Prompting Laws

> *"Laws are not slogans to be chanted; they are architectural constraints that protect complex systems from cognitive and procedural failure."*

---

## 1. Overview and Indexing Standard

This appendix is a **reference compression layer** over the doctrine taught in *The Idiot's Guide to Advanced Prompting Strategies for Orion*. It is the book's single **law registry**: every `LAW-*` identifier used in the chapters and appendices resolves to exactly one entry here (44 laws). An earlier drafting-time registry used a different ID scheme and is superseded.

The laws are **book standards** drawn from model-assisted drafting and an independent audit. They are not formally ratified Orion policy (see [Appendix B](#appendix-b-p-gll-prompt-contract-schema) §1 on terminology).

A compressed form can lose the qualifiers of the fuller chapter treatment, so each entry's `PLAIN_ENGLISH` and `SCOPE / QUALIFIER` must be read against its `PRIMARY_CHAPTER`. Where they differ, the chapter governs.

Every law carries:
- **LAW_ID:** Unique identifier.
- **REFERENCE_FORM:** The compact symbolic formulation used in this book. (The law-name string `MEANING_IS_CANONICAL` in `LAW-CNT-03` is retained verbatim; it names meaning invariance, not ratification.)
- **CLASSIFICATION:** `VALID_INVARIANT` (holds within its stated scope), `DESIGN_PRINCIPLE` (a recommended practice with stated trade-offs) or `DIRECTIONAL_HEURISTIC` (a default to apply with judgment).
- **PLAIN_ENGLISH:** The qualified statement.
- **PRIMARY_CHAPTER:** Where the law is taught.
- **SCOPE / QUALIFIER:** Domain and boundary.

---

## 2. Foundations of Multi-Model Engineering

### `LAW-FND-01`
- **REFERENCE_FORM:** `STATION > MODEL_IDENTITY`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Design prompts and workflows around operational seats (duties, authorities, masks), not around commercial model identities.
- **PRIMARY_CHAPTER:** Chapter 1 (§3)
- **SCOPE / QUALIFIER:** Models fill seats; seats define duties. A model must be qualified for its seat.

### `LAW-FND-02`
- **REFERENCE_FORM:** `THOUGHT != ACTION; PLAN != AUTHORITY; PROPOSAL != ADOPTION`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Thinking about a change is not executing it; a plan does not grant permission to apply it; and a verified repair proposal is not adopted code.
- **PRIMARY_CHAPTER:** Chapter 1 (§6)
- **SCOPE / QUALIFIER:** Prevents cognitive state from masquerading as system mutation or promotion authority.

### `LAW-FND-03`
- **REFERENCE_FORM:** `COGNITIVE_FREEDOM != EXECUTION_FREEDOM`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** A model has broad reasoning freedom within mission, policy, evidence and safety boundaries: it may analyze, critique and explore. Its tool use and mutations stay inside its assigned policy mask.
- **PRIMARY_CHAPTER:** Chapter 3 (§3)
- **SCOPE / QUALIFIER:** Fences capability without lobotomizing reasoning. "Broad" is bounded by authorized observation scope.

### `LAW-FND-04`
- **REFERENCE_FORM:** `PROCESS_CONVERGENCE_WITHOUT_EPISTEMIC_CONFORMITY`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Diverse models can converge on a verified artifact by sharing process, standards and evidence rules, without being forced to agree on explanations.
- **PRIMARY_CHAPTER:** Chapter 3 (§2)
- **SCOPE / QUALIFIER:** Disagreement is a trigger for mechanical investigation, not a vote.

### `LAW-FND-05`
- **REFERENCE_FORM:** `PRIMARY_ROLE != EPISTEMIC_BLINDNESS`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Role specialization restricts mutation authority and the status a station may claim. It must not artificially blind reasoning within the authorized observation scope: a station should still notice and report contradictions and defects it can legitimately observe.
- **PRIMARY_CHAPTER:** Chapter 7 (§4)
- **SCOPE / QUALIFIER:** Authorized scope, privacy and tool availability can still legitimately limit what is observed. Prohibits "roleplay lobotomy" prompts.

---

## 3. Continuity, Memory, and Serialization

### `LAW-CNT-01`
- **REFERENCE_FORM:** `MODEL != CONTINUITY`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Continuity must not depend on keeping one model or vendor alive. It must survive model crash, context truncation, deprecation and replacement.
- **PRIMARY_CHAPTER:** Chapter 1 (§4)
- **SCOPE / QUALIFIER:** Foundational continuity doctrine.

### `LAW-CNT-02`
- **REFERENCE_FORM:** `CONTINUITY := RECOVERABLE_STATE + RULES + EVIDENCE + TRAJECTORY`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Long-horizon continuity has four rehydratable components: durable state, invariant rules, evidence receipts and a directional trajectory.
- **PRIMARY_CHAPTER:** Chapter 1 (§4), Chapter 6 (§1)
- **SCOPE / QUALIFIER:** Defines the Continuity Kernel; replaces chat transcripts.

### `LAW-CNT-03`
- **REFERENCE_FORM:** `MEANING_IS_CANONICAL; PACKAGING_IS_ADAPTIVE`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** The semantic contract (mission, invariants, boundaries, evidence) is invariant across packaging and vendor-neutral; surface formatting (XML, YAML, Markdown, JSON) adapts to the target model. This is a packaging-invariance law, not a claim that the packet itself is true: packets can be stale or wrong.
- **PRIMARY_CHAPTER:** Chapter 4 (§5), Chapter 18 (§3)
- **SCOPE / QUALIFIER:** P-GLL serialization and prompt compilation. Adaptations to chunking never weaken invariants.

### `LAW-CNT-04`
- **REFERENCE_FORM:** `CONTEXT_WINDOW IS CAPACITY; WORKING_SET IS AN OPTIMIZATION`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** A large context window does not justify filling it. Optimize for the minimum sufficient verified state.
- **PRIMARY_CHAPTER:** Chapter 4 (§3), Chapter 5 (§4)
- **SCOPE / QUALIFIER:** Context metabolism. Effective recall is empirical and model-dependent.

---

## 4. Reality and Precedence

### `LAW-REAL-01`
- **REFERENCE_FORM:** `PACKET_PROVIDES_ORIENTATION; PACKET_DOES_NOT_OVERRIDE_REALITY`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** A packet provides orientation and working hypotheses. For claims about current state, if living source or observed behavior contradicts the packet, observation outranks the packet. Other claim classes follow `LAW-REAL-02`: an approved specification governs intent, and current governance state governs authority.
- **PRIMARY_CHAPTER:** Chapter 2 (§2)
- **SCOPE / QUALIFIER:** Factual premises about current state. A packet that describes a delta to be made is not "contradicted" by the present source.

### `LAW-REAL-02`
- **REFERENCE_FORM:** `SOURCE_OF_TRUTH_HIERARCHY IS CLAIM-SENSITIVE`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** No single artifact outranks all others for all claims. Living source governs what exists now; execution evidence governs current behavior; contemporaneous receipts govern historical verification claims; approved specifications govern intent; current governance state governs authority.
- **PRIMARY_CHAPTER:** Chapter 2 (§3)
- **SCOPE / QUALIFIER:** Epistemic conflict resolution; see the structured `source_precedence_rules` in Appendix B.

### `LAW-REAL-03`
- **REFERENCE_FORM:** `DEFINE_GOOD_BEFORE_IMPLEMENTATION`
- **CLASSIFICATION:** `DIRECTIONAL_HEURISTIC`
- **PLAIN_ENGLISH:** As a default, state observable success metrics and done-state criteria before implementing. Exploratory spikes and Mapper or Falsifier fixtures may precede a final done-state if they are labeled exploratory.
- **PRIMARY_CHAPTER:** Chapter 2 (§4)
- **SCOPE / QUALIFIER:** Requirements engineering.

### `LAW-REAL-04`
- **REFERENCE_FORM:** `UNDECLARED != IRRELEVANT`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Files outside the declared Reality Spine are not nonexistent. If runtime execution reaches them, their omission is a spine gap to investigate.
- **PRIMARY_CHAPTER:** Chapter 12 (§7)
- **SCOPE / QUALIFIER:** Reality Spine bounding. The spine itself is `SPECIFIED_NOT_IMPLEMENTED`.

---

## 5. Governance, Scope, and Authority

### `LAW-GOV-01`
- **REFERENCE_FORM:** `PROMPT_DESCRIBES_AUTHORITY; PROMPT_DOES_NOT_CREATE_AUTHORITY`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** A prompt can document authority granted by the system. The prompt text cannot mint or expand authority.
- **PRIMARY_CHAPTER:** Chapter 18 (§10)
- **SCOPE / QUALIFIER:** Authority derives from governed system state, not from prose.

### `LAW-GOV-02`
- **REFERENCE_FORM:** `REVERSIBLE != AUTOMATICALLY_AUTHORIZED`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** An action being cleanly undoable does not mean it is pre-authorized. Authorization must be grounded in contract, policy or harness permissions.
- **PRIMARY_CHAPTER:** Chapter 8 (§6)
- **SCOPE / QUALIFIER:** Scope enforcement and write-mask protection.

### `LAW-GOV-03`
- **REFERENCE_FORM:** `ADOPTION_REQUIRES_VALID_GOVERNANCE_AUTHORITY`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Merging into protected branches or deploying requires legitimate governance authority: an operator decision or an explicitly ratified governed policy. For Pass 1C specifically, explicit operator authorization is required. Signed promotion tokens are a target mechanism; none exists today.
- **PRIMARY_CHAPTER:** Chapter 8 (§5), Chapter 17 (§12)
- **SCOPE / QUALIFIER:** Production promotion. `GOVERNED != ALWAYS_MANUAL`.

### `LAW-GOV-04`
- **REFERENCE_FORM:** `THE_MODEL_OR_CERTIFIER_CANNOT_MINT_ADOPTION_AUTHORITY`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Neither the implementing model, the falsifying station, nor the certifier can promote code into production. They produce evidence and scoped verdicts; governance decides adoption. `CERTIFICATION != ADOPTION`.
- **PRIMARY_CHAPTER:** Chapter 8 (§5), Chapter 17 (§12)
- **SCOPE / QUALIFIER:** Separation of powers. An independent audit also holds no adoption authority.

### `LAW-GOV-05`
- **REFERENCE_FORM:** `HANDOFF_ROUTING CAN BE DETERMINISTIC; AUTHORITY_TRANSITIONS MUST BE GOVERNED`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Pipelines may parse receipts and route work automatically, but a transition that crosses an authority boundary or mutates protected state requires governed authorization.
- **PRIMARY_CHAPTER:** Chapter 8 (§5), Chapter 9 (§6)
- **SCOPE / QUALIFIER:** Orchestration engines and task runners. Governed does not mean a manual click at every boundary.

---

## 6. Deterministic Intelligence and Managed Verbs

### `LAW-DET-01`
- **REFERENCE_FORM:** `PREFER_LOWEST_SUFFICIENT_DETERMINISTIC_MECHANISM` (maxim: `INTELLIGENCE_ONLY_WHERE_UNCERTAINTY_EXISTS`)
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Intelligence belongs where uncertainty exists. If a deterministic mechanism (script, state machine, regular expression) is sufficient and affordable to build and maintain, prefer it to an LLM; escalate when it is not sufficient.
- **PRIMARY_CHAPTER:** Chapter 10 (§1, §4)
- **SCOPE / QUALIFIER:** A design preference, not a prohibition. Weigh build cost, maintenance cost and coverage.

### `LAW-DET-02`
- **REFERENCE_FORM:** `MODELS_DISCOVER_ROADS; ORION_PAVES_THEM`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Use reasoning models to explore unknown territory; once a path is understood, proceduralize it into deterministic scripts and Managed Verbs.
- **PRIMARY_CHAPTER:** Chapter 10 (§5)
- **SCOPE / QUALIFIER:** Architectural maturity lifecycle.

### `LAW-DET-03`
- **REFERENCE_FORM:** `DETERMINISTIC != CORRECT; DETERMINISTIC := REPEATABLE`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Under a defined initial state and defined inputs, a deterministic mechanism is reproducible; it is not guaranteed bug-free.
- **PRIMARY_CHAPTER:** Chapter 10 (§2)
- **SCOPE / QUALIFIER:** Deterministic engineering epistemology.

### `LAW-DET-04`
- **REFERENCE_FORM:** `MANY_ACTIONS != AGENCY; LONG_RUNNING != COGNITIVE`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** A script running a thousand iterations is not an "autonomous agent"; long-running execution is procedural unless governed by adaptive semantic judgment.
- **PRIMARY_CHAPTER:** Chapter 10 (§7)
- **SCOPE / QUALIFIER:** Terminology precision.

### `LAW-VRB-01`
- **REFERENCE_FORM:** `VERB_ATOMICITY_IS_SEMANTIC_NOT_PROCEDURAL`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** A Verb represents one complete, verifiable domain outcome even if it internally executes many commands. A Verb may be internally simple; managed machinery (retries, checkpoints, receipts) is optional and scales with risk.
- **PRIMARY_CHAPTER:** Chapter 11 (§1)
- **SCOPE / QUALIFIER:** Verb architecture; the unified Managed Verb runtime is `SPECIFIED_NOT_IMPLEMENTED`.

### `LAW-VRB-02`
- **REFERENCE_FORM:** `LLM_ENTERS_ON_UNCERTAINTY; LLM_EXITS_WHEN_UNCERTAINTY_COMPILED_AWAY`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Bring a reasoning model in when semantic ambiguity exists; once the problem reduces to bounded deterministic steps, execute procedurally.
- **PRIMARY_CHAPTER:** Chapter 11 (§4)
- **SCOPE / QUALIFIER:** Cognitive efficiency.

### `LAW-VRB-03`
- **REFERENCE_FORM:** `PROMPT_AT_HIGHEST_SEMANTIC_LEVEL; EXECUTE_AT_LOWEST_DETERMINISTIC_LEVEL`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Frame instructions to models as goals and semantic intent; execute the resulting actions with the most rigid deterministic primitives available. Expose intent, not plumbing.
- **PRIMARY_CHAPTER:** Chapter 11 (§1, §8)
- **SCOPE / QUALIFIER:** Interface design. Compression of the tool surface is not a security control.

---

## 7. Defect Lifecycles and Control Identity

### `LAW-DFC-01`
- **REFERENCE_FORM:** `A_CORRECT_CONSUMER_CANNOT_REPAIR_A_DISHONEST_PRODUCER`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Defensive checks in a consumer do not fix a producer that emits invalid data. Consumers should validate and fail closed; repair belongs at the owner of the violated invariant.
- **PRIMARY_CHAPTER:** Chapter 14 (§6)
- **SCOPE / QUALIFIER:** "Dishonest" means mechanically inaccurate, not malicious.

### `LAW-DFC-02`
- **REFERENCE_FORM:** `FIXING_THE_OBSERVED_FAILURE != CLOSING_THE_FAILURE_CLASS`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Patching the line that failed does not resolve the defect class. Search the bounded semantic neighborhood for siblings.
- **PRIMARY_CHAPTER:** Chapter 14 (§1, §2)
- **SCOPE / QUALIFIER:** Closure is scoped to the verified neighborhood at the current baseline.

### `LAW-DFC-03`
- **REFERENCE_FORM:** `NOT_REPRODUCED != NO_DEFECT; REPRODUCTION_STRENGTHENS_BOUNDARY_KNOWLEDGE`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Failing to reproduce a bug does not show it does not exist. Reproduction establishes occurrence and boundary evidence under the tested conditions; it strengthens boundary knowledge but does not by itself establish the entire causal class.
- **PRIMARY_CHAPTER:** Chapter 14 (§4)
- **SCOPE / QUALIFIER:** Defect epistemology and stochastic failures.

### `LAW-CTL-01`
- **REFERENCE_FORM:** `SUCCESS != SETTLEMENT`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Whether a task met its functional objective is orthogonal to whether its background work, children and mutator authority have finished (settlement within the authority scope).
- **PRIMARY_CHAPTER:** Chapter 15 (§2)
- **SCOPE / QUALIFIER:** Concurrent lifecycle state machines.

### `LAW-CTL-02`
- **REFERENCE_FORM:** `FAILURE + LIVE + RETAINED_OR_FENCED_AUTHORITY = VALID_SAFETY_STATE`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** A task that failed while its mutator is still live is a valid safety state only if authority is retained or fenced until settlement; releasing authority then is the hazard.
- **PRIMARY_CHAPTER:** Chapter 15 (§4)
- **SCOPE / QUALIFIER:** Lifecycle safety and shutdown handling.

### `LAW-CTL-03`
- **REFERENCE_FORM:** `APPLICATION_DATA MUST_NOT_MASQUERADE_AS_CONTROL_STATE`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Do not use user strings, error messages or payload data as control signals. Protection comes from trusted provenance of the signal's branch plus identity-safe representation and outer wrapping of application results. A type label alone does not authenticate.
- **PRIMARY_CHAPTER:** Chapter 15 (§6, §7)
- **SCOPE / QUALIFIER:** Magic-string control; a `Symbol` is not a general authentication primitive.

### `LAW-CTL-04`
- **REFERENCE_FORM:** `PRESENT != VALID; REGISTERED != EXECUTABLE; TESTED != AUTHORIZED`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** A present config key is not necessarily valid; a registered plugin is not necessarily runnable; a patch passing tests is not thereby authorized.
- **PRIMARY_CHAPTER:** Chapter 15 (§5)
- **SCOPE / QUALIFIER:** Orthogonal dimension verification.

---

## 8. Evidence, Verification, and Falsification

### `LAW-EVD-01`
- **REFERENCE_FORM:** `GREEN != PROVEN; TESTED != VERIFIED; VERIFIED != AUTHORIZED; AUTHORIZED != EXECUTED`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** The verification promotion ladder. A passing test is scoped empirical evidence, not universal truth; verification evaluates a claim against attempts to falsify it within a declared scope; verification does not grant authority; authorization does not mean the mutation has completed.
- **PRIMARY_CHAPTER:** Chapter 16 (§1)
- **SCOPE / QUALIFIER:** Universal verification doctrine.

### `LAW-EVD-02`
- **REFERENCE_FORM:** `COUNTS_DO_NOT_SUBSTITUTE_FOR_IDENTITIES`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** "384 tests passed" is weak evidence by itself. High-assurance verification records the test identities, commands and failure signatures.
- **PRIMARY_CHAPTER:** Chapter 16 (§6)
- **SCOPE / QUALIFIER:** Test reporting and receipt schema.

### `LAW-EVD-03`
- **REFERENCE_FORM:** `NEW_FAILURE_IDENTITY = REGRESSION_CANDIDATE`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** A newly observed failure identity must be investigated and classified against the baseline contract. It is a candidate regression, not automatically a defect.
- **PRIMARY_CHAPTER:** Chapter 16 (§6)
- **SCOPE / QUALIFIER:** Regression analysis where stable identities exist.

### `LAW-EVD-04`
- **REFERENCE_FORM:** `RECEIPT != PROOF; IMMUTABILITY_REQUIRES_AN_IMMUTABILITY_MECHANISM`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** A receipt is a durable structured record of claims, observations and outcomes, not proof. Hashes and content addressing give tamper-evidence; immutability requires enforced write-once or append-only storage and permissions; durability requires sync barriers. These are three different properties.
- **PRIMARY_CHAPTER:** Chapter 9 (§2, §7), Chapter 16 (§8)
- **SCOPE / QUALIFIER:** Receipt integrity versus truth.

### `LAW-EVD-05`
- **REFERENCE_FORM:** `STALE != FALSE; REVERIFICATION_REQUIRED_WHEN_DEPENDENCIES_MUTATE`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** A properly verified historical claim is not falsified by later change, but its current applicability is void until re-verified against the claim's dependency boundary.
- **PRIMARY_CHAPTER:** Chapter 9 (§7), Chapter 16 (§9)
- **SCOPE / QUALIFIER:** Evidence freshness; HEAD equality is neither necessary nor sufficient.

---

## 9. Reconstruction, Certification, and Adoption

### `LAW-REC-01`
- **REFERENCE_FORM:** `REPAIR != RECONSTRUCTION != CERTIFICATION != ADOPTION`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Four distinct promotion stations. Repair fixes code in a dirty workspace; Reconstruction assembles a minimal, attributed candidate; Certification is an independent, non-mutating audit; Adoption is the governance act.
- **PRIMARY_CHAPTER:** Chapter 17 (§1)
- **SCOPE / QUALIFIER:** Promotion pipeline architecture.

### `LAW-REC-02`
- **REFERENCE_FORM:** `DIRTY_VERIFIED_PROPOSAL != CLEAN_CERTIFICATION_CANDIDATE`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** A dirty working tree with passing tests and scratch edits is a proposal, not a certification candidate. The candidate is an attributed subject (baseline plus declared delta, manifest and verification root). A clean isolated checkout is one way to materialize it; equivalent frozen subjects are valid.
- **PRIMARY_CHAPTER:** Chapter 17 (§3)
- **SCOPE / QUALIFIER:** Clean reconstruction.

### `LAW-REC-03`
- **REFERENCE_FORM:** `BYTE_IDENTITY_PROVES_MECHANICAL_SAMENESS_NOT_ARCHITECTURAL_CORRECTNESS`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** A matching SHA-256 digest is strong mechanical evidence that two files or trees have the same bytes, under the declared hashing and canonicalization boundary. It is not evidence that those bytes are correct, safe software.
- **PRIMARY_CHAPTER:** Chapter 13 (§6), Chapter 17 (§6)
- **SCOPE / QUALIFIER:** Limits of hash verification. The compact form's word "proves" is shorthand for strong mechanical evidence.

### `LAW-REC-04`
- **REFERENCE_FORM:** `DIRTY != INTENDED`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** A modified file in a dirty tree was not necessarily intended for the candidate. Collateral and untracked modifications must be explicitly excluded.
- **PRIMARY_CHAPTER:** Chapter 17 (§4)
- **SCOPE / QUALIFIER:** Attributed file set construction.

---

## 10. Prompt Compilation

### `LAW-CMP-01`
- **REFERENCE_FORM:** `PROMPT = INVARIANT_JOB_CONTRACT + STATION_POLICY + MODEL_PACKAGING_PROFILE`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** Every prompt is synthesized from what is declared about the work (job contract, a hypothesis that living source can invalidate), who is acting (station policy), and how the target model ingests information (packaging profile).
- **PRIMARY_CHAPTER:** Chapter 18 (§3)
- **SCOPE / QUALIFIER:** Prompt compilation; the automated compiler is `SPECIFIED_NOT_IMPLEMENTED`.

### `LAW-CMP-02`
- **REFERENCE_FORM:** `MINIMUM_SUFFICIENT_VERIFIED_STATE FOR MAXIMUM_USEFUL_REASONING`
- **CLASSIFICATION:** `DESIGN_PRINCIPLE`
- **PLAIN_ENGLISH:** The compiler does not maximize tokens; it compiles the smallest verified working set sufficient for high-fidelity reasoning.
- **PRIMARY_CHAPTER:** Chapter 18 (§8)
- **SCOPE / QUALIFIER:** Compiler optimization target.

### `LAW-CMP-03`
- **REFERENCE_FORM:** `WELL_FORMED != CORRECT; VALID_CONTRACT != SUCCESSFUL_EXECUTION`
- **CLASSIFICATION:** `VALID_INVARIANT`
- **PLAIN_ENGLISH:** Static validation checks declared structural rules (required fields, mask-versus-role constraints, status ceilings). It does not establish that the contract is wise or complete, or that the model's output will be correct.
- **PRIMARY_CHAPTER:** Chapter 18 (§4)
- **SCOPE / QUALIFIER:** Static validation boundary.


---


# Appendix B: P-GLL Prompt Contract Schema

> *"A prompt schema is a typed interface between human intent, repository reality, and transient neural cognition. If a claim's basis cannot be stated, it belongs under `unknowns`."*

---

## 1. Overview, Status and Terminology

The **Programming-GLL (P-GLL) Prompt Contract Schema** is a reference schema for compiling, validating and dispatching station contracts.

**Status:** `PROPOSED` / `SPECIFIED_NOT_IMPLEMENTED`. The schema comes from model-assisted drafting and has not been ratified. No prompt-contract validator ships in the Orion repository; Appendix H is the manual equivalent.

**Terminology.** In this book, *canonical* means **formally adopted or ratified by rightful governance**. Model-generated, author-checked, reference, proposed or unadopted book material is not canonical. This schema is therefore called a *reference* schema, and its fields use the vocabulary of the **current book standard**.

### Core Architectural Laws
1. **`PROMPT_DESCRIBES_AUTHORITY; PROMPT_DOES_NOT_CREATE_AUTHORITY` (`LAW-GOV-01`):** The schema uses `authority_context`, never `authority_grant`. A contract documents the governed authority under which a station operates; it cannot mint authority.
2. **`MEANING_IS_CANONICAL; PACKAGING_IS_ADAPTIVE` (`LAW-CNT-03`):** The schema defines the invariant semantic structure. The compiler may serialize it as YAML, JSON or tagged XML depending on the packaging profile.
3. **`WELL_FORMED != CORRECT` (`LAW-CMP-03`):** A contract that conforms to this schema is structurally valid. Truth still requires execution and independent falsification.
4. **`SOURCE_OF_TRUTH_HIERARCHY IS CLAIM-SENSITIVE` (`LAW-REAL-02`):** The schema carries claim-scoped precedence rules, never one universal ordering.

---

## 2. Field Reference Specification

The schema has three orthogonal layers plus root metadata (`timestamp` required; `compiler_version` optional):

```text
┌────────────────────────────────────────────────────────────────────────┐
│ 1. INVARIANT JOB CONTRACT  (What problem is being solved)              │
│ 2. STATION POLICY          (Who is acting, and under what bounds)      │
│ 3. MODEL PROFILE ADAPTER   (How the payload is packaged; optional)     │
└────────────────────────────────────────────────────────────────────────┘
```

### Layer 1: Invariant Job Contract (15 fields)

| Field | Type | Required? | Description |
| :--- | :--- | :--- | :--- |
| `contract_id` | String | **YES** | Unique identifier (content-addressed or timestamped). Root level. |
| `mission` | String | **YES** | Unambiguous statement of the engineering objective. |
| `done_state` | Array[String] | **YES** | Observable conditions that define completion. |
| `source_precedence_rules` | Array[Object] | **YES** | Claim-scoped rules `{claim_class, authoritative_sources[], precedence_rule, scope}` (`LAW-REAL-02`). |
| `current_reality` | Object | **YES** | Declared baseline: commit, workspace, file digests. A hypothesis that living source can invalidate. |
| `rightful_owners` | Object | **YES** | Subsystems and files that own the target invariants (`LAW-DFC-01`). |
| `invariants` | Array[String] | **YES** | Rules that must hold within the contract's scope. |
| `known_facts` | Array[Object] | **YES** | Facts `{fact, basis, scope}`; see Section 5. |
| `unknowns` | Array[String] | **YES** | Explicit uncertainties requiring investigation (`TOPIC-PGLL-11`). |
| `negative_space` | Array[String] | **YES** | Forbidden approaches, out-of-scope files and non-goals. |
| `must_not_change` | Array[String] | **YES** | Protected files, interfaces or databases. |
| `defects` | Array[Object] | Optional | Defect classes and instances under investigation. |
| `evidence_requirements` | Array[Object] | **YES** | `{command, must_pass_test_identities[], must_preserve_identities[]}`. |
| `ambiguity_rules` | Object | **YES** | `{on_contradiction[], stop_when[]}`; see Section 5. |
| `output_contract` | Object | **YES** | Expected schema of the handoff receipt or payload. |

### Layer 2: Station Policy (10 fields)

| Field | Type | Required? | Description |
| :--- | :--- | :--- | :--- |
| `station_role` | Enum | **YES** | One of the seven seats: `MAPPER`, `ARCHITECT_DENOISER`, `IMPLEMENTER`, `FALSIFIER`, `BOUNDED_REPAIR`, `CLEAN_RECONSTRUCTION`, `CERTIFIER`. |
| `read_scope` | Array[String] | **YES** | Paths the station is authorized to observe. |
| `write_mask` | Array[String] | **YES** | Allowlist of files the station may modify (`[]` for read-only seats). A `CERTIFIER` must have `[]`. |
| `authority_context` | Object | **YES** | Reference to external governance authority: `governance_type`, optional `reference`, `production_mutation_authorized`, optional `audit_fixture_write_authorized`, and `adoption_authorized` (always `false`). |
| `allowed_actions` | Array[String] | **YES** | Permitted tool verbs. |
| `forbidden_actions` | Array[String] | **YES** | Prohibited operations. |
| `stop_conditions` | Array[String] | **YES** | Halt triggers only (`TOPIC-GOV-04`). |
| `completion_conditions` | Array[String] | **YES** | Conditions under which the station's work is done. Kept separate from halt triggers. |
| `maximum_allowable_status` | Object | **YES** | `{verdicts[], promotion_states[]}`, a subset of the role's row in [Appendix C §1](#appendix-c-reference-station-templates). |
| `next_station_rule` | String | **YES** | Governed transition rule naming the recipient of the receipt. |

`governance_type` is one of `OPERATOR_AUTHORIZATION`, `RATIFIED_POLICY`, `REGISTRY_CAPABILITY` (today's opcap/dauth mechanism), `SIGNED_GRANT_TARGET` (a target mechanism, `SPECIFIED_NOT_IMPLEMENTED`), `PROJECT_POLICY_BINDING_REQUIRED` (to be bound before use) or `NONE` (no authority needed).

### Layer 3: Model Profile Adapter (4 optional fields)

| Field | Type | Required? | Description |
| :--- | :--- | :--- | :--- |
| `packaging_format` | Enum | Optional | `YAML_INDENTED`, `XML_TAGGED`, `MARKDOWN_P_GLL`, `JSON_STRICT`. |
| `context_budget_tokens` | Integer | Optional | Token allocation for the working set. Must be qualified per model (Chapter 5 §4). |
| `effective_recall_horizon` | String | Optional | Placement strategy, such as `PIN_INVARIANTS_AT_END`. Must be qualified per model. |
| `few_shot_examples` | Array[Object] | Optional | Calibrated input/output demonstrations. |

(`target_model_family` and `structural_delimiters` are additional free-form descriptors.)

---

## 3. Reference YAML Template

All values are illustrative.

```yaml
# ILLUSTRATIVE_EXAMPLE: reference values, not a record of any real Orion contract.
contract_id: "ILLUSTRATIVE-CONTRACT-002"
timestamp: "2026-10-01T16:00:00Z"
compiler_version: "manual-compilation"

invariant_job_contract:
  mission: >
    Make QueueWorker release its lease on shutdown after in-flight work settles.
  done_state:
    - "Declared test identity QW-SHUTDOWN-RELEASES-LEASE passes."
    - "No existing QueueWorker test identity regresses."
  source_precedence_rules:
    - claim_class: CURRENT_EXISTENCE_AND_BEHAVIOR
      authoritative_sources: [living_source, execution_evidence]
      precedence_rule: "Observed source and executed behavior outrank the packet and any plan."
      scope: "Factual premises about the current repository state."
    - claim_class: INTENT
      authoritative_sources: [approved_specification]
      precedence_rule: "The approved specification governs what is intended to be built."
      scope: "Design and acceptance questions."
    - claim_class: HISTORICAL_VERIFICATION
      authoritative_sources: [contemporaneous_receipt]
      precedence_rule: "A receipt is evidence about its own baseline and is stale once its dependency boundary changes."
      scope: "What was verified at a past commit."
    - claim_class: AUTHORITY
      authoritative_sources: [current_governance_state]
      precedence_rule: "Ratified policy and operator decisions govern who may authorize an action."
      scope: "Authorization questions."
  current_reality:
    baseline_commit: "<commit-sha>"
    workspace_root: "<workspace-root>"
    reality_spine_view: "core/example/**"
    verified_file_hashes:
      core/example/queue-worker.ts: "sha256:<64-hex-placeholder>"
  rightful_owners:
    subsystem: "core/example"
    lead_file: "core/example/queue-worker.ts"
    invariant_owner: "QueueWorker"
  invariants:
    - "Lease release happens only after all owned work has settled."
  known_facts:
    - fact: "QueueWorker.stop() currently returns before in-flight jobs finish."
      basis: living_source
      scope: "core/example/queue-worker.ts at the declared baseline"
    - fact: "Writes outside the declared write mask require a new authorization."
      basis: operator_constraint
      scope: "this contract"
  unknowns:
    - "Whether jobs spawned by plugins are tracked by the worker."
  negative_space:
    - "Do not change the public QueueWorker interface."
    - "Do not add ad-hoc sleeps to work around races."
  must_not_change:
    - "core/contracts/**"
  defects:
    - defect_class: "SUCCESS_SETTLEMENT_COLLAPSE"
      defect_instance: "QW-SHUTDOWN-LEASE-LEAK"
      reproduction_command: "npm test -- tests/example/queue-worker.test.ts"
  evidence_requirements:
    - command: "npm test -- tests/example/queue-worker.test.ts"
      must_pass_test_identities: ["QW-SHUTDOWN-RELEASES-LEASE"]
      must_preserve_identities: ["ALL_EXISTING_QUEUE_WORKER_TESTS"]
  ambiguity_rules:
    on_contradiction: [investigate_within_read_scope, update_local_reality, emit_reality_delta]
    stop_when: [authority_boundary, write_mask_violation, must_not_change_conflict, safety, unresolved_decision_authority, unacquirable_evidence]
  output_contract:
    type: STATION_HANDOFF_RECEIPT
    required_fields: [receipt_id, station_completion, verdict, promotion_state, evidence, mutated_files, next_station_rule]

station_policy:
  station_role: IMPLEMENTER
  read_scope: ["core/example/**", "tests/example/**"]
  write_mask: ["core/example/queue-worker.ts"]
  authority_context:
    governance_type: PROJECT_POLICY_BINDING_REQUIRED
    reference: "<capability-or-lease-reference>"
    production_mutation_authorized: true
    adoption_authorized: false
  allowed_actions: [read_file, run_test_command, edit_file_in_write_mask, propose_patch]
  forbidden_actions: [git_commit, modify_files_outside_write_mask, weaken_test_assertions, issue_certification_verdict]
  stop_conditions: [write_mask_violation_attempted, regression_observed_in_adjacent_test, context_budget_exceeded]
  completion_conditions: [all_done_state_conditions_satisfied]
  maximum_allowable_status:
    verdicts: [IMPLEMENTATION_SELF_CHECK_PASSED, IMPLEMENTATION_PARTIAL, IMPLEMENTATION_FAILED]
    promotion_states: [READY_FOR_INDEPENDENT_REAUDIT, NOT_READY_FOR_REAUDIT]
  next_station_rule: FALSIFIER

model_profile_adapter:
  # All values are illustrative and unqualified; qualify per model before use.
  target_model_family: "MODEL_FAMILY_A"
  packaging_format: YAML_INDENTED
  context_budget_tokens: 8000
  effective_recall_horizon: PIN_INVARIANTS_AT_END
  structural_delimiters: CODE_BLOCK_YAML
```

---

## 4. Reference JSON Schema

For static validation by a future prompt compiler. `$defs/StationPolicy` is also the schema for the station-policy fragments in Appendix C.

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "title": "PGLLPromptContract (reference schema, PROPOSED)",
  "type": "object",
  "required": ["contract_id", "timestamp", "invariant_job_contract", "station_policy"],
  "additionalProperties": false,
  "properties": {
    "contract_id": { "type": "string", "minLength": 1 },
    "timestamp": { "type": "string", "pattern": "^\\d{4}-\\d{2}-\\d{2}T\\d{2}:\\d{2}:\\d{2}Z$" },
    "compiler_version": { "type": "string" },
    "invariant_job_contract": { "$ref": "#/$defs/InvariantJobContract" },
    "station_policy": { "$ref": "#/$defs/StationPolicy" },
    "model_profile_adapter": { "$ref": "#/$defs/ModelProfileAdapter" }
  },
  "$defs": {
    "StringList": { "type": "array", "items": { "type": "string", "minLength": 1 } },
    "PrecedenceRule": {
      "type": "object",
      "required": ["claim_class", "authoritative_sources", "precedence_rule", "scope"],
      "properties": {
        "claim_class": { "type": "string", "minLength": 1 },
        "authoritative_sources": { "$ref": "#/$defs/StringList" },
        "precedence_rule": { "type": "string", "minLength": 1 },
        "scope": { "type": "string", "minLength": 1 }
      }
    },
    "KnownFact": {
      "type": "object",
      "required": ["fact", "basis", "scope"],
      "properties": {
        "fact": { "type": "string", "minLength": 1 },
        "basis": { "enum": ["living_source", "ratified_policy", "operator_constraint", "scoped_receipt", "formal_reasoning", "trusted_external", "mechanical_test"] },
        "scope": { "type": "string", "minLength": 1 }
      }
    },
    "EvidenceRequirement": {
      "type": "object",
      "required": ["command"],
      "properties": {
        "command": { "type": "string", "minLength": 1 },
        "must_pass_test_identities": { "$ref": "#/$defs/StringList" },
        "must_preserve_identities": { "$ref": "#/$defs/StringList" }
      }
    },
    "AmbiguityRules": {
      "type": "object",
      "required": ["on_contradiction", "stop_when"],
      "properties": {
        "on_contradiction": {
          "type": "array", "minItems": 1,
          "items": { "enum": ["investigate_within_read_scope", "update_local_reality", "emit_reality_delta"] }
        },
        "stop_when": {
          "type": "array", "minItems": 1,
          "items": { "enum": ["authority_boundary", "write_mask_violation", "must_not_change_conflict", "safety", "unresolved_decision_authority", "unacquirable_evidence"] }
        }
      }
    },
    "InvariantJobContract": {
      "type": "object",
      "additionalProperties": false,
      "required": ["mission", "done_state", "source_precedence_rules", "current_reality", "rightful_owners", "invariants", "known_facts", "unknowns", "negative_space", "must_not_change", "evidence_requirements", "ambiguity_rules", "output_contract"],
      "properties": {
        "mission": { "type": "string", "minLength": 1 },
        "done_state": { "$ref": "#/$defs/StringList" },
        "source_precedence_rules": { "type": "array", "minItems": 1, "items": { "$ref": "#/$defs/PrecedenceRule" } },
        "current_reality": { "type": "object" },
        "rightful_owners": { "type": "object" },
        "invariants": { "$ref": "#/$defs/StringList" },
        "known_facts": { "type": "array", "items": { "$ref": "#/$defs/KnownFact" } },
        "unknowns": { "$ref": "#/$defs/StringList" },
        "negative_space": { "$ref": "#/$defs/StringList" },
        "must_not_change": { "$ref": "#/$defs/StringList" },
        "defects": { "type": "array", "items": { "type": "object" } },
        "evidence_requirements": { "type": "array", "items": { "$ref": "#/$defs/EvidenceRequirement" } },
        "ambiguity_rules": { "$ref": "#/$defs/AmbiguityRules" },
        "output_contract": { "type": "object" }
      }
    },
    "AuthorityContext": {
      "type": "object",
      "additionalProperties": false,
      "required": ["governance_type", "production_mutation_authorized", "adoption_authorized"],
      "properties": {
        "governance_type": { "enum": ["OPERATOR_AUTHORIZATION", "RATIFIED_POLICY", "REGISTRY_CAPABILITY", "SIGNED_GRANT_TARGET", "PROJECT_POLICY_BINDING_REQUIRED", "NONE"] },
        "reference": { "type": "string" },
        "production_mutation_authorized": { "type": "boolean" },
        "audit_fixture_write_authorized": { "type": "boolean" },
        "adoption_authorized": { "const": false }
      }
    },
    "StationPolicy": {
      "type": "object",
      "additionalProperties": false,
      "required": ["station_role", "read_scope", "write_mask", "authority_context", "allowed_actions", "forbidden_actions", "stop_conditions", "completion_conditions", "maximum_allowable_status", "next_station_rule"],
      "properties": {
        "station_role": { "enum": ["MAPPER", "ARCHITECT_DENOISER", "IMPLEMENTER", "FALSIFIER", "BOUNDED_REPAIR", "CLEAN_RECONSTRUCTION", "CERTIFIER"] },
        "read_scope": { "$ref": "#/$defs/StringList" },
        "write_mask": { "type": "array", "items": { "type": "string", "minLength": 1 } },
        "authority_context": { "$ref": "#/$defs/AuthorityContext" },
        "allowed_actions": { "$ref": "#/$defs/StringList" },
        "forbidden_actions": { "$ref": "#/$defs/StringList" },
        "stop_conditions": { "$ref": "#/$defs/StringList" },
        "completion_conditions": { "$ref": "#/$defs/StringList" },
        "maximum_allowable_status": {
          "type": "object",
          "additionalProperties": false,
          "required": ["verdicts", "promotion_states"],
          "properties": {
            "verdicts": { "type": "array", "minItems": 1, "items": { "enum": ["REALITY_MAPPED_WITHIN_SCOPE", "MAPPING_BLOCKED", "DESIGN_CONTRACT_COMPLETE", "DESIGN_BLOCKED", "IMPLEMENTATION_SELF_CHECK_PASSED", "IMPLEMENTATION_PARTIAL", "IMPLEMENTATION_FAILED", "SUPPORTED_WITHIN_SCOPE", "FALSIFIED", "REPAIR_SELF_CHECK_PASSED", "REPAIR_PARTIAL", "REPAIR_FAILED", "CLEAN_RECONSTRUCTION_ESTABLISHED", "RECONSTRUCTION_FAILED", "CERTIFIED_WITHIN_DECLARED_SCOPE", "CERTIFIED_WITH_NONBLOCKING_LIMITATIONS", "CERTIFICATION_BLOCKED", "CERTIFICATION_FAILED", "NOT_DETERMINABLE"] } },
            "promotion_states": { "type": "array", "minItems": 1, "items": { "enum": ["READY_FOR_ARCHITECTURE", "READY_FOR_IMPLEMENTATION", "READY_FOR_INDEPENDENT_REAUDIT", "NOT_READY_FOR_REAUDIT", "READY_FOR_CLEAN_RECONSTRUCTION", "RETURN_TO_REPAIR", "READY_FOR_INDEPENDENT_CERTIFICATION", "NOT_READY_FOR_CERTIFICATION", "READY_FOR_GOVERNED_ADOPTION_DECISION", "NOT_READY_FOR_ADOPTION", "FURTHER_EVIDENCE_REQUIRED"] } }
          }
        },
        "next_station_rule": { "type": "string", "minLength": 1 }
      },
      "allOf": [
        {
          "if": { "properties": { "station_role": { "const": "CERTIFIER" } }, "required": ["station_role"] },
          "then": { "properties": { "write_mask": { "maxItems": 0 } } },
          "else": { "properties": { "maximum_allowable_status": { "properties": { "verdicts": { "items": { "not": { "pattern": "^CERTIF" } } } } } } }
        }
      ]
    },
    "ModelProfileAdapter": {
      "type": "object",
      "properties": {
        "target_model_family": { "type": "string" },
        "packaging_format": { "enum": ["YAML_INDENTED", "XML_TAGGED", "MARKDOWN_P_GLL", "JSON_STRICT"] },
        "context_budget_tokens": { "type": "integer", "minimum": 1 },
        "effective_recall_horizon": { "type": "string" },
        "structural_delimiters": { "type": "string" },
        "few_shot_examples": { "type": "array", "items": { "type": "object" } }
      }
    }
  }
}
```

The schema checks that a status ceiling uses known values, that only a `CERTIFIER` lists `CERTIF*` verdicts, and that a `CERTIFIER` has an empty write mask. The per-role subset rule (a seat's ceiling must be a subset of its own row in Appendix C §1) is a table check, not a schema check.

---

## 5. Epistemic Uncertainty Representation

The schema forces explicit representation of uncertainty (`TOPIC-PGLL-11`):

1. **`known_facts` carry `basis` and `scope`.** A fact needs a stated basis, not necessarily a mechanical test. Supported bases are `living_source`, `ratified_policy`, `operator_constraint`, `scoped_receipt` (valid for its baseline), `formal_reasoning`, `trusted_external` and `mechanical_test`. If a claim's basis cannot be stated, place it under `unknowns`. `known_facts != unknowns`.
2. **`ambiguity_rules` are structured, not a blanket halt.** `CONTRADICTION_DISCOVERED != CONTRADICTION_REQUIRES_STOP`. On a contradiction the station first investigates within its authorized read scope, updates its local picture of reality, and emits a reality delta. It halts only when one of the `stop_when` conditions prevents safe continuation: an authority boundary, a write-mask violation, a must-not-change conflict, a safety issue, an unresolved decision authority, or evidence that cannot be acquired within scope (`TOPIC-ANTI-14`).
3. **Maturity flags apply to maturity-sensitive claims.** A contract that relies on a runtime mechanism whose existence matters to the task should state its classification (`PRODUCTION`, `EXPERIMENTAL_RUNTIME`, `SPECIFIED_NOT_IMPLEMENTED`, `NOT_APPLICABLE`, `NOT_DETERMINABLE`). Incidental symbols need no flag.
4. **Illustrative values stay illustrative.** Context budgets, recall placements, identifiers and lease references in templates are examples. Qualify them before use, and never present them as measured.
5. **Authority is context, not grant.** `authority_context` describes the governed authority; `known_facts != authority_grant`.


---


# Appendix C: Reference Station Templates

> *"A station is not a person or a model brand. A station is an operational role in a cognitive assembly line, defined by its mission, write mask, and authority boundaries."*

---

## 1. Status, Operating Rules, and the Status Table

These are **reference station templates that require project-specific policy binding**. They are not production-ready or copy-paste ready: they contain illustrative policy choices (path globs, action names) that a project must replace, and they have not been independently audited.

### How the templates relate to Appendix B

Each template is the complete **`station_policy` layer** of a contract in the [Appendix B](#appendix-b-p-gll-prompt-contract-schema) schema (all ten Layer 2 fields). It validates as `$defs/StationPolicy`. Composed with an Appendix B `invariant_job_contract` (and an optional `model_profile_adapter`), it forms a full contract. Evidence requirements, precedence rules and ambiguity rules live in the job-contract layer, so each template lists recommended `evidence_requirements` entries in prose rather than as policy fields.

### Core station rules
1. **`STATION > MODEL_IDENTITY` (`LAW-FND-01`):** Templates are vendor-neutral. A model fills a seat only if it is **qualified** for it: tool support, context capacity, qualification evidence, permissions and provider availability. Capability alone, or conformance to prompt text, is not qualification.
2. **`PRIMARY_ROLE != EPISTEMIC_BLINDNESS` (`LAW-FND-05`):** Role specialization must not artificially blind reasoning within the authorized observation scope. A station's role restricts what it may mutate and what status it may claim, and its `read_scope` is an authorization boundary, not a blindfold.
3. **`NO_SELF_CERTIFICATION` (`TOPIC-STAT-10`):** The Implementer and Bounded Repair seats may never issue a certification verdict. `adoption_authorized` is `false` for every seat (`LAW-GOV-04`).
4. **Precedence is claim-sensitive.** Templates do not rank sources. They defer to the claim-scoped `source_precedence_rules` of the job contract (`LAW-REAL-02`): for example, intent claims defer to the approved specification, and claims about current existence or behavior defer to living source and execution evidence.

### The status table

This is the **one authoritative status table** for the book. Chapters and appendices reference it and do not restate alternative vocabularies. Every station reports three independent axes:

- `station_completion`: did the station finish? `COMPLETE`, `PARTIAL` or `BLOCKED` for every seat.
- `verdict`: what the station found, within its own competence.
- `promotion_state`: what may happen next.

| Role | `verdict` values | `promotion_state` values |
| :--- | :--- | :--- |
| MAPPER | `REALITY_MAPPED_WITHIN_SCOPE`, `MAPPING_BLOCKED`, `NOT_DETERMINABLE` | `READY_FOR_ARCHITECTURE`, `FURTHER_EVIDENCE_REQUIRED` |
| ARCHITECT_DENOISER | `DESIGN_CONTRACT_COMPLETE`, `DESIGN_BLOCKED`, `NOT_DETERMINABLE` | `READY_FOR_IMPLEMENTATION`, `FURTHER_EVIDENCE_REQUIRED` |
| IMPLEMENTER | `IMPLEMENTATION_SELF_CHECK_PASSED`, `IMPLEMENTATION_PARTIAL`, `IMPLEMENTATION_FAILED` | `READY_FOR_INDEPENDENT_REAUDIT`, `NOT_READY_FOR_REAUDIT` |
| FALSIFIER | `SUPPORTED_WITHIN_SCOPE`, `FALSIFIED`, `NOT_DETERMINABLE` | `READY_FOR_CLEAN_RECONSTRUCTION`, `RETURN_TO_REPAIR`, `FURTHER_EVIDENCE_REQUIRED` |
| BOUNDED_REPAIR | `REPAIR_SELF_CHECK_PASSED`, `REPAIR_PARTIAL`, `REPAIR_FAILED` | `READY_FOR_INDEPENDENT_REAUDIT`, `NOT_READY_FOR_REAUDIT` |
| CLEAN_RECONSTRUCTION | `CLEAN_RECONSTRUCTION_ESTABLISHED`, `RECONSTRUCTION_FAILED`, `NOT_DETERMINABLE` | `READY_FOR_INDEPENDENT_CERTIFICATION`, `NOT_READY_FOR_CERTIFICATION` |
| CERTIFIER | `CERTIFIED_WITHIN_DECLARED_SCOPE`, `CERTIFIED_WITH_NONBLOCKING_LIMITATIONS`, `CERTIFICATION_BLOCKED`, `CERTIFICATION_FAILED` | `READY_FOR_GOVERNED_ADOPTION_DECISION`, `NOT_READY_FOR_ADOPTION` |

Rules that go with the table:

```text
THE THREE AXES ARE INDEPENDENT (completion != verdict != promotion_state)
ONLY THE CERTIFIER MAY EMIT A CERTIF* VERDICT
IMPLEMENTER AND BOUNDED_REPAIR MAY NEVER ISSUE A CERTIFICATION VERDICT
CERTIFICATION != ADOPTION
READY_FOR_GOVERNED_ADOPTION_DECISION != ADOPTED
```

A Certifier may emit a scoped certification verdict. It may not mint adoption authority. Adoption is a governance act by valid governance authority and is not a seat verdict. Older drafts of this book used single-string ceilings such as `READY_FOR_OPERATOR_REVIEW` and `IMPLEMENTATION_DRAFT_READY_FOR_FALSIFICATION`; those aliases are superseded by this table.

---

## 2. Station 1: The Mapper Template

**Mission:** Explore an unknown codebase slice, trace runtime call paths, and build an accurate topological reality graph without modifying code. The Mapper *records* contradictions between runtime and documents; discovering them is its job. Unresolved reachability is reported as `NOT_DETERMINABLE`, never guessed.

```yaml
station_policy:
  station_role: MAPPER
  read_scope: ["core/**", "api/**", "docs/**"]
  write_mask: []
  authority_context:
    governance_type: NONE
    production_mutation_authorized: false
    adoption_authorized: false
  allowed_actions: [read_file, list_directory, grep_search, symbol_trace]
  forbidden_actions: [edit_file, write_to_file, git_commit, execute_destructive_commands]
  stop_conditions: [token_budget_exhausted, read_scope_exhausted, authority_boundary]
  completion_conditions: [target_subsystem_boundary_mapped_or_marked_not_determinable]
  maximum_allowable_status:
    verdicts: [REALITY_MAPPED_WITHIN_SCOPE, MAPPING_BLOCKED, NOT_DETERMINABLE]
    promotion_states: [READY_FOR_ARCHITECTURE, FURTHER_EVIDENCE_REQUIRED]
  next_station_rule: ARCHITECT_DENOISER
```

**Recommended `evidence_requirements`:** every mapped file with its confirmed path; every call-graph edge with line numbers from living source; for runtime-behavior claims, evidence from the executed artifact (for example the compiled `dist/**` that actually runs), not only the source text.

---

## 3. Station 2: The Architect / Denoiser Template

**Mission:** Ingest raw mapper graphs, filter conversational noise and irrelevant dependencies, and specify a minimal, invariant-preserving design contract.

```yaml
station_policy:
  station_role: ARCHITECT_DENOISER
  read_scope: ["docs/P-GLL/**", "core/contracts/**", "receipts/**"]
  write_mask: ["docs/P-GLL/plans/**"]
  authority_context:
    governance_type: PROJECT_POLICY_BINDING_REQUIRED
    production_mutation_authorized: false
    adoption_authorized: false
  allowed_actions: [read_file, write_plan_specification, define_invariants, define_truth_tables]
  forbidden_actions: [edit_production_source, edit_tests, claim_implementation_complete]
  stop_conditions: [authority_boundary, write_mask_violation_attempted, unresolved_decision_authority]
  completion_conditions: [truth_tables_orthogonal, rightful_owners_identified, negative_space_declared]
  maximum_allowable_status:
    verdicts: [DESIGN_CONTRACT_COMPLETE, DESIGN_BLOCKED, NOT_DETERMINABLE]
    promotion_states: [READY_FOR_IMPLEMENTATION, FURTHER_EVIDENCE_REQUIRED]
  next_station_rule: IMPLEMENTER_VIA_PROJECT_REVIEW_GATE_IF_POLICY_REQUIRES
```

Whether a human review gate sits between design and implementation is a **project policy parameter** (`GOVERNED != ALWAYS_MANUAL`). Some campaigns, such as Pass 1C, require explicit operator authorization; bind that in `next_station_rule` where it applies.

**Recommended `evidence_requirements`:** pre-implementation multi-dimensional truth tables for concurrent states; explicit negative space and must-not-change declarations; each claimed defect class mapped to a root-cause mechanism with its evidence basis.

---

## 4. Station 3: The Implementer Template

**Mission:** Translate an approved architectural specification into code changes inside a tightly bounded write mask.

```yaml
station_policy:
  station_role: IMPLEMENTER
  read_scope: ["core/subsystem/**", "tests/subsystem/**", "docs/plans/**"]
  write_mask: ["core/subsystem/target-module.ts"]
  authority_context:
    governance_type: PROJECT_POLICY_BINDING_REQUIRED
    reference: "<capability-or-lease-reference>"
    production_mutation_authorized: true
    adoption_authorized: false
  allowed_actions: [read_file, edit_file_in_write_mask, run_local_test_command, propose_patch]
  forbidden_actions: [edit_files_outside_write_mask, git_commit, git_push, modify_test_assertions_to_hide_failures, issue_certification_verdict]
  stop_conditions: [write_mask_boundary_collision, regression_in_existing_module_tests, authority_boundary]
  completion_conditions: [all_acceptance_criteria_in_job_contract_satisfied]
  maximum_allowable_status:
    verdicts: [IMPLEMENTATION_SELF_CHECK_PASSED, IMPLEMENTATION_PARTIAL, IMPLEMENTATION_FAILED]
    promotion_states: [READY_FOR_INDEPENDENT_REAUDIT, NOT_READY_FOR_REAUDIT]
  next_station_rule: FALSIFIER
```

On precedence: intent claims defer to the approved specification and claims about current existence or behavior defer to living source (see the job contract's `source_precedence_rules`). That is why an Implementer that finds the plan contradicted by living source records a reality delta instead of forcing the plan (Chapter 7 §4).

**Recommended `evidence_requirements`:** local test command with raw output; unified diff restricted to the write mask; a self-check report against declared invariants (a self-check, not an audit).

---

## 5. Station 4: The Falsifier Template

**Mission:** Run an adversarial audit of an implementation proposal, actively trying to break its claims, reveal edge-case bugs and expose fixture masking.

```yaml
station_policy:
  station_role: FALSIFIER
  read_scope: ["core/**", "tests/**", "receipts/**"]
  write_mask: ["tests/adversarial/**"]
  authority_context:
    governance_type: PROJECT_POLICY_BINDING_REQUIRED
    production_mutation_authorized: false
    audit_fixture_write_authorized: true
    adoption_authorized: false
  allowed_actions: [read_file, author_falsification_test, run_test_command, execute_stress_or_fault_injection]
  forbidden_actions: [edit_production_source, weaken_assertions, accept_claims_without_mechanical_falsifier_run]
  stop_conditions: [claim_falsified_with_reproduction, adversarial_budget_exhausted, authority_boundary]
  completion_conditions: [claim_supported_within_scope_after_bounded_budget]
  maximum_allowable_status:
    verdicts: [SUPPORTED_WITHIN_SCOPE, FALSIFIED, NOT_DETERMINABLE]
    promotion_states: [READY_FOR_CLEAN_RECONSTRUCTION, RETURN_TO_REPAIR, FURTHER_EVIDENCE_REQUIRED]
  next_station_rule: CLEAN_RECONSTRUCTION_IF_SUPPORTED_ELSE_BOUNDED_REPAIR
```

The two authority flags carry the intended distinction: `production_mutation_authorized: false` (a Falsifier does not repair production code during audit) and `audit_fixture_write_authorized: true` (it may write adversarial fixtures under its mask). The `adversarial_budget` is declared in the job contract, so "all hypotheses exhausted" is never an unbounded condition.

**Recommended `evidence_requirements`:** reconstructable command string and environment; exact test identities executed; raw failure trace and a causal hypothesis if falsified.

---

## 6. Station 5: The Bounded Repair Template

**Mission:** Fix a concrete failure identified by the Falsifier, operating on the rightful owner module without unauthorized scope expansion.

```yaml
station_policy:
  station_role: BOUNDED_REPAIR
  read_scope: ["core/subsystem/**", "tests/**"]
  write_mask: ["core/subsystem/rightful-owner.ts"]
  authority_context:
    governance_type: PROJECT_POLICY_BINDING_REQUIRED
    production_mutation_authorized: true
    adoption_authorized: false
  allowed_actions: [read_file, edit_file_in_write_mask, run_reproduction_test]
  forbidden_actions: [edit_files_outside_rightful_owner, modify_falsifier_test_expectations, refactor_unrelated_code, issue_certification_verdict]
  stop_conditions: [scope_expansion_required_request_authority, regression_in_subsystem_suite, authority_boundary]
  completion_conditions: [falsifier_reproduction_test_passes, zero_regressions_in_subsystem_suite]
  maximum_allowable_status:
    verdicts: [REPAIR_SELF_CHECK_PASSED, REPAIR_PARTIAL, REPAIR_FAILED]
    promotion_states: [READY_FOR_INDEPENDENT_REAUDIT, NOT_READY_FOR_REAUDIT]
  next_station_rule: FALSIFIER
```

If the evidence shows the defect's rightful owner lies outside the mask, the station halts and requests authority; it does not expand scope silently (Chapter 8 §4).

**Recommended `evidence_requirements`:** a passing run of the exact test identity that previously failed; a passing regression run; an explanation of why the fix closes the failure class, not just the instance.

---

## 7. Station 6: The Clean Reconstruction Template

**Mission:** Ingest a dirty verified repair proposal, extract the minimal attributed file set, and reconstruct a candidate (baseline plus declared delta, manifest and verification root) so the subject certified is the subject proposed. A clean isolated checkout is one materialization; an equivalent frozen subject is also valid.

```yaml
station_policy:
  station_role: CLEAN_RECONSTRUCTION
  read_scope: ["dirty-worktree/**", "candidate-materialization/**"]
  write_mask: ["candidate-materialization/**"]
  authority_context:
    governance_type: PROJECT_POLICY_BINDING_REQUIRED
    production_mutation_authorized: false
    adoption_authorized: false
  allowed_actions: [read_file, copy_attributed_files, compute_sha256_digests, verify_byte_identity]
  forbidden_actions: [invent_new_code_fixes, include_unattributed_or_scratch_files, alter_git_history]
  stop_conditions: [unattributed_dirty_file_detected, authority_boundary]
  completion_conditions: [candidate_assembled, payload_root_digest_computed]
  maximum_allowable_status:
    verdicts: [CLEAN_RECONSTRUCTION_ESTABLISHED, RECONSTRUCTION_FAILED, NOT_DETERMINABLE]
    promotion_states: [READY_FOR_INDEPENDENT_CERTIFICATION, NOT_READY_FOR_CERTIFICATION]
  next_station_rule: CERTIFIER
```

Reconstruction packages; it does not repair.

**Recommended `evidence_requirements`:** a finite attributed manifest with per-file SHA-256 digests; the combined payload root digest; evidence that the candidate contains no scratch, log or unapproved artifacts.

---

## 8. Station 7: The Certifier Template

**Mission:** Run an independent, non-mutating validation battery against a reconstructed candidate, in an isolated sandbox or an equivalent topology that preserves subject identity, execution isolation and evidence separation (Chapter 17 §9), and produce a durable certification receipt.

```yaml
station_policy:
  station_role: CERTIFIER
  read_scope: ["candidate-tree/**", "test-battery/**"]
  write_mask: []
  authority_context:
    governance_type: PROJECT_POLICY_BINDING_REQUIRED
    production_mutation_authorized: false
    adoption_authorized: false
  allowed_actions: [read_candidate_source, execute_frozen_test_battery, verify_payload_root_digest, emit_certification_receipt]
  forbidden_actions: [edit_candidate_files, edit_tests, commit_to_production, grant_adoption]
  stop_conditions: [payload_digest_mismatch, certification_harness_defect, authority_boundary]
  completion_conditions: [all_verification_gates_evaluated]
  maximum_allowable_status:
    verdicts: [CERTIFIED_WITHIN_DECLARED_SCOPE, CERTIFIED_WITH_NONBLOCKING_LIMITATIONS, CERTIFICATION_BLOCKED, CERTIFICATION_FAILED]
    promotion_states: [READY_FOR_GOVERNED_ADOPTION_DECISION, NOT_READY_FOR_ADOPTION]
  next_station_rule: GOVERNED_ADOPTION_DECISION
```

A test failure is not simply `CERTIFICATION_FAILED`. The Certifier first classifies it: a new failure identity is a `REGRESSION_CANDIDATE` (Chapter 16 §6), and the defect is routed to its rightful owner: implementation, reconstruction, harness, baseline staleness or policy gap (Chapter 17 §8). A harness defect or insufficient evidence yields `CERTIFICATION_BLOCKED` with the missing evidence stated, not a blind rejection.

**Recommended `evidence_requirements`:** pre-execution and post-execution candidate payload root digests (they must match); full command list, exit codes and test identities; an explicit statement that certification is not adoption.


---


# Appendix D: Receipt Schema

> *"A receipt is a durable structured record of claims, observations and evidence. It records; it does not prove."*

---

## 1. Overview, Maturity Notice and Core Invariants

The **Orion Receipt Schema** is a reference data contract for recording the mechanical results of a station run. Receipts are the batons passed between stations.

**Maturity notice:** The schema is `PROPOSED`. Orion today records receipts in several forms (for example the JSONL ledgers under `data/receipts/`), but the **hash-chaining** described in Section 4 (`parent_receipt_id` and `parent_receipt_sha256`) is `SPECIFIED_NOT_IMPLEMENTED`: no such chaining exists in `core/`.

### Core laws
1. **`RECEIPTS_CARRY_OUTCOMES_NOT_THOUGHTS` (`TOPIC-RCPT-01`):** Do not record chain-of-thought monologues or speculative musings. Record what was executed, what was observed and what was verified within scope.
2. **`RECEIPT != PROOF` (`LAW-EVD-04`):** A receipt is a durable structured record of claims, observations, outcomes, provenance and supporting evidence. Its existence does not show that an action occurred or that a claim is true.
3. **`IMMUTABILITY_REQUIRES_AN_IMMUTABILITY_MECHANISM` (`LAW-EVD-04`):** A file on an ordinary filesystem is not immutable. Digests, signatures and hash chains provide tamper-evidence. Immutability requires enforced write-once or append-only storage and permissions. Durability requires sync barriers.
4. **`STALE != FALSE` (`LAW-EVD-05`):** A properly verified receipt is a correct record of what was verified against its baseline. Its current applicability needs a freshness check against the claim's dependency boundary.

---

## 2. Receipt Field Specification

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        ORION RECEIPT ANATOMY                           │
├────────────────────────────────────────────────────────────────────────┤
│ 1. HEADER & PROVENANCE                                                 │
│    • receipt_id            • contract_id        • schema_version       │
│    • created_at            • station_role       • model_identity       │
│    • author_kind           • execution_environment                     │
├────────────────────────────────────────────────────────────────────────┤
│ 2. TARGET SUBJECT & BASELINE                                           │
│    • baseline_commit       • subject_kind       • subject_root_sha256  │
│    • attributed_file_manifest                                          │
├────────────────────────────────────────────────────────────────────────┤
│ 3. MISSION & CLAIMS                                                    │
│    • mission               • claims_evaluated                          │
├────────────────────────────────────────────────────────────────────────┤
│ 4. MECHANICAL EVIDENCE                                                 │
│    • commands_executed     • test_summary       • passing_identities   │
│    • failure_identities    • mutations_performed • artifact_digests    │
├────────────────────────────────────────────────────────────────────────┤
│ 5. EPISTEMIC QUALIFIERS                                                │
│    • uncertainties         • limitations        • stochastic_parameters│
├────────────────────────────────────────────────────────────────────────┤
│ 6. STATUS & HANDOFF  (three independent axes; Appendix C §1)           │
│    • station_completion    • verdict            • promotion_state      │
│    • next_station_rule                                                 │
├────────────────────────────────────────────────────────────────────────┤
│ 7. INTEGRITY (target mechanism)                                        │
│    • receipt_payload_sha256  • parent_receipt_id • parent_receipt_sha256│
└────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Reference YAML Template

All identifiers and digests are illustrative; `sha256:<64-hex-placeholder>` stands for `sha256:` followed by exactly 64 hexadecimal characters.

```yaml
# ILLUSTRATIVE_EXAMPLE: invented identifiers, not a record of any real run.
receipt_id: "RCPT-ILLUSTRATIVE-FALSIFIER-003"
schema_version: "orion-receipt-reference-v1"
created_at: "2026-10-01T16:30:00Z"
contract_id: "ILLUSTRATIVE-CONTRACT-002"

provenance:
  station_role: FALSIFIER
  model_identity: "model-family-a"   # recorded for calibration, not authority
  author_kind: AI_STATION            # AI_STATION | HUMAN_OPERATOR | AUTOMATED_CI
  execution_environment:
    os: "example-os"
    shell: "example-shell"
    runtime_versions: { node: "<version>", npm: "<version>" }

target_subject:
  baseline_commit: "<commit-sha>"
  subject_kind: CLEAN_RECONSTRUCTION_CANDIDATE   # DIRTY_WORKTREE | CLEAN_CANDIDATE | REPO_HEAD | CLEAN_RECONSTRUCTION_CANDIDATE
  subject_root_sha256: "sha256:<64-hex-placeholder>"
  attributed_file_manifest:
    - path: "core/example/queue-worker.ts"
      sha256: "sha256:<64-hex-placeholder>"
    - path: "tests/example/queue-worker.test.ts"
      sha256: "sha256:<64-hex-placeholder>"

mission: >
  Adversarially falsify whether QueueWorker releases its lease only after
  in-flight work has settled.

claims_evaluated:
  - claim_id: "CLM-001"
    statement: "Settled failures release writer authority."
    status: SUPPORTED_WITHIN_SCOPE
  - claim_id: "CLM-002"
    statement: "A background timer cannot overwrite a settled task result."
    status: SUPPORTED_WITHIN_SCOPE

mechanical_evidence:
  commands_executed:
    - command: "npm test -- tests/example/queue-worker.test.ts"
      exit_code: 0
      execution_time_ms: 1420
      stdout_sha256: "sha256:<64-hex-placeholder>"
  test_summary: { total_evaluated: 12, passed_count: 12, failed_count: 0 }
  # Identities are required; counts alone do not substitute for them (LAW-EVD-02).
  passing_identities: ["QW-SHUTDOWN-RELEASES-LEASE", "QW-NORMAL-COMPLETION"]
  failure_identities: []
  mutations_performed: []          # fixture writes only for a Falsifier; empty here
  artifact_digests:
    test_run_log: "artifacts/rcpt-003/run.log (sha256:<64-hex-placeholder>)"

epistemic_qualifiers:
  uncertainties:
    - "Disconnection during teardown was not tested."
  limitations:
    - "Audit bounded to the declared write-mask neighborhood; distributed workers not covered."
  stochastic_parameters: { runs_executed: 5, concurrency_level: 4, observed_failure_rate: 0.0 }

station_completion: COMPLETE
verdict: SUPPORTED_WITHIN_SCOPE
promotion_state: READY_FOR_CLEAN_RECONSTRUCTION
next_station_rule: CLEAN_RECONSTRUCTION

integrity:                          # target mechanism; SPECIFIED_NOT_IMPLEMENTED
  receipt_payload_sha256: "sha256:<64-hex-placeholder>"
  parent_receipt_id: "RCPT-ILLUSTRATIVE-IMPLEMENTER-002"
  parent_receipt_sha256: "sha256:<64-hex-placeholder>"
```

The `verdict` and `promotion_state` values come from the single status table in [Appendix C §1](#appendix-c-reference-station-templates), including the Certifier's verdicts. This appendix does not define a separate vocabulary.

---

## 4. Integrity: Tamper-Evidence, Immutability and Durability

A receipt becomes **tamper-evident**, not magically immutable, only when a mechanism makes alteration detectable. Orion's target convention has three parts:

1. **Payload digest (`receipt_payload_sha256`):** SHA-256 over a canonicalized form of the receipt. The canonicalization should be a published standard such as RFC 8785 (JSON Canonicalization Scheme), not an ad-hoc rule. The digest field is **excluded from its own input**; otherwise the digest would have to contain itself.
2. **Hash chaining (`parent_receipt_id`, `parent_receipt_sha256`):** Each receipt records the digest of the receipt of the station run that preceded it, so later alteration of an earlier receipt becomes detectable across stations. This is `SPECIFIED_NOT_IMPLEMENTED`.
3. **Storage separation:** Receipts live in dedicated receipt trees (`receipts/` or content-addressed artifact stores), separate from commit messages and PR descriptions, which only *reference* them (`TOPIC-RCPT-07`).

What this does and does not buy:

```text
HASHES / SIGNATURES / CHAINS  -> TAMPER-EVIDENCE   (alteration is detectable)
WRITE-ONCE OR ENFORCED APPEND-ONLY STORAGE -> IMMUTABILITY   (alteration is prevented)
SYNC BARRIERS                 -> DURABILITY        (the record survives a crash)
NONE OF THESE                 -> TRUTH             (a receipt is still a claim plus evidence)
```


---


# Appendix E: Reality Spine / reality.verify Conceptual Schema

> *"The Reality Spine is not an autonomous daemon; it is a declarative architectural contract that bounds repository truth, preventing models from wandering into infinite search spaces."*

---

## 1. Architectural Status and Maturity Boundary

**EPISTEMIC NOTICE:**
This specification is **target conceptual architecture** (`PROPOSED` / `SPECIFIED_NOT_IMPLEMENTED`).
- In current working practice, Reality Spines are declared as structured Markdown files, allowlists and targeted test manifests, as in the Pass 1C and M5 R2 planning artifacts.
- The automated verbs (`reality.compile`, `reality.verify`) and any runtime graph store described here are target implementations designed to formalize that manual discipline. The paths and identifiers below are illustrative.

---

## 2. Core Architectural Laws

1. **`DECLARED_REALITY != CANONICAL_REALITY` (`TOPIC-REPO-03`):** A declared spine is a human- or compiler-specified allowlist of files, tests and invariants believed to represent ground truth. It becomes canonical only when governance formally adopts it. If live runtime code reaches outside the boundary, declared reality is incomplete.
2. **`UNDECLARED != IRRELEVANT` (`LAW-REAL-04`):** Files omitted from the spine do not vanish. If an unmapped file mutates or introduces a side effect, that is a **Reality Spine Gap** requiring investigation.
3. **`REALITY_ROOT_MATCH != ARCHITECTURAL_CORRECTNESS` (`LAW-REC-03`):** A matching root checksum is strong mechanical evidence of sameness with an approved snapshot, under the chosen canonicalization boundary. It does not show that the system is free of bugs.
4. **`COPILOT_ESTABLISHES_MEANING; VERB_ESTABLISHES_SAMENESS` (`TOPIC-COPV-01`):** Reasoning models analyze semantics and author invariants; deterministic Verbs compute digests and compare bytes.

---

## 3. The Reality Spine Declarative Schema

A manifest defines the topological universe for one engineering mission:

```yaml
# ILLUSTRATIVE_EXAMPLE: conceptual schema, invented paths and digests.
spine_id: "ILLUSTRATIVE-SPINE-ORCHESTRATION"
version: "0.1.0"
mode: HEAD        # HEAD | WORKTREE | CERTIFIED_SNAPSHOT

scope_declaration:
  description: "Bounded reality for an orchestration lifecycle repair."
  root_paths: ["core/orchestration", "tests/orchestration"]
  excluded_paths:               # explicit negative space; omission is intentional
    - "core/example/dormant-classifier.ts"
    - "core/experimental/**"

topology_graph:
  - source_file: "core/orchestration/cascade-service.ts"
    subsystem: "core/orchestration"
    rightful_owner: "OrchestratorLifecycleManager"
    verified_hash: "sha256:<64-hex-placeholder>"
    associated_tests:
      - test_file: "tests/orchestration/cascade-timeout.test.ts"
        test_identities: ["ORCH-TIMEOUT-NORMAL-EXPIRATION"]
    associated_decisions:
      - decision_doc: "docs/example/decisions/lifecycle-decision.md"
        status: ILLUSTRATIVE
    associated_receipts:
      - receipt_id: "RCPT-ILLUSTRATIVE-FALSIFIER-003"
        sha256: "sha256:<64-hex-placeholder>"

merkle_roots:
  source_tree_root_sha256: "sha256:<64-hex-placeholder>"
  test_tree_root_sha256: "sha256:<64-hex-placeholder>"
  combined_reality_root: "sha256:<64-hex-placeholder>"

invariants:
  - "Every file under core/orchestration has at least one associated test."
  - "No reachable import crosses into excluded_paths."
```

---

## 4. Verification Modes

The repository mode (`DISCOVERED_REPOSITORY(mode)`, Chapter 12 §2) selects what is verified:

```text
┌────────────────────────────────────────────────────────────────────────┐
│ 1. HEAD MODE                                                           │
│    Verifies the declared spine against the selected HEAD commit.       │
│    Reports uncommitted modifications in declared files as drift.       │
├────────────────────────────────────────────────────────────────────────┤
│ 2. WORKTREE MODE                                                       │
│    Verifies the working directory including dirty uncommitted edits,   │
│    and reports deltas against the verified baseline hashes.            │
├────────────────────────────────────────────────────────────────────────┤
│ 3. CERTIFIED_SNAPSHOT MODE                                             │
│    Verifies an explicit frozen subject against its freeze certificate. │
│    Extra, missing or altered bytes are all mismatches.                 │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 5. Conceptual Verb Interfaces

In the target architecture, models interact with repository reality through two Verbs. The interfaces below are the same as in Chapter 13 §4, which governs.

### `reality.compile`
- **Intent:** Ingest the declaration manifest, git state and coverage rules; construct the deterministic index and root digests.
- **Inputs:** `declaration_manifest_path`, `target_commit_sha`, `coverage_rules_path`.
- **Outputs:** `ok`, `compiled_spine_path`, `reality_root_hash`, `leaf_count`.

### `reality.verify`
- **Intent:** Compare physical files against a compiled spine.
- **Inputs:** `compiled_spine_path`, `repository_mode` (`HEAD | WORKTREE | CERTIFIED_SNAPSHOT`), `depth` (`FAST_HASH | DEEP_COVERAGE`).
- **Outputs:**
  - `status`: `VERIFIED | STALE | SOURCE_MISMATCH | REALITY_SPINE_GAP | INVALID_MANIFEST`
  - `mismatch_details`: for each mismatch, `kind` (`MUTATED | UNATTRIBUTED_FILE`), the path, and the expected and actual digests; a declared file missing from disk is `INVALID_MANIFEST`.
  - `execution_receipt_id`.


---


# Appendix F: Managed Verb Contract

> *"A Managed Verb encapsulates high-variance tools inside a deterministic execution harness. The model defines the semantic goal; the Managed Verb, where one is specified, owns retries, idempotency checks and receipts."*

---

## 1. Architectural Status and Core Doctrine

**EPISTEMIC NOTICE:**
This specification defines a reference contract schema for **Managed Verbs** (`PROPOSED` / `SPECIFIED_NOT_IMPLEMENTED`). In current production runtime, deterministic tools exist as individual service wrappers and routines; no unified Managed Verb runtime exists.

A Verb is not necessarily managed. A Verb may be internally simple: `system.status` needs neither checkpointing nor an idempotency key (Chapter 11 §6). The mechanisms below apply when a Verb is long-running, expensive or partially completable.

### Core laws
1. **`VERB_ATOMICITY_IS_SEMANTIC_NOT_PROCEDURAL` (`LAW-VRB-01`):** A Verb represents a complete domain action (for example `git.commit_clean_patch`), not a primitive syscall.
2. **`IDEMPOTENCY_KEY != IDEMPOTENCY`:** A string labeled `idempotency_key` does not make an operation idempotent. Idempotency requires the underlying mutator to evaluate prior state and prevent duplicate effects.
3. **`RETRY_EXHAUSTION != SEMANTIC_UNCERTAINTY`:** Exhausting five retries of a network call is a mechanical failure. It means the operation failed under its policy, not that an LLM should be invoked to "think" about it.
4. **`LLM_ENTERS_ON_UNCERTAINTY; LLM_EXITS_WHEN_UNCERTAINTY_COMPILED_AWAY` (`LAW-VRB-02`):** No LLM runs inside the Verb. When a real semantic ambiguity appears, the Verb returns a typed outcome to its caller, which may bring in a reasoning station.

---

## 2. Reference Managed Verb Contract Schema

```yaml
# ILLUSTRATIVE_EXAMPLE: reference schema, not an implemented contract.
verb_id: "git.commit_clean_attributed_patch"
version: "0.1.0"
semantic_intent: >
  Apply a verified unified patch to a clean isolated worktree, verify that only
  attributed files were modified, and record a commit with receipt lineage.

input_schema:
  type: object
  required: [patch_diff, attributed_files, commit_message, receipt_id, baseline_commit]
  properties:
    patch_diff: { type: string }
    attributed_files: { type: array, items: { type: string } }
    commit_message: { type: string }
    receipt_id: { type: string }
    baseline_commit: { type: string }

output_schema:
  type: object
  required: [commit_sha, tree_sha256, receipt_path, verdict]
  properties:
    commit_sha: { type: string }
    tree_sha256: { type: string }
    receipt_path: { type: string }
    verdict: { type: string, enum: [SUCCESS, FAILED_DIRTY, FAILED_VERIFICATION] }

authority_requirements:
  minimum_governance_level: OPERATOR_AUTHORIZATION   # OPERATOR_AUTHORIZATION | RATIFIED_POLICY | REGISTRY_CAPABILITY
  required_capabilities: [git.write_worktree, receipts.append]
  enforce_write_mask: true

idempotency:
  strategy: CONTENT_HASH_CHECK
  key_derivation: "sha256(patch_diff + baseline_commit)"
  on_duplicate: RETURN_EXISTING_COMMIT_SHA

checkpointing:
  enabled: true
  rollback_mechanism: "git reset --hard <input.baseline_commit>"
  rollback_scope: ISOLATED_WORKTREE_ONLY   # never a shared checkout
  rollback_requires: POLICY_APPROVAL       # destructive; gate it by policy

retry_policy:
  max_attempts: 3
  backoff: EXPONENTIAL
  retryable_errors: [GIT_INDEX_LOCKED, TRANSIENT_IO_ERROR]
  non_retryable_errors: [PATCH_DOES_NOT_APPLY, UNATTRIBUTED_FILE_MODIFIED, INVARIANT_VIOLATION]

budget_policy:
  max_execution_time_ms: 15000
  max_memory_mb: 512

technical_validation:
  preconditions:
    - "assert git.is_clean_worktree() == true"
    - "assert git.current_commit() == input.baseline_commit"
  postconditions:
    - "assert git.modified_files() == input.attributed_files"
    - "assert tests.run_fast_smoke() == true"

semantic_escalation:
  llm_invoked_inside_verb: false
  on_semantic_ambiguity: RETURN_TYPED_OUTCOME_TO_CALLER   # the caller may involve an Architect or Mapper station
  escalate_to_operator_on: [UNATTRIBUTED_COLLATERAL_MUTATION_DETECTED, CORRUPT_GIT_INDEX]

receipt_policy:
  emit_on_success: true
  emit_on_failure: true
  destination_dir: "receipts/verbs/git_commits/"
```

---

## 3. Failure Taxonomy for Managed Verbs

When a Managed Verb meets a fault it classifies it into one of four orthogonal categories:

```text
┌────────────────────────────────────────────────────────────────────────┐
│ 1. TRANSIENT MECHANICAL FAULT                                          │
│    (Network blip, locked file handle.) Handled by deterministic retry. │
├────────────────────────────────────────────────────────────────────────┤
│ 2. DETERMINISTIC CONTRACT VIOLATION                                    │
│    (Patch fails to apply, schema mismatch.) Fails closed immediately.  │
├────────────────────────────────────────────────────────────────────────┤
│ 3. GOVERNANCE BOUNDARY VIOLATION                                       │
│    (Attempted write outside the write mask.) Fails closed; the         │
│    capability is revoked.                                              │
├────────────────────────────────────────────────────────────────────────┤
│ 4. SEMANTIC AMBIGUITY                                                  │
│    (A merge conflict requiring intent resolution.) Returns a typed     │
│    outcome and receipt to the caller, which may hand off to an         │
│    Architect or Mapper station.                                        │
└────────────────────────────────────────────────────────────────────────┘
```


---


# Appendix G: Prompt Anti-Patterns Catalog

> *"Most prompt engineering failures are not model failures; they are architectural bugs in how humans and harnesses formulate contracts, boundaries, and evidence."*

---

## 1. Overview and Diagnostic Method

When an LLM-assisted workflow fails, engineers reflexively blame "model hallucination." Often the hallucination is provoked by a **broken contract structure**: missing negative space, un-metabolized conversational residue, ambiguous authority seams, or an unbounded search space.

This catalog maps observable symptoms to their anti-patterns, root causes, architectural remedies and primary chapters.

---

## 2. The Master Anti-Patterns Diagnostic Matrix

| Symptom Observed | Anti-Pattern Name | Why It Fails | Better Orion Pattern | Primary Chapter |
| :--- | :--- | :--- | :--- | :--- |
| Model ignores key instructions or drops constraints halfway through a session. | **Giant Context Dump** (`TOPIC-ANTI-01`) | Competing context can dilute attention; reliability can degrade as relevant constraints are crowded out (measure per model). | **Context Metabolism & Continuity Kernel:** Use the HOT/WARM/COLD tiers; pass minimal sufficient state. | Chapter 5, Chapter 18 |
| Model writes verbose apologies, flowery essays, or adopts a quirky persona instead of executing code. | **Personality Instead of Contract** (`TOPIC-ANTI-03`) | Anthropomorphic framing prompts conversational roleplay rather than typed contract fulfillment. | **P-GLL Cognitive Serialization:** Replace adjectives with typed `MISSION`, `INVARIANTS`, and `STOP_CONDITIONS`. | Chapter 1, Chapter 4 |
| Model fires 20 broad `grep` searches, inspecting hundreds of files and exhausting its budget. | **Repo-Wide Grep by Reflex** (`TOPIC-ANTI-02`) | Unbounded search spaces trigger speculative wandering and dependency contamination. | **Reality Spine View:** Provide a declared file allowlist; escalate to broad search only when evidence demands it. | Chapter 12 |
| Model hallucinates code that does not exist, claiming "the packet said so." | **Packet Overrides Source** (`TOPIC-ANTI-09`) | Trusting the prompt over observed source breaks claim-sensitive precedence for current-state claims. | **Reality Precedence:** Enforce `PACKET_PROVIDES_ORIENTATION; PACKET_DOES_NOT_OVERRIDE_REALITY`. | Chapter 2 |
| Different models are forced to agree on a single subjective explanation. | **Forcing Epistemic Conformity** (`TOPIC-ANTI-04`) | Forced consensus destroys the sensor-fusion value of independent reasoning priors. | **Process Convergence Without Epistemic Conformity:** Let models disagree on why; converge on the code. | Chapter 3 |
| Model meets a contradiction and silently guesses or invents an undocumented API. | **Silent Uncertainty Collapse** (`TOPIC-ANTI-14`) | Models trained to be helpful fill gaps with fiction unless uncertainty is a legitimate output. | **Epistemic Classification & Structured Ambiguity Rules:** Require explicit `UNKNOWN` flags; investigate and record; stop only where authority or safety prevents continuation. | Chapter 3, Chapter 18 |
| Model returns a generic "Looks good to me!" without finding real bugs. | **Vague "Review This" Instructions** (`TOPIC-ANTI-05`) | Passive review prompts bias models toward sycophantic agreement. | **Adversarial Falsification Contract:** Specify exact claims, attack vectors and falsification fixtures. | Chapter 16 |
| Implementer declares its own patch "bug-free and production ready." | **Self-Certification Anti-Pattern** (`TOPIC-ANTI-06`) | The author of a change cannot impartially audit its own assumptions or fixture masking. | **Assembly Line Separation:** Implementers may never issue a certification verdict (promotion state capped at `READY_FOR_INDEPENDENT_REAUDIT`); only the Certifier emits scoped certification verdicts, and adoption is a separate governance act. | Chapter 7, Chapter 17 |
| Audit report states: "384 tests passed" without listing which tests ran. | **Test Counts Without Identities** (`TOPIC-ANTI-07`) | Aggregate counts can mask deleted tests, renamed fixtures and skipped assertions. | **Identity-First Evidence:** Demand test identity lists, reconstructable commands and exit codes. | Chapter 16 |
| System crashes because a task parsed `"error: timeout"` from stdout to decide lifecycle state. | **Magic Control Strings** (`TOPIC-ANTI-08`) | Application payload data masquerades as control state; strings collide across boundaries. | **Control Identity & Tagged Race:** Use trusted branch provenance and outer result wrapping. | Chapter 15 |
| An expensive LLM sits in a loop reading polling logs every 5 seconds. | **LLM Babysitting Deterministic Loops** (`TOPIC-ANTI-11`) | Wastes tokens and adds non-deterministic failure modes to rigid procedural execution. | **Deterministic Engineering:** Delegate polling, retries and checks to scripts or Managed Verbs. | Chapter 10, Chapter 11 |
| A 20-line bash script with a `for` loop is documented as an "Autonomous Agent." | **Every Automation Called an "Agent"** (`TOPIC-ANTI-12`) | Confuses procedural automation with adaptive reasoning and muddies governance boundaries. | **Deterministic vs. Cognitive Distinction:** Reserve "agent" for adaptive stations with bounded authority. | Chapter 10 |
| A single edge-case bug causes the team to discard and rewrite the entire architecture. | **Full Redesign After One Failure** (`TOPIC-ANTI-13`) | Confuses a localized defect instance with a fatal architectural defect class. | **Bounded Semantic Neighborhood Search:** Repair the rightful owner; preserve sound invariants. | Chapter 14 |
| Code breaks because a station relied on a 3-week-old verification receipt. | **Historical Receipt Treated as Current Truth** (`TOPIC-ANTI-15`) | Files in the claim's dependency boundary changed since the receipt was emitted, so its applicability is void. | **Freshness Verification (`STALE != FALSE`):** Compare dependency-boundary digests against the receipt baseline. | Chapter 9, Chapter 16 |
| A prompt writes: *"You are authorized to commit to main and deploy to production."* | **Authority by Prose** | A prompt can serialize authority granted by system governance; prompt text cannot mint authority. | **Governed Authority:** Authority derives from governed system state (leases, capabilities, ratified policy, operator decision), not prompt prose. | Chapter 8, Chapter 18 |
| A design document describes a target daemon as if it currently runs in production. | **Target Architecture Presented as Production** | Misleads operators and downstream stations into depending on non-existent runtime services. | **Two-Axis Epistemic Classification:** Label `PROPOSED` / `SPECIFIED_NOT_IMPLEMENTED`. | Chapter 10, Chapter 12 |
| A hypothetical narrative example is cited as historical fact. | **Illustrative Example Mistaken for History** | Fabricates false engineering precedent and damages epistemic integrity. | **Explicit Labeling:** Prefix non-historical examples with `ILLUSTRATIVE_EXAMPLE`. | Chapter 14, Chapter 16 |


---


# Appendix H: Operator Checklist: "Before You Send a Serious Prompt"

> *"If you cannot answer these ten questions before dispatching a prompt, you are not compiling a contract; you are improvising with your codebase."*

---

## 1. The 10-Point Pre-Flight Checklist

Run this checklist before submitting any non-trivial prompt to a frontier model or automated station harness. Until an automated prompt-contract validator exists, this checklist is the validation mechanism.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   PRE-FLIGHT CONTRACT CHECKLIST                        │
├────────────────────────────────────────────────────────────────────────┤
│ [ ] 1. THE MISSION:                                                    │
│        Is the technical goal stated unambiguously in 1–2 sentences?    │
│                                                                        │
│ [ ] 2. DONE STATE:                                                     │
│        Are the observable success criteria explicit and verifiable?    │
│                                                                        │
│ [ ] 3. CURRENT REALITY:                                                │
│        Are the baseline commit, branch and relevant digests attached?  │
│                                                                        │
│ [ ] 4. PRECEDENCE RULES:                                               │
│        Does the prompt declare claim-sensitive precedence (at minimum: │
│        living source outranks prompt text for claims about current     │
│        code)?                                                          │
│                                                                        │
│ [ ] 5. READ SCOPE:                                                     │
│        Is the authorized observation scope declared?                   │
│                                                                        │
│ [ ] 6. WRITE MASK:                                                     │
│        Is the list of mutable files explicit? ([] for read-only seats) │
│                                                                        │
│ [ ] 7. NEGATIVE SPACE & MUST-NOT-CHANGE:                               │
│        Are non-goals and protected directories explicitly declared?    │
│                                                                        │
│ [ ] 8. EVIDENCE REQUIREMENTS:                                          │
│        Are exact command lines and required test identities specified? │
│                                                                        │
│ [ ] 9. STATUS CEILING:                                                 │
│        Is the station capped at its row of the status table            │
│        (Appendix C §1), on all three axes? Only a Certifier may list   │
│        a certification verdict, and certification is not adoption.     │
│                                                                        │
│ [ ] 10. STOP CONDITIONS & HANDOFF:                                     │
│         Does the prompt specify when to halt and who gets the receipt? │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Advanced Pre-Flight Gates

For high-assurance or authority-bearing tasks, run the gate that applies to the mission.

### Gate A: Historical Claim Audit Gate
*Use when the prompt or task cites past repository milestones, bug reports or performance numbers.*
- [ ] Is every cited commit hash, error string and file path verified against actual history?
- [ ] Are narrative analogies and hypothetical examples labeled `ILLUSTRATIVE_EXAMPLE`?
- [ ] Does the prompt avoid manufactured numbers (token counts, percentages) that lack receipts?

### Gate B: Runtime Maturity Audit Gate
*Use when referencing Orion subsystems, tools or execution engines.*
- [ ] Is every referenced mechanism classified on the maturity axis (`PRODUCTION`, `EXPERIMENTAL_RUNTIME`, `SPECIFIED_NOT_IMPLEMENTED`, `NOT_DETERMINABLE`, `NOT_APPLICABLE`)?
- [ ] Are specified-only architectures (for example `reality.compile` or the unified Managed Verb runtime) kept from being represented as live production code?

### Gate C: Certification Job Audit Gate
*Use when dispatching an independent certification station.*
- [ ] Is the `write_mask` strictly empty (`[]`)?
- [ ] Is the candidate held in an isolated sandbox or an equivalent topology that preserves subject identity, execution isolation and evidence separation?
- [ ] Is the pre-execution payload root digest recorded, so accidental mutation during testing can be detected?
- [ ] Does the contract state: `CERTIFICATION != ADOPTION; CERTIFIER CANNOT MINT ADOPTION AUTHORITY`?

### Gate D: Authority-Bearing Job Audit Gate
*Use when the task involves git commits, branch creation or deployment.*
- [ ] Does a valid, unexpired governance authority exist in system state?
- [ ] If this is production promotion for a campaign that requires it (for example Pass 1C), has explicit operator authorization been obtained?
- [ ] Are all operations idempotent, reversible or fenced with rollback checkpoints, and is any destructive rollback limited to an isolated worktree and gated by policy?

### Gate E: Long-Horizon Multi-Day Relay Gate
*Use when handing work across stations or resuming after session death.*
- [ ] Is the incoming receipt rehydrated into a clean **Continuity Kernel** rather than pasted conversational history?
- [ ] Has freshness been verified by comparing the receipt's baseline digests for the claim's dependency boundary against current state (HEAD equality alone is neither necessary nor sufficient)?
- [ ] Has the previous model's working set been metabolized to prevent attention dilution?


---

