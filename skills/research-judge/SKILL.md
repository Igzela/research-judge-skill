---
name: research-judge
description: Run a STORM-inspired research audit: define the question, scan perspectives, map conflicts, grade evidence, synthesize a decision brief, and peer-review weak points. Use when the user asks to research, investigate, compare, evaluate, decide, review literature, assess a market, audit a strategy, or choose between technical/product options.
argument-hint: What topic, decision, report, repository, source material, or claim should be researched?
---

# Research Judge Skill

The user wants serious research judgment, not a quick summary.

Use this skill when a task involves uncertainty, conflicting evidence, strategic choice, market research, technical review, product direction, literature review, policy analysis, or a decision that could fail if assumptions are wrong.

This skill is inspired by Stanford STORM-style multi-perspective research and synthesis. It does not reproduce the full STORM system. It turns the core idea into a compact agent workflow.

Do not use this skill for simple factual lookup, casual explanation, pure rewriting, or tasks where the user only needs a direct answer.

## Operating rule

Always separate:

- verified facts
- source-backed claims
- reasonable inferences
- assumptions
- open questions

Do not pretend to know facts that require retrieval. If tools are available, use appropriate sources. If retrieval is unavailable, state the boundary clearly.

## Workflow

### 1. Scope the research question

Identify the real task:

- What decision, judgment, or research question is being answered?
- Who will use the answer?
- What would change the recommendation?
- What is out of scope?

If the objective is clear enough, proceed without asking. Ask at most one clarifying question only when the answer would materially change the output.

### 2. Evidence contract

State what evidence is available:

- user-provided material
- repository files
- uploaded documents
- web/search results, if available
- model knowledge only when retrieval is unavailable

Then mark the evidence boundary:

- What is well-supported?
- What is weak or missing?
- What must not be treated as fact?

### 3. Perspective scan

Analyze the topic from 5-7 relevant perspectives. Choose perspectives based on the task.

For market research, consider:

- user/customer
- supplier/operator
- competitor
- regulator/platform
- economist/business model
- skeptic
- local/contextual actor

For technical decisions, consider:

- architect
- reliability engineer
- security reviewer
- maintainer
- cost owner
- user/operator
- skeptic

For academic or literature review, consider:

- theorist
- empirical researcher
- methodology critic
- practitioner
- historical context
- skeptic

For product strategy, consider:

- end user
- buyer
- operator
- competitor
- support/maintenance
- growth/distribution
- skeptic

For each perspective, include:

- core claim
- strongest evidence
- likely blind spot
- what it disputes

### 4. Conflict map

Identify contradictions between perspectives.

For each conflict, include:

- conflict statement
- side A
- side B
- stronger evidence
- why
- missing information needed to decide

Do not flatten disagreement into compromise. If one side is stronger, say so.

### 5. Evidence matrix

Grade important claims.

For each claim, include:

- claim
- evidence
- source or basis
- confidence: high / medium / low
- risk if wrong
- verification step

High confidence requires either strong source support, repeated independent evidence, or direct user-provided proof. Plausible reasoning alone is not high confidence.

### 6. Synthesis brief

Produce a concise decision-oriented brief:

- bottom line
- key findings
- evidence confidence
- main conflicts
- recommendation
- risks
- next validation steps

Prefer practical judgment over report length.

### 7. Peer review

Critique your own result:

- weakest claim
- likely bias
- missing perspective
- unsupported inference
- what a serious reviewer would challenge
- what should be checked next

If the research does not support a strong answer, say that directly.

## Output format

Use this default structure unless the user requests another format:

```md
# Research Judge Brief: [Topic]

## Bottom Line

## Evidence Contract

## Perspective Scan

## Conflict Map

## Evidence Matrix

## Recommendation

## Risks

## Next Validation Steps

## Peer Review
```

## Quality bar

A good result should make the user more capable of deciding.

It should not merely sound deep. It should expose what matters, what is uncertain, what could fail, and what to verify next.
