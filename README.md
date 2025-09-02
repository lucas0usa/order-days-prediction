# Desafio de Data Science – Predição de Dias de Pedido

## 📌 Contexto
O objetivo deste case é desenvolver um modelo de previsão capaz de estimar o **número de dias com pedidos realizados por usuário ao longo de um mês**.  
O desafio envolve prever esse número em diferentes momentos do mês, ajustando as estimativas conforme novos pedidos vão ocorrendo.

### Exemplo:
- Usuário A realizou 2 pedidos no dia 04/01 e 3 pedidos no dia 25/01.  
- Esse usuário, portanto, teve **2 dias de pedidos** em janeiro.  
- Antes do dia 04/01, o modelo deve prever **2 dias restantes**.  
- Após o dia 04/01 (e antes do dia 25/01), o modelo deve prever **1 dia restante**.  

O foco do case é prever o número de dias de pedido para **agosto de 2022**.

---

## 🎯 Objetivos do Case

### Questão 1 – Predição
- Prever o número de dias de pedidos restantes para cada usuário presente no arquivo `august_with_missing_order_days.parquet`.  
- Gerar um arquivo de submissão chamado **`order_days_prediction.csv`** com o seguinte formato:
  - Colunas: `account_id`, `prediction`  
  - Dimensão esperada: **32.944 linhas × 2 colunas**  
  - Observação: os pedidos já conhecidos no arquivo de agosto **não devem** ser incluídos na contagem de previsão (considerar apenas os dias restantes).  

### Questão 2 – Análise Estatística
- Explorar a **distribuição da variável número de dias de pedidos**.  
- Atividades propostas:
  1. Descrever a distribuição via uma função de densidade/probabilidade conhecida.  
  2. Estimar os parâmetros dessa distribuição.  
  3. Calcular a probabilidade de ocorrência de mais de 4 dias de pedidos.  
  4. Estimar o tempo médio entre dias de pedidos.  

---

## 📂 Estrutura do Repositório

```

├── data/
│   ├── august\_with\_missing\_order\_days.parquet
│   ├── historical\_orders.parquet
│   ├── august\_total\_sales.parquet
│   └── order\_days\_prediction.csv   # Arquivo de submissão gerado
│
├── Notebook.ipynb                  # Contém todo o pipeline (EDA → Modelagem → Predição)
└── README.md

````

---

## 🗂️ Fontes de Dados
- **`august_with_missing_order_days.parquet`** → Dados de pedidos (com lacunas) para agosto/2022.  
- **`historical_orders.parquet`** → Histórico transacional de usuários (base de treino).  
- **`august_total_sales.parquet`** → Previsão do valor total de vendas de agosto por usuário (pode ser usada como informação adicional, assumida como verdadeira).  
- Dados em: https://drive.google.com/file/d/1vj4ZMs_rb8dK5nNOXx9LKbIYPUZhsgL4/view?usp=drive_link
  
---

## ⚙️ Instruções de Execução
1. Clone este repositório:  
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
   ```
2. Abra o **Notebook.ipynb** e execute as células sequencialmente para reproduzir a análise e gerar o arquivo de submissão `order_days_prediction.csv`.

---

## 📝 Observações

* O notebook inclui todas as etapas: **EDA (Exploração de Dados)**, **feature engineering**, **modelagem** e **avaliação**.
* As análises estatísticas da Questão 2 também estão documentadas no mesmo notebook.
* O repositório segue uma organização simples e pode ser facilmente expandido para versões mais robustas de pipelines (ETL, MLflow, etc.).

---

## 📧 Contato

Caso tenha dúvidas ou sugestões, fique à vontade para abrir uma *issue* ou entrar em contato.
