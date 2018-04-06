|    Data    | Versão | Modificação | Autor |
|:----------:|:------:|:-----------:|:-----:|
| 04/04/2018 | 1.0 | Estruturação básica e escrita do documento | Lucas Martins |
| 05/04/2018 | 1.1 | Escrita das descrições de _Features_ e _User Stories_ | Lucas Martins |
---

# Plano de Gerenciamento de Requisitos

## 1. Introdução

Este documento tem como objetivo descrever o processo de gerenciamento de requisitos do projeto. Nele será abordado desde a elicitação dos requisitos até sua documentação, passando por pontos como as técnicas selecionadas para a coleta e rastreabilidade.  

## 2. Elicitação de Requisitos

Uma das práticas mais importantes da Engenharia de Software é a atividade de Elicitação de Requisitos. A qual busca entender as necessidades do cliente e suas regras de negócio.

Não tratando simplesmente da prática de levantamento de requisitos, alguns profissionais utilizam o termo de elicitação, pois tratam também da identificação dos fatos que os compõem e os solucionando.

Para a execução desta fase adequadamente existem diversas estratégias bem definidas para elicitação de requisitos, propostas por vários autores. Cada uma destas técnicas oferece insumos úteis para a elicitação, porém algumas se adequam mais a determinados contextos que outras. Seguindo esse ponto de vista, a equipe selecionou as seguintes técnicas de elicitação:

* Observação Participativa
* _Brainstorming_

### 2.1. Observação Participativa

Aplicações de _e-commerce_ estão amplamente disponíveis no mercado, abordando diversos contextos e oportunidades de negócio. Isso resulta em um conjunto de requisitos, necessidades, ferramentas, funcionalidades e práticas bem definidas e conhecidas. Nesse contexto, entra a técnica de observação participativa, que é baseada no estudo e análise por imersão em outras plataformas concorrentes, realizados por um Engenheiro de _Software_. Assim, a equipe decidiu utilizar esta técnica para identificar o máximo de requisitos possíveis utilizando-se de base outros sites.

Deste modo, cada integrante do grupo ficará responsável por acessar plataformas que se assemelham com a ideia do projeto para que possa entender melhor o funcionamento do produto que entrará em fase de desenvolvimento.

Partindo da análise das funcionalidades, estudadas por cada membro do grupo, a equipe será capaz de compreender o contexto em que a plataforma será inserida do ponto de vista de um usuário, possibilitando o levantamento de requisitos suficientes para compor o projeto. Todas as funcionalidades utilizadas serão analisadas e algumas repensadas para melhor se adequar ao plano de negócio.


### 2.2. _Brainstorming_

A utilização do _Brainstorm_ nos auxiliará na identificação de requisitos e na tomada de algumas decisões importantes relacionadas ao projeto, sendo realizado em reuniões semanais com a presença de todo o grupo e, eventualmente, outros _stakeholders_.

O Brainstorm são reuniões em que participam todos os envolvidos no projeto. Todos os participantes devem expor suas ideias e necessidades em relação ao produto. Após a exposição das ideias, chega-se a hora de organizá-las e verificar realmente o que é importante para compor todo o projeto.

A escolha da técnica em questão se dá para a elicitação de requisitos iniciais e um pouco mais técnicos, os quais, a equipe de desenvolvimento irá focar no construção da plataforma.

No primeiro momento, a técnica será utilizada para compreender a oportunidade de negócio em que a aplicação se insere, listar os requisitos iniciais e decidir sobre quais ferramentas serão utilizadas para a construção do projeto, além de fornecer suporte para tomadas de decisão de gerência a partir de ideias provenientes dos membros do grupo.
O _brainstorm_ será aplicado logo após a finalização da técnica de observação participativa, deste modo todos os requisitos elicitados por cada membro na técnica citada anteriormente serão debatidos e analisados, considerando sua devida importância para a plataforma que irá ser construída.

## 3. Análise de Requisitos

Dentro do contexto do projeto os requisitos serão classificados em 7 níveis de rastreabilidade, sendo eles: **Problema**, **Necessidades**, **Características**, **Requisitos Funcionais e Não-Funcionais**, **Casos de Uso** (?), **Features** e, por fim, **User Stories**.

No contexto do projeto, a utilização de casos de uso serve como apoio para a criação de features e user stories, além de auxiliar na compreensão dos fluxos que o usuário irá encontrar na aplicação, o que será documentado utilizando a notação IStar.

## 4. Rastreabilidade de Requisitos

### 4.1. Rastreabilidade de Requisitos

A rastreabilidade serve para mapear um elemento do projeto com outros elementos correlatos. Para compreender a origem dos requisitos, eles serão organizados com os níveis e atributos descritos nas subseções a seguir.

#### 4.1.1. Atributos de Requisitos

Para controlar as informações associadas a um item de rastreabilidade são usados os atributos de requisitos. Os atributos que serão usados no projeto são:

