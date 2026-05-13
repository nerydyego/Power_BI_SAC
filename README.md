# 📊 Dashboard SAC - Power BI

## 📌 Sobre o Projeto

Este projeto consiste no desenvolvimento de um dashboard analítico de SAC (Serviço de Atendimento ao Cliente), criado no Power BI, com o objetivo de monitorar indicadores operacionais, desempenho do suporte e principais problemas reportados pelos usuários.

O dashboard permite acompanhar:

- Quantidade de chamados
- Tempo médio de atendimento
- Status dos atendimentos
- Principais tipos de problemas
- Performance dos atendentes
- Perfil dos usuários
- Tendências temporais de chamados

---

# 🎯 Objetivos do Dashboard

- Centralizar indicadores de SAC
- Facilitar análise operacional
- Identificar gargalos no atendimento
- Monitorar SLA e tempo de resposta
- Apoiar tomada de decisão
- Melhorar experiência do usuário

---

# 🗂️ Estrutura do Modelo de Dados

O modelo foi estruturado utilizando conceitos de modelagem dimensional (Star Schema).

## 📌 Tabela Fato

### `f_ocorrencia`

Tabela responsável por armazenar os eventos de atendimento/chamados.

| Campo | Descrição |
|---|---|
| data_chamado | Data de abertura do chamado |
| data_atendimento | Data de atendimento |
| atendente | Responsável pelo atendimento |
| tempo | Tempo de atendimento |
| tipo_problema | Categoria do problema |
| status | Status do chamado |

---

# 📌 Tabelas Dimensão

## `d_problemas`

Tabela contendo os tipos de problemas registrados.

| Campo | Descrição |
|---|---|
| codigo_problema | Identificador do problema |
| tipo_problema | Descrição/categoria do problema |

---

## `d_suporte`

Tabela contendo informações da equipe de suporte.

| Campo | Descrição |
|---|---|
| id_atendente | Identificador do atendente |
| nome_atendente | Nome do colaborador |
| sexo | Sexo do atendente |
| data_nascimento | Data de nascimento |

---

## `d_usuario`

Tabela contendo informações dos usuários/clientes.

| Campo | Descrição |
|---|---|
| id_usuario | Identificador do usuário |
| nome | Nome do usuário |
| sexo | Sexo |
| data_nascimento | Data de nascimento |
| data_inscricao | Data de cadastro do usuário |

---

# 🔗 Relacionamentos

O modelo segue estrutura dimensional com relacionamentos do tipo:

- Dimensão → Fato
- Cardinalidade 1:N

Exemplo:

```text
d_problemas[codigo_problema]
        ↓
f_ocorrencia[tipo_problema]
```

---

# 📈 Indicadores (KPIs)

Os principais indicadores desenvolvidos são:

- Total de Chamados
- Chamados por Status
- Tempo Médio de Atendimento
- Chamados por Tipo de Problema
- Quantidade de Chamados por Atendente
- Usuários Cadastrados
- Evolução Mensal de Chamados
- SLA de Atendimento

---

# 🛠️ Tecnologias Utilizadas

| Ferramenta | Finalidade |
|---|---|
| Power BI | Construção do dashboard |
| Power Query | ETL e tratamento de dados |
| DAX | Criação de medidas e cálculos |
| Excel/CSV | Fonte de dados |

---

# 🧹 Tratamento de Dados

Durante o processo ETL foram realizados:

- Padronização de nomes
- Tratamento de valores nulos
- Conversão de tipos de dados
- Criação de colunas temporais
- Ajuste de relacionamentos
- Criação de métricas DAX

---

# 📅 Estrutura Temporal

O projeto utiliza segmentações por:

- Dia
- Mês
- Ano
- Trimestre
- Quadrimestre

---

# 📊 Principais Visualizações

O dashboard possui:

- Cards de KPI
- Gráficos de barras
- Gráficos de linhas
- Segmentações de dados
- Tabelas analíticas
- Indicadores temporais

---

# 🔒 Regras de Negócio

- Cada ocorrência representa um chamado único.
- Chamados podem possuir diferentes status.
- Tempo de atendimento é calculado entre abertura e conclusão.
- Problemas são categorizados para análise operacional.

---

# 🚀 Melhorias Futuras

- Implementação de SLA avançado
- Análise preditiva de chamados
- Classificação automática de problemas
- Integração com banco de dados
- Atualização automática dos dados
- Publicação no Power BI Service

---

# 👨‍💻 Autor

Dyego Nery

Projeto desenvolvido para estudos e aprimoramento em Análise de Dados e Business Intelligence.

---

# 📌 Status do Projeto

🚧 Em desenvolvimento