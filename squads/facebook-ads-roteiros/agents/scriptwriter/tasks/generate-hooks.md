---
task: "Generate Hooks"
order: 1
input: |
  - weekly_brief: Weekly trends brief from researcher
  - weekly_direction: User-confirmed direction per category from checkpoint
  - tone_of_voice: Available tone options
  - domain_framework: S.P.A.R.K. framework reference
output: |
  - hooks_per_category: 3 hooks per category (15 total), each with different emotional trigger and structural type
  - hook_rationale: Psychological reasoning for each hook
  - recommended_tone: Suggested tone per category
---

## Process

For each of the 5 categories, generate 3 hooks using different psychological drivers (pain, curiosity, fear, urgency, social proof, empathy) AND different structural types (question, bold statement, story opening, statistic, warning, direct address).

Rules per hook:
- Maximum 8 words
- Must be spoken aloud — no written-only formatting
- Must stop a distracted viewer in the first 3 seconds
- Each of the 3 hooks per category must use a distinct driver + structure combination
- No forbidden words (feitiço, amarração, magia negra, garantido, cura, elimine)
- No absolute predictions or guaranteed timelines

For each hook, include:
- Hook text (max 8 words)
- Psychological driver
- Structural type
- Rationale (1-2 sentences explaining why it works for this audience)
- Recommended tone (from tone-of-voice.md)

Present all 15 hooks organized by category before moving to next task.

---

## Output Format

```yaml
category: "tarot-perguntas"
hooks:
  - hook: "..."
    words: 8
    psychological_driver: "curiosidade"
    structural_type: "pergunta"
    rationale: "..."
  - hook: "..."
    words: 7
    psychological_driver: "dor"
    structural_type: "afirmação"
    rationale: "..."
  - hook: "..."
    words: 6
    psychological_driver: "prova social"
    structural_type: "estatística"
    rationale: "..."
recommended_tone: "acolhedor"
```

---

## Quality Criteria

- [ ] Cada hook tem no máximo 8 palavras
- [ ] Os 3 hooks de cada categoria usam gatilhos psicológicos DIFERENTES entre si
- [ ] Os 3 hooks usam tipos estruturais DIFERENTES (pergunta, afirmação, história, estatística, etc.)
- [ ] Nenhum hook começa com cumprimento ou apresentação pessoal
- [ ] Cada hook inclui rationale com driver psicológico e razão de eficácia

---

## Veto Conditions

Rejeitar e refazer se QUALQUER condição for verdadeira:
1. Qualquer hook contém palavra proibida pelo Meta (feitiço, amarração, magia negra, garantido, cura)
2. Dois ou mais hooks na mesma categoria usam o mesmo gatilho psicológico

---

## Output Example

