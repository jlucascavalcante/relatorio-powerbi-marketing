# 📣 Análise de Campanhas de Marketing — Power BI

Dashboard de análise de perfil de clientes e efetividade de campanhas de marketing, com foco em identificar quais segmentos convertem mais e onde direcionar investimento de forma mais eficiente.

## 🎯 Problema de negócio

Times de marketing costumam distribuir budget de campanha proporcionalmente ao tamanho dos segmentos de clientes — focando nos grupos mais numerosos. Esta análise testa essa premissa: será que o segmento mais numeroso é também o mais eficiente em conversão? Os dados mostram que não, o que tem implicação direta em alocação de orçamento.

## 🔍 Principais insights

- **Taxa de conversão geral: ~16%** (1.703 de 10.649 interações de campanha resultaram em compra).
- **O segmento mais numeroso não é o mais eficiente.** Clientes com Curso Superior são o maior grupo da base (999 de 1.999 clientes, ~50%), mas convertem apenas 14,3%. Clientes com Doutorado são o 2º maior grupo (437 clientes, ~22% da base) e têm a maior taxa de conversão entre todos os níveis de escolaridade: 22,0%. Ou seja, quase um quarto da base converte significativamente melhor que o grupo prioritário — argumento direto para realocação de budget.
- **Mais filhos, menos conversão.** A taxa de conversão cai de forma consistente conforme o número de filhos aumenta: 18,2% (sem filhos) → 13,5% (1 filho) → 5,1% (2 filhos).
- **Achado contraintuitivo no estado civil.** Divorciados convertem mais (20,9%) que solteiros (16,2%) e que casados (12,8%) — na maioria das hipóteses de senso comum, seria o oposto.
- **Clientes convertidos têm renda maior.** Salário médio anual de quem comprou via campanha é R$ 59 mil, contra R$ 51 mil de quem não comprou (+15,7%).
- **Concentração geográfica forte nos EUA**, com o maior volume de gasto entre os 7 países analisados (2018–2023), incluindo recuperação visível após queda em 2021.

## 📄 Estrutura do dashboard

**👤 Cliente**
Perfil demográfico da base: 1.999 clientes, segmentados por escolaridade e estado civil, com métricas de canal de compra (loja, web, catálogo, desconto).

**🧠 Comportamento**
Relação entre salário anual e gasto total; cruzamento de escolaridade x estado civil; impacto de filhos e adolescentes em casa no gasto total.

**📢 Campanhas**
Taxa de conversão por número de filhos, resultado geral das campanhas, matriz de conversão por escolaridade x estado civil, comparação de salário médio entre convertidos e não convertidos.

**🏪 Ponto de Vendas**
Gasto por categoria e país; evolução do gasto por ano e país entre 2018 e 2023.

## 🛠️ Stack técnica

- **Ferramenta:** Power BI Desktop
- **Modelagem e visualização:** segmentações cruzadas (escolaridade x estado civil), gráficos de dispersão, matrizes e séries temporais
- **Transformação de dados:** 
## 📊 Fonte dos dados

Dataset baseado no **["Customer Personality Analysis"](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)**, disponível publicamente no Kaggle, com adaptações feitas pela **Data Science Academy (DSA)** para o curso (incluindo a lista de países analisados). O dashboard, a modelagem e as análises foram refeitos de forma independente a partir do material do curso, com exploração de gráficos, formatações e cruzamentos próprios.

## 🔗 Acesse o relatório

[Acesse o dashboard](https://app.powerbi.com/view?r=eyJrIjoiNjkzZWU4OGItMjFmMi00YTlkLWI3ZDktZDkwNmVmNjFjMjc0IiwidCI6ImIyZTE2Mjk3LTJlZDYtNDFiOC1iODIyLWE5NTRlOTViZDJmMCIsImMiOjR9&pageName=7687c5be0b1a0280779a)

## 📌 Limitações e próximos passos

- Os valores de "gasto x filhos em casa" e "gasto x adolescentes em casa" são **totais por grupo**, não médias por cliente — como a maioria da base não tem filhos, o total maior nesse grupo pode refletir apenas volume, não necessariamente maior gasto individual. Próximo passo: normalizar por média de gasto por cliente em cada grupo.
- A definição de "conversão" usada aqui considera resposta positiva a pelo menos uma campanha; não foi feita segmentação por campanha individual (1 a 5).
- Próxima iteração: cruzar a taxa de conversão por escolaridade com o canal de compra (loja vs. web vs. catálogo) para entender se o canal influencia o padrão encontrado.
