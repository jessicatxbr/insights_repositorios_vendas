# Cálculo da Quantidade de Vendas

## Prompt 1

*Me indique a quantidade de vendas por site e faça a análise*

**Resposta - Em tabela, conforme instruções**

![image](https://github.com/user-attachments/assets/87bb4e9f-6318-49f3-9f35-3fa5d20db849)

**Resposta - Em texto, conforme instruções**

📊 Análise por site:
1. Shopee lidera as vendas com 64 unidades vendidas, o que indica forte presença e competitividade da plataforma para o público-alvo da marca. Pode estar associada à base de usuários sensível a preço e promoções.
2. AliExpress aparece logo atrás com 58 unidades, sugerindo bom alcance internacional e/ou aproveitamento de demanda por produtos de nicho.
3. Etsy registrou 56 vendas, um volume comparável ao AliExpress, o que é notável considerando seu foco em produtos personalizados e criativos, sugerindo que os produtos Meganium possuem apelo estético ou de colecionador.
✅ Conclusão:
As vendas estão bem distribuídas entre as três plataformas, com leve vantagem para a Shopee. Essa diversificação é saudável e permite à empresa atingir públicos diferentes. A performance equilibrada indica que estratégias de marketing e logística estão bem alinhadas em múltiplos canais. Recomenda-se manter a presença nas três plataformas, enquanto se observa oportunidades de expansão ou diferenciação em cada uma. 

**Código**

- Python:

#Agrupar por site e somar as quantidades vendidas
vendas_por_site = df.groupby('site')['quantity'].sum().reset_index()

#Ordenar do maior para o menor
vendas_por_site = vendas_por_site.sort_values(by='quantity', ascending=False).reset_index(drop=True)

import ace_tools as tools; tools.display_dataframe_to_user(name="Vendas por Site", dataframe=vendas_por_site)

## Prompt 2

*Me indique a quantidade de vendas por país*

**Resposta - Em planilha, conforme instruções _ estrutura da pergunta**

![image](https://github.com/user-attachments/assets/d02a6dd0-38d5-4fc9-a82d-5399b997e6a7)

**Resposta - Em texto, conforme instruções**
Aqui está a tabela com a quantidade de vendas por país.
Se desejar, posso analisar esses resultados e apontar tendências, oportunidades de mercado e estratégias baseadas no desempenho por região. Deseja que eu faça isso? 

**Prompt Complementar**

*Sim*

**Responsta - Em texto, conforme instruções**

Com base nos dados de vendas por país, temos os seguintes destaques:
🌍 Principais mercados por volume de vendas:
🇨🇦 Canadá – 46 unidades vendidas
O Canadá lidera o ranking, mostrando-se como o mercado mais forte para os produtos da Meganium. Isso pode estar relacionado à familiaridade com e-commerce internacional, bom poder aquisitivo e possível interesse por tecnologia de nicho.
🇫🇷 França – 36 unidades vendidas
A França também se destaca como um mercado estratégico. O apelo por design, inovação e produtos diferenciados pode ter contribuído para o bom desempenho.
🇦🇺 Austrália – 28 unidades vendidas
Um mercado distante, mas altamente digitalizado e consumidor de produtos importados. O sucesso indica eficácia logística e aceitação do produto.
🇯🇵 Japão – 27 unidades vendidas
A presença do Japão no topo da lista é notável, especialmente por ser um mercado exigente. Isso pode sinalizar que os produtos Meganium têm apelo estético e funcional que agrada ao consumidor japonês.
🇩🇪 Alemanha – 23 unidades vendidas
Forte mercado europeu com consumidores criteriosos. A boa performance pode refletir confiança na qualidade e bom posicionamento em marketplaces.
📌 Conclusão:
As vendas estão concentradas em países desenvolvidos com forte cultura de compras online e boa infraestrutura logística. Isso sugere que os produtos têm apelo internacional e são bem recebidos em mercados exigentes e competitivos. Recomenda-se:
Reforçar estoques e campanhas promocionais nos países líderes.
Explorar oportunidades de fidelização, como programas de recompra ou parcerias locais.
Avaliar a viabilidade de fretes otimizados e local fulfillment (como armazéns regionais) nos mercados mais relevantes.
Essa análise reforça o potencial global da marca e direciona estratégias de crescimento internacional.


