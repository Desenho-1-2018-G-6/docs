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

>[7. Pós-Condições](#7-pós-condição)

>[8. Regras de Negócio](#8-regras-de-negócio)

***

# 1. Descrição
 <p align="justify"> &emsp;&emsp; Este caso de uso representa a funcionalidade de excluir determinado produto, caso a loja virtual não trabalhe mais com ele.</p>

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
|   Ator principal   |   Administrador   |
|   Ator secundário   |   Sistema   |

# 3. Pré-Condições

&emsp;&emsp; O administrador deve acessar a plataforma <i>online</i> <i>(website)</i> e, previamente, ter feito o [cadastro do produto](https://github.com/Desenho-1-2018-G-6/docs/wiki/Cadastrar-Produto) que atualmente será excluído.

# 4. Fluxo Básico

| Passo | Descrição |
|:----:|:----:|
|   P01   |   O administrador seleciona a opção de excluir produto   |
|   P02   |   O administrador seleciona a categoria a qual o produto pertence   |
|   P03   |   O administrador seleciona o produto associado a categoria previamente selecionada   |
|   P04   |   O administrador pressiona o botão para excluir produto   |
|   P05   |   O administrador confirma a exclusão do produto   |
|   P06   |   O administrador recebe uma mensagem validando a ação de exclusão do produto   |

# 5. Fluxo Alternativo

| Passo | Descrição |
|:----:|:----:|
|   P01   |   O administrador realiza a busca de determinado produto   |
|   P02   |   O administrador visualiza a lista filtrada pela busca   |
|   P03   |   O administrador seleciona um produto da lista filtrada   |
|   P04   |   O administrador pressiona o botão para excluir produto   |
|   P05   |   O administrador confirma a exclusão do produto   |
|   P06   |   O administrador recebe uma mensagem validando a ação de exclusão do produto   |

# 6. Fluxo de Exceção

Não se aplica.

# 7. Pós-Condição
 <p align="justify"> &emsp;&emsp; O produto é excluído da lista de produtos disponíveis na loja virtual. </p>

# 8. Regras de negócio

Não se aplica.
