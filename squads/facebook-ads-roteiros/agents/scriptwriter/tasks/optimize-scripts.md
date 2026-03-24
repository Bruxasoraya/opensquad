---
task: "Optimize Scripts"
order: 3
input: |
  - scripts: All 15 draft scripts
  - quality_criteria: Quality criteria reference
  - anti_patterns: Anti-patterns reference
output: |
  - optimized_scripts: All 15 scripts after optimization pass
  - optimization_notes: Changes made per script with reasoning
---

## Process

Run a systematic optimization pass across all 15 scripts. For each script, check and fix the following:

### 1. Word Count Reduction
- Target: 110-140 words per script (45-60 seconds at natural speech pace)
- If over 140 words: reduce 15-25% by cutting filler phrases, redundant qualifiers, and padding in the Pain or Result sections
- Never cut the hook, the authority line, or the CTA destination

### 2. Meta Compliance Check
- Scan every script for forbidden words: feitiço, amarração, magia negra, garantido, cura, elimine
- Scan for absolute predictions: "ele vai voltar", "vai funcionar", "você vai conseguir"
- Scan for guaranteed timelines: "em 7 dias", "em 24 horas", "em uma semana"
- Replace any violations with compliant alternatives before flagging

### 3. CTA Strength
- CTA must name the exact destination (URL or channel)
- CTA must include one action verb (acessa, entra, clica, fala comigo)
- CTA must not be longer than 2 sentences
- Weak CTAs ("saiba mais", "entre em contato") must be replaced with specific ones

### 4. Hook Sharpness
- Re-read hook out loud — does it stop a scroll in 3 seconds?
- Is it max 8 words?
- Does it activate a clear emotional driver?
- If hook feels generic after full script review, sharpen or flag for user review

### 5. Brand Voice Alignment
- Check for corporate or overly formal language — replace with conversational equivalents
- Ensure Soraya sounds like a real person, not a marketing copy template
- Verify that emojis are absent (scripts are spoken content, no emojis in text)

### 6. Differentiation Check
- Group the 3 scripts per category together
- Confirm each uses a different hook structure and different emotional driver
- If 2 scripts in the same category feel too similar in tone or argument, flag and suggest a rewrite angle for one of them

---

## Output Format

After optimization, output:

1. All 15 optimized scripts (full text, same format as write-scripts output)
2. An optimization notes block per script:

```markdown
### Notas de Otimização — [CATEGORIA-NN]

- **Contagem de palavras:** [antes] → [depois] ([X]% redução)
- **Compliance:** [Nenhuma violação encontrada / Alterações: descrever]
- **CTA:** [Aprovado / Alteração: descrever]
- **Hook:** [Aprovado / Alteração: descrever]
- **Voz da marca:** [Aprovado / Alteração: descrever]
- **Diferenciação:** [Aprovado / Risco: descrever]
```

3. A summary table at the end:

```markdown
## Resumo da Otimização

| Script      | Palavras Antes | Palavras Depois | Compliance | CTA | Status |
|-------------|---------------|-----------------|------------|-----|--------|
| TAROT-01    | 138           | 118             | OK         | OK  | Aprovado |
| TAROT-02    | 152           | 121             | OK         | OK  | Aprovado |
| ...         | ...           | ...             | ...        | ... | ...    |
```

Scripts with unresolved issues are marked "Revisão necessária" in the Status column with a note explaining what requires user decision.

---

## Quality Criteria

- [ ] Word count reduzido 15-25% quando acima do target (160 palavras)
- [ ] Todas as palavras proibidas pelo Meta foram removidas
- [ ] CTA de cada roteiro verificado contra landing page correto
- [ ] Os 3 roteiros de cada categoria são suficientemente diferentes entre si

---

## Veto Conditions

Rejeitar e refazer se QUALQUER condição for verdadeira:
1. Qualquer roteiro otimizado ainda contém palavra proibida pelo Meta
2. Otimização alterou o hook selecionado pelo usuário sem justificativa
