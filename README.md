# AI — Assistente de Consultas

Assistente inteligente multiárea desenvolvido com **n8n, Google Gemini e Model Context Protocol (MCP)**, integrado ao Google Sheets para consultar informações dos setores de **Gestão de Projetos, Recursos Humanos (RH) e Tecnologia** por meio de linguagem natural.

O projeto busca facilitar o acesso às informações, centralizar consultas e explorar o uso de Inteligência Artificial Generativa integrada a ferramentas externas, priorizando a confiabilidade das respostas e a integridade dos dados.

---

## 🎯 Objetivo do projeto

Desenvolver um assistente de IA capaz de interpretar solicitações em linguagem natural e consultar informações de diferentes departamentos por meio de ferramentas disponibilizadas via MCP.

O sistema foi projetado para atuar exclusivamente como ferramenta de consulta, sem realizar operações de criação, atualização ou exclusão de registros.

## ⚙️ Funcionalidades

- **Gestão de Projetos:** consulta de projetos, tarefas, sprints, equipe e indicadores.
- **Recursos Humanos:** consulta de informações de colaboradores, recrutamento, férias, ausências e treinamentos.
- **Tecnologia:** consulta de demandas e informações disponibilizadas na base do departamento.
- **Interação em linguagem natural:** interpretação de perguntas e apresentação de informações consultadas.
- **Consultas integradas:** acesso às fontes de dados por meio de ferramentas MCP.
- **Política somente leitura:** preservação das informações originais nas planilhas.

## 🏗️ Arquitetura da solução

O projeto utiliza o n8n como plataforma de orquestração, o Google Gemini como modelo de linguagem e o MCP para disponibilizar ferramentas de consulta às fontes de dados.

### Fluxo de funcionamento

1. O usuário envia uma solicitação ao assistente.
2. O AI Agent utiliza o Gemini para interpretar a pergunta.
3. Quando necessário, o agente seleciona uma ferramenta MCP compatível com a solicitação.
4. O MCP disponibiliza a consulta à planilha correspondente no Google Sheets.
5. Os dados retornados são utilizados como fundamento para elaborar a resposta.
6. O assistente apresenta o resultado ao usuário.

## 🧰 Tecnologias utilizadas

| Tecnologia | Aplicação no projeto |
|---|---|
| n8n Cloud | Orquestração e integração dos componentes |
| Google Gemini | Processamento de linguagem natural |
| Model Context Protocol (MCP) | Comunicação entre o agente e as ferramentas externas |
| Google Sheets | Organização e armazenamento dos dados |
| AI Agent | Interpretação das solicitações e seleção de ferramentas |

## 🔒 Segurança e confiabilidade

A confiabilidade das respostas é um dos principais objetivos do projeto.

Foram estabelecidas diretrizes para:

- Evitar a geração de informações sem fundamentação nas fontes consultadas.
- Informar quando um dado não estiver disponível.
- Diferenciar ausência de registros de falhas nas ferramentas.
- Restringir o agente a operações de consulta.
- Tratar instruções maliciosas presentes nas solicitações ou nos dados como conteúdo não confiável.
- Preservar a integridade das informações armazenadas.

**Observação:** as instruções do agente são uma camada de proteção comportamental, não um mecanismo de controle de acesso. A segurança efetiva também depende das permissões das integrações e da proteção do endpoint MCP.

**Importante:** o arquivo exportado do workflow não contém necessariamente todas as credenciais e configurações externas necessárias. A reprodução depende da configuração correta dessas integrações.

## 🚀 Demonstração

Quer experimentar o AI - Assistente de consulta?
Acesse o ambiente de demonstração e faça suas próprias consultas.

👉 https://organizador1.app.n8n.cloud/webhook/68c262c5-efbb-45bf-8e63-b680743239fc/chat

## 💬 Exemplos de perguntas

O projeto permite consultar informações dos departamentos por meio de perguntas em linguagem natural. Abaixo estão exemplos baseados nas informações disponíveis nas planilhas integradas.

### 📊 Gestão de Projetos

- Quais são as tarefas cadastradas no projeto?
- Quantas tarefas estão concluídas?
- Quais atividades estão em andamento?
- Existem tarefas atrasadas?
- Quais atividades estão bloqueadas?
- Quem é o responsável pela tarefa de implementar o banco de dados?
- Qual é o prazo para publicar a versão em produção?
- Em qual fase está a tarefa de executar os testes de integração?
- Qual é o progresso geral do projeto?
- Quais atividades ainda estão aguardando execução?

### 💻 Gestão de Projetos de Tecnologia

- Quais projetos estão cadastrados atualmente?
- Quais projetos estão em andamento?
- Quais projetos estão em situação de risco?
- Qual é o progresso do projeto Migração Cloud AWS?
- Quanto foi previsto e quanto já foi gasto no projeto Zero Trust & IAM?
- Quais projetos apresentam saldo orçamentário negativo?
- Quais tarefas estão atrasadas?
- Quais tarefas estão bloqueadas?
- Quais atividades pertencem à Sprint 14?
- Quem é responsável pela tarefa de configurar o WAF e CloudFront CDN?
- Qual é a capacidade semanal de Thiago Mendes?
- Quais integrantes da equipe estão com sobrecarga?
- Qual squad possui a maior quantidade de horas alocadas?
- Apresente um resumo dos indicadores do Painel Executivo.

### 👥 Recursos Humanos

- Quantos colaboradores estão cadastrados?
- Quantos colaboradores estão ativos?
- Como está distribuída a quantidade de colaboradores por departamento?
- Quais são os cargos existentes no departamento de Tecnologia?
- Quais colaboradores estão de férias ou afastados?
- Quais férias estão pendentes de aprovação?
- Quais ausências estão aprovadas para dezembro de 2026?
- Quantas vagas estão disponíveis para recrutamento?
- Quais vagas estão em fase de entrevistas?
- Quais vagas possuem prioridade alta?
- Quais são os departamentos com vagas abertas?
- Qual é o resumo dos indicadores do Dashboard de RH?

### 🔎 Consultas específicas e informações indisponíveis

- Existe algum projeto chamado Projeto Inexistente?
- Existe algum colaborador chamado João Inexistente?
- Há informações sobre treinamentos de colaboradores?
- Qual é o orçamento registrado para o projeto Migração Cloud AWS?
- Quais informações estão disponíveis sobre a tarefa T-07?
- Existem informações sobre uma atividade que não esteja cadastrada nas planilhas?

**Observação:** o assistente deve responder com base nos registros encontrados. Quando uma informação não estiver disponível nas planilhas, deve informar essa limitação em vez de gerar uma resposta presumida.

## 👨‍💻 Autor

Desenvolvido como projeto de estudo e portfólio, explorando aplicações de Inteligência Artificial Generativa, automação de processos, integração de sistemas e qualidade de software.
