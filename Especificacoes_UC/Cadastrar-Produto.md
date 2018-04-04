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

> * [6.1. FE01 - Produto já existente](#61-fe01---produto-já-existente)

> * [6.2. FE02 - Informações incompletas do produto](#62-fe02---informações-incompletas-do-produto)

>[7. Pós-Condições](#7-pós-condição)

>[8. Regras de Negócio](#8-regras-de-negócio)

***

# 1. Descrição
 <p align="justify"> &emsp;&emsp; Este caso de uso representa a realizaçao do cadastro dos produtos, permitindo a disponibilidade de mais produtos para serem disponíveis aos clientes. </p>

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
|   Ator principal   |   Administrador   |
|   Ator secundário  |   Sistema         |

# 3. Pré-Condições
&emsp;&emsp; O usuário deve acessar a plataforma online (website) como um administrador, para obter privilégios para [atualizar estoque](https://github.com/Desenho-1-2018-G-6/docs/wiki/Atualizar-Estoque), [cadastrar produtos](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Produtos) e [cadastrar categoria de um produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Categoria-de-Produto). Outra pré-condição é que a categoria do produto exista dentro da base de dados da plataforma.

# 4. Fluxo Básico

| Passo | Descrição |
|:----:|:----:|
|   P01   |   O administrador clica no botão de cadastrar produto   |
|   P02   |   O administrador seleciona a categoria do produto a ser adicionado   |
|   P03   |   O administrador visualiza os produtos já contidos dentro da categoria selecionada   |
|   P04   |   O administrador insere nos campos disponíveis as informações referentes ao produto que será cadastrado  |
|   P05   |   O administrador confirma as informações inseridas  |
|   P06   |   O administrador recebe uma mensagem confirmando o cadastro de um novo produto |

# 5. Fluxo Alternativo

Não se aplica.

# 6. Fluxo de Exceção

## FE01 - Produto já existente

| Passo | Descrição | Referência |
|:----:|:----:|:----------------:|
|   P01   |   O administrador clica no botão de cadastrar produto   |        FB - P01        |
|   P02   |   O administrador seleciona a categoria do produto a ser adicionado   |        FB - P02         |
|   P03   |   O administrador visualiza os produtos já contidos dentro da categoria selecionada   |        FB - P03         |
|   P04   |   O administrador insere nos campos disponíveis as informações referentes ao produto que será cadastrado, tais elas o valor, as espeficicações, o suporte para outras categorias, quantidade de estoque e seu nome  |     FB - P04             |
|   P05   |   O administrador confirma as informações inseridas |     FB - P05      |
|   P06   |   O administrador recebe uma mensagem informando que o produto que está sendo inserido já existe na base de dados da plataforma   |        RN01        |

## FE02 - Informações incompletas do produto

| Passo | Descrição | Referência |
|:----:|:----:|:----------------:|
|   P01   |   O administrador clica no botão de cadastrar produto   |         FB - P01         |
|   P02   |   O administrador seleciona a categoria do produto a ser adicionado   |        FB - P02          |
|   P03   |   O administrador visualiza os produtos já contidos dentro da categoria selecionada   |         FB - P03         |
|   P04   |   O administrador insere em parte dos campos disponíveis as informações referentes ao produto que será cadastrado   |        FB - P04          |
|   P05   |  O administrador confirma as informações inseridas    |        FB - P05          |
|   P06   |  O administrador recebe uma mensagem informando que existe a necessidade de todos os campos solicitados sejam preenchidos com alguma informação relevante sobre o produto   |       RN02       |

# 7. Pós-Condição
 <p align="justify"> &emsp;&emsp; O novo produto será cadastrado e estará disponível na loja virtual. </p>

# 8. Regras de negócio

| ID | Descrição | Passo do Fluxo Associado |
|:----:|:----:|:----------------:|
|   RN01   |  É necessário que o produto seja novo para a realização do cadastro, caso já exista será retornado uma mensagem de erro informando a cópia   |   FE01 - P06    |
|   RN02   |  É necessário que a listagem de informações de um produto, em seu cadastro, esteja completa, para assim validar o acréscimo de um novo produto    |     FE02 - P06     |
