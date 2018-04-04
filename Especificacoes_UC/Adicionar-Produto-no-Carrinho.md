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

> * [4.1. FB01 - Adiciona produtos realizando busca](#41-fb01---adiciona-produtos-realizando-busca)

>[5. Fluxo Alternativo](#5-fluxo-alternativo)

> * [5.1. FA01 - Adiciona produto sem realizar busca](#51-fa01---adiciona-produto-sem-realizar-busca)

>[6. Fluxo de Exceção](#6-fluxo-de-exceção)

> * [6.1 FE01 - Produto indisponível](#61-fe01---produto-indisponível)

>[7. Pós-Condições](#7-pós-condição)

>[8. Regras de Negócio](#8-regras-de-negócio)

***

# 1. Descrição
&emsp;&emsp; Este caso de uso representa a opção do usuário normal e o usuário cadastrado adicionar produtos ao carrinho virtual de compras do site, podendo no fim [realizar a compra](https://github.com/Desenho-1-2018-G-6/docs/wiki/Realizar-Compra) dos itens contidos dentro dele.

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
|   Ator(es) principa(is)  |   Usuário normal e Usuário cadastrado   |
|   Ator secundário   |   Sistema   |

# 3. Pré-Condições
<p align="justify"> &emsp;&emsp; O usuário deve acessar a plataforma online (website). </p>

# 4. Fluxo Básico

## FB01 - Adiciona produtos realizando busca

| Passo | Descrição |
|:----:|:----:|
| P01 | O usuário digita o produto de desejo na barra de pesquisa |
| P02 | O usuário clica no botão de confirmar para realizar a busca do produto |
| P03 | O usuário seleciona um item filtrado pela busca |
| P04 | O usuário adiciona o item selecionado ao carrinho |

# 5. Fluxo Alternativo

## FA01 - Adiciona produtos sem realizar busca

| Passo | Descrição |
|:----:|:----:|
| P01 | O usuário clica no item disponível no feed da página principal |
| P02 | O usuário adiciona o item selecionado ao carrinho |

# 6. Fluxo de Exceção

## FE01 - Produto indisponível

| Passo | Descrição | Referência |
|:----:|:----:|:----:|
| P01 | O usuário digita o produto de desejo na barra de pesquisa | FB01 - P01 |
| P02 | O usuário clica no botão de confirmar para realizar a busca do produto | FB01 - P02  |
| P03 | O usuário encontra o item indisponível para compra | RN01 |

# 7. Pós-Condição
 <p align="justify"> &emsp;&emsp; O usuário consegue adicionar o item desejado ao carrinho de compras. </p>

# 8. Regras de negócio

| ID | Descrição | Passo do Fluxo Associado |
|:----:|:----:|:----:|
| RN01 | O item só poderá ser adicionado ao carrinho se existir a quantidade suficiente ao solicitado pelo usuário | FA01 - P02 ou  FE01 - P03 |
