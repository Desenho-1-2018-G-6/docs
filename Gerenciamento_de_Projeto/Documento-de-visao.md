|    Data    | Versão |                                         Modificação                                        |                Autor                |
|:----------:|:------:|:----------------------------------------------------------------------------------------:|:-----------------------------------:|
| 05/04/2018 | 1.0 | Versão Inicial | Ateldy Brasil |
| 05/04/2018 | 2.0 | Adicionando tabelas | Lucas Martins |

# Documento de Visão

## 1. Introdução

Este documento visa o entendimento geral do projeto, ao definir as necessidades para o desenvolvimento do Mamid, site de e-commerce para vendas de artigos de tecnologia, com a capacidade de auxílio ao usuário de construir seu próprio computador. As informações contidas neste documento são apresentadas em alto nível de abstração, de forma que a concepção sobre o sistema esteja clara para todos os envolvidos no projeto. 

## 2. Posicionamento
### 2.1 Descrição do Problema

<table class="tg">
  <tr>
    <th class="tg-yw4l">O problema de</td>
    <td class="tg-yw4l">adquirir de equipamentos eletrônicos</td>
  </tr>
  <tr>
    <th class="tg-yw4l">afeta</td>
    <td class="tg-yw4l">compradores interessados em produtos personalizados</td>
  </tr>
  <tr>
    <th class="tg-yw4l">cujo impacto é</td>
    <td class="tg-yw4l">a compra de equipamentos inadequados ou com o preço bem maior que o necessário</td>
  </tr>
  <tr>
    <th class="tg-yw4l">uma boa solução seria</td>
    <td class="tg-yw4l">fornecer uma plataforma que permita a compra de equipamentos eletrônicos somente com as especificações e características desejadas pelo comprador.</td>
  </tr>
</table>   

### 2.2 Sentença de Posição do Produto

<table class="tg">
  <tr>
    <th class="tg-yw4l">Para</td>
    <td class="tg-yw4l">Clientes de lojas de eletrônicos</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Que </td>
    <td class="tg-yw4l">querem comprar artigos de tecnologia</td>
  </tr>
  <tr>
    <th class="tg-yw4l">O Mamid</td>
    <td class="tg-yw4l">é um e-commerce</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Que</td>
    <td class="tg-yw4l">fornece a compra de um computador personalizado</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Ao contrário de </td>
    <td class="tg-yw4l">lojas de varejo</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Nosso Produto</td>
    <td class="tg-yw4l">oferece a montagem do produto on demand</td>
  </tr>
</table> 

## 3. Descrições dos Envolvidos e dos Usuários
### 3.1 Resumo dos Envolvidos

| Nome | Descrição | Responsabilidades |
|:--------:|:-------------:|:---------:|
| Equipe de Desenvolvimento | Equipe de alunos da UnB de Arquitetura e Desenho de Software | Planejar, desenvolver e implementar o sistema.|

### 3.2 Resumo dos Usuários

| Nome | Descrição | Responsabilidades | Envolvido |
|:--------:|:-------------:|:---------------------------:|:-------------:|
| Administrador | Administra os itens disponíveis do site | Disponibilizar itens para compra, preços do produto e quantidade em estoque | Dono do e-commerce |
| Usuário | Visitante do site que deseja efetuar uma compra ou consultar os produtos disponíveis | Navegar pelo site, visualizar os produtos, montar um produto e adicionar itens ao carrinho  | Potencial comprador |
| Cliente | Usuário cadastrado no site que pode efetuar uma compra | Os mesmos que o usuário além de realizar uma compra, escolher forma de pagamento e visualizar compras anteriores | Comprador de produtos do site |

### 3.3 Ambiente do Usuário
O Mamid é uma aplicação web que pode ser acessada e utilizada em navegadores como:

* Google Chrome
* Mozilla Firefox
* Microsoft Edge
* Safari
* Opera

## 4. Perfis dos envolvidos
### 4.1 Equipe de Desenvolvimento

