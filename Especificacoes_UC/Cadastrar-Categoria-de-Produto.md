# Histórico de Revisão

|    Data    | Versão |                                         Modificação                                        |                Autor                |
|:----------:|:------:|:----------------------------------------------------------------------------------------:|:-----------------------------------:|
| 29/03/2018 | 1.0 | Adicionando estrutura do documento e preenchendo por completo | Guilherme Lacerda e Guilherme Augusto |

***

# Sumário

>[1. Descrição](#1-descrição)

>[2. Atores](#2-atores)

>[3. Pré-Condições](#3-pré-condições)

>[4. Fluxo Básico](#4-fluxo-básico)

>[5. Fluxo Alternativo](#5-fluxo-alternativo)

>[6. Fluxo de Exceção](#6-fluxo-de-exceção)

> * [6.1 FE01 - Categoria já existente](#61-fe01---categoria-já-existente)

>[7. Pós-Condições](#7-pós-condição)

>[8. Regras de Negócio](#8-regras-de-negócio)

***

# 1. Descrição
 <p align="justify"> &emsp;&emsp;  Este caso de uso representa a realizaçao do cadastro de categorias, permitindo a disponibilidade de mais opções para os produtos serem disponíveis aos clientes, além de uma nova combinação de computadores. </p>

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
|   Ator principal   |   Administrador   |
|   Ator secundário  |   Sistema         |

# 3. Pré-Condições

&emsp;&emsp; O usuário deve acessar a plataforma online (website) como um administrador, para obter privilégios para [atualizar estoque](https://github.com/Desenho-1-2018-G-6/docs/wiki/Atualizar-Estoque), [cadastrar produtos](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Produtos) e [cadastrar categoria de um produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Categoria-de-Produto).

# 4. Fluxo Básico

| Passo | Descrição |
|:----:|:----:|
|   P01   |   O administrador clica no botão de cadastrar categoria   |
|   P02   |   O administrador visualiza as categorias já existentes   |
|   P03   |   O administrador insere nos campos disponíveis as informações referentes à categoria que será cadastrada   |
|   P04   |   O administrador confirma as informações inseridas   |
|   P05   |   O administrador recebe uma mensagem confirmando o cadastro de uma nova categoria de produto  |

# 5. Fluxo Alternativo

Não se aplica.

# 6. Fluxo de Exceção

## FE01 - Categoria já existente

| Passo | Descrição | Referência |
|:----:|:----:|:----------------:|
|   P01   |   O administrador clica no botão de cadastrar categoria   |
|   P02   |   O administrador visualiza as categorias já existentes   |
|   P03   |   O administrador insere nos campos disponíveis as informações referentes à categoria que será cadastrada   |
|   P04   |   O administrador confirma as informações inseridas   |
|   P05   |   O administrador recebe uma mensagem informando que não foi possível realizar a criação de uma nova categoria pois a inserida já existia na base de dados  |

# 7. Pós-Condição
 <p align="justify"> &emsp;&emsp; A nova categoria será implementada dando mais opções para produtos e para montagens de setups diferentes.</p>

# 8. Regras de negócio

| ID | Descrição | Passo do Fluxo Associado |
|:----:|:----:|:----------------:|
|   RN01   |    É necessário que a categoria seja nova para a realização do cadastro, caso já exista será retornado uma mensagem de erro informando a cópia   |        FE01 - P05         |