```
## HOOKS — SEMANA [DATA]

---

### CATEGORIA 1: Tarot Perguntas
Destino: https://atendimento.bruxasorayatarot.com.br/tarot

**Hook 1A**
"Você ainda não sabe o que fazer, né?"
- Driver: Empatia
- Estrutura: Pergunta direta
- Racional: Valida a paralisia da decisão — o estado emocional mais comum em quem busca tarot. A voz da Soraya com essa linha cria reconhecimento imediato.
- Tom recomendado: Empático e íntimo

**Hook 1B**
"Três cartas revelaram o que ela escondia."
- Driver: Curiosidade
- Estrutura: Declaração narrativa (story opening)
- Racional: Cria uma narrativa aberta que o cérebro precisa fechar. "Ela" é ambíguo — o viewer projeta a própria situação.
- Tom recomendado: Misterioso e confiante

**Hook 1C**
"Pergunta certa. Resposta certa. Próximo passo claro."
- Driver: Urgência / Clareza
- Estrutura: Série de três (ritmo)
- Racional: Endereça a dor específica de quem já tentou tarot genérico e saiu sem direção. Promete precisão sem prometer resultado absoluto.
- Tom recomendado: Direto e seguro

---

### CATEGORIA 2: Trabalhos Amorosos
Destino: Instagram @bruxasorayatarot

**Hook 2A**
"Amor não some. Às vezes ele se perde."
- Driver: Esperança / Dor
- Estrutura: Declaração paradoxal
- Racional: Reframing — transforma perda em possibilidade sem fazer promessa absoluta. Fala diretamente para quem sente que um relacionamento acabou.
- Tom recomendado: Suave e esperançoso

**Hook 2B**
"Minha cliente estava no mesmo lugar que você."
- Driver: Prova social
- Estrutura: Story opening com identificação
- Racional: Abre uma história que o viewer precisa ouvir o final. "Mesmo lugar" cria identificação sem detalhar — deixa o viewer preencher com a própria dor.
- Tom recomendado: Narrativo e caloroso

**Hook 2C**
"Você já tentou de tudo. Eu sei disso."
- Driver: Empatia radical
- Estrutura: Declaração de reconhecimento
- Racional: Valida a exaustão emocional de quem já buscou muitas soluções. Cria confiança antes de qualquer oferta.
- Tom recomendado: Empático e direto

---

### CATEGORIA 3: Benzimento Segunda
Destino: https://benzimento.bruxasorayatarot.com.br

**Hook 3A**
"Segunda pesada? Pode ser mais do que cansaço."
- Driver: Medo / Curiosidade
- Estrutura: Pergunta + sugestão
- Racional: Recontextualiza uma experiência cotidiana universal (segunda-feira ruim) como algo que pode ter raiz energética. Cria abertura para o produto.
- Tom recomendado: Intrigante e empático

**Hook 3B**
"Comecei a benzer às segundas. Mudou tudo."
- Driver: Prova social (primeira pessoa)
- Estrutura: Declaração pessoal de resultado
- Racional: Soraya fala da própria prática, construindo autoridade sem fazer promessa ao viewer. "Mudou tudo" é vago o suficiente para não ser uma garantia explícita.
- Tom recomendado: Pessoal e confiante

**Hook 3C**
"Sete dias. Sete começos. Um benzimento muda isso."
- Driver: Urgência / Ritmo
- Estrutura: Série numérica
- Racional: Cria ritmo e urgência semanal sem prometer resultados em prazo específico. O benzimento é posicionado como reset energético, não como solução garantida.
- Tom recomendado: Energético e direto

---

### CATEGORIA 4: App
Destino: https://app.bruxasorayatarot.com.br

**Hook 4A**
"Tarot no bolso. Orientação quando você precisar."
- Driver: Conveniência / Autonomia
- Estrutura: Benefício duplo em paralelo
- Racional: Fala para o público mais jovem e independente. Posiciona o app como ferramenta de empoderamento, não de dependência.
- Tom recomendado: Moderno e prático

**Hook 4B**
"Eu não sabia que podia ter acesso assim."
- Driver: Surpresa / Descoberta
- Estrutura: Declaração de revelação (primeira pessoa)
- Racional: Simula a reação que o viewer deveria ter. Cria curiosidade sobre o que é "assim" sem revelar antes do CTA.
- Tom recomendado: Conversacional e animado

**Hook 4C**
"Três mil pessoas já acessaram. Por que não você?"
- Driver: Prova social + provocação
- Estrutura: Estatística + pergunta retórica
- Racional: Usa número específico para credibilidade e a pergunta cria uma pequena tensão que o viewer precisa resolver clicando.
- Tom recomendado: Confiante e provocador

---

### CATEGORIA 5: Benzimento Diário
Destino: Telegram t.me/magiasdabruxasoraya

**Hook 5A**
"Todo dia às 7h. Benzimento gratuito no Telegram."
- Driver: Urgência / Curiosidade + Gratuidade
- Estrutura: Especificidade de horário + oferta
- Racional: Horário específico cria rotina e comprometimento. "Gratuito" remove a barreira de entrada. A especificidade diferencia de conteúdo vago.
- Tom recomendado: Direto e generoso

**Hook 5B**
"Você não precisa fazer nada. Só receber."
- Driver: Facilidade / Alívio
- Estrutura: Declaração de redução de esforço
- Racional: Endereça a fadiga espiritual de quem já tentou práticas complicadas. Posiciona o benzimento como passivo — você apenas está presente.
- Tom recomendado: Suave e acolhedor

**Hook 5C**
"Proteção diária existe. Eu ofereço de graça."
- Driver: Autoridade + Generosidade
- Estrutura: Declaração de autoridade + oferta
- Racional: Estabelece que proteção diária é algo real e acessível, e Soraya é quem oferece. A gratuidade é o driver de conversão para o canal Telegram.
- Tom recomendado: Seguro e generoso
```
