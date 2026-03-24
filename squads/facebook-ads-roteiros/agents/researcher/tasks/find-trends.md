---
task: "Find Weekly Trends"
order: 1
input: |
  - research_focus: User-defined research focus from checkpoint (topic, time range)
  - company_context: Bruxa Soraya Tarot profile and services
output: |
  - trending_hooks: List of 10+ hooks currently performing well in spiritual/relationship niche
  - platform_updates: Any recent Meta/Facebook policy changes or algorithm updates
  - competitor_activity: What top spiritual advertisers are doing this week
  - seasonal_angles: Date-based or seasonal opportunities (moon phases, holidays, etc.)
---

# Find Weekly Trends

Search the current digital landscape for what is converting in spiritual and relationship Facebook Ads right now. This task produces raw intelligence — unfiltered trend data, hook patterns, competitor signals, and seasonal angles — that the compile-weekly-brief task will synthesize into a structured brief. Freshness is the primary quality criterion: every finding must be traceable to a source within the user-defined time range.

## Process

1. **Search for current trending hooks in the spiritual Facebook Ads niche.** Query Meta Ads Library for active ads from spiritual service accounts (tarot, love spells, benzimento, amarração, orações). Identify recurring language patterns in headlines, primary text openers, and CTAs. Note engagement signals where visible. Also search web for "Facebook Ads tarot 2026", "anúncio espiritual Facebook tendências", "hooks para anúncios de tarot", and variations. Tag each hook with its apparent archetype (urgency, curiosity, social proof, pain-point, transformation promise, specificity).

2. **Identify Meta/Facebook platform and policy updates.** Search for recent announcements from Meta regarding ad policies, especially any updates affecting spiritual services, relationship content, or claims of guaranteed outcomes. Check for enforcement pattern reports from digital marketing communities. Query: "Meta Ads policy update 2026", "Facebook anúncio espiritual reprovado", "Meta restricted categories spiritual". Flag any new restrictions or enforcement trends that could affect the client's ad creative.

3. **Analyze competitor activity.** Search Meta Ads Library for the top active spiritual advertisers in Brazil. Look for Bruxa Soraya Tarot competitors — tarot readers, trabalho espiritual providers, benzimento services — running active Facebook campaigns. Document their hook styles, offer framing, visual/copy patterns, and apparent CTAs. Note any new angles that were not present in prior weeks.

4. **Map seasonal and astrological angles for the current production week.** Research upcoming moon phases, astrological transits, and spiritual/cultural calendar events for the coming week. Query: "lua fase março 2026", "trânsito astral semana", "datas especiais espiritual março 2026". Cross-reference with Brazilian holidays or commemorative dates that may carry emotional resonance for the target audience.

## Output Format

```yaml
trending_hooks:
  - hook: "<hook text or pattern>"
    archetype: "<urgency|curiosity|social_proof|pain_point|transformation|specificity>"
    source: "<source name and date>"
    confidence: "<HIGH|MEDIUM|LOW>"
    category_fit: ["<category1>", "<category2>"]
  # repeat for 10+ hooks

platform_updates:
  - update: "<description of policy or algorithm change>"
    impact: "<how this affects ad creation for this client>"
    source: "<source and date>"
    risk_level: "<HIGH|MEDIUM|LOW>"

competitor_activity:
  - advertiser: "<name or identifier>"
    hook_pattern: "<observed hook style>"
    offer_framing: "<how they frame the offer>"
    notable_angle: "<anything new or notable>"
    source: "<Meta Ads Library or other, date>"

seasonal_angles:
  - angle: "<specific opportunity>"
    date_or_event: "<when>"
    resonance: "<why this works for the spiritual audience>"
    category_fit: ["<category1>"]
```

## Output Example