<table class="tg">
  <tr>
    <th class="tg-yw4l">Representantes</th>
    <td class="tg-yw4l">André Bedran, Ateldy Brasil Filho, Guilherme Augusto, Guilherme Lacerda, Ícaro Oliveira, Lucas Malta, Lucas Martins, Thalisson Melo</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Descrição</th>
    <td class="tg-yw4l">Exercem o papel tanto de  engenheiros de requisitos quanto de desenvolvedores de software</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Tipo</td>
    <td class="tg-yw4l">Equipe de alunos da UnB de Arquitetura e Desenho de Software</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Responsabilidade</td>
    <td class="tg-yw4l">Coletar requisitos, idealizar, implementar e testar o software e suas funcionalidades</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Critérios de sucesso</td>
    <td class="tg-yw4l">Entregar um produto de software seguindo os padrões arquiteturais e de projeto propostos pela disciplina, além de sua documentação completa</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Envolvimento</td>
    <td class="tg-yw4l">Alto</td>
  </tr>
</table>

## 5. Perfis de Usuários
### 5.1 Administrador


<table class="tg">
  <tr>
    <th class="tg-yw4l">Representantes</th>
    <td class="tg-yw4l">Administrador do e-commerce</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Descrição</th>
    <td class="tg-yw4l">Empreendedores que possuem um e-commerce e desejam fornecer um sistema de compras de produtos personalizados ao seus clientes</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Tipo</td>
    <td class="tg-yw4l">Proprietários de lojas na modalidade e-commerce</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Responsabilidade</td>
    <td class="tg-yw4l">Administrar o sistema de e-commerce, seus produtos no que diz respeito à disponibilidade em estoque e preço e organização.</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Critérios de sucesso</td>
    <td class="tg-yw4l">Administrar um sistema de e-commerce rentável que forneça a funcionalidade de personalização dos produtos.</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Envolvimento</td>
    <td class="tg-yw4l">Alto</td>
  </tr>
</table>

### 5.2 Usuário

<table class="tg">
  <tr>
    <th class="tg-yw4l">Representantes</th>
    <td class="tg-yw4l">Usuários visitantes</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Descrição</th>
    <td class="tg-yw4l">Clientes em potencial que podem visualizar e adicionar itens ao carrinho</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Tipo</td>
    <td class="tg-yw4l">Visitantes do site</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Responsabilidade</td>
    <td class="tg-yw4l">Navegar na aplicação, visualizar os produtos, sua disponibilidade em estoque e preço, montar o produto desejado e adicioná-lo ao carrinho</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Critérios de sucesso</td>
    <td class="tg-yw4l">Navegar livremente no site e escolher quaisquer que sejam os produtos que lhe agrade</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Envolvimento</td>
    <td class="tg-yw4l">Alto</td>
  </tr>
</table>

### 5.3 Cliente

<table class="tg">
  <tr>
    <th class="tg-yw4l">Representantes</th>
    <td class="tg-yw4l">Clientes já cadastrados </td>
  </tr>
  <tr>
    <th class="tg-yw4l">Descrição</th>
    <td class="tg-yw4l">Usuário que deseja efetivar uma compra de produto, voltar a comprar após já ter adquirido um item na loja e visualizar suas compras anteriores</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Tipo</td>
    <td class="tg-yw4l">Usuário cadastrado na aplicação</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Responsabilidade</td>
    <td class="tg-yw4l">Todas as do Usuário, além de concretizar uma compra, escolher forma de pagamento, e visualizar compras anteriores</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Critérios de sucesso</td>
    <td class="tg-yw4l">Concretizar uma compra na aplicação e ser capaz de ver seu histórico de compras</td>
  </tr>
  <tr>
    <th class="tg-yw4l">Envolvimento</td>
    <td class="tg-yw4l">Alto</td>
  </tr>
</table>

## 6. Visão Geral do Produto
O site de comércio eletrônico fornecerá um produto customizável, no caso computadores. O site disponibiliza filtros de busca de produtos e forma de pagamentos para efetuar compras. O administrador terá um menu diferenciado para adicionar produtos e preços. O cliente só precisará se cadastrar na fase de compra.

## 7. Recursos do Produto
* Catálogo de produtos;
* Página para montar computador; 
* Página de pagamento;
* Página personalizada para administrador.

## 8. Outros Requisitos do Produto
### 8.1 Requisitos do Sistema
Por ser uma aplicação web, deverá ser acessada por navegadores de internet comuns, como Google Chrome, Mozilla Firefox, Microsoft Edge entre outros.

### 8.2 Requisitos de Portabilidade
O sistema deverá ser disponibilizado em formato de site, no qual será melhor acessado através dos navegadores como Google Chrome e Mozilla Firefox. A aplicação deverá ser acessível também por navegador móvel.

### 8.3 Requisitos de Design
O design deve ser projetado de forma atrativa ao usuário e que seja de fácil navegação, para que, dessa forma, atraia clientes.