* **Risco**
* **Benefício**
* **Esforço**
* **Estabilidade**
* **Impacto na Arquitetura**

Estes atributos são utilizados para definir os requisitos em cada um dos níveis de rastreabilidade.

#### 4.1.2. Níveis de Rastreabilidade

##### 4.1.2.1. Problema

Dentro do contexto do projeto, os Problemas são o nível mais alto de requisito. Os Problemas geralmente descrevem um contexto indesejado que levou à demanda de uma solução de software. Sua documentação deve conter os seguintes campos:

* **Identificador**: deve-se usar a sigla **PB + número** do requisito de acordo com a sequência crescente dos identificadores.

```
PB n
```

* **Nome**: nome do requisito;
* **Descrição**: descrição do problema;
* **Impactos**: os impactos identificados no qual o problema causa se não for solucionado.

##### 4.1.2.2. Necessidades

As Necessidades são requisitos potenciais, que visam com a sua completude sanar um determinado problema. Sua documentação deve conter os seguintes campos:

* **Identificador**: deve-se usar a sigla **NE + número** do requisito de acordo com a sequência crescente dos identificadores.

```
NE n
```

* **Nome**: nome do requisito;
* **Descrição**: informação resumo da necessidade;
* **Contexto atual**: soluções atuais da necessidade;

##### 4.1.2.3. Características

A Característica é o requisito onde podem ser definidos os elementos e atributos que compõem uma solução de software, baseado nas necessidades a serem atendidas. Sua documentação deve conter os seguintes campos:

* **Identificador**: Deve-se usar a sigla **CA + número** do requisito de acordo com a sequência crescente dos identificadores.

```
CA n
```

* **Nome**: Nome do requisito;
* **Descrição**: Descrição do requisito;

##### 4.1.2.4. Requisitos Funcionais e Não-Funcionais

Os Requisitos Funcionais mapeiam as características do sistema em funcionalidades requeridas que derivarão ações a serem executadas, ou em atributos não funcionais que caracterizam o sistema. Sua documentação deve conter os seguintes campos:

* **Identificador**: Para identificação de Requisitos Funcionais deve-se usar a sigla **RF + número** do requisito de acordo com a sequência crescente dos identificadores. Para identificação de Requisitos Não-Funcionais deve-se usar a sigla **RNF + número** do requisito de acordo com a sequência crescente dos identificadores.

```
RE n
```

* **Nome**: Nome do requisito;
* **Descrição**: Descrição do requisito;

##### 4.1.2.5. Caso de Uso

Os Casos de Uso podem ser caracterizados dentro do sistema como ações a serem realizadas por um determinado Ator. A Documentação dos UC devem ser feitas da seguinte forma:

* **Identificador**: Deve-se usar a sigla **UC + número** do requisito de acordo com a sequência crescente dos identificadores.

```
UC n
```

* **Descrição**: Descrição do requisito; 
* **Ator Principal**
* **Condições**
    * *Pré-Condições*
    * *Pós-Condições*
* **Fluxo de Eventos**
    * Fluxo Básico
    * Fluxo Alternativo
    * Fluxo de Exceção

##### 4.1.2.6. _Features_

As _Features_ representam as funcionalidades que devem ser implementadas ao longo do desenvolvimento do produto. Elas agrupam _User Stories_ relacionadas, e devem conter os seguintes campos:

* **Identificador**: deve-se usar a sigla **FT + número** do requisito de acordo com a sequência crescente dos identificadores.

```
FT n
```

* **Nome**: nome da feature;
* **Descrição**: descrição da feature;

##### 4.1.2.7. _User Stories_

As _User Stories_ são o nível mais baixo da rastreabilidade neste projeto, e se referem às partes de uma _Feature_, auto-contidas, que abordam a funcionalidade do ponto de vista do usuário. Sua documentação deve conter os seguintes campos: 

* **Identificador**: deve-se usar a sigla **US + número** do requisito de acordo com a sequência crescente dos identificadores.

```
US n
```

* **Nome**: nome da User Story;
* **Critérios de Aceitação**: Descrição, utilizando “voz de usuário” dos critérios necessários para que a história seja considerada completa;
* **Prioridade**: Tipo de prioridade definida com o _framework_ MoSCoW;
* **Status**: Representa o andamento da US (To Do, Doing, Done, por exemplo).


#### 4.1.3. Matriz de Rastreabilidade de Requisitos

A organização dos requisitos da maneira citada anteriormente permite montar uma matriz de rastreabilidade sabendo a quais níveis superiores cada funcionalidade pertence. Um requisito pode ter relação hierárquica com mais de um requisito, ou seja, uma funcionalidade pode estar associado a mais de um requisito.

Há também a possibilidade de um requisito ter relação de dependência com outros requisitos, neste caso os requisitos mais prioritários devem ser implementados primeiro.

### 4.2. - NFR