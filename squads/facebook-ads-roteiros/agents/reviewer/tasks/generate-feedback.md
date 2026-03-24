---
task: "Generate Feedback"
order: 2
input: |
  - scoring_table: Per-script scores from score-scripts task
  - compliance_flags: Any compliance issues found
output: |
  - review_verdict: APPROVE or REJECT with detailed feedback per script
  - required_changes: List of must-fix items (if REJECT)
  - suggestions: Non-blocking improvement suggestions
  - summary: Overall quality summary with strengths and areas for improvement
---

## Process

**Step 1 — Determine verdict per script.**
Using the completed scoring table from `score-scripts`:
- APPROVE: average ≥ 7.0/10 AND no criterion below its minimum floor AND no compliance flags
- REJECT: average < 7.0/10 OR any minimum-floor criterion below its threshold OR any compliance flag present

For every REJECT, document all reasons. A script may fail for multiple reasons simultaneously.

**Step 2 — Write per-script feedback.**
For each script, produce:
1. Verdict badge: **APPROVE** or **REJECT**
2. Score summary (average and individual criteria scores)
3. Strengths (cite specific passages for criteria scoring ≥ 8/10)
4. Required changes (cite specific passages for criteria scoring < 7/10 or failing compliance)
5. Suggestions (non-blocking improvements for criteria scoring 7–7.9/10)

**Step 3 — Determine batch verdict.**
- APPROVE batch: ≥ 13 of 15 scripts approve
- REJECT batch: ≥ 3 scripts reject — return all failing scripts for revision
- Conditional APPROVE: exactly 1–2 scripts reject — batch approves with those scripts flagged for revision before production

**Step 4 — Write overall quality summary.**
Identify patterns across the 15 scripts:
- Recurring strengths (e.g., "CTA consistency is a batch highlight")
- Recurring weaknesses (e.g., "Authority citation is underdeveloped across 8 scripts")
- Differentiation quality per category
- Any systemic issues to address in the next batch briefing

**Step 5 — Write to output file.**
Save full feedback to `squads/facebook-ads-roteiros/output/review-verdict.md`.

---

## Output Example

### Script: Tarot Perguntas #01 — APPROVE

**Average Score: 8.4/10**

**Strengths:**
- `Strength (CTA):` "clique no link agora" — single action, direct, urgency present. This is the benchmark CTA for the batch.
- `Strength (Pain Accuracy):` "ficou sem saber o que fazer num momento importante" — second-person, audience language, specific emotional state.

**Required Changes:** None.

**Suggestions (non-blocking):**
- `Suggestion:` Criterion 3 (Authority) — consider adding "X anos ajudando pessoas" or a client volume reference to strengthen credibility without overclaiming.
- `Suggestion:` Criterion 4 (Social Proof) — "pode mudar" is safe but vague; an anonymized outcome ("uma cliente minha conseguiu...") would strengthen specificity.

---

### Script: Benzimento #02 — REJECT

**Average Score: 6.1/10**

**Compliance Flag:** FORBIDDEN WORD detected — "garantido" found in line: *"resultado garantido para quem busca proteção"*. Automatic REJECT.

**Required Changes:**
- `Required change (Compliance):` Remove "garantido" entirely. Replace with safe framing: "muitas pessoas relatam sentir uma diferença já nas primeiras semanas."
- `Required change (Hook Power, 5/10):` "Você precisa de proteção?" is too generic. Replace with a specific, emotionally charged scenario: e.g., "Você sente que algo invisível está bloqueando tudo na sua vida?"
- `Required change (Brand Voice, 6/10):` Lines 4–6 use formal, distant language ("é necessário que o cliente esteja disposto"). Rewrite in Soraya's direct, personal voice: "você só precisa querer."

---

### Batch Summary

**Overall Verdict: APPROVE (Conditional)**
**Scripts Approved:** 13/15 | **Scripts Rejected:** 2/15

**Batch Strengths:**
- CTA Effectiveness is consistently strong across all 13 approved scripts — this is a repeatable pattern to maintain.
- S.P.A.R.K. structure adherence is high; 12/15 scripts hit the 30–60s duration target.

**Areas for Improvement (next batch briefing):**
- Authority & Credibility averaged 6.9/10 across the batch — writers need more specific credibility anchors embedded naturally.
- Differentiation within the Benzimento category is borderline; scripts #01 and #03 share nearly the same hook angle.

**Required Actions Before Production:**
1. Revise Benzimento #02: fix compliance flag + hook + brand voice (see above).
2. Revise [Script X]: [reason].
3. Resubmit revised scripts for checkpoint approval before production scheduling.

---

## Output Format

```yaml
verdict: "APPROVE" | "REJECT" | "CONDITIONAL APPROVE"
overall_score: 8.1
scripts_approved: 13
scripts_rejected: 2
required_changes:
  - script_id: "trabalhos-amorosos-02"
    issue: "Hook ultrapassa 8 palavras"
    fix: "Reduzir hook para máximo 8 palavras mantendo o gatilho de dor"
suggestions:
  - script_id: "tarot-perguntas-03"
    suggestion: "CTA poderia ser mais específico sobre o tempo de resposta (3 horas)"
summary: "..."
```

---

## Quality Criteria

- [ ] Veredicto é consistente com os scores (média >= 7 = APPROVE, < 7 = REJECT)
- [ ] Cada rejeição inclui fix específico e acionável
- [ ] Pelo menos 1 "Strength:" identificado mesmo em reviews REJECT
- [ ] Feedback distingue claramente "Required change:" de "Suggestion (non-blocking):"

---

## Veto Conditions

Rejeitar e refazer se QUALQUER condição for verdadeira:
1. Veredicto contradiz os scores (ex: APPROVE com média abaixo de 7)
2. Roteiro com compliance flag não foi marcado como REJECT
