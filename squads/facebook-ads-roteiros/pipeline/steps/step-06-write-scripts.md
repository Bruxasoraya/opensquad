---
execution: inline
agent: squads/facebook-ads-roteiros/agents/scriptwriter
inputFile: squads/facebook-ads-roteiros/output/hooks-selection.md
outputFile: squads/facebook-ads-roteiros/output/all-scripts.md
---

## Step 06 — Write Scripts

Gabi Gancho executes this step after the user has selected 1 hook per category at step-05 checkpoint.

---

## Context Loading

Load the following files before starting:

1. `squads/facebook-ads-roteiros/output/hooks-selection.md` — confirmed hooks and tone selections per category
2. `squads/facebook-ads-roteiros/context/domain-framework.md` — S.P.A.R.K. framework structure and category landing pages
3. `squads/facebook-ads-roteiros/context/output-examples.md` — approved reference scripts showing expected quality and format
4. `squads/facebook-ads-roteiros/context/anti-patterns.md` — common mistakes to avoid
5. `squads/facebook-ads-roteiros/context/tone-of-voice.md` — tone definitions and delivery guidance

---

## Instructions

### Process
1. Carregar hooks selecionados pelo usuário e tom de voz confirmado para cada categoria
2. Para cada hook selecionado, escrever roteiro completo seguindo framework S.P.A.R.K. (Stop, Pain, Authority, Result, Kick)
3. Incluir marcadores de tempo para cada seção do roteiro e contagem de palavras
4. Verificar que o CTA de cada roteiro direciona para o landing page correto da categoria
5. Executar otimização: reduzir word count 15-25% se acima de 160 palavras, verificar compliance Meta, checar diferenciação entre os 3 roteiros de cada categoria
6. Organizar todos os 15 roteiros em seções por categoria

Write 15 complete video scripts — 3 per category — using the selected hooks and confirmed tone per category.

For each script, follow S.P.A.R.K. structure:

- **S — Stop the Scroll** (~3s): Open with the selected hook, verbatim as confirmed. Do not alter the hook.
- **P — Pain** (~12s): 2-3 sentences validating the viewer's emotional reality. No solution yet. Mirror their experience without judgment.
- **A — Authority** (~8s): 1-2 sentences establishing Soraya's credibility. Natural, earned, not boastful. Name + years + client results signal.
- **R — Result** (~12s): 2-3 sentences describing the transformation. Use softening language: "clientes relatam", "muitas pessoas percebem", "pode ajudar", "é possível". No absolute claims.
- **K — Kick to Action** (~8s): One CTA, one destination, one action. Specific URL or channel. 1-2 sentences maximum.

Compliance rules for every script:
- No forbidden words: feitiço, amarração, magia negra, garantido, cura, elimine
- No absolute predictions: "ele vai voltar", "vai funcionar", "você vai conseguir [resultado específico]"
- No guaranteed timelines: "em 7 dias", "em 24 horas", "em uma semana"
- Target: 110-140 words per script (45-60 seconds at natural speaking pace)

---

## Output Format

Organize all 15 scripts by category in the output file. Use this structure for each script:

```markdown
## [CATEGORIA-NN] — [Hook text]

**Categoria:** [Nome]
**Tom:** [Tom confirmado]
**Destino CTA:** [URL ou canal]
**Duração estimada:** [XX-XX] segundos
**Contagem de palavras:** ~[XXX] palavras

---

### Script

[S - STOP] (~3s)
[Hook — exatamente como selecionado]

[P - PAIN] (~12s)
[Pain validation]

[A - AUTHORITY] (~8s)
[Authority establishment]

[R - RESULT] (~12s)
[Result without absolute claims]

[K - KICK TO ACTION] (~8s)
[Specific CTA]

---

**Notas de entrega para Soraya:**
- [Delivery cue 1 — specific line + instruction]
- [Delivery cue 2]
- [Delivery cue 3]
```

---

## Output Example

```markdown
## TAROT-01 — "Você ainda não sabe o que fazer, né?"

**Categoria:** Tarot Perguntas
**Tom:** Empático e íntimo
**Destino CTA:** https://atendimento.bruxasorayatarot.com.br/tarot
**Duração estimada:** 48-52 segundos
**Contagem de palavras:** ~118 palavras

---

### Script

[S - STOP] (~3s)
Você ainda não sabe o que fazer, né?

[P - PAIN] (~12s)
Você fica girando a mesma situação na cabeça, olha pro celular esperando uma mensagem que não vem, e cada dia que passa parece que a resposta fica mais longe. Essa sensação de ficar parado sem saber qual caminho tomar é exaustiva.

[A - AUTHORITY] (~8s)
Sou Soraya, trabalho com tarot há seis anos, e já ajudei muitas pessoas que estavam exatamente nesse lugar de incerteza.

[R - RESULT] (~12s)
Clientes relatam que depois de uma consulta de tarot elas finalmente conseguem ver a situação com mais clareza — não porque o tarot decide por elas, mas porque revela o que já estava lá esperando ser visto.

[K - KICK TO ACTION] (~8s)
Se você quer essa clareza agora, acessa o link aqui no perfil e agenda sua consulta de tarot online comigo.

---

**Notas de entrega para Soraya:**
- "Você ainda não sabe o que fazer, né?" — pausa de 0,5s depois, olho direto na câmera, tom de reconhecimento suave, não de julgamento
- "Essa sensação de ficar parado" — desacelerar aqui, dar peso emocional à frase
- CTA: falar com naturalidade, sem urgência artificial — convidar, não empurrar
```

After saving all 15 scripts to output file, trigger step-07-approve-content.md checkpoint.

---

## Veto Conditions

Rejeitar e refazer se QUALQUER condição for verdadeira:
1. Qualquer roteiro contém palavra proibida pelo Meta (feitiço, amarração, magia negra, garantido, cura, "ele vai voltar")
2. CTA direciona para landing page incorreto
3. Roteiro ultrapassa 160 palavras ou fica abaixo de 65 palavras
4. Roteiro não segue framework S.P.A.R.K. (falta uma das 5 seções)

---

## Quality Criteria

- [ ] 15 roteiros completos (3 por categoria × 5 categorias)
- [ ] Cada roteiro segue S.P.A.R.K. com todas as 5 seções presentes
- [ ] Duração estimada entre 30-60 segundos (65-160 palavras)
- [ ] CTA correto para cada categoria
- [ ] Zero palavras proibidas pelo Meta em todos os roteiros
- [ ] Os 3 roteiros de cada categoria são suficientemente diferentes (hooks, ângulos, abordagens)
- [ ] Tom de voz consistente com a seleção do usuário
