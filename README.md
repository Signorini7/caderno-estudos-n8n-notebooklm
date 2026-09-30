# Caderno Temático: Mastering Enterprise Automation with n8n

## 1. Contexto e Objetivos
Este repositório consolida o projeto prático desenvolvido no bootcamp Santander / DIO, utilizando o **Google NotebookLM** como ferramenta de aprendizagem ativa e curadoria técnica. O foco central foi o estudo aprofundado de arquitetura de automação corporativa com **n8n**, abordando desde o fluxo de dados em JSON até a orquestração avançada de modelos de linguagem (LLMs locais) em ambientes self-hosted.

## 2. Curadoria de Fontes
Foram curadas e processadas 19 referências técnicas oficiais e especializadas, com destaque para:
- **n8n Level 1 Certification & Fundamentals:** Ciclo de vida de execução, nós de gatilho e transporte de dados.
- **Enterprise Patterns & Error Handling:** Padrões de resiliência em produção e uso do `Error Trigger Node`.
- **Arquitetura de Dados:** Manipulação estruturada de listas e objetos em JSON e nós de Webhooks.
- **Integração de Inteligência Artificial:** Guias técnicos de integração de instâncias self-hosted com modelos locais (Ollama, LangChain e AI Agent nodes).

## 3. Engenharia de Prompts e Cicatrizes
- **Prompt Estratégico Avaliado:**
  > *"Como integrar LLMs locais no n8n auto-hospedado?"*
- **Resposta Técnica Consolidada pela IA:**
  1. Uso de nós dedicados de IA (`Ollama Chat Model`, `Basic LLM Chain` e `AI Agent`).
  2. Execução em rede privada segura via Docker/VPS sem exposição externa de dados corporativos.
  3. Respostas em streaming via Webhooks para retorno ágil token a token.
  4. Gestão de contexto e persistência conversacional com nós de memória (`Window Buffer Memory`).
- **Cicatriz / Aprendizado Técnico:**
  Perguntas genéricas sobre "como usar IA no n8n" retornavam apenas exemplos triviais de APIs em nuvem. Ao refinar o prompt especificando o ambiente (*self-hosted*) e modelos locais (*Ollama*), o NotebookLM extraiu com precisão as configurações de rede fechada e os nós nativos suportados.

## 4. Miniguia de Estudo (Entrega Consolidada)
### Resumo Estruturado
O n8n atua como uma engine de automação baseada em nós. Em cenários avançados com IA, ele orquestra pipelines completos: recebe o evento (Webhook), recupera histórico via nós de memória, consulta bases vetoriais e aciona LLMs locais para tomar decisões autônomas antes de executar ações de negócio.

### Glossário Técnico
- **Self-Hosted:** Instalação do n8n em infraestrutura própria, permitindo integração direta com modelos locais e bancos de dados privados.
- **AI Agent Node:** Nó orquestrador que recebe modelos de IA, ferramentas e conexões de memória para raciocínio autônomo.
- **Error Trigger Node:** Nó de contingência ativado automaticamente quando qualquer falha interrompe a cadeia de automação.
- **Streaming Response:** Técnica de emissão em tempo real de tokens de resposta através de Webhook, reduzindo a latência percebida pelo usuário final.

### Prompts Reutilizáveis para Revisão
1. *"Quais as diferenças práticas de performance e custo entre usar um modelo Ollama local vs API da OpenAI em fluxos corporativos no n8n?"*
2. *"Como estruturar uma esteira de fallback para automações críticas quando o nó de IA local sofrer timeout?"*
3. *"Quais são os passos para depurar payloads JSON complexos entre nós de dados e nós de ferramentas do AI Agent?"*
