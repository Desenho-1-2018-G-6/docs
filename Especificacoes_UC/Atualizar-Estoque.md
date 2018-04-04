# Histórico de Revisão

|    Data    | Versão |                                         Modificação                                        |                Autor                |
|:----------:|:------:|:----------------------------------------------------------------------------------------:|:-----------------------------------:|
| 28/03/2018 | 1.0 | Adicionando estrutura do documento e preenchendo por completo | Guilherme Lacerda e Guilherme Augusto |

***

# Sumário

>[1. Descrição](#1-descrição)

>[2. Atores](#2-atores)

>[3. Pré-Condições](#3-pré-condições)

>[4. Fluxo Básico](#4-fluxo-básico)

>[5. Fluxo Alternativo](#5-fluxo-alternativo)

>[6. Fluxo de Exceção](#6-fluxo-de-exceção)

> * [6.1. FE01 - Erro na inserção do estoque](#61-fe01---erro-na-inserção-do-estoque)

>[7. Pós-Condições](#7-pós-condição)

>[8. Regras de Negócio](#8-regras-de-negócio)

***

# 1. Descrição
<p align="justify"> &emsp;&emsp; Este caso de uso representa a operação que o administrador da plataforma pode realizar sobre a quantidade de produtos dentro do site, podendo incrementar mais produtos de determinada categoria ou retirar produtos obsoletos. </p>

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
|   Ator principal   |   Administrador   |
|   Ator secundário   |   Sistema   |

# 3. Pré-Condições

&emsp;&emsp; O usuário deve acessar a plataforma online (website) como um administrador, para obter privilégios para [atualizar estoque](https://github.com/Desenho-1-2018-G-6/docs/wiki/Atualizar-Estoque), [cadastrar produtos](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Produtos) e [cadastrar categoria de um produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Categoria-de-Produto). Outra condição é que o produto e a categoria já existam dentro da base de dados do aplicação.

# 4. Fluxo Básico

| Passo | Descrição |
|:----:|:----:|
|   P01   |   O administrador clica no botão de atualizar estoque   |
|   P02   |   O administrador visualiza as informações referentes à categoria e ao nome do produto   |
|   P03   |   O administrador seleciona o produto   |
|   P04   |   O administrador altera a quantidade no estoque do produto selecionado   |
|   P05   |   O administrador confirma a quantidade adicionada ao estoque do produto |

# 5. Fluxo Alternativo

Não se aplica.

# 6. Fluxo de Exceção

## FE01 - Erro na inserção do estoque

| Passo | Descrição | Referência |
|:----:|:----:|:----------------:|
|   P01   |   O administrador clica no botão de atualizar estoque |
|   P02   |   O administrador visualiza as informações referentes à categoria e ao nome do produto   |
|   P03   |   O administrador seleciona o produto |
|   P04   |   O administrador altera a quantidade no estoque do produto selecionado |
|   P05   |   O administrador comete um erro e adiciona uma quantidade inválida no estoque do produto selecionado |
|   P06   |   O administrador recebe uma mensagem informando que o valor inserido para atualização é inválido |

# 7. Pós-Condição
&emsp;&emsp; Ao final da atualização, o estoque dos produtos atualizados serão repostos para os clientes conseguirem [adicionar os produtos ao carrinho](https://github.com/Desenho-1-2018-G-6/docs/wiki/Adicionar-Produto-no-Carrinho).

# 8. Regras de negócio

| ID | Descrição | Passo do Fluxo Associado |
|:----:|:----:|:----------------:|
|   RN01   |   A quantidade a ser inserida não pode ser um valor menor que 0 e maior que 10000   |  FE01 - P05 ou FB - P04  |
