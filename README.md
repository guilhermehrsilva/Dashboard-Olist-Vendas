# 🛒 Segmentação de Clientes (RFM) com SQL e Power BI

## 🏢 O Desafio de Negócio
Uma grande plataforma de E-commerce (Olist) precisava identificar seus melhores clientes para otimizar campanhas de marketing. O desafio era processar uma base de 100 mil pedidos, onde a lógica de classificação não poderia ser feita manualmente. O objetivo era criar uma matriz **RFM** (Recência, Frequência, Monetário).

## 🛠️ Solução (Arquitetura de Dados)
Diferente de projetos tradicionais de BI, neste case atuei como **Analytics Engineer**:
1.  **Engenharia de Dados (SQL):** Criação de um banco de dados MySQL local. Importação e tratamento de arquivos CSV brutos (`ETL`).
2.  **Lógica de Negócio (SQL):** Desenvolvimento de script SQL utilizando *Window Functions* (`NTILE`) para classificar automaticamente os clientes em quintis (notas de 1 a 5) para cada critério do RFM.
3.  **Visualização (Power BI):** Conexão direta ao banco de dados MySQL para garantir performance. Criação de medidas DAX para segmentar os clientes em clusters ("Campeões", "Em Risco", "Novos").

## 📊 Principais Insights
* **Dependência de Novos Clientes:** A análise revelou que a maior fatia da receita (R$ 5MM+) provém do grupo "Em Risco" e "Novos", indicando uma estratégia focada em aquisição e baixo índice de retenção.
* **Ticket Médio VIP:** O grupo "Campeões", apesar de representar menos de 2% da base, possui um Ticket Médio (R$ 348) que é **110% superior** à média dos demais clientes (R$ 165).
* **Oportunidade:** Apenas 25% da base é considerada "Fiel". Estratégias de CRM devem focar urgentemente em recuperar o grupo "Em Risco" antes que virem "Hibernando".

---
**Stack Tecnológica:** MySQL, VS Code, Power BI, DAX.
**Autor:** Guilherme Risson
