# Research Judge Skill

A STORM-inspired agent skill for turning messy research topics into evidence-graded, multi-perspective decision briefs.

This repository is based on the research idea behind Stanford STORM: use multi-perspective question asking and synthesis to explore a topic before writing or deciding. This project is not an official Stanford STORM implementation. It adapts the core research workflow into a lightweight skill that can be used by AI coding agents, research agents, and chat-based assistants.

## Main functions

Research Judge helps an agent do five things:

1. **Perspective scan** — examine a topic from multiple relevant viewpoints instead of producing a single flat summary.
2. **Conflict map** — identify where perspectives disagree, which side has stronger evidence, and what information is still missing.
3. **Evidence matrix** — separate verified facts, source-backed claims, reasonable inferences, assumptions, and open questions.
4. **Synthesis brief** — turn messy research into a concise decision-oriented brief.
5. **Peer review** — critique the answer itself by finding weak claims, missing perspectives, likely bias, and unsupported inference.

## Best for

- market research
- startup idea validation
- product strategy
- technical decision reviews
- literature review planning
- policy or industry analysis
- post-Deep-Research audit
- comparing competing claims or implementation options

## Not for

- pretending guesses are evidence
- replacing domain experts
- generating uncited factual claims when retrieval is required
- legal, medical, financial, or safety-critical advice without qualified sources
- bypassing system, organization, or safety instructions

## Repository structure

```text
research-judge-skill/
  README.md
  LICENSE
  CONTRIBUTING.md
  CHANGELOG.md
  skills/
    research-judge/
      SKILL.md
      templates/
        evidence-matrix.md
        perspective-scan.md
        conflict-map.md
        synthesis-brief.md
        peer-review.md
      examples/
        market-research.md
        technical-decision.md
        paper-review.md
```

## Usage

Use this skill when the user asks for serious research, comparison, evaluation, strategy, literature review, or decision support.

Example:

```text
Use the research-judge skill to evaluate whether a local adult learning service marketplace can work in Zhuhai.
Separate source-backed facts from assumptions, map conflicts, and give a decision-oriented brief.
```

Another example:

```text
Use research-judge on this technical plan.
Focus on failure assumptions, reliability risks, evidence gaps, and the smallest validation test.
```

## Core workflow

1. Scope the research question.
2. Establish the evidence contract.
3. Run a multi-perspective scan.
4. Map conflicts.
5. Build an evidence matrix.
6. Produce a synthesis brief.
7. Peer-review the result.

## Design principles

Research Judge is intentionally conservative:

- It does not call speculation “research.”
- It does not hide weak evidence behind confident writing.
- It prefers a useful decision brief over a long report.
- It treats disagreement between perspectives as signal, not noise.
- It makes verification steps explicit.

## Relationship to STORM

This skill is inspired by STORM-style multi-perspective research and synthesis. The goal is not to reproduce the full STORM system, but to package a practical research-judgment workflow that agents can apply to source material, Deep Research outputs, repository files, or user-provided context.

Reference projects and papers:

- Stanford OVAL STORM: https://github.com/stanford-oval/storm
- STORM paper: https://aclanthology.org/2024.naacl-long.347/

## License

MIT
