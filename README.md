# 📊 Dashboard SAC - Power BI

## 📌 Sobre o Projeto

Projeto desenvolvido em Power BI com foco na análise operacional de um SAC (Serviço de Atendimento ao Cliente), permitindo monitorar indicadores de atendimento, tempo de resposta, desempenho da equipe e principais problemas reportados pelos usuários.

---

# 🎯 Objetivos

- Monitorar atendimentos realizados
- Analisar tempo médio de resposta
- Avaliar tempo médio de atendimento
- Identificar principais problemas
- Acompanhar desempenho dos atendentes
- Criar indicadores para apoio à tomada de decisão

---

# 🛠️ Tecnologias Utilizadas

- Power BI
- Power Query
- DAX
- Excel / CSV
- GitHub

---

# 🗂️ Modelagem de Dados

O projeto foi desenvolvido utilizando modelagem dimensional (Star Schema).

## 📌 Tabela Fato

### `fOcorrencias`

- Data do chamado
- Data do atendimento
- Atendente
- Tempo de atendimento
- Tipo de problema
- Status

---

## 📌 Tabelas Dimensão

### `dProblemas`

- Código do problema
- Tipo de problema

### `dSuporte`

- ID atendente
- Nome atendente
- Sexo
- Data de nascimento

### `dUsuarios`

- ID usuário
- Nome
- Sexo
- Data de nascimento
- Data de inscrição

---

# 🔄 Tratamento de Dados (ETL)

Durante o processo ETL no Power Query foram realizados:

- Remoção de linhas e colunas vazias
- Ajuste de tipos de dados
- Cálculo de tempo de atendimento em minutos
- Cálculo de dias para resposta
- Padronização de sexo (Masculino/Feminino)
- Separação de nome e sobrenome
- Cálculo de idade e faixa etária

---

# 📐 Medidas DAX

Principais métricas desenvolvidas:

- Total de Atendimentos
- Tempo Médio de Retorno
- Tempo Médio de Atendimento
- Média Diária de Chamados
- % de Chamados Cancelados

Funções utilizadas:

- COUNTROWS
- AVERAGE
- CALCULATE
- DIVIDE
- AVERAGEX

---

# 📊 Visualizações

O dashboard possui:

- KPIs
- Gráfico de chamados mensais
- Média de tempo de atendimento
- Chamados por status
- Top 8 problemas
- Chamados por atendente
- Segmentações temporais

---

# 📈 Principais Indicadores

- Tempo médio de atendimento
- Quantidade de atendimentos por funcionário
- Top 8 problemas com mais chamados
- Percentual de chamados cancelados
- Média diária de chamados

---

# 🚀 Funcionalidades

- Atualização de base de dados
- Reaproveitamento das etapas ETL
- Relacionamentos entre tabelas
- Segmentação temporal
- Dashboard interativo

---

# 👨‍💻 Autor

Dyego Nery

Projeto desenvolvido para estudos e aprimoramento em Business Intelligence, Power BI e Análise de Dados.

---

# ✅ Status do Projeto

✔️ Projeto Finalizado