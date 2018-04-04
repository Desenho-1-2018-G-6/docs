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

> * [4.1. FB01 - Realizar o cadastro antes da compra](#41-fb01-realizar-o-cadastro-antes-da-compra)   

> * [4.2. FB02 - Realizar o cadastro no momento da compra](#42-fb02-realizar-o-cadastro-no-momento-da-compra)    

>[5. Fluxo Alternativo](#5-fluxo-alternativo)

>[6. Fluxo de Exceção](#6-fluxo-de-exceção)

> * [6.1. FE01 - E-mail inválido](#61-e-mail-inválido)   

> * [6.2. FE02 - Nome inválido](#62-nome-inválido)    

> * [6.3. FE03 - CPF inválido](#63-cpf-inválido)     

> * [6.4. FE04 - Telefone inválido](#64-telefone-inválido)    

> * [6.5. FE05 - Senha inválida](#65-senha-inválida)     

> * [6.6. FE06 - Confirmação de senha incorreta ](#66-confirmação-de-senha-incorreta)    

>[7. Pós-Condições](#7-pós-condição)

>[8. Regras de Negócio](#8-regras-de-negócio)

***

# 1. Descrição
<p align="justify"> &emsp;&emsp; Este caso de uso representa a realização do cadastro dos clientes, permitindo o acesso de todas as funcionalidades de um usuário comum, incluindo a realização do pagamento e a consulta do pedido feito. </p>

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
|   Ator principal   |   Usuário   |
|   Ator secundário   |   Sistema   |

# 3. Pré-Condições

&emsp;&emsp; O usuário deve acessar a plataforma online (website) como um administrador, para obter privilégios para [atualizar estoque](https://github.com/Desenho-1-2018-G-6/docs/wiki/Atualizar-Estoque), [cadastrar produtos](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Produtos) e [cadastrar categoria de um produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Categoria-de-Produto).

# 4. Fluxo Básico

## FB01 - Realizar o cadastro antes da compra

| Passo | Descrição |
|:----:|:----:|
| P01 | O usuário clica na opção cadastrar |
| P02 | O usuário preenche os dados nos campos indicados |
| P03 | O usuário concorda com a política de privacidade da plataforma |
| P04 | O usuário seleciona o botão de confirmação  |


## FB02 - Realizar o cadastro no momento da compra

| Passo | Descrição |
|:----:|:----:|
| P01 | O usuário monta o carrinho de produtos |
| P02 | O usuário conclui a compra do(s) produto(s) |
| P03 | O usuário preenche os dados nos campos indicados |
| P04 | O usuário concorda com a política de privacidade da plataforma |
| P05 | O usuário seleciona o botão de confirmação |

# 5. Fluxo Alternativo

Não se aplica.

# 6. Fluxo de Exceção

## FE01 - E-mail inválido

| Passo | Descrição | Referência |
|:----:|:----:|:----:|
| P01 | O usuário clica na opção cadastrar | FB01 - P01 ou FB02 - P02 |
| P02 | O usuário insere um e-mail fora dos padrões definidos na regra de negócio | FB01 - P02 ou FB02 - P03, RN01 |
| P03 | O usuário recebe uma mensagem informando a invalidade do e-mail | RN01 |

## FE02 - Nome inválido

| Passo | Descrição | Referência |
|:----:|:----:|:----:|
| P01 | O usuário clica na opção cadastrar | FB01 - P01 ou FB02 - P02 |
| P02 | O usuário insere um nome fora dos padrões definidos na regra de negócio | FB01 - P02 ou FB02 - P03, RN02 |
| P03 | O usuário recebe uma mensagem informando a invalidade do nome | RN02 |

## FE03 - CPF inválido

| Passo | Descrição | Referência |
|:----:|:----:|:----:|
| P01 | O usuário clica na opção cadastrar | FB01 - P01 ou FB02 - P02 |
| P02 | O usuário insere um CPF fora dos padrões definidos na regra de negócio | FB01 - P02 ou FB02 - P03, RN03 |
| P03 | O usuário recebe uma mensagem informando a invalidade do CPF | RN03 |

## FE04 - Telefone inválido

| Passo | Descrição | Referência |
|:----:|:----:|:----:|
| P01 | O usuário clica na opção cadastrar | FB01 - P01 ou FB02 - P02 |
| P02 | O usuário insere um telefone fora dos padrões definidos na regra de negócio | FB01 - P02 ou FB02 - P03, RN04 |
| P03 | O usuário recebe uma mensagem informando a invalidade do telefone | RN04 |

## FE05 - Senha inválida

| Passo | Descrição | Referência |
|:----:|:----:|:----:|
| P01 | O usuário clica na opção cadastrar | FB01 - P01 ou FB02 - P02 |
| P02 | O usuário insere uma senha fora dos padrões definidos na regra de negócio | FB01 - P02 ou FB02 - P03, RN05 |
| P03 | O usuário recebe uma mensagem informando a invalidade da senha | RN05 |

## FE06 - Confirmação de senha incorreta

| Passo | Descrição | Referência |
|:----:|:----:|:----:|
| P01 | O usuário clica na opção cadastrar | FB01 - P01 ou FB02 - P02 |
| P02 | O usuário insere a confirmação de senha de forma diferente da inserida no campo de criação de senha, ferindo o padrão definido na regra de negócio | FB01 - P02 ou FB02 - P03, RN06 |
| P03 | O usuário recebe uma mensagem informando a invalidade da confirmação da senha | RN06 |

# 7. Pós-Condição
 <p align="justify"> &emsp;&emsp; O usuário cria uma conta na plataforma online com todas as informações solicitadas no processo de cadastro. </p>

# 8. Regras de negócio

| ID | Descrição | Passo do fluxo associado |
|:----:|:----:|:----:|
| RN01 | Utilizar o modelo básico de email: example@domínio | FB01 - P02 ou FB02 - P03 |
| RN02 | Não utilizar caracteres especiais (como ponto, vírgula, hífen, número, símbolos matemáticos entre outros) | FB01 - P02 ou FB02 - P03 |
| RN03 | Utilizar o modelo padrão de CPF, contendo 11 dígitos | FB01 - P02 ou FB02 - P03 |
| RN04 | Senha padronizada com um campo de texto com no mínimo 6 caracteres e no máximo 16 | FB01 - P02 ou FB02 - P03 |
| RN05 | Confirmação de senha padronizada com um campo de texto contendo exatamente a mesma senha digitada no campo senha | FB01 - P02 ou FB02 - P03 |
