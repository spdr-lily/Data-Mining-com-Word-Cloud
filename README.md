# Relatório de Projeto: Mineração de Dados em Avaliações de Produtos com Visualização em Nuvem de Palavras

## 1. Introdução

A análise de sentimentos aplicada a avaliações de clientes é uma técnica para compreender a percepção dos consumidores em relação a produtos e serviços. Este projeto tem como objetivo aplicar técnicas de *Data Mining* (Mineração de Dados) e Processamento de Linguagem Natural (PLN) em uma base de dados de avaliações de uma loja de roupas. A análise visa extrair padrões linguísticos, com foco na identificação de adjetivos e frequências de palavras, culminando na visualização em forma de nuvem de palavras para representar as impressões predominantes dos consumidores.

## 2. Metodologia

### 2.1 Base de Dados

Foi utilizada uma base de dados contendo avaliações textuais de clientes. O arquivo original, no formato CSV, foi carregado utilizando a biblioteca **pandas**. O campo principal de interesse foi o texto da avaliação ("Texto da Avaliação").

### 2.2 Pré-processamento

As etapas de pré-processamento incluíram:
- Remoção de registros com avaliações ausentes (`dropna`);
- Conversão explícita do conteúdo para o tipo string;
- Tokenização das avaliações, segmentando o texto em palavras individuais.

### 2.3 Análise de Frequência de Palavras

A frequência de cada palavra foi computada utilizando a biblioteca **collections.Counter**, e os dados foram visualizados por meio da biblioteca **WordCloud**, gerando uma nuvem de palavras que destaca os termos mais frequentes nas avaliações.

### 2.4 Extração de Adjetivos

Utilizou-se a biblioteca **spaCy**, com o modelo `pt_core_news_sm`, para realizar o *Part-of-Speech Tagging* e isolar os adjetivos nas avaliações, por serem os elementos linguísticos mais indicativos de julgamento subjetivo (ex.: "ótimo", "ruim", "lindo"). Após a identificação dos adjetivos, foi criada uma contagem de frequência dos mesmos.

## 3. Resultados

- A nuvem de palavras mostrou que os termos mais recorrentes nas avaliações eram, em sua maioria, palavras de valoração positiva, como elogios ao produto e à experiência de compra.
- Entre os adjetivos mais frequentes, destacaram-se termos como:
  - **“bom”**, **“lindo”**, **“ótimo”**, **“confortável”**, **“leve”**
- A análise indicou uma tendência predominantemente positiva nas avaliações, sugerindo um alto grau de satisfação do consumidor com os produtos analisados.
- A visualização pela nuvem de palavras se mostrou eficaz para identificar rapidamente os principais aspectos destacados pelos clientes.

## 4. Conclusão

O presente projeto demonstrou como técnicas básicas de mineração de texto e PLN podem ser aplicadas para extrair informações úteis a partir de avaliações de clientes. A utilização de nuvens de palavras e análise de adjetivos revelou padrões de linguagem relevantes que podem ser explorados por empresas para orientar decisões de marketing, controle de qualidade e desenvolvimento de produtos.
