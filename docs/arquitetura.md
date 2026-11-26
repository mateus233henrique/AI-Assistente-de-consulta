# Arquitetura do AI - Assistente de consulta

## 1. Visão geral

O AI - Assistente de consulta é um assistente de Inteligência Artificial desenvolvido na plataforma n8n, utilizando o Google Gemini como modelo de linguagem e o Model Context Protocol (MCP) para disponibilizar ferramentas de consulta de dados.

O sistema permite consultar informações organizadas em planilhas Google Sheets, distribuídas entre três áreas:

- Gestão de Projetos;
- Recursos Humanos (RH);
- Tecnologia.

## 2. Tecnologias utilizadas

| Tecnologia | Finalidade |
|---|---|
| n8n Cloud | Orquestração dos workflows |
| Google Gemini | Processamento de linguagem natural |
| MCP | Comunicação e disponibilização de ferramentas |
| Google Sheets | Armazenamento das informações consultadas |

## 3. Arquitetura lógica

O usuário envia uma pergunta ao agente. O Gemini interpreta a solicitação e, quando necessário, utiliza as ferramentas MCP disponíveis para consultar os dados no Google Sheets.

Os resultados retornados são utilizados como base para construir a resposta.

## 4. Restrição operacional

O AI - Assistente de consulta possui finalidade exclusivamente consultiva.

Não são permitidas operações de criação, atualização ou exclusão de registros nas fontes de dados.

## 5. Objetivos técnicos

- Facilitar consultas em linguagem natural.
- Centralizar o acesso às informações de diferentes departamentos.
- Reduzir respostas sem fundamentação nos dados.
- Preservar a integridade das fontes consultadas.
- Validar a confiabilidade das respostas geradas por IA.
