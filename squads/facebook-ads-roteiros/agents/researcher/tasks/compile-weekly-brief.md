---
task: "Compile Weekly Brief"
order: 2
input: |
  - trending_hooks: Results from find-trends task
  - platform_updates: Meta policy/algorithm changes
  - competitor_activity: Competitor analysis results
  - seasonal_angles: Seasonal opportunities found
output: |
  - weekly_brief: Structured brief with recommended angles per category, hook inspirations, and warnings
---

# Compile Weekly Brief

Synthesize all raw trend findings into a structured, production-ready weekly brief organized by the 5 script categories. This task transforms raw intelligence into clear creative direction — every category gets specific angle recommendations, hook inspirations with confidence ratings, and any compliance warnings the writers must observe. The output is the direct input for step-03-weekly-direction checkpoint review.

## Process

1. **Organize findings by category.** Map each trending hook, competitor pattern, and seasonal angle to the relevant categories: Tarot Perguntas, Trabalhos Amorosos, Benzimento Segunda, App, and Benzimento Diário. A single finding can apply to multiple categories but must be placed under each one explicitly. Prioritize findings with HIGH confidence for the primary angle recommendation per category; use MEDIUM confidence findings as secondary options.

2. **Synthesize recommended angles per category.** For each of the 5 categories, formulate 2-3 distinct angle recommendations. Each angle should be specific enough to brief a copywriter — it must name the hook archetype, suggest a copy direction, reference the supporting data, and note any seasonal tie-in. Ensure that across all 5 categories, there are at least 3 distinct hook archetypes represented so the 15 scripts produced do not all sound the same.

3. **Flag compliance risks and production warnings.** Review all platform update findings. For any HIGH or MEDIUM risk policy update, create an explicit warning block in the brief that names the prohibited pattern, explains the risk, and suggests a compliant alternative phrasing. These warnings must be visible at the top of the brief — writers must see them before they see the creative direction.

## Output Format

```yaml
weekly_brief:
  week: "<ISO week date range>"
  generated: "<date>"
  compliance_warnings:
    - warning: "<prohibited pattern>"
      risk: "<HIGH|MEDIUM>"
      compliant_alternative: "<suggested replacement approach>"

  categories:
    tarot_perguntas:
      primary_angle:
        direction: "<copy direction>"
        hook_archetype: "<archetype>"
        hook_inspiration: "<example hook text>"
        data_source: "<source>"
        confidence: "<HIGH|MEDIUM|LOW>"
        seasonal_tie: "<optional>"
      secondary_angles:
        - direction: "<direction>"
          hook_inspiration: "<example>"
          confidence: "<level>"

    trabalhos_amorosos:
      # same structure

    benzimento_segunda:
      # same structure

    app:
      # same structure

    benzimento_diario:
      # same structure

  hook_library:
    - hook: "<hook text>"
      archetype: "<archetype>"
      confidence: "<level>"
      categories: ["<cat1>", "<cat2>"]
```

## Output Example

