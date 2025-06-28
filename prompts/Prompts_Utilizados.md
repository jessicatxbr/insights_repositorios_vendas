# Prompts Utilizados

- Faça uma análise demográfica do público alvo, considerando inclusive a idade dos compradores e tente identificar o sexo a partir do nome do comprador

- Me mostre a média de idade dos compradores de cada produto

- Me indique qual o produto mais vendido, com análise conclusiva

- Me indique a quantidade de vendas por site e faça a análise

- Me indique a quantidade de vendas por país

- Calcule o valor total das vendas por mês

- Transforme essa análise em resultado conclusivo

# Códigos

- **Python:**

import pandas as pd import os

#Caminhos dos arquivos arquivos = [ "/mnt/data/Meganium_Sales_Data_-AliExpress.csv", "/mnt/data/Meganium_Sales_Data-Etsy.csv", "/mnt/data/Meganium_Sales_Data-_Shopee.csv", "/mnt/data/Updated_Anbernic_Sales_Data.csv", "/mnt/data/Meganium_Sales_Data.csv" ]

#Lê todos os arquivos em um único DataFrame dfs = [pd.read_csv(arquivo) for arquivo in arquivos] df_total = pd.concat(dfs, ignore_index=True)

#Verifica as colunas disponíveis df_total.columns

- **Python:**

#Agrupar por site e somar as quantidades vendidas vendas_por_site = df.groupby('site')['quantity'].sum().reset_index()

#Ordenar do maior para o menor vendas_por_site = vendas_por_site.sort_values(by='quantity', ascending=False).reset_index(drop=True)

import ace_tools as tools; tools.display_dataframe_to_user(name="Vendas por Site", dataframe=vendas_por_site)

- **Python:**

#Remover entradas com valores ausentes nas colunas relevantes df = df.dropna(subset=['product_sold', 'quantity'])

#Agrupar por produto e somar as quantidades vendidas produtos_mais_vendidos = df.groupby('product_sold')['quantity'].sum().reset_index()

#Ordenar do mais vendido para o menos vendido produtos_mais_vendidos = produtos_mais_vendidos.sort_values(by='quantity', ascending=False).reset_index(drop=True)

#Exibir o produto mais vendido produto_top = produtos_mais_vendidos.iloc[0] produto_top
