# 🍔 Análise de Dados SQL - Hamburgueria Brasa & Pão

Projeto prático de Administrador de Banco de Dados e Análise de Dados em SQL Server (T-SQL) com foco na resolução de problemas de negócio, consultas complexas, agregações e cruzamento de dados para auxílio na tomada de decisão estratégica do primeiro trimestre de 2026.

---

## 📌 Sobre o Projeto

A **Brasa & Pão** é uma hamburgueria de bairro que atende por delivery e retirada no balcão. A proprietária (Dona Marta) registrou as movimentações de vendas no primeiro trimestre de 2026 (janeiro a março) e precisava tomar 4 decisões estratégicas para o próximo trimestre:
1. **Cardápio:** Identificar produtos sem saída para possível remoção.
2. **Entregador do Trimestre:** Definir o entregador destaque para premiação/bônus.
3. **Fidelidade:** Mapear os clientes mais frequentes/valiosos para o programa de fidelidade.
4. **Mapeamento de Bairros:** Identificar regiões com alta e baixa adesão.

---

## 🛠️ Tecnologias e Conceitos Praticados

- **SGBD:** SQL Server (SSMS)
- **Linguagem:** T-SQL (DQL - Data Query Language)
- **Comandos & Clausulas Utilizadas:**
  - `WHERE`, `LIKE`, `IN`, `BETWEEN` (Filtros de dados)
  - `COUNT`, `SUM`, `AVG` (Funções de agregação)
  - `GROUP BY`, `HAVING` (Agrupamento e filtros sobre agregações)
  - `ORDER BY` (Ordenação)
  - `INNER JOIN`, `LEFT JOIN` (Cruzamento de tabelas simples e Múltiplos JOINs)

---

## 🗄️ Estrutura do Banco de Dados

O banco de dados `HamburgueriaBrasa` é composto por 5 tabelas:

- **`Clientes`** (16 registros): Dados cadastrais dos clientes (Nome, Bairro, Telefone).
- **`Entregadores`** (5 registros): Cadastro da equipe de entregas.
- **`Produtos`** (14 registros): Itens do cardápio e preços atuais.
- **`Pedidos`** (40 registros): Histórico de pedidos, tipo de atendimento, taxa e status.
- **`ItensPedido`** (91 registros): Detalhes dos produtos comprados por pedido e preço praticado na data da venda.

---

## 📋 Resumo das Consultas Desenvolvidas

As consultas foram organizadas em 3 níveis de complexidade:

### Nível 1 — Aquecimento (Consultas em Tabela Única)
- **Q1:** Contagem de clientes cadastrados no bairro Centro.
- **Q2:** Filtro e ordenação de hambúrgueres acima de R$ 30,00.
- **Q3:** Mapeamento de pedidos entregues vs. cancelados.
- **Q4:** Métrica de avaliações e nota média dos pedidos entregues.
- **Q5:** Evolução mensal de pedidos por tipo de atendimento (Delivery vs. Retirada).

### Nível 2 — Cruzando Tabelas (`JOIN`, Agrupamentos e Regras de Negócio)
- **Q6:** Listagem detalhada dos pedidos de janeiro/2026 unindo Clientes e Pedidos.
- **Q7:** Ranking de volume de entregas por entregador.
- **Q8:** Apuração de unidades vendidas e faturamento total por produto.
- **Q9:** Faturamento bruto de produtos agrupado por categoria.
- **Q10:** Identificação de bairros com volume relevante de entregas (`HAVING >= 7`).
- **Q11:** Análise de histórico de preços do produto X-Bacon.

### Nível 3 — Desafio (Múltiplos `JOIN`s e Regras Avançadas)
- **Q12:** Top 3 clientes com maior valor investido para o programa de fidelidade.
- **Q13:** Análise do comportamento do faturamento total ao longo dos três meses