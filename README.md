#AI — Assistente de Consultas

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

## 👨‍💻 Autor

Desenvolvido como projeto de estudo e portfólio, explorando aplicações de Inteligência Artificial Generativa, automação de processos, integração de sistemas e qualidade de software.
