# Histórico de Revisão

|    Data    | Versão |                                         Modificação                                        |                Autor                |
|:----------:|:------:|:----------------------------------------------------------------------------------------:|:-----------------------------------:|
| 28/03/2018 | 1.0 | Adicionando estrutura do documento e preenchendo por completo | Guilherme Lacerda e Guilherme Augusto |
| 29/03/2018 | 1.1 | Conserta erro de markdown com relação a escrita em HTML | Guilherme Lacerda e Guilherme Augusto |

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
 <p align="justify"> &emsp;&emsp;Este caso de uso permite com que o usuário modifique e atualize os dados já cadastrados para futuras compras. </p>

# 2. Atores

| Tipo | Nome |
|:----:|:----:|
|   Ator Principal   | Usuário |
| Ator Secundário | Sistema |

# 3. Pré-Condições

&emsp;&emsp;O usuário precisa acessar a plataforma e ter [realizado o <i>login</i>](https://github.com/Desenho-1-2018-G-6/docs/wiki/Realizar-Login).  

# 4. Fluxo Básico

| Passo | Descrição |
|:----:|:----:|
| P01 | O usuário deve acessar o seu perfil |
| P02 | O usuário deve clicar na aba sobre suas informações |
| P03 | O usuário deve alterar as informações que acha necessária |
| P04 | O usuário clica em salvar alterações |
| P05 | O sistema atualiza as informações para futuras compras |

# 5. Fluxo Alternativo

<p align="justify"> &emsp;&emsp;Não se aplica. </p>


# 6. Fluxo de Exceção

| Passo | Descrição | Referência |
|:----:|:----:|:----------------:|
|   P01   |   O usuário clica sem propósito na aba sobre suas informações   | FB01 - P02 |
| P02 | A interface disponibiliza meio para que possa retornar para o perfil | - |
| P03 | O usuário clica na opção de voltar | - |
| P04 | O usuário agora encontra-se no seu perfil | - |

# 7. Pós-Condição
 <p align="justify"> &emsp;&emsp;As próximas compras realizadas pelo usuário utilizaram dos seus dados atualizados. </p>

# 8. Regras de negócio

&emsp;&emsp;Aplicam-se as mesmas regras de negócio do [Realizar Cadastro](https://github.com/Desenho-1-2018-G-6/docs/wiki/Realizar-Cadastro) e [Realizar Login](https://github.com/Desenho-1-2018-G-6/docs/wiki/Realizar-Login).