```yaml
weekly_brief:
  week: "2026-03-23 to 2026-03-29"
  generated: "2026-03-24"
  compliance_warnings:
    - warning: "Frases com resultado garantido ('garanto que seu ex volta', 'resultado em X dias garantido')"
      risk: HIGH
      compliant_alternative: "Use linguagem de possibilidade e transformação: 'pode mudar', 'abre o caminho', 'muitas clientes relatam'"

  categories:
    tarot_perguntas:
      primary_angle:
        direction: "Curiosidade baseada em pergunta direta sobre situação amorosa atual"
        hook_archetype: curiosity
        hook_inspiration: "3 sinais que o tarot mostrou que sua relação ainda tem futuro"
        data_source: "Meta Ads Library BR, 2026-03-21"
        confidence: HIGH
        seasonal_tie: "Lua Cheia em Libra (2026-03-27) amplifica perguntas sobre relacionamentos"
      secondary_angles:
        - direction: "Especificidade com número + prazo — tiragem rápida como oferta de entrada"
          hook_inspiration: "Receba sua tiragem em 3 minutos — sem cadastro, sem espera"
          confidence: HIGH
        - direction: "Pain point: incerteza sobre o futuro de uma relação"
          hook_inspiration: "Você ainda não sabe se ele vai voltar. O tarot sabe."
          confidence: MEDIUM

    trabalhos_amorosos:
      primary_angle:
        direction: "Urgência com janela de poder temporal — Lua Cheia como gatilho de ação"
        hook_archetype: urgency
        hook_inspiration: "Lua Cheia em Libra é a janela mais poderosa do mês para o trabalho amoroso. Abre segunda."
        data_source: "Seasonal research + Meta Ads Library pattern, 2026-03-22"
        confidence: HIGH
        seasonal_tie: "Lua Cheia 2026-03-27 — Libra rege amor e uniões"
      secondary_angles:
        - direction: "Prova social com depoimento estruturado + especificidade geográfica"
          hook_inspiration: "Ana, de São Paulo, me disse que era impossível. Em 7 dias, tudo mudou."
          confidence: MEDIUM
        - direction: "Transformação antes/depois sem garantia explícita"
          hook_inspiration: "De silêncio total a mensagem às 2h da manhã. O que mudou?"
          confidence: HIGH

    benzimento_segunda:
      primary_angle:
        direction: "Especificidade do dia — segunda como momento de poder estabelecido"
        hook_archetype: specificity
        hook_inspiration: "Toda segunda-feira é o dia mais poderoso para limpar o que está bloqueando seu amor."
        data_source: "Meta Ads Library BR, 2026-03-18"
        confidence: HIGH
        seasonal_tie: null
      secondary_angles:
        - direction: "Urgência de acesso limitado — vagas semanais como gatilho de escassez"
          hook_inspiration: "Apenas 10 vagas abertas para o benzimento de segunda. Já quase esgotado."
          confidence: MEDIUM
        - direction: "Ritual de abertura de semana — ancoragem emocional em novo começo"
          hook_inspiration: "Como você começa a semana define como ela termina. Comece com proteção."
          confidence: MEDIUM

    app:
      primary_angle:
        direction: "Velocidade + gratuidade como barreira zero de entrada"
        hook_archetype: transformation
        hook_inspiration: "Baixe agora e receba sua tiragem gratuita em menos de 3 minutos."
        data_source: "Meta Ads Library BR, 2026-03-22"
        confidence: HIGH
        seasonal_tie: "Virada de mês (março/abril) — novo ciclo, nova ferramenta"
      secondary_angles:
        - direction: "Curiosidade sobre o app como porta para conteúdo espiritual diário"
          hook_inspiration: "Todo dia um sinal diferente. O app que lê o que você ainda não viu."
          confidence: MEDIUM
        - direction: "Social proof implícito — volume de usuários como validação"
          hook_inspiration: "Mais de 50 mil consultas feitas. O que elas descobriram?"
          confidence: LOW

    benzimento_diario:
      primary_angle:
        direction: "Hábito como proteção — enquadrar benzimento como rotina de autocuidado espiritual"
        hook_archetype: pain_point
        hook_inspiration: "O que você faz todo dia para proteger sua energia? Quem não faz nada, acumula o que não quer."
        data_source: "Pattern from competitor activity analysis, 2026-03-21"
        confidence: MEDIUM
        seasonal_tie: "Fim de março — encerramento de ciclo amplia receptividade a limpeza energética"
      secondary_angles:
        - direction: "Transformação rápida — benzimento diário como micro-ritual acessível"
          hook_inspiration: "5 minutos por dia. Sua energia muda. Sua vida muda."
          confidence: HIGH
        - direction: "Urgência via acúmulo — o custo de não fazer o benzimento"
          hook_inspiration: "Cada dia sem proteção é um dia que o bloqueio se fortalece."
          confidence: MEDIUM

  hook_library:
    - hook: "Hoje à meia-noite, seu ex vai pensar em você — se você fizer isso agora"
      archetype: urgency
      confidence: HIGH
      categories: ["Trabalhos Amorosos", "Benzimento Segunda"]
    - hook: "Lua Cheia em Libra é a janela mais poderosa do mês para o trabalho amoroso"
      archetype: specificity
      confidence: HIGH
      categories: ["Trabalhos Amorosos", "Benzimento Segunda", "Benzimento Diário"]
    - hook: "Baixe agora e receba sua tiragem gratuita em 3 minutos"
      archetype: transformation
      confidence: HIGH
      categories: ["App", "Tarot Perguntas"]
```

## Quality Criteria

- [ ] All 5 categories present with at least one primary angle and one secondary angle each
- [ ] Minimum 3 distinct hook archetypes represented across all category recommendations
- [ ] Compliance warnings section present and populated (even if empty, must include a "no new warnings" confirmation)
- [ ] Every angle recommendation includes a data source and confidence level — no undocumented assertions

## Veto Conditions

- **Veto if fewer than 3 categories have HIGH confidence primary angles.** A brief built mostly on LOW confidence findings does not provide reliable creative direction and must be flagged for expanded research before delivery to the checkpoint.
- **Veto if compliance warnings are absent entirely.** The compliance section is a structural requirement. If it is missing from the output, the brief is incomplete regardless of the quality of the creative direction. This protects the client's ad account from policy violations.