```yaml
trending_hooks:
  - hook: "Hoje à meia-noite, seu ex vai pensar em você — se você fizer isso agora"
    archetype: urgency
    source: "Meta Ads Library BR, 2026-03-22"
    confidence: HIGH
    category_fit: ["Trabalhos Amorosos", "Benzimento Segunda"]
  - hook: "3 sinais que o tarot mostrou que seu relacionamento tem cura"
    archetype: curiosity
    source: "Meta Ads Library BR, 2026-03-21"
    confidence: HIGH
    category_fit: ["Tarot Perguntas", "Trabalhos Amorosos"]
  - hook: "Ela me disse que era impossível. O trabalho de 7 dias provou o contrário."
    archetype: social_proof
    source: "Web search: depoimento trabalho espiritual Facebook, 2026-03-20"
    confidence: MEDIUM
    category_fit: ["Trabalhos Amorosos", "Benzimento Diário"]
  - hook: "Você sabia que toda segunda-feira é o dia mais poderoso para o benzimento?"
    archetype: specificity
    source: "Meta Ads Library BR, 2026-03-18"
    confidence: HIGH
    category_fit: ["Benzimento Segunda"]
  - hook: "Baixe agora e receba sua tiragem gratuita em 3 minutos"
    archetype: transformation
    source: "Meta Ads Library BR, 2026-03-22"
    confidence: HIGH
    category_fit: ["App", "Tarot Perguntas"]

platform_updates:
  - update: "Meta reforçou restrições em anúncios com linguagem de 'resultado garantido' em serviços espirituais"
    impact: "Evitar frases como 'garanto que seu ex volta' ou 'resultado em X dias garantido'"
    source: "Meta Business Help Center, 2026-03-15"
    risk_level: HIGH
  - update: "Vídeos curtos (15-30s) estão recebendo prioridade de entrega no feed mobile no Brasil"
    impact: "Scripts para formato vídeo devem ter hook nos primeiros 3 segundos"
    source: "Meta for Business blog, 2026-03-10"
    risk_level: LOW

competitor_activity:
  - advertiser: "Tarot da Mãe Joana (BR)"
    hook_pattern: "Pergunta direta sobre situação amorosa atual"
    offer_framing: "Consulta gratuita como isca, upgrade pago"
    notable_angle: "Usando urgência de vagas limitadas pela primeira vez esta semana"
    source: "Meta Ads Library, 2026-03-22"
  - advertiser: "Mestre Espiritual Claudio (BR)"
    hook_pattern: "Depoimento de cliente em texto longo com nome e cidade"
    offer_framing: "Trabalho completo com prazo de 7 dias"
    notable_angle: "Novo criativo com fundo de vela vermelha — alta frequência de veiculação"
    source: "Meta Ads Library, 2026-03-21"

seasonal_angles:
  - angle: "Lua Cheia em Libra — signos do amor e equilíbrio"
    date_or_event: "2026-03-27"
    resonance: "Audiência espiritual responde fortemente a janelas de poder lunar para trabalhos amorosos"
    category_fit: ["Trabalhos Amorosos", "Benzimento Segunda", "Benzimento Diário"]
  - angle: "Fim de março — véspera de abril, mês de recomeços"
    date_or_event: "2026-03-28 a 2026-03-31"
    resonance: "Transição de mês cria abertura para ângulos de 'novo ciclo' e transformação"
    category_fit: ["Tarot Perguntas", "App"]
```

## Quality Criteria

- [ ] Minimum 10 hooks identified, each with source, confidence level, and category fit tags
- [ ] At least one Meta policy update or enforcement pattern documented (even if status is "no new updates this week")
- [ ] At least 2 competitors analyzed with hook pattern and offer framing documented
- [ ] At least 1 seasonal or astrological angle identified and mapped to a specific date within the production window

## Veto Conditions

- **Veto if all hooks lack citations.** Hooks without traceable sources must not be passed to the brief compilation step. Fabricated or uncited hooks could pollute the entire production pipeline with unverified patterns.
- **Veto if no category coverage exists for 2 or more categories.** If the research yields no relevant findings for Tarot Perguntas, Trabalhos Amorosos, Benzimento Segunda, App, or Benzimento Diário, the task must flag this gap explicitly and request a broadened search scope rather than delivering an incomplete output silently.
