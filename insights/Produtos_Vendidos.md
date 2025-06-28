# Análise dos Produtos Mais Vendidos

**Prompt 1**
*Me indique qual o produto mais vendido, com análise conclusiva*

**Resposta - Em texto, conforme instruções + estrutura da pergunta**

O produto mais vendido foi o modelo NEW MEGANIUM RG 40XXV, com um total de 41 unidades comercializadas.
🔍 Conclusão:
O desempenho de vendas do NEW MEGANIUM RG 40XXV se destaca entre os demais itens do portfólio, indicando forte aceitação do produto no mercado. Esse resultado pode ser reflexo de uma combinação eficaz de posicionamento, promoção e desempenho técnico percebido, sendo um forte candidato para reforço de estoque, ações promocionais ou campanhas de marketing específicas. Avaliar os canais onde ele teve maior saída pode gerar oportunidades adicionais de crescimento. 

**Código** 
- Python:

# Remover entradas com valores ausentes nas colunas relevantes
df = df.dropna(subset=['product_sold', 'quantity'])

# Agrupar por produto e somar as quantidades vendidas
produtos_mais_vendidos = df.groupby('product_sold')['quantity'].sum().reset_index()

# Ordenar do mais vendido para o menos vendido
produtos_mais_vendidos = produtos_mais_vendidos.sort_values(by='quantity', ascending=False).reset_index(drop=True)

# Exibir o produto mais vendido
produto_top = produtos_mais_vendidos.iloc[0]
produto_top
