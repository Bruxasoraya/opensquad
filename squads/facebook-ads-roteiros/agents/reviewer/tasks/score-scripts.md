---
task: "Score Scripts"
order: 1
input: |
  - all_scripts: All 15 approved scripts
  - quality_criteria: Scoring rubric (10 criteria)
  - anti_patterns: Mistakes to check for
output: |
  - scoring_table: Per-script scoring on all 10 criteria
  - compliance_flags: Any Meta compliance issues found
  - category_differentiation_score: How different the 3 scripts in each category are
---

## Process

**Step 1 — Load and organize scripts.**
Read `all-scripts.md`. Identify the 5 categories and confirm 3 scripts per category (15 total). If the count is wrong, stop and flag the discrepancy before scoring.

**Step 2 — Compliance pre-scan.**
Before scoring any criterion, scan every script for forbidden words: `feitiço`, `amarração`, `magia negra`, `garantido`, `cura`, `elimine`, `"ele vai voltar"`. Also scan for absolute guarantees (e.g., "resultado garantido", "vai funcionar", "100%"). Any match triggers an immediate compliance flag and automatic REJECT for that script. Document the exact offending passage and line.

**Step 3 — Score each script on all 10 criteria.**
For each of the 15 scripts, apply the scoring rubric from `quality-criteria.md`:

| # | Criterion | Weight |
|---|-----------|--------|
| 1 | Hook Power | High |
| 2 | Pain Accuracy | High |
| 3 | Authority & Credibility | Medium |
| 4 | Social Proof & Result | Medium |
| 5 | CTA Effectiveness | High |
| 6 | Meta Compliance | Critical |
| 7 | Brand Voice Alignment | High |
| 8 | Script Structure (S.P.A.R.K.) | Medium |
| 9 | Category Accuracy | Medium |
| 10 | Differentiation | Medium |

Score each criterion 1–10. Cite the specific passage from the script for criteria 1, 2, 5, and 7.

**Step 4 — Check differentiation within each category.**
After scoring all 3 scripts in a category, compare:
- Hook angles (are they meaningfully different?)
- Pain point framings (same pain, different angle, or same angle?)
- CTA phrasing (different enough to test as variants?)

Assign a Differentiation Score (1–10) to each category group. If two scripts score the same angle, flag both for revision.

**Step 5 — Compile scoring tables.**
Produce one detailed table per script and one summary table for all 15.

---

## Output Example

### Detailed Scoring — Script: Tarot Perguntas #01

**Script excerpt:**
> "Você já ficou sem saber o que fazer num momento importante da sua vida? [...]"

| Criterion | Score | Justification |
|-----------|-------|---------------|
| 1. Hook Power | 8/10 | "Você já ficou sem saber o que fazer" targets indecision pain directly. Under 8 words. Loses 2 points: no sensory or emotional intensifier. |
| 2. Pain Accuracy | 9/10 | "momento importante" is specific; second-person address is consistent throughout. Strength: audience language mirrors how clients describe their situation. |
| 3. Authority & Credibility | 7/10 | Soraya's experience is mentioned but not quantified. Suggestion: add years or number of clients served. |
| 4. Social Proof & Result | 7/10 | Result framing is safe ("pode mudar"). No absolute guarantees. Could be more specific with a anonymized client outcome. |
| 5. CTA Effectiveness | 9/10 | Single action, clear landing page reference, urgency present. Strength: "clique no link agora" is direct and unambiguous. |
| 6. Meta Compliance | 10/10 | No forbidden words detected. No guarantees. Compliant. |
| 7. Brand Voice Alignment | 8/10 | Empathetic and personal tone throughout. One sentence ("transforme sua vida") veers toward generic; flagged as suggestion. |
| 8. Script Structure | 8/10 | S.P.A.R.K. structure followed. Estimated duration: 38 seconds. Short sentences. Natural speech rhythm. |
| 9. Category Accuracy | 10/10 | Correct product (Tarot Perguntas), correct landing page reference. |
| 10. Differentiation | 8/10 | Hook angle distinct from #02 and #03 in this category. Pain framing overlaps slightly with #02 — flagged for review. |

**Script #01 Average: 8.4/10 — APPROVE**
**Compliance Flags:** None

---

### Summary Scoring Table — All 15 Scripts

| Script | Cat. | H | P | A | SP | CTA | MC | BV | SS | CA | Diff | Avg | Verdict |
|--------|------|---|---|---|----|-----|----|----|----|----|------|-----|---------|
| TP-01 | Tarot Perguntas | 8 | 9 | 7 | 7 | 9 | 10 | 8 | 8 | 10 | 8 | 8.4 | APPROVE |
| TP-02 | Tarot Perguntas | — | — | — | — | — | — | — | — | — | — | — | — |
| ... | ... | — | — | — | — | — | — | — | — | — | — | — | — |

*(Full table populated after all 15 scripts are scored.)*

**Column Key:** H=Hook, P=Pain, A=Authority, SP=Social Proof, CTA=CTA, MC=Meta Compliance, BV=Brand Voice, SS=Structure, CA=Category Accuracy, Diff=Differentiation

---

## Output Format

```yaml
scripts:
  - id: "tarot-perguntas-01"
    scores:
      hook_power: 8
      pain_accuracy: 7
      authority_credibility: 8
      social_proof_result: 7
      cta_effectiveness: 9
      meta_compliance: 10
      brand_voice: 8
      script_structure: 8
      category_accuracy: 9
      differentiation: 7
    overall: 8.1
    verdict: "APPROVE"
    compliance_flags: []
```

---

## Quality Criteria

- [ ] Todos os 10 critérios foram avaliados para cada roteiro
- [ ] Cada score tem justificativa escrita (não apenas o número)
- [ ] Flags de compliance identificados imediatamente
- [ ] Score de diferenciação avaliado por categoria (não por roteiro individual)

---

## Veto Conditions

Rejeitar e refazer se QUALQUER condição for verdadeira:
1. Qualquer critério foi avaliado sem justificativa escrita
2. Meta Compliance não foi verificado para todos os 15 roteiros
