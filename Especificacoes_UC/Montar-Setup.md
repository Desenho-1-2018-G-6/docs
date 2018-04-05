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

>[7. Pós-Condições](#7-pós-condição)

>[8. Regras de Negócio](#8-regras-de-negócio)

***

# 1. Descrição
 <p align="justify"> &emsp;&emsp; Este caso de uso permite com que o usuário monte o seu próprio produto final, escolhendo peças à sua escolha. Resultando em um produto completo no final. </p>

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
|   Ator Principal   |   Usuário e usuário cadastrado   |

# 3. Pré-Condições

&emsp;&emsp; O usuário tem que acessar a plataforma <i>online</i>.

# 4. Fluxo Básico

## FB01

| Passo | Descrição |
|:-----:|:---------:|
| P01 | O usuário deverá acessar a opção de "Montar Setup" |
| P02 | O usuário deverá escolher as peças obrigatórias com base nas categorias disponibilizadas |
| P03 | O usuário poderá escolher produtos opcionais ao seu gosto e que completemente o seu <i>setup</i> |
| P04 | O usuário poderá ver o orçamento total |
| P05 | O usuário clicará em finalizar <i>setup</i> |
| P06 | O sistema redirecionará para a [conclusão da compra](https://github.com/Desenho-1-2018-G-6/docs/wiki/Realizar-Compra) |

# 5. Fluxo Alternativo

&emsp;&emsp; Nao se aplica.


# 6. Fluxo de Exceção

| Passo | Descrição | Referência |
|:-----:|:---:|:----------------:|
| P01 | O usuário acessa a opção de "Montar Setup"  | FB01 - P01 |
| P02 | O usuário escolheu algumas peças obrigatórias com base nas categorias disponibilizadas | FB01 - P02 |
| P03 | O usuário poderá escolher produtos opcionais ao seu gosto e que complemente o seu <i>setup</i> | FB01 - P03 |
| P04 | O usuário poderá ver o orçamento total | FB01 - P04 |
| P05 | O usuário clicará em finalizar <i>setup</i> | FB01 - P05 |
| P06 | O sistema irá alertar o usuário de que ainda existem campos obrigatórios não escolhidos | - |

# 7. Pós-Condição
 &emsp;&emsp; O usuário conseguirá montar o próprio produto final com peças escolhidas a sua vontade, e conseguindo [efetuar a compra](https://github.com/Desenho-1-2018-G-6/docs/wiki/Realizar-Compra) no final do processo.

# 8. Regras de Negócio

| ID | Descrição | Passo do Fluxo Associado |
|:----:|:----:|:----------------:|
| RN01 | O usuário não poderá deixar nenhuma opção obrigatória sem ser escolhida | FB01 |
| RN02 | O usuário poderá escolher cada produto com um limite de quantidade de acordo com a [categoria do produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Categoria-de-Produto) | FB01 |
