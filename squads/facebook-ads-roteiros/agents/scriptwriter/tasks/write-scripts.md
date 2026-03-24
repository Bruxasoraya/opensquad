---
task: "Write Scripts"
order: 2
input: |
  - selected_hooks: User-selected hooks (1 per script = 15 hooks selected)
  - weekly_direction: Confirmed angles per category
  - tone_selection: Chosen tone per category
  - domain_framework: S.P.A.R.K. framework
  - output_examples: Reference examples
  - anti_patterns: Mistakes to avoid
output: |
  - scripts: 15 complete video scripts (3 per category), each 45-60 seconds
---

## Process

For each of the 15 selected hooks, write one complete video script following the S.P.A.R.K. framework:

- **S — Stop the Scroll**: Open with the selected hook, delivered directly to camera. Max 3 seconds.
- **P — Pain**: Validate the viewer's emotional reality in 2-3 sentences. No solutions yet. Mirror their experience.
- **A — Authority**: Establish Soraya's credibility in 1-2 sentences. Name, years of experience, client results (without absolute promises). Natural, not boastful.
- **R — Result**: Describe the transformation or shift clients experience. Use "clientes relatam", "muitas pessoas percebem", "pode ajudar". Never use absolute claims.
- **K — Kick to Action**: One clear CTA tied to the specific category landing page. Tell them exactly where to go and what to do.

Each script must include:
- Category label and script number (e.g., TAROT-01)
- Selected hook
- Tone in use
- Full script text with S.P.A.R.K. section markers
- Timing estimate per section and total (target: 45-60 seconds)
- Word count estimate (target: 110-140 words for 45-60 seconds at natural pace)
- Delivery notes for Soraya (pauses, emphasis, eye contact cues)
- Landing page / CTA destination

Save all scripts organized in the output file by category.

---

## Output Format

```markdown
## [CATEGORIA-NN] — [Hook text]

**Categoria:** [Nome da categoria]
**Tom:** [Tom selecionado]
**Destino CTA:** [URL ou canal]
**Duração estimada:** [XX-XX segundos]
**Contagem de palavras:** ~[XXX] palavras

---

### Script

[S - STOP] (~3s)
[Hook text — exatamente como selecionado]

[P - PAIN] (~12s)
[2-3 sentences validating the viewer's emotional pain]

[A - AUTHORITY] (~8s)
[1-2 sentences establishing Soraya's credibility naturally]

[R - RESULT] (~12s)
[2-3 sentences describing transformation without absolute claims]

[K - KICK TO ACTION] (~8s)
[Direct, specific CTA with destination]

---

**Notas de entrega para Soraya:**
- [Delivery cue 1]
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
- "Essa sensação de ficar parado" — desacelerar aqui, dar peso emocional
- CTA: falar com naturalidade, não com urgência artificial — o link está lá, basta clicar
```

---

## Quality Criteria

- [ ] Cada roteiro segue o framework S.P.A.R.K. com todas as 5 seções presentes
- [ ] Duração estimada entre 30-60 segundos (65-160 palavras)
- [ ] CTA direciona para o landing page correto da categoria
- [ ] Zero palavras proibidas pelo Meta
- [ ] Roteiro soa natural quando lido em voz alta (frases curtas, conversacional)

---

## Veto Conditions

Rejeitar e refazer se QUALQUER condição for verdadeira:
1. Roteiro contém palavra proibida pelo Meta (feitiço, amarração, magia negra, garantido, cura, "ele vai voltar")
2. CTA direciona para landing page incorreto
3. Roteiro ultrapassa 160 palavras ou fica abaixo de 65 palavras
