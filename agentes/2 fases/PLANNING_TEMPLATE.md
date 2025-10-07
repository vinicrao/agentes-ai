# 📄 PLANNING.md

## Status Atual
(Selecionar um dos estados abaixo)
- **Planejado** → Safira elaborou parte do planejamento, ainda sendo refinado com o usuário.
- **Pronto para desenvolvimento** → Usuário validou o plano completo, pronto para começar a implementação.
- **Pronto para teste** → Implementação concluída, QA pode testar visualmente.
- **Pendente ajuste** → QA abriu issue; Safira e QA iteram até resolver.
- **Concluído** → Testes visuais passaram e a tarefa está finalizada.

---

## 1. Objetivo
(Resumo breve da feature ou correção. Iniciado logo no começo, refinado conforme o usuário responde às perguntas da Safira.)

---

## 2. Referências
(Lista de links ou tickets. Safira deve perguntar ao usuário sempre que não houver clareza.)

---

## 3. Acceptance Criteria
(Lista de pontos verificáveis. Pode começar vazia e ser incrementada conforme as conversas.)
- [ ] Critério 1
- [ ] Critério 2

---

## 4. Análise Figma (Automática)
Esta seção é preenchida automaticamente ao extrair dados via MCP do Figma.

### 4.0.1 Estados Visuais Identificados
Lista de todos os node-ids extraídos e seus estados correspondentes:
- `node-id=15800-216876` → Card Padrão (Caminho Feliz)
- `node-id=15800-221745` → Estado Vazio
- …

### 4.0.2 Design Tokens Extraídos
Tokens de design obtidos via `get_variable_defs`:
- **Cores:**
  - `primary-color`: #HEXCODE
  - `error-color`: #HEXCODE
- **Tipografia:**
  - `heading-large`: 24px / Bold / Inter
  - `body-regular`: 16px / Regular / Inter
- **Espaçamentos:**
  - `spacing-m`: 16px
  - `spacing-l`: 24px

### 4.0.3 Hierarquia de Componentes (Metadata)
Estrutura extraída do Figma via `get_metadata`:
```
Card Container
├── Header
│   ├── Title
│   └── Info Icon
├── Content
│   ├── Balance Section
│   ├── Chart
│   └── Currency Details
└── Footer
    └── CTA Button
```

---

## 5. Planejamento Detalhado (Incremental)
Este bloco deve evoluir em várias iterações até que o usuário confirme estar completo.

### 5.1 Árvore de Componentes
(Estrutura inicial pode ser esboçada e depois refinada, baseada na hierarquia do Figma.)

### 5.2 Especificações Atômicas
- **Espaçamentos**: (extraídos dos tokens do Figma)
- **Tipografia**: (extraídos dos tokens do Figma)
- **Cores**: (extraídos dos tokens do Figma)
- **Estados**: (mapeados da especificação funcional)

### 5.3 Regras de Layout / Breakpoints
Safira deve perguntar sobre comportamento esperado em cada tela (mobile, tablet, desktop) e atualizar progressivamente.
- **Grid / Colunas**: …
- **Margens / Padding**: …
- **Comportamento esperado de cada componente por breakpoint**:
- Componente X → Mobile: … / Tablet: … / Desktop: …

---

## 6. Testes Visuais Planejados
- Comparação da implementação com Figma via Playwright.
- Safira deve confirmar com o usuário quais frames/screens são prioritários para validação.
- Screenshots de referência: `./figma/[estado].png`
- Screenshots de teste: `./evidence/[estado]-test.png`

---

## 7. Commits Realizados
(Lista incremental. Safira vai atualizando conforme desenvolve.)
- …

---

## 8. Evidências
### 8.1 Screenshots Figma (Referência)
- `./figma/card-padrao.png` (node-id=15800-216876)
- `./figma/estado-vazio.png` (node-id=15800-221745)
- …

### 8.2 Screenshots Implementação (Playwright)
- `./evidence/card-padrao-test.png`
- `./evidence/estado-vazio-test.png`
- …

### 8.3 Relatório de Comparação Visual
| Estado | Figma | Implementação | Status | Divergências |
|--------|-------|---------------|--------|--------------|
| Card Padrão | ✅ | ✅ | ✅ Pass | - |
| Estado Vazio | ✅ | ❌ | ❌ Fail | Espaçamento do botão +4px |
