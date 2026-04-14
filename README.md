# Centro de Inteligência Analítica — Bootstrap Nível 4-6

**Versão:** 4.2 (2026-04-14)  
**Status:** 100% pronto para replicar  
**Tempo de setup:** ~15 minutos

---

## 🚀 Quick Start (Para Seu Amigo)

### Passo 1: Copie a Pasta
```bash
cd C:\Users\seu_usuario\
git clone <este_repositorio> seu_centro_inteligencia
cd seu_centro_inteligencia
```

### Passo 2: Abra no Claude Code
```bash
# Na pasta raiz do seu centro
claude-code .
```

### Passo 3: Execute Bootstrap
Cole no chat do Claude Code:

```
Você é meu agente de inteligência analítica. Vamos configurar um centro de inteligência Nível 4-6 (grafo + RAG + decay + hooks).

Leia: _templates/BOOTSTRAP_INTELIGENCIA.json

Execute a FASE 1-6 de bootstrap_6_passos completa. Depois pergunte 3 coisas:
1. Qual é a empresa e segmento?
2. Quais são os principais clientes/projetos?
3. Qual é seu cargo e ferramentas?
```

### Passo 4: Deixar Rodar
Agente cria tudo automaticamente:
- ✅ Estrutura de pastas
- ✅ Arquivos base (CLAUDE.md, MEMORY.md, etc.)
- ✅ Scripts Python (15 scripts)
- ✅ Configuração de hooks
- ✅ Conceitos iniciais baseado nas respostas

---

## 📚 Documentação Completa

### Para Entender o Sistema
1. **BOOTSTRAP_INTELIGENCIA.json** — Especificação técnica completa (4.2 KB)
   - 7 regras de memória agressiva
   - 15 scripts Python documentados
   - Configuração de hooks (Stop + PreToolUse)
   - Roadmap 8 níveis
   - Exemplos de uso

2. **PADRAO_MEMORIA.md** — Como estruturar memórias
3. **RAG_GUIA.md** — Como buscar semanticamente
4. **ROADMAP_MEMORIA_AVANCADA.md** — Evolução do sistema

---

## 🎯 Protocolo de Memória (7 Regras AGRESSIVAS)

Sempre que você menciona algo relevante, agente captura **AUTOMATICAMENTE**:

| Regra | Se Você Disser | Agente Cria |
|-------|---|---|
| **1** | "Weverson é meu chefe" | `memoria/pessoas/weverson.md` |
| **2** | "Sortimento é 50% da nota" | `memoria/conceitos/sortimento.md` |
| **3** | "Decidimos usar Haiku padrão" | `memoria/decisoes/2026-04-14_usar_haiku.md` |
| **4** | Menciona Weverson + arquivo existe | Cria `[[weverson]]` (wikilink) |
| **5** | Aprendi algo sobre Sortimento | Atualiza `conceitos/sortimento.md` (não duplica) |
| **6** | Criou/atualizou arquivo(s) | Avisa: `📝 Memória: [criado: X] [atualizado: Y]` |
| **7** | Ao encerrar sessão | Hook Stop: roda auto_memoria.py automático |

---

## 🔧 Scripts (15 Python)

| Script | Trigger | O que faz |
|--------|---------|----------|
| `auto_memoria.py` | Hook Stop (automático) | Regenera grafo + timeline + registra sessão |
| `classificar_modelo.py` | Hook PreToolUse (automático) | Detecta tarefa complexa → sugere Sonnet |
| `grafo_memoria.py` | Manual ou via outro script | Constrói grafo JSON/HTML (vis.js) |
| `rag_memoria.py` | Manual | Busca semântica em sua base |
| `memory_decay.py` | Manual (periódico) | Notas antigas perdem peso (exponencial) |
| `entity_extractor.py` | Manual | Detecta pessoas, conceitos, decisões (NER) |
| `anomaly_detector.py` | Manual | Encontra links quebrados, orfãos, gaps |
| `gap_analyzer.py` | Manual | Que documentação falta? |
| `timeline_generator.py` | Manual | Timeline visual de eventos |
| ... + 6 mais | — | Utilitários e validadores |

---

## 🌐 Grafo de Conhecimento

**Gerado automaticamente:** `output/grafo_memoria.html`

- **Nós:** Conceitos, Pessoas, Projetos, Decisões
- **Arestas:** Relacionamentos (wikilinks)
- **Cores:** Verde (conceito), Laranja (pessoa), Ciano (projeto), Vermelho (decisão)
- **Tamanho:** Proporcional ao weight (importância)
- **Temperatura:** Vermelho (recente) → Azul (antiga)
- **Interatividade:** Clique → aponta para / referenciado por

---

## 💾 Estrutura de Pastas (Pronta)

