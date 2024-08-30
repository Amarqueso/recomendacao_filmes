# Sistema de Recomendação de Filmes
Este projeto implementa um sistema de recomendação de filmes utilizando similaridade cosseno para sugerir filmes com base nas avaliações dos usuários.

Visão Geral do Projeto: O objetivo principal deste projeto é recomendar filmes semelhantes a um filme selecionado, calculando a similaridade cosseno entre as avaliações dos usuários. O processo envolve a fusão dos dados de filmes com as avaliações dos usuários, criando uma tabela dinâmica para organizar os dados e aplicando similaridade cosseno para identificar e classificar os filmes mais semelhantes.

# Arquivos Utilizados

movies.csv: Contém detalhes sobre os filmes, incluindo seus títulos e IDs únicos.

ratings.csv: Contém as avaliações dos usuários para diferentes filmes, incluindo IDs de usuários, IDs de filmes e as notas atribuídas.

# Etapas Implementadas

Carregamento dos Dados:

Os dados dos filmes são carregados a partir do arquivo movies.csv e os dados de avaliação dos usuários do arquivo ratings.csv utilizando o pandas.
Fusão dos Dados:

Os dois datasets são unidos utilizando a coluna comum movieId para combinar os títulos dos filmes com suas respectivas avaliações por diferentes usuários.
Criação da Tabela Dinâmica:

Uma tabela dinâmica (pivot table) é criada onde os títulos dos filmes são utilizados como índices e os IDs dos usuários como colunas, com as notas correspondentes como valores. Valores ausentes são preenchidos com zero.
Cálculo da Similaridade Cosseno:

A similaridade cosseno entre os filmes é calculada com base nas avaliações dos usuários utilizando a função cosine_similarity do módulo sklearn.metrics.pairwise.
DataFrame de Recomendações:

Os resultados da similaridade cosseno são armazenados em um DataFrame onde tanto as colunas quanto o índice são títulos de filmes, permitindo a fácil consulta de similaridades entre filmes.
Exemplo de Recomendação:

Um exemplo é fornecido onde o sistema gera uma lista de filmes semelhantes a "X-Men: First Class (2011)" com base nas avaliações dos usuários. As 10 principais recomendações são exibidas.

![recomendacoes_filmes](https://github.com/user-attachments/assets/b64ed7e6-207f-454f-a45f-e66911ec059f)
