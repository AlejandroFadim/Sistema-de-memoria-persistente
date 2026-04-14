# 🧠 Sistema de Memória Persistente

**Inteligência Analítica Nível 4-6 — Arquitetura Obsidian Style**

> Memória agressiva + Grafo de Conhecimento + RAG Local + Memory Decay + Automação via Hooks

---

## 📊 O Que É Este Sistema?

Um **sistema completo de inteligência analítica** que funciona como sua "segunda mente":

- ✅ **Captura TUDO automaticamente** (pessoas, conceitos, decisões, insights)
- ✅ **Conecta informações** em grafo de conhecimento (25+ nós, 188+ links)
- ✅ **Busca semântica** em sua base de conhecimento (RAG local)
- ✅ **Memória temporal** — notas antigas perdem peso automaticamente
- ✅ **Automação** — hooks que regeneram grafo, extraem entidades, detectam gaps
- ✅ **Continua entre sessões** — você nunca perde contexto

**Status:** ✅ Operacional (Nível 4-6) | 🚀 Roadmap para Nível 7-8

---

## 🎯 Para Quem É?

- **BI Analysts** — aprendendo base de dados, explorando SQL
- **Data Scientists** — rastreando experimentos, insights, decisões
- **Product Managers** — documentando roadmap, feedback, estratégia
- **Consultores** — mantendo contexto entre múltiplos clientes
- **Qualquer profissional** — que precisa de inteligência acumulada

---

## 🚀 Quick Start (15 minutos)

### **1. Copie Esta Pasta**

```bash
# Opção 1: Git
git clone https://github.com/AlejandroFadim/Sistema-de-memoria-persistente seu_centro_ia
cd seu_centro_ia

# Opção 2: Download manual
# Baixe como ZIP → descompacte em C:\seu_centro_ia
```

### **2. Instale Dependências**

```bash
pip install openpyxl pandas networkx flask chroma-db openai
```

### **3. Abra no Claude Code**

```bash
claude-code .
```

### **4. Cole Este Comando no Chat**

```
/iniciar
```

Sistema carrega contexto. Depois:

```
/bootstrap
```

Responda 3 perguntas simples:
- **Qual é sua empresa?** (ex: "Sou Analytics em fintech")
- **Quais são seus projetos?** (ex: "Dashboard Transações, Relatório Fraude")
- **Qual é seu cargo?** (ex: "Analista de Dados Senior")

**✅ Pronto!** Sistema operacional em ~15 minutos.

---

## 📖 Como Usar (Passo-a-Passo)

### **Dia 1 — Primeira Sessão**

#### Passo 1: Inicializar
```bash
claude-code .
```

No chat, digite:
```
/iniciar
```

**Sistema mostra:**
```
✅ Sistema de Inteligência carregado.

Quem você é:
- Cargo: Analista de Dados Senior
- Empresa: ACME Corp Fintech
- Clientes: Banco XYZ, Varejo ABC
- Ferramentas: Power BI, SQL, Python

Projetos ativos: 3
- Dashboard Transações (em andamento)
- Relatório Fraude (planejado)
- Análise de Churn (em análise)

Pronto para trabalhar. O que vamos fazer?
```

#### Passo 2: Trabalhe Normalmente

Você diz algo como:
```
Preciso explorar a tabela de transações no banco de dados.
Quantas transações temos por dia? Há padrões sazonais?
```

**Sistema faz:**
1. ✅ Escreve query SQL
2. ✅ Executa análise
3. ✅ **CAPTURA AUTOMATICAMENTE:**
   - Novo conceito: `memoria/conceitos/transacoes.md`
   - Decisão: `memoria/decisoes/2026-04-14_explorar_transacoes.md`
   - Insight: "3.2M transações/dia em média"

#### Passo 3: Ao Terminar

Digite:
```
/encerrar
```

**Automático:**
- ✅ Grafo regenerado (`output/grafo_memoria.html`)
- ✅ Sessão registrada (`memoria/sessoes/sessao_2026-04-14.md`)
- ✅ Backlinks atualizados
- ✅ Próximos passos mapeados

---

### **Dia 2 — Continuidade**

```bash
claude-code .
```

Digite:
```
/iniciar
```

**Sistema mostra:**
```
✅ Sistema carregado.

Últimos próximos passos:
- Você estava explorando transações
- Descobriu: 3.2M/dia em média, padrão semanal
- Próximo: investigar causa da sazonalidade

Grafo conecta:
  Transações ← Banco XYZ ← Casos de Uso ← PDV
  Transações ← Sazonalidade ← [novo conceito]

Pronto para continuar?
```

Você já tem contexto completo. **Continua exatamente de onde parou.**

---

## 🧭 Arquitetura em 8 Níveis