```
seu_centro_inteligencia/
├── CLAUDE.md                          (missão + 7 regras + tabela projetos)
├── memoria/
│   ├── MEMORY.md                      (índice: user, feedback, project, reference, conceito, pessoa, decisao)
│   ├── PADRAO_MEMORIA.md              (template frontmatter)
│   ├── user_profile.md                (seu perfil)
│   ├── feedback_memoria.md            (regras de colaboração)
│   ├── RAG_GUIA.md                    (busca semântica)
│   ├── DECAY_CONFIG.json              (parâmetros de decay)
│   ├── conceitos/                     (1 conceito = 1 arquivo)
│   ├── pessoas/                       (stakeholders, chefes, clientes)
│   ├── decisoes/                      (YYYY-MM-DD_titulo.md)
│   └── sessoes/                       (sessao_YYYY-MM-DD.md — automático)
├── scripts/
│   ├── auto_memoria.py                (hook Stop)
│   ├── classificar_modelo.py          (hook PreToolUse)
│   ├── grafo_memoria.py               (grafo JSON/HTML)
│   ├── rag_memoria.py                 (busca semântica)
│   ├── memory_decay.py                (decay temporal)
│   ├── entity_extractor.py            (NER automática)
│   ├── anomaly_detector.py            (detecta problemas)
│   └── ... (8 mais scripts)
├── _templates/
│   ├── BOOTSTRAP_INTELIGENCIA.json    (este arquivo)
│   ├── ROADMAP_MEMORIA_AVANCADA.md   (8 níveis)
│   └── TEMPLATE_CLAUDE_PROJETO.md    (novos projetos)
├── .claude/
│   └── settings.local.json            (hooks + modelo)
├── output/
│   ├── grafo_memoria.html             (gerado automaticamente)
│   ├── grafo_memoria.json             (dados do grafo)
│   ├── timeline.html                  (eventos)
│   ├── anomalies.json                 (alertas)
│   └── gap_analysis.json              (gaps)
└── <nome-projeto>/
    ├── CLAUDE.md                      (contexto do projeto)
    ├── DATA/                          (dados de entrada)
    └── output/                        (resultados)
```

---

## ⚙️ Configuração (Automática via Bootstrap)

**File:** `.claude/settings.local.json`

```json
{
  "model": "claude-haiku-4-5-20251001",
  "hooks": {
    "Stop": [{
      "hooks": [{"type": "command", "command": "py '<RAIZ>/scripts/auto_memoria.py'"}]
    }],
    "PreToolUse": [{
      "matcher": "Bash|Write|Edit|Agent|NotebookEdit",
      "hooks": [{"type": "command", "command": "py '<RAIZ>/scripts/classificar_modelo.py'"}]
    }]
  }
}
```

---

## 🎓 Aprender o Sistema

### Nível 1: O Básico (30 min)
- Leia `CLAUDE.md` raiz
- Leia `memoria/PADRANO_MEMORIA.md`
- Explore `output/grafo_memoria.html` (veja as conexões)

### Nível 2: Uso Diário (1 semana)
- Comece a trabalhar (dados, dashboards, análises)
- Agente captura automaticamente (7 regras)
- Use `/iniciar` ao abrir sessão
- Veja grafo atualizar após cada resposta

### Nível 3: Avançado (2 semanas)
- Execute scripts manualmente:
  - `py scripts/rag_memoria.py 'sua pergunta'`
  - `py scripts/anomaly_detector.py`
  - `py scripts/gap_analyzer.py`
- Customize DECAY_CONFIG.json
- Integre com seus sistemas

### Nível 4+: Expert (1 mês)
- Entenda cada um dos 15 scripts
- Contribua melhorias
- Configure RAG com seus embeddings
- Integre com GitHub/Slack (Nível 8 futuro)

---

## 🆘 Troubleshooting

| Problema | Solução |
|----------|---------|
| Hook não roda | Verifique `<RAIZ>` em settings.local.json (path absoluto) |
| Grafo não atualiza | Execute manualmente: `py scripts/auto_memoria.py` |
| RAG não funciona | Instale: `pip install chroma-db openai` |
| Python não encontrado | Use caminho completo: `C:\Python\python.exe` |
| Backlinks quebrados | Run: `py scripts/anomaly_detector.py` |

---

## 📊 Roadmap (8 Níveis)

| Nível | Status | Features |
|-------|--------|----------|
| 1 | ✅ | Arquivos .md |
| 2 | ✅ | Índice + tags + wikilinks |
| 3 | ✅ | RAG local |
| 4 | ✅ | Grafo de conhecimento |
| 5 | ✅ | Memory decay temporal |
| 6 | ✅ | Extração automática + hooks |
| 7 | ❌ Futuro | Multi-agente especializado |
| 8 | ❌ Futuro | Inteligência proativa (cron/webhook) |

---

## 📝 Primeiros Passos com Seu Amigo

1. **Ele cria pasta nova** → executa bootstrap
2. **Responde 3 perguntas:**
   - Empresa?
   - Clientes/Projetos?
   - Seu cargo?
3. **Sistema cria conceitos iniciais** com base nas respostas
4. **Ele começa a trabalhar** → agente captura automaticamente
5. **Ao final do dia** → `/encerrar` (ou deixa Stop rodar) → grafo atualiza
6. **Próxima sessão** → `/iniciar` → contexto carregado, RAG pronto

---

## 💡 Pro Tips

- **Use /iniciar sempre** — carrega contexto automático
- **Mencione decisões** — agente cria nota de decisão
- **Cruzamento entre projetos** — diga "isso impacta Projeto X" → grafo conecta
- **Export do grafo** — `output/grafo_memoria.html` é um relatório completo
- **Backup** — versione `memoria/` no Git (não versione `output/`)

---

## 🔗 Links

- **Especificação:** `_templates/BOOTSTRAP_INTELIGENCIA.json`
- **Padrão de memória:** `memoria/PADRAO_MEMORIA.md`
- **Guia RAG:** `memoria/RAG_GUIA.md`
- **Roadmap:** `_templates/ROADMAP_MEMORIA_AVANCADA.md`

---

**Pronto para replicar!** 🚀  
Seu amigo pode começar agora mesmo. Qualquer dúvida, envie este README + JSON.
