---
execution: inline
agent: squads/facebook-ads-roteiros/agents/scriptwriter
inputFile: squads/facebook-ads-roteiros/output/weekly-trends-brief.md
outputFile: squads/facebook-ads-roteiros/output/hooks-selection.md
---

## Step 04 — Generate Hooks

Gabi Gancho executes this step after the researcher's brief is ready and the user has confirmed weekly direction at step-03 checkpoint.

---

## Context Loading

Load the following files before starting:

1. `squads/facebook-ads-roteiros/output/weekly-trends-brief.md` — weekly trending topics, content signals, and audience observations from the researcher
2. `squads/facebook-ads-roteiros/context/tone-of-voice.md` — available tone options with descriptions
3. `squads/facebook-ads-roteiros/context/domain-framework.md` — S.P.A.R.K. framework reference, category definitions, and landing page destinations
4. `squads/facebook-ads-roteiros/output/weekly-direction.md` — confirmed direction per category from step-03 checkpoint

---

## Instructions

### Process
1. Carregar o weekly-trends-brief.md e identificar tendências relevantes para cada categoria
2. Carregar o domain-framework.md e revisar as fórmulas de hook do S.P.A.R.K.
3. Para cada uma das 5 categorias, gerar 3 hooks usando gatilhos psicológicos e tipos estruturais diferentes
4. Incluir rationale para cada hook explicando o driver psicológico e por que funciona para o público-alvo
5. Recomendar um tom de voz para cada categoria baseado nas tendências da semana

Generate 3 hooks per category = 15 hooks total.

For each category, apply these rules:
- Each of the 3 hooks must use a **different psychological driver** (pain, curiosity, fear, urgency, social proof, empathy, hope, authority)
- Each of the 3 hooks must use a **different structural type** (question, bold statement, story opening, statistic, warning, series/rhythm, direct address, paradox)
- Maximum 8 words per hook
- No forbidden words: feitiço, amarração, magia negra, garantido, cura, elimine
- No absolute predictions or guaranteed timelines
- Hooks must be speakable — written for voice, not for reading

For each hook, include:
- Hook text
- Psychological driver
- Structural type
- Rationale (why this works for this audience segment)
- Recommended tone from tone-of-voice.md

---

## Output

Present all 15 hooks organized by category. Use this structure:

```
## HOOKS — SEMANA [DATA]

### CATEGORIA 1: [Name]
Destino: [URL ou canal]

Hook 1A — [texto]
- Driver: [driver]
- Estrutura: [tipo]
- Racional: [reasoning]
- Tom: [tone]

Hook 1B — [texto]
...

Hook 1C — [texto]
...

[repeat for all 5 categories]
```

Save full output to `squads/facebook-ads-roteiros/output/hooks-selection.md`.

---

## Output Example

