# Histórico de Revisão

|    Data    | Versão |                                         Modificação                                        |                Autor                |
|:----------:|:------:|:----------------------------------------------------------------------------------------:|:-----------------------------------:|
| 30/03/2018 | 1.0 | Adicionando estrutura do documento e preenchendo por completo | Guilherme Lacerda e Guilherme Augusto |

***

# Sumário

>[1. Descrição](#1-descrição)

>[2. Atores](#2-atores)

>[3. Pré-Condições](#3-pré-condições)

>[4. Fluxo Básico](#4-fluxo-básico)

>[5. Fluxo Alternativo](#5-fluxo-alternativo)

>[6. Fluxo de Exceção](#6-fluxo-de-exceção)
> * [6.1. FE01 - CEP inválido](#61-fe01---cep-inválido)

>[7. Pós-Condições](#7-pós-condição)

>[8. Regras de Negócio](#8-regras-de-negócio)

***

# 1. Descrição
 <p align="justify"> &emsp;&emsp; Este caso de uso a ação do cliente (usuário normal e cadastrado) ao finalizar uma compra de determinado conjunto de produtos.</p>

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
|   Ator(es) principa(is)   |   Usuário Normal e Usuário Cadastrado   |
| Ator secundário | Sistema |

# 3. Pré-Condições
&emsp;&emsp; O usuário deve entrar na plataforma <i>online</i> <i>(website)</i>, estar ter [realizado o login](https://github.com/Desenho-1-2018-G-6/docs/wiki/Realizar-Login) e ter [adicionado um ou mais produtos no carrinho](https://github.com/Desenho-1-2018-G-6/docs/wiki/Adicionar-Produto-no-Carrinho).

# 4. Fluxo Básico

| Passo | Descrição |
|:----:|:----:|
|   P01   |   O usuário deve finalizar a compra do(s) produto(s)   |
|   P02   |   O usuário deve escolher a forma de pagamento do(s) produto(s) |
|   P03   |   O usuário insere o CEP correspondente ao local de entrega do produto   |
|   P04   |   O usuário confirma o CEP   |
|   P05   |   O usuário clica no botão de finalizar o pagamento  |
|   P06   |   O usuário recebe uma mensagem de que a compra foi realizada com sucesso |

# 5. Fluxo Alternativo

Não se aplica.

# 6. Fluxo de Exceção

## FE01 - CEP inválido

| Passo | Descrição | Referência |
|:----:|:----:|:----------------:|
|   P01   |   O usuário deve finalizar a compra do(s) produto(s)   |  FB01 - P01  |
|   P02   |   O usuário deve escolher a forma de pagamento do(s) produto(s)   |  FB01 - P02  |
|   P03   |   O usuário insere o CEP correspondente ao local de entrega do produto   |   FB01 - P03   |
|   P04   |   O CEP fornecido não atende aos requisitos apontados pela regra de negócio correspondente |    RN01    |

# 7. Pós-Condição
 <p align="justify"> &emsp;&emsp; A compra é realizada com sucesso e os produtos são deduzidos do estoque. </p>

# 8. Regras de negócio

| ID | Descrição | Passo do Fluxo Associado |
|:----:|:----:|:----------------:|
|   RN01   |   O CEP deve conter exatamente 8 dígitos   |       FB01 - P03, FE01 - P04      |
