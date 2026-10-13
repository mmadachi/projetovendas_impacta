# Fórmulas usadas no Power BI (DAX) — explicadas de forma simples

DAX é a "linguagem de fórmulas" do Power BI. É parecida com fazer uma fórmula
no Excel (por exemplo `=SOMA(A1:A10)`), só que aqui as fórmulas ficam
guardadas com um nome (chamado de "medida") e são usadas dentro dos gráficos
e cartões do painel.

Cada fórmula abaixo está organizada por entrega — na ordem em que foi criada.

---

## Entrega 1 (AC1) — fórmulas básicas

**Valor Vendas**
```
SUMX(Fato_Vendas, Fato_Vendas[Quantidade] * Fato_Vendas[ValorUnitario])
```
O que faz: em cada linha da tabela de vendas, multiplica a quantidade pelo
preço, e depois soma tudo. Isso dá o total vendido em reais.

**Quantidade Vendida**
```
SUM(Fato_Vendas[Quantidade])
```
O que faz: soma a coluna de quantidade — dá quantos itens foram vendidos
ao todo.

**Qtd Notas Fiscais**
```
DISTINCTCOUNT(Fato_Vendas[NotaFiscal])
```
O que faz: conta quantas notas fiscais diferentes existem (ou seja, quantas
vendas foram feitas).

**Ticket Médio**
```
DIVIDE([Valor Vendas], [Qtd Notas Fiscais])
```
O que faz: divide o total vendido pelo número de notas — dá o valor médio
gasto em cada venda. Usei `DIVIDE` em vez do sinal de "/" porque essa função
evita erro quando não há nenhuma nota (dividir por zero).

---

## Entrega 2 (AC2) — vendedores

**% Participação Vendedor**
```
DIVIDE([Valor Vendas], CALCULATE([Valor Vendas], ALL(Dim_Vendedor)))
```
O que faz: calcula que fatia, em porcentagem, cada vendedor representa do
total vendido pela empresa.

**Ranking Vendedor**
```
RANKX(ALL(Dim_Vendedor[Vendedor]), [Valor Vendas],, DESC)
```
O que faz: coloca os vendedores em ordem, do que mais vendeu para o que
menos vendeu.

---