```
## HOOKS — SEMANA 24 MAR 2026

### CATEGORIA 1: Tarot Perguntas
Destino: https://atendimento.bruxasorayatarot.com.br/tarot

Hook 1A — "Você ainda não sabe o que fazer, né?"
- Driver: Empatia
- Estrutura: Pergunta direta
- Racional: Valida a paralisia de decisão — estado emocional mais comum em quem busca tarot. Reconhecimento imediato.
- Tom: Empático e íntimo

Hook 1B — "Três cartas revelaram o que ela escondia."
- Driver: Curiosidade
- Estrutura: Declaração narrativa
- Racional: Abre uma história que o cérebro precisa fechar. "Ela" é ambíguo — viewer projeta a própria situação.
- Tom: Misterioso e confiante

Hook 1C — "Pergunta certa. Resposta certa. Próximo passo claro."
- Driver: Urgência / Clareza
- Estrutura: Série de três
- Racional: Endereça a dor de quem já tentou tarot genérico e saiu sem direção.
- Tom: Direto e seguro

---

### CATEGORIA 2: Trabalhos Amorosos
Destino: Instagram @bruxasorayatarot

Hook 2A — "Amor não some. Às vezes ele se perde."
- Driver: Esperança / Dor
- Estrutura: Declaração paradoxal
- Racional: Reframing que transforma perda em possibilidade sem promessa absoluta.
- Tom: Suave e esperançoso

Hook 2B — "Minha cliente estava no mesmo lugar que você."
- Driver: Prova social
- Estrutura: Story opening com identificação
- Racional: Abre história que viewer precisa ouvir o final. "Mesmo lugar" cria identificação.
- Tom: Narrativo e caloroso

Hook 2C — "Você já tentou de tudo. Eu sei disso."
- Driver: Empatia radical
- Estrutura: Declaração de reconhecimento
- Racional: Valida exaustão emocional de quem já buscou muitas soluções.
- Tom: Empático e direto

---

### CATEGORIA 3: Benzimento Segunda
Destino: https://benzimento.bruxasorayatarot.com.br

Hook 3A — "Segunda pesada? Pode ser mais do que cansaço."
- Driver: Medo / Curiosidade
- Estrutura: Pergunta + sugestão
- Racional: Recontextualiza experiência cotidiana como algo com raiz energética.
- Tom: Intrigante e empático

Hook 3B — "Comecei a benzer às segundas. Mudou tudo."
- Driver: Prova social (primeira pessoa)
- Estrutura: Declaração pessoal de resultado
- Racional: Soraya fala da própria prática, construindo autoridade sem promessa ao viewer.
- Tom: Pessoal e confiante

Hook 3C — "Sete dias. Sete começos. Um benzimento muda isso."
- Driver: Urgência / Ritmo
- Estrutura: Série numérica
- Racional: Cria ritmo e urgência semanal sem prometer resultados em prazo específico.
- Tom: Energético e direto

---

### CATEGORIA 4: App
Destino: https://app.bruxasorayatarot.com.br

Hook 4A — "Tarot no bolso. Orientação quando você precisar."
- Driver: Conveniência / Autonomia
- Estrutura: Benefício duplo em paralelo
- Racional: Posiciona o app como ferramenta de empoderamento para público independente.
- Tom: Moderno e prático

Hook 4B — "Eu não sabia que podia ter acesso assim."
- Driver: Surpresa / Descoberta
- Estrutura: Declaração de revelação
- Racional: Simula a reação que o viewer deveria ter. Cria curiosidade sobre o que é "assim".
- Tom: Conversacional e animado

Hook 4C — "Três mil pessoas já acessaram. Por que não você?"
- Driver: Prova social + provocação
- Estrutura: Estatística + pergunta retórica
- Racional: Número específico cria credibilidade; pergunta cria tensão que viewer resolve clicando.
- Tom: Confiante e provocador

---

### CATEGORIA 5: Benzimento Diário
Destino: Telegram t.me/magiasdabruxasoraya

Hook 5A — "Todo dia às 7h. Benzimento gratuito no Telegram."
- Driver: Urgência + Gratuidade
- Estrutura: Especificidade de horário + oferta
- Racional: Horário específico cria rotina. "Gratuito" remove barreira de entrada.
- Tom: Direto e generoso

Hook 5B — "Você não precisa fazer nada. Só receber."
- Driver: Facilidade / Alívio
- Estrutura: Declaração de redução de esforço
- Racional: Endereça fadiga espiritual de quem já tentou práticas complicadas.
- Tom: Suave e acolhedor

Hook 5C — "Proteção diária existe. Eu ofereço de graça."
- Driver: Autoridade + Generosidade
- Estrutura: Declaração de autoridade + oferta
- Racional: Estabelece que proteção diária é real e acessível, com Soraya como fonte.
- Tom: Seguro e generoso
```

After saving output, trigger step-05-select-hooks.md checkpoint.

---

## Veto Conditions

Rejeitar e refazer se QUALQUER condição for verdadeira:
1. Qualquer hook contém palavra proibida pelo Meta (feitiço, amarração, magia negra, garantido, cura)
2. Dois ou mais hooks na mesma categoria usam o mesmo gatilho psicológico
3. Qualquer hook ultrapassa 8 palavras

---

## Quality Criteria

- [ ] 15 hooks gerados no total (3 por categoria × 5 categorias)
- [ ] Cada hook tem no máximo 8 palavras
- [ ] Os 3 hooks de cada categoria usam gatilhos psicológicos DIFERENTES
- [ ] Os 3 hooks usam tipos estruturais DIFERENTES
- [ ] Cada hook inclui rationale com driver psicológico
- [ ] Tom de voz recomendado para cada categoria
