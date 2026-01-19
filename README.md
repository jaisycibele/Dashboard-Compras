# 📊 Análise de Dados de Compras com Python, Pandas e Streamlit

## 📌 Sobre o Projeto
Este repositório reúne uma série de **análises de dados e dashboards interativos** desenvolvidos em Python, utilizando **Pandas** e **Streamlit**, com base em dados de compras fictícios.

O projeto foi desenvolvido durante o curso **Análise de Dados com Python e Pandas (Udemy)**, com o objetivo de aplicar na prática conceitos fundamentais de **análise de dados**, **manipulação de DataFrames** e **visualização interativa**.

---

## 🛠️ Tecnologias Utilizadas
- **Python**
- **Pandas**
- **Streamlit**

---

## ▶️ Como Executar os Projetos com Streamlit

### 🔧 Pré-requisitos
- Python 3 instalado
- Pip configurado

Execute o projeto com o comando:

```bash
streamlit run {nome_do_arquivo.py}
```

---

### 📦 Instalação das Dependências
```bash
pip install pandas streamlit
```

---

## 📈 Descrição dos Projetos

### 🔹 Visualização Inicial da Tabela de Compras  
**Arquivo:** `1_Visualizando_TBL.py`

Este script utiliza as bibliotecas **Pandas** e **Streamlit** para realizar a **visualização inicial dos dados de compras**, permitindo uma exploração rápida e interativa do dataset.

#### O que é feito neste arquivo:
- Importação das bibliotecas **Streamlit** e **Pandas**
- Leitura do arquivo `compras.csv`, localizado na pasta `datasets`
- Definição do separador de colunas (`;`) e do separador decimal (`,`)
- Exibição do DataFrame completo em uma tabela interativa no navegador

#### Objetivo:
Permitir uma **análise exploratória inicial dos dados**, facilitando a visualização das colunas, valores e estrutura do dataset antes da realização de análises mais avançadas.

#### Resultado:
Ao executar o arquivo com o Streamlit, o usuário visualiza uma **tabela interativa**, com funcionalidades como rolagem, ordenação e busca, diretamente no navegador.


### 🔹 Seleção de Colunas e Filtros Dinâmicos  
**Arquivo:** `2_Selecionando_Colunas.py`

Este script utiliza **Pandas** e **Streamlit** para criar uma interface interativa que permite **selecionar colunas específicas e aplicar filtros dinâmicos** sobre os dados de compras.

#### O que é feito neste arquivo:
- Leitura do arquivo `compras.csv`, localizado na pasta `dataset`
- Definição da coluna de índice ao carregar o CSV
- Listagem dinâmica das colunas disponíveis no DataFrame
- Seleção interativa das colunas a serem exibidas
- Criação de filtros dinâmicos na barra lateral (sidebar)
- Aplicação de filtros por coluna e valor selecionado

#### Funcionalidades:
- Seleção de múltiplas colunas para visualização
- Filtro dos dados com base em valores únicos de uma coluna
- Botão para aplicar o filtro
- Botão para limpar o filtro e exibir os dados completos

#### Objetivo:
Permitir uma **análise exploratória interativa**, dando ao usuário controle sobre **quais colunas visualizar** e **como filtrar os dados**, sem necessidade de alterar o código.

#### Resultado:
Ao executar o arquivo com Streamlit, o usuário visualiza uma **tabela dinâmica**, podendo selecionar colunas, aplicar filtros e limpar a visualização diretamente pelo navegador.

### 🔹 Adição de Novos Registros de Compras  
**Arquivo:** `3_Adicionando_Linhas.py`

Este script utiliza **Pandas** e **Streamlit** para criar uma interface interativa que permite **adicionar novos registros de compras** diretamente no dataset, simulando um pequeno sistema de cadastro.

