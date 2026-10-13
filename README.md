# Projeto de BI — Análise de Vendas 2019

Trabalho da disciplina de BI/Análise de Dados. A ideia é pegar duas planilhas
de Excel com vendas de 2019 e transformar isso num painel visual (dashboard)
no Power BI, feito em 4 partes ao longo do semestre.

> **Regra principal:** cada entrega nova mantém tudo o que já foi feito antes
> e adiciona uma parte nova. Na entrega final, o painel inteiro (as 4 partes
> juntas) deve estar funcionando.

## As entregas

| Entrega | Data | O que essa parte mostra | Status |
|---|---|---|---|
| AC1 | 14/09 | Resumo geral das vendas (total vendido, quantidade, etc.) | Concluído |
| AC2 | 13/10 | Quanto cada vendedor vendeu | Concluído |

## Links do projeto

- Quadro no Trello: `<colar aqui o link do quadro>`
- Vídeo da entrega 1 (14/09): `<colar link do YouTube/Drive>`
- Vídeo da entrega 2 (13/10): `<colar link do YouTube/Drive>`
- Vídeo da entrega 3 (08/11): `<colar link do YouTube/Drive>`
- Vídeo da entrega final (22/11): `<colar link do YouTube/Drive>`

## O que tem em cada pasta

```
/data     -> a planilha já organizada, que deve ser aberta no Power BI
/powerbi  -> as fórmulas usadas dentro do Power BI (explicadas abaixo)
/docs     -> o documento explicando o projeto todo, e prints de cada entrega
```

- **`/data/BaseVendas_ModeloPowerBI.xlsx`** — a planilha de vendas já
  arrumada e organizada, pronta para abrir no Power BI.
- **`/powerbi/medidas-dax.md`** — todas as fórmulas usadas para calcular os
  números que aparecem no painel (o "DAX" é a linguagem de fórmulas do Power
  BI, parecida com fazer fórmula no Excel).
- **`/powerbi/m-queries/`** — os passos usados para arrumar os dados antes de
  virarem gráfico (chamado de "Power Query").
- **`/docs/PlanoDoProjeto...docx`** — o documento completo explicando o
  projeto, com tudo em linguagem simples.
- **`/docs/screenshots/`** — imagens de cada tela do painel, separadas por
  entrega.

## Como abrir isso no Power BI

1. Baixe o arquivo `data/BaseVendas_ModeloPowerBI.xlsx`.
2. Abra o Power BI Desktop → Página Inicial → Obter Dados → Pasta de
   Trabalho do Excel → escolha o arquivo.
3. Dentro do Power BI, ligue as 4 tabelas (Fato_Vendas, Dim_Data,
   Dim_Produto, Dim_Vendedor) pelas colunas de código que elas têm em comum.
4. Copie as fórmulas do arquivo `powerbi/medidas-dax.md` para dentro do
   Power BI (Modelagem → Nova Medida).
5. Monte as telas do painel seguindo o documento em `/docs`.
