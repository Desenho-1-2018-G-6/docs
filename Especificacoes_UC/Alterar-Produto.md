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
> * [5.1. FA01 - Editar preço pela pesquisa do produto](#51-fa01---editar-preço-pela-pesquisa-do-produto)

>[6. Fluxo de Exceção](#6-fluxo-de-exceção)
> * [6.1. FE01 - Deixar o campo do preço vazio](#61-fe01---deixar-o-campo-do-preço-vazio)
> * [6.2. FE02 - Deixar o campo das especificações vazio](#62-fe02---deixar-o-campo-das-especificações-vazio)
> * [6.3. FE03 - Deixar o campo do nome do produto vazio](#63-fe03---deixar-o-campo-do-nome-do-produto-vazio)

>[7. Pós-Condições](#7-pós-condição)

>[8. Regras de Negócio](#8-regras-de-negócio)

***

# 1. Descrição
<p align="justify"> &emsp;&emsp; Este caso de uso representa a ação do administrador alterar as informações dos produtos disponíveis na loja. </p>

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
|   Ator principal   |   Administrador   |
|   Ator secundário  |      Sistema      |

# 3. Pré-Condições
&emsp;&emsp; O usuário deve acessar a plataforma <i>online</i> (<i>website</i>) como um administrador, para obter privilégios para alterar os preços dos produtos já contidos dentro da loja virtual, tendo também os novos valores dos produtos em mãos, além de alterar outras informações contidas no [cadastro do produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Produto).

# 4. Fluxo Básico

| Passo | Descrição |
|:----:|:----:|
|   P01   |   O administrador clica na opção para alterar dados de um produto  |
|   P02   |   O administrador escolhe a categoria do produto a ser editado |
|   P03   |   O administrador escolhe o produto a ser editado   |
|   P04   |   O administrador altera as informações do produto   |
|   P05   |   O administrador confirma as novas informações do produto  |
|   P06   |   O administrador recebe uma mensagem informando-o que as informações do produto foram atualizadas |

# 5. Fluxo Alternativo

## FA01 - Editar preço pela pesquisa do produto

| Passo | Descrição |
|:----:|:----:|
|   P01   |   O administrador realiza a pesquisa de determinado produto   |
|   P02   |   O administrador seleciona o produto que se encontra na lista filtrada   |
|   P03   |   O administrador clica no botão de [alterar informações do produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Alterar-Produto)   |
|   P04   |   O administrador altera o preço do produto   |
|   P05   |   O administrador confirma o novo preço do produto  |
|   P06   |   O administrador recebe uma mensagem informando-o que o preço do produto foi atualizado |

# 6. Fluxo de Exceção

## FE01 - Deixar o campo do preço vazio

| Passo | Descrição | Referência |
|:----:|:----:|:----------------:|
|   P01   |   O administrador clica na opção para alterar dados de um produto   |       FB - P01 ou FA01 - P03         |
|   P02   |   O administrador escolhe a categoria do produto a ser editado |        FB - P02        |
|   P03   |   O administrador escolhe o produto a ser editado   |        FB - P03 ou FA01 - P02          |
|   P04   |   O administrador deixa o campo do preço do produto vazio    |         FB - P04 ou FA01 - P04         |
|   P05   |   O administrador confirma sem o novo preço do produto   |        FB - P05 ou FA01 - P05          |
|   P06   |   O administrador recebe uma mensagem informando a invalidade da ação de acordo com as regras de negócio   |         RN01         |

## FE02 - Deixar o campo das especificações vazio

| Passo | Descrição | Referência |
|:----:|:----:|:----------------:|
|   P01   |   O administrador clica na opção para alterar dados de um produto   |       FB - P01 ou FA01 - P03         |
|   P02   |   O administrador escolhe a categoria do produto a ser editado |        FB - P02        |
|   P03   |   O administrador escolhe o produto a ser editado   |         FB - P03 ou FA01 - P02         |
|   P04   |   O administrador deixa o campo de especificações vazio   |         FB - P04 ou FA01 - P04         |
|   P05   |   O administrador confirma com o campo de especificações vazio   |         FB - P05 ou FA01 - P05         |
|   P06   |   O administrador recebe uma mensagem informando a invalidade da ação de acordo com as regras de negócio   |         RN02         |

## FE03 - Deixar o campo do nome do produto vazio

| Passo | Descrição | Referência |
|:----:|:----:|:----------------:|
|   P01   |   O administrador clica na opção para alterar dados de um produto   |         FB - P01 ou FA01 - P03          |
|   P02   |   O administrador escolhe a categoria do produto a ser editado |        FB - P02        |
|   P03   |   O administrador escolhe o produto a ser editado   |         FB - P03 ou FA01 - P02         |
|   P04   |   O administrador deixa o campo do nome do produto vazio   |        FB - P04 ou FA01 - P04          |
|   P05   |   O administrador confirma com o campo do nome do produto vazio   |         FB - P05 ou FA01 - P05         |
|   P06   |   O administrador recebe uma mensagem informando a invalidade da ação de acordo com as regras de negócio   |        RN03          |

# 7. Pós-Condição
 <p align="justify"> &emsp;&emsp; As informações do produto serão atualizadas. </p>

# 8. Regras de negócio

| ID | Descrição | Passo do Fluxo Associado |
|:----:|:----:|:----------------:|
|   RN01   |   O preço deve ter um valor existente, sendo maior que 0 reais   |                  |
|   RN02   |   As espeficicações devem conter mais que 0 caracter e menos que 2000 caracteres   |                  |
|   RN03   |   O produto deve ter um nome com 1 à 50 caracteres  |                  |