#### O que é feito neste arquivo:
- Leitura dos arquivos `compras.csv`, `lojas.csv` e `produtos.csv` a partir da pasta `dataset`
- Criação de campos interativos na barra lateral (sidebar) para seleção e preenchimento dos dados
- Associação dinâmica entre lojas e vendedores
- Seleção de produto, cliente, gênero e forma de pagamento
- Geração automática do identificador da compra
- Inserção de um novo registro no DataFrame
- Persistência dos dados no arquivo CSV

#### Funcionalidades:
- Seleção da loja e do vendedor de forma dinâmica
- Cadastro de novas compras via interface Streamlit
- Atualização automática do arquivo `compras.csv`
- Exibição do DataFrame atualizado após a inclusão do registro

#### Objetivo:
Demonstrar como utilizar o **Streamlit não apenas para visualização**, mas também para **interação e modificação de dados**, integrando entrada de dados com manipulação de DataFrames em Pandas.

#### Resultado:
Ao executar o arquivo, o usuário pode **cadastrar novas compras** por meio da interface, visualizar a confirmação da operação e acompanhar os dados atualizados em tempo real.

### 🔹 Dashboard de Volume de Dados e Indicadores  
**Arquivo:** `4_volume_dados.py`

Este script utiliza **Pandas** e **Streamlit** para criar um **dashboard interativo de indicadores de compras**, permitindo analisar o volume de dados e o desempenho de lojas e vendedores em um período selecionado.

#### O que é feito neste arquivo:
- Leitura dos arquivos `compras.csv`, `lojas.csv` e `produtos.csv` a partir da pasta `dataset`
- Tratamento e enriquecimento dos dados com informações de preço dos produtos
- Junção dos dados de compras com os dados de produtos utilizando `merge`
- Cálculo de comissão sobre o valor das vendas
- Criação de filtros de data interativos na barra lateral (sidebar)
- Geração de métricas consolidadas e indicadores de desempenho

#### Funcionalidades:
- Filtro por período (data inicial e final)
- Exibição do valor total de compras no período
- Exibição da quantidade de compras realizadas
- Identificação da loja com maior volume de vendas
- Identificação do vendedor com melhor desempenho
- Cálculo de comissão por vendedor
- Exibição de métricas visuais utilizando `st.metric`

#### Objetivo:
Fornecer uma **visão gerencial dos dados de compras**, permitindo análises rápidas de desempenho e volume por período, loja e vendedor, através de uma interface simples e interativa.

#### Resultado:
Ao executar o arquivo com Streamlit, o usuário visualiza um **dashboard de indicadores**, com métricas atualizadas dinamicamente conforme o período selecionado.

### 🔹 Tabela Dinâmica Interativa (Pivot Table)  
**Arquivo:** `5_TB_Dinamica.py`

Este script utiliza **Pandas** e **Streamlit** para criar uma **tabela dinâmica interativa**, permitindo ao usuário realizar análises personalizadas dos dados de compras.

#### O que é feito neste arquivo:
- Leitura dos arquivos `compras.csv`, `lojas.csv` e `produtos.csv` a partir da pasta `datasets`
- Tratamento e enriquecimento dos dados com informações de preço dos produtos
- Cálculo de comissão com base em um percentual definido em variável
- Criação de filtros interativos na barra lateral (sidebar)
- Construção dinâmica de tabelas do tipo **Pivot Table** utilizando `pd.pivot_table`

#### Funcionalidades:
- Seleção dinâmica de índices (ex.: loja, vendedor, produto, gênero do cliente, forma de pagamento)
- Seleção dinâmica de colunas para análise
- Escolha do valor numérico a ser analisado (preço ou comissão)
- Escolha da métrica de agregação (soma ou contagem)
- Cálculo automático de totais por linha e total geral
- Visualização interativa da tabela dinâmica

#### Objetivo:
Permitir uma **análise flexível e personalizada dos dados**, possibilitando diferentes combinações de dimensões e métricas sem necessidade de alterar o código.

#### Resultado:
Ao executar o arquivo com Streamlit, o usuário pode **montar sua própria tabela dinâmica**, explorando os dados de forma interativa diretamente no navegador.