```
┌─────────────────────────────────────────┐
│         NÍVEL 8: Inteligência Proativa  │ 🔮 Futuro
│  (Alertas automáticos, recomendações)   │ 2026-06-01
└─────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────┐
│     NÍVEL 7: Multi-Agente Especializado │ 🚀 Próximo
│  (Agentes dados, negócio, design, memory)│ 2026-05-01
└─────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────┐
│  NÍVEL 6: Extração Automática + Hooks   │ ✅ AQUI
│  (NER, PreToolUse, Stop, gap analysis)  │ Operacional
└─────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────┐
│    NÍVEL 5: Memória Temporal + Decay    │ ✅ Implementado
│   (Timeline, decay exponencial, anomalias) │
└─────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────┐
│    NÍVEL 4: Grafo de Conhecimento       │ ✅ Implementado
│  (25+ nós, 188+ links, vis.js interativo) │
└─────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────┐
│      NÍVEL 3: RAG Local + Embeddings    │ ✅ Implementado
│  (Busca semântica em sua base, ChromaDB) │
└─────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────┐
│     NÍVEL 2: Índice Semântico + Tags    │ ✅ Implementado
│  (MEMORY.md, frontmatter, wikilinks)    │
└─────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────┐
│          NÍVEL 1: Memória Estática      │ ✅ Implementado
│        (Arquivos .md em pasta)          │
└─────────────────────────────────────────┘
```

---

## 💡 Exemplo Real: Fintech

### **Cenário**
Você é novo em uma fintech. Precisa aprender:
- Base de transações (100M+ linhas/mês)
- Regras de fraude
- Padrões de clientes

### **Sem Sistema**
```
Dia 1: Exploro tabelas, tomo notas (ou não)
Dia 5: "Qual era aquele padrão mesmo?"
       → Procuro em emails, chats, notebooks
       → Perco 1h
Dia 10: Novo projeto similar
        → Reexploro tudo (já fiz isso?)
        → Reescrevo queries
        → Desperdiço 8h em repetição
```

### **Com Sistema**
```
Dia 1: Exploro tabelas
       ✅ Sistema cria: memoria/conceitos/transacoes.md
       ✅ Conecta: Transação ← Cliente ← Fraude

Dia 5: Preciso lembrar
       → /iniciar carrega contexto
       → RAG busca "padrão semanal"
       → Encontra em 30 segundos

Dia 10: Novo projeto (Churn)
        → Sistema sugere: "Churn relaciona com Transações (já explorado)"
        → Reutiliza 80% do contexto
        → Ganha 6h produtivas
```

---

## 📁 Estrutura de Pastas (Criada Automaticamente)

```
seu_centro_ia/
├── CLAUDE.md                          ← Missão + 7 regras
├── memoria/
│   ├── MEMORY.md                      ← Índice (carregado sempre)
│   ├── PADRAO_MEMORIA.md              ← Template de estrutura
│   ├── user_profile.md                ← Seu perfil (preenchido)
│   ├── feedback_memoria.md            ← Regras de colaboração
│   ├── RAG_GUIA.md                    ← Como buscar
│   ├── DECAY_CONFIG.json              ← Parâmetros decay
│   ├── conceitos/                     ← 1 conceito = 1 arquivo
│   │   ├── transacoes.md              (criado automaticamente)
│   │   ├── fraude.md
│   │   └── ...
│   ├── pessoas/                       ← Stakeholders
│   │   ├── seu_chefe.md               (criado automaticamente)
│   │   └── ...
│   ├── decisoes/                      ← Decisões datadas
│   │   ├── 2026-04-14_explorar_transacoes.md
│   │   └── ...
│   └── sessoes/                       ← Diários de sessão (automático)
│       ├── sessao_2026-04-14.md
│       └── ...
├── scripts/                           ← 15 scripts Python
│   ├── auto_memoria.py                (hook Stop)
│   ├── classificar_modelo.py          (hook PreToolUse)
│   ├── grafo_memoria.py               (constrói grafo)
│   ├── rag_memoria.py                 (busca semântica)
│   ├── memory_decay.py                (decay temporal)
│   └── ... (10 mais)
├── .claude/
│   └── settings.local.json            ← Hooks (Stop + PreToolUse)
├── output/
│   ├── grafo_memoria.html             (gerado automaticamente)
│   ├── grafo_memoria.json
│   ├── timeline.html
│   ├── anomalies.json
│   └── gap_analysis.json
└── <seu_projeto>/                     ← Projetos individuais
    ├── CLAUDE.md
    ├── DATA/
    └── output/
```

---

## ⚙️ Comandos Principais

### **Iniciar Sessão**
```
/iniciar
```
Carrega contexto completo: CLAUDE.md, MEMORY.md, últimas sessões, grafo.

### **Bootstrap (Primeira Vez)**
```
/bootstrap
```
Cria estrutura automática. Responda 3 perguntas (empresa, projetos, cargo).

### **Encerrar Sessão**
```
/encerrar
```
Hook Stop executa: regenera grafo, registra sessão, atualiza backlinks.

