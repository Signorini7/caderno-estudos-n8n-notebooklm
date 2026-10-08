# Desafio Criativo: Planejando Automações com n8n Usando Apenas Bons Prompts

## Passo 1: Definição da Automação
Quero criar uma automação no N8N para triagem e roteamento automatizado de chamados de suporte de TI.
Público ou responsável:
Equipe de Suporte e Infraestrutura de TI.

Resultado esperado:
Classificar automaticamente a prioridade do chamado com base no texto, registrar o ticket no sistema de chamados e disparar um alerta imediato caso o problema seja crítico.

## Passo 2: Contexto e Regras
Ferramentas envolvidas: Webhook, Ollama (LLM Local), Jira Service Desk e Microsoft Teams.

Fluxo desejado:
1. Receber uma requisição Webhook contendo os dados do formulário de abertura de chamado.
2. Analisar a descrição do problema via LLM para definir a severidade (Baixa, Média, Alta ou Crítica).
3. Criar o chamado categorizado dentro do Jira Service Desk.
4. Enviar mensagem de alerta via Microsoft Teams se a severidade for "Crítica".

Regras importantes:
Ignorar e abortar o fluxo se a descrição do chamado tiver menos de 10 caracteres ou contiver apenas palavras de teste. Se houver falha de resposta do LLM, aplicar severidade padrão "Média" por contingência.

## Passo 3: Prompt Final Estruturado

Atue como um especialista em automação e engenharia de fluxos no N8N.
Crie uma automação para triagem e roteamento automatizado de chamados de suporte de TI.

Público:
Equipe de Suporte e Infraestrutura de TI.

Ferramentas envolvidas:
Webhook, Ollama (LLM Local), Jira Service Desk e Microsoft Teams.

Fluxo:
Receber dados de chamado via Webhook, processar a severidade através de um modelo de linguagem local, registrar o ticket categorizado no Jira e enviar alerta imediato no canal do Microsoft Teams apenas quando a severidade for classificada como Crítica.

Regras:
Filtrar chamados com descrições vazias ou menores que 10 caracteres. Em caso de indisponibilidade da IA, atribuir fallback de severidade Média.

Explique quais nós do N8N (ex: Webhook, IF, HTTP Request, LLM Chain) devem ser utilizados e descreva a arquitetura de execução do workflow nó a nó.
