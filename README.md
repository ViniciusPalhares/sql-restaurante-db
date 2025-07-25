# 📦 Sistema de Pedidos — Restaurante em SQL

Este projeto simula um sistema de pedidos para restaurante, utilizando **SQL puro** para construção do banco de dados, manipulação e análise de dados. A proposta é integrar tabelas como clientes, produtos, pedidos e funcionários com consultas otimizadas para relatórios e decisões gerenciais.

---

## 🛠️ Funcionalidades Desenvolvidas

- Criação de banco e tabelas normalizadas
- Inserção e manipulação de dados
- Consultas com filtros (`SELECT`, `WHERE`, `BETWEEN`)
- Agregações e agrupamentos (`COUNT`, `SUM`, `AVG`, `GROUP BY`)
- `JOINs` entre múltiplas tabelas
- Criação de `VIEW` e `FUNCTION` para relatórios
- Relatórios de produtos mais vendidos e clientes mais ativos

---

## 🧱 Estrutura do Projeto
```
sql-restaurante-db/
├── 01_criacao_tabelas.sql
├── 02_insercao_dados.sql
├── 03_consultas_basicas.sql
├── 04_agregacoes.sql
├── 05_joins_multiplas_tabelas.sql
├── 06_views_funcoes.sql
├── 07_relatorios_analiticos.sql
├── README.md
└── dados_csv/
├── cliente_informatica_csv.csv
├── produto_informatica_csv.csv
└── pedido_informatica_csv.csv
```
---

## 📊 Exemplos de Consultas

```sql
-- Clientes que mais compraram
SELECT c.nome, COUNT(p.id_pedido) AS total_pedidos
FROM pedidos p
JOIN clientes c ON p.id_cliente = c.id_cliente
GROUP BY c.nome
ORDER BY total_pedidos DESC;

-- Produtos mais vendidos
SELECT pr.nome, SUM(p.quantidade) AS total_vendido
FROM pedidos p
JOIN produtos pr ON p.id_produto = pr.id_produto
GROUP BY pr.nome
ORDER BY total_vendido DESC;
```
---

## 💡 Aprendizados

Este projeto reforça conceitos essenciais de SQL, como:
- Modelagem de dados
- Integridade referencial (chaves estrangeiras)
- Lógica de negócios com funções SQL
- Estruturação de consultas complexas para relatórios gerenciais

---

## 📁 Como usar

Você pode executar os scripts SQL usando:
- MySQL Workbench
- DBeaver
- phpMyAdmin
- ou qualquer outro cliente SQL compatível

**Recomendado:** Executar os scripts na ordem de numeração para construir o banco e populá-lo corretamente.

---

## 🚀 Autor

Vinícius Palhares  
📫 [LinkedIn](https://www.linkedin.com/in/viniciuspalhares)

---