### **Compactar (Avançado)**
```
/compactar
```
Executa todas as análises: memory_decay, anomaly_detector, gap_analyzer, entity_extractor.

### **Buscar Semanticamente (Avançado)**
```
/rag "sua pergunta aqui"
```
Busca semântica em memoria/ por relevância. Retorna top-5 arquivos.

---

## 🎓 Curva de Aprendizado

| Tempo | O Que Você Sabe |
|-------|-----------------|
| **Hora 0-1** | "Entendi, vou tentar" |
| **Hora 1-2** | "Como busco na memória?" → Usa `/rag` |
| **Dia 1-2** | "Sistema está capturando coisas sozinho!" |
| **Semana 1** | "Grafo mostra conexões que não esperava" |
| **Semana 2** | "Consigo encontrar insights antigos em 10s" |
| **Semana 3** | "Comecei a usar RAG semanticamente" |
| **Semana 4+** | "Reutilizo contexto entre projetos" |

---

## 📊 Métricas (Sistema em Produção)

Sistema testado em produção (SPOT Promo × Camil):

- ✅ **25+ nós no grafo** (conceitos, pessoas, projetos)
- ✅ **188+ links** (relacionamentos)
- ✅ **7+ projetos** ativos em paralelo
- ✅ **4+ decisões** registradas por semana
- ✅ **15 scripts** funcionais
- ✅ **0 contexto perdido** entre sessões

---

## ❓ FAQ

### P: Preciso saber programação?
**R:** Não para começar. Sistema funciona via Claude Code (interface IA). Python é para customizações avançadas.

### P: Funciona com qualquer domínio?
**R:** Sim! Funciona com SQL, Power BI, dados, análises, qualquer empresa, qualquer indústria.

### P: Quanto custa?
**R:** Haiku (padrão) é ~10x mais barato que Sonnet. Tudo local em seu PC.

### P: Posso compartilhar com um colega?
**R:** Sim! Clone para nova pasta com novo perfil. Sistema independente por pasta.

### P: Como backup a memória?
**R:** Pasta `memoria/` é seu backup. Versione no Git. `output/` é gerado — não versione.

### P: Posso integrar GitHub/Slack?
**R:** Sim! Nível 8 (futuro) terá isso automático. Por enquanto manual.

---

## 🚨 Troubleshooting

| Problema | Solução |
|----------|---------|
| `/iniciar` não carrega | Execute `/bootstrap` primeiro |
| Grafo não atualiza | Execute manualmente: `py scripts/auto_memoria.py` |
| RAG não funciona | Instale: `pip install chroma-db openai` |
| Wikilinks quebrados | Execute: `py scripts/anomaly_detector.py` |
| Gaps na memória | Execute: `py scripts/gap_analyzer.py` |

---

## 🔄 Workflow Típico (Diário)

```
MANHÃ:
  09:00 — claude-code .
  09:05 — /iniciar (carrega contexto)
  09:10 — Trabalha normalmente ("Preciso analisar...")
          Sistema captura automaticamente

DURANTE O DIA:
  Você menciona: "Decidi usar Power BI para dashboard"
  Sistema cria: memoria/decisoes/2026-04-14_usar_powerbi.md
  Conecta: [[dashboard]] [[power_bi]] [[projeto_x]]

FIM DO DIA:
  17:00 — /encerrar (ou /compactar)
  Hook Stop executa: memory_decay + auto_memoria + entity_extractor
  ✅ Grafo atualizado
  ✅ Sessão registrada
  ✅ Próximos passos mapeados

PRÓXIMO DIA:
  09:05 — /iniciar
  → Sistema carrega TUDO de onde parou
  → Você continua imediatamente
```

---

## 📚 Arquivos Importantes

| Arquivo | Propósito |
|---------|----------|
| **BOOTSTRAP_INTELIGENCIA.json** | Especificação técnica (482 linhas) |
| **README.md** | Este guia (o que está lendo) |
| **CLAUDE.md** (raiz) | Missão + 7 regras + tabela projetos |
| **memoria/PADRAO_MEMORIA.md** | Como estruturar novas memórias |
| **memoria/RAG_GUIA.md** | Como buscar semanticamente |
| **_templates/ROADMAP_MEMORIA_AVANCADA.md** | Roadmap 8 níveis |

---

## 🚀 Começar Agora

1. **Clone/Copie esta pasta**
2. **Instale dependências:** `pip install -r requirements.txt`
3. **Abra no Claude Code:** `claude-code .`
4. **Execute:** `/iniciar`
5. **Execute:** `/bootstrap`
6. **Trabalhe normalmente**

**Sistema captura tudo automaticamente.** ✅

---

## 📞 Suporte / Feedback

Este sistema foi desenvolvido e testado em produção.

Dúvidas? Ideias? Abra issue ou discuta com seu agente de IA.

---

**v4.2 — 2026-04-14**

Desenvolvido em produção para SPOT Promo × Camil

Feito com 🧠 + 🔗 + ⚡ + ☕
