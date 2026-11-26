# Segurança e Limitações

## 1. Política de acesso

O AI-Assistente de Consulta foi projetado para realizar exclusivamente consultas às informações disponibilizadas pelas ferramentas MCP.

## 2. Restrições

- Não criar registros.
- Não atualizar informações.
- Não excluir dados.
- Não executar operações de escrita.
- Não inventar informações ausentes nas fontes.

## 3. Tratamento de informações

As respostas devem ser fundamentadas nos resultados retornados pelas ferramentas conectadas.
Quando não houver registros ou quando uma ferramenta apresentar falha, o agente deverá informar a situação sem presumir resultados.

## 4. Limitações conhecidas

- A qualidade das respostas depende da organização e atualização das planilhas.
- O modelo pode interpretar incorretamente solicitações ambíguas.
- O prompt não substitui controles técnicos de autenticação e autorização.
- A disponibilidade do agente depende das integrações externas.

## 5. Segurança das integrações

As credenciais, tokens e chaves de API não devem ser armazenados no repositório.
O acesso às ferramentas e às fontes de dados deve ser limitado por permissões técnicas apropriadas.
