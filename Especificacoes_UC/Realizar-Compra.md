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

 <p align="justify"> &emsp;&emsp;Permite com que o usuário consiga efetuar uma compra na plataforma.</p>

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
| Ator Principal | Usuário Cadastrado |
| Ator Secundário | Sistema |

# 3. Pré-Condições

<p align="justify"> &emsp;&emsp;O usuário deverá acessar a plataforma <i>online</i>.</p>

# 4. Fluxo Básico

## FB01 - Usuário não cadastrado

| Passo | Descrição |
|:----:|:----:|
|  P01  | O usuário irá [buscar por um produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Buscar-Produto) |
|  P02  | O usuário deverá [adicionar o produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Adicionar-Produto-no-Carrinho) pesquisa e desejado ao carrinho |
| P03 | O usuário deverá [acessar o carrinho](https://github.com/Desenho-1-2018-G-6/docs/wiki/Visualizar-Carrinho) |
| P04 | O usuário clicará no botão de finalizar compra |
| P05 | O sistema encaminhará o usuário para a tela de cadastro |
| P06 | O usuário [realizará o cadastro](https://github.com/Desenho-1-2018-G-6/docs/wiki/Realizar-Cadastro) |
| P07 | O usuário será redirecionado para a [tela de realização de pagamento](https://github.com/Desenho-1-2018-G-6/docs/wiki/Realizar-Pagamento) |
| P08 | O sistema irá validar todas as informações necessárias e processará a compra |

# 5. Fluxo Alternativo

## FA01 - Usuário já cadastrado

| Passo | Descrição |
|:----:|:----:|
|  P01  | O usuário irá [buscar por um produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Buscar-Produto) |
|  P02  | O usuário deverá [adicionar o produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Adicionar-Produto-no-Carrinho) pesquisa e desejado ao carrinho |
| P03 | O usuário deverá finalizar [acessar o carrinho](https://github.com/Desenho-1-2018-G-6/docs/wiki/Visualizar-Carrinho) |
| P04 | O usuário clicará no botão de finalizar compra |
| P05 | O usuário será redirecionado para a [tela de pagamento](https://github.com/Desenho-1-2018-G-6/docs/wiki/Realizar-Pagamento) |
| P06 | O sistema irá validar todas as informações necessárias e processará a compra |

## FA02 - Compra através da <i>home</i>

| Passo | Descrição |
|:----:|:----:|
|  P01  | O usuário visualizará o produto na <i>home</i> |
|  P02  | Caso seja usuário cadastrado, seguir o FA01 |
|  P03  | Caso seja usuário não cadastrado, seguir o FB01 |

# 6. Fluxo de Exceção

## FE01

| Passo | Descrição | Referência |
|:----:|:----:|:----------------:|
|  P01  | Realizará a compra através de alguns dos fluxos estabelecidos | FB01 ou FA01 ou FA02 |
|  P02  | O pagamento não foi processado pela operadora do cartão de crédito | - |
|  P03  | O sistema irá notificá-lo de que não conseguiu processar o pedido | - |

# 7. Pós-Condição
 <p align="justify"> &emsp;&emsp; O usuário conseguirá efetuar a compra e acompanhar o pedido através dos seus pedidos.</p>


# 8. Regras de negócio

<p align="justify"> &emsp;&emsp;Não se aplica.</p>
