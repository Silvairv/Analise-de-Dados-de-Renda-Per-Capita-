# Analise-de-Dados-de-Renda-Per-Capita-
Este notebook Python utiliza dados da PNADC (Pesquisa Nacional por Amostra de Domicílios Contínua) para analisar a renda per capita (RDPC) no Brasil, com foco nos anos de 2014 a 2017. O objetivo é visualizar e comparar a renda per capita entre as diferentes regiões e estados do país.

Conteúdo do Notebook
O notebook executa as seguintes etapas:

Instalação de Pacotes: Instala as bibliotecas necessárias para o processamento e visualização dos dados (unidecode, openpyxl, pandas, plotly.express, nbformat).

Carregamento e Pré-processamento dos Dados:
Carrega os dados de uma planilha Excel (BASE PNADC 2012 A 2017 ABR2019 10042019.xlsx).
Remove acentos e padroniza os nomes das colunas NOME_AGREGA e SIGLA_AGREGA.
Filtra os dados para incluir apenas os anos de 2014 a 2017.
Remove linhas com valores ausentes na coluna RDPC.
Cria novas colunas (REG_AGREGA e ESTADO_PARA_AGREGACAO) para mapear a região e o estado de cada agregação (incluindo Regiões Metropolitanas e Brasil).

Agregação dos Dados:
Agrega os dados por estado (df_estado) e por região (df_regiao), calculando o primeiro valor de RDPC para cada grupo.

Visualização dos Dados:
Define funções (plot_regiao e plot_estado) para gerar gráficos de barras interativos utilizando a biblioteca Plotly Express.
Gera e exibe um gráfico de barras da renda per capita por Região e Brasil.
Gera e exibe um gráfico de barras da renda per capita por Estado.

Salvamento dos Dados Tratados: Salva o dataframe filtrado e tratado em um novo arquivo Excel (dados_pnadc_tratados.xlsx).

Como Executar o Notebook
Certifique-se de ter o arquivo de dados original (BASE PNADC 2012 A 2017 ABR2019 10042019.xlsx) no mesmo diretório do notebook ou atualize o caminho do arquivo no código.
Execute as células do notebook sequencialmente.
Os gráficos serão exibidos no output das células correspondentes.
O arquivo dados_pnadc_tratados.xlsx será criado com os dados processados.

Requisitos
Python 3.6+
Bibliotecas Python listadas na primeira célula (unidecode, openpyxl, pandas, plotly.express, nbformat). Essas bibliotecas serão instaladas automaticamente ao executar a primeira célula.

Dados
Os dados utilizados neste notebook são provenientes da PNADC. A coluna RDPC representa a renda per capita.

Análise
Os gráficos gerados fornecem uma visão da distribuição da renda per capita entre as diferentes regiões e estados do Brasil no período de 2014 a 2017. É possível observar as diferenças regionais e estaduais na renda.
