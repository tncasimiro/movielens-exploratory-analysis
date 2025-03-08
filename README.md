# Análise Explorátoria dos Dados - DataSet 'small' do Group Lens

## Introdução

A análise exploratória dos dados do dataset 'small' do Group Lens tem como objetivo entender e interpretar uma coleção de dados relacionados a filmes. O dataset oferece insights valiosos sobre filmes, avaliações de usuários e tags, proporcionando uma visão abrangente das preferências e tendências dos filmes. Ao analisar esse dataset, podemos descobrir padrões e correlações entre gêneros, avaliações e interações dos usuários, contribuindo para o desenvolvimento de sistemas de recomendação, análise de tendências de filmes e muito mais. Este trabalho faz parte de uma atividade avaliativa para a matéria de Eletiva II - Ambientes Inteligentes, ministrada pelo professor Elias Kento Tomiyama, da Faculdade Engenheiro Salvador Arena. Neste documento, são descritos a estrutura do dataset, os principais atributos dos dados e os passos realizados para limpar e preparar os dados para análise.

## Descrição da Base de Dados

O dataset consiste em quatro arquivos principais que contêm informações sobre filmes, incluindo títulos, identificadores, avaliações de usuários e tags associadas. Esses dados foram extraídos de diversas fontes, como IMDb e TMDb, e cobrem uma vasta gama de filmes e suas respectivas avaliações.

### Arquivos do Dataset

- **links.csv**: Contém identificadores únicos para cada filme, além dos links para IMDb e TMDb.
- **movies.csv**: Apresenta detalhes sobre os filmes, incluindo título e gêneros.
- **ratings.csv**: Armazena as avaliações de filmes feitas pelos usuários, com as notas e os timestamps.
- **tags.csv**: Fornece tags associadas aos filmes, atribuídas pelos usuários, incluindo o timestamp da criação de cada tag.

### Atributos e Tipos de Dados

#### links.csv:
- `movieId`: Identificador único do filme (Integer)
- `imdbId`: Identificador único no IMDb (Integer)
- `tmdbId`: Identificador único no TMDb (Integer)

#### movies.csv:
- `movieId`: Identificador único do filme (Integer)
- `title`: Título do filme, incluindo o ano de lançamento (String)
- `genres`: Gêneros do filme (String)

#### ratings.csv:
- `userId`: Identificador único do usuário (Integer)
- `movieId`: Identificador único do filme (Integer)
- `rating`: Nota atribuída ao filme (Float)
- `timestamp`: Momento da avaliação (Unix Timestamp)

#### tags.csv:
- `userId`: Identificador único do usuário (Integer)
- `movieId`: Identificador único do filme (Integer)
- `tag`: Tag atribuída ao filme (String)
- `timestamp`: Momento da criação da tag (Unix Timestamp)

## Preparação da Base de Dados

Durante a análise, foram identificados alguns problemas nos dados, que foram corrigidos da seguinte maneira:

- **Conversão de tipos de dados**: O campo `tmdbId` estava armazenado como `float`, mas foi convertido corretamente para o tipo `Integer`.
- **Padronização dos gêneros**: Alguns gêneros estavam mal formatados no arquivo `movies.csv`. Foi realizado um ajuste para utilizar um delimitador consistente (`|`).
- **Conversão de Timestamps**: Os campos de timestamp em `tags.csv` e `ratings.csv` estavam no formato Unix Timestamp, que foi convertido para o formato `datetime64[ns]` para facilitar a análise temporal.

---

# Exploratory Data Analysis - Group Lens 'small' Dataset

## Introduction

The exploratory data analysis of the 'small' dataset from Group Lens aims to understand and interpret a collection of data related to movies. The dataset provides valuable insights into movies, user ratings, and associated tags, offering a comprehensive view of movie preferences and trends. By analyzing this dataset, we can uncover patterns and correlations between genres, ratings, and user interactions, contributing to the development of recommendation systems, movie trend analysis, and much more. This work is part of an evaluation activity for the course Eletiva II - Ambientes Inteligentes, taught by Professor Elias Kento Tomiyama, from the Faculdade Engenheiro Salvador Arena. This document describes the dataset structure, the main attributes of the data, and the steps taken to clean and prepare the data for analysis.

## Dataset Description

The dataset consists of four main files that contain information about movies, including titles, identifiers, user ratings, and associated tags. These data were extracted from various sources, such as IMDb and TMDb, and cover a wide range of movies and their respective ratings.

### Dataset Files

- **links.csv**: Contains unique identifiers for each movie, along with links to IMDb and TMDb.
- **movies.csv**: Provides details about the movies, including titles and genres.
- **ratings.csv**: Stores the movie ratings given by users, with the ratings and timestamps.
- **tags.csv**: Provides tags associated with the movies, assigned by users, including the timestamp of each tag's creation.

### Attributes and Data Types

#### links.csv:
- `movieId`: Unique movie identifier (Integer)
- `imdbId`: Unique identifier in IMDb (Integer)
- `tmdbId`: Unique identifier in TMDb (Integer)

#### movies.csv:
- `movieId`: Unique movie identifier (Integer)
- `title`: Movie title, including the release year (String)
- `genres`: Movie genres (String)

#### ratings.csv:
- `userId`: Unique user identifier (Integer)
- `movieId`: Unique movie identifier (Integer)
- `rating`: Rating given to the movie (Float)
- `timestamp`: Time of the rating (Unix Timestamp)

#### tags.csv:
- `userId`: Unique user identifier (Integer)
- `movieId`: Unique movie identifier (Integer)
- `tag`: Tag assigned to the movie (String)
- `timestamp`: Time of tag creation (Unix Timestamp)

## Data Preparation

During the analysis, some issues with the data were identified and corrected as follows:

- **Data Type Conversion**: The `tmdbId` field was stored as `float`, but it was correctly converted to the `Integer` type.
- **Genre Standardization**: Some genres were improperly formatted in the `movies.csv` file. Adjustments were made to use a consistent delimiter (`|`).
- **Timestamp Conversion**: The timestamp fields in `tags.csv` and `ratings.csv` were in Unix Timestamp format, which was converted to the `datetime64[ns]` format to facilitate temporal analysis.
