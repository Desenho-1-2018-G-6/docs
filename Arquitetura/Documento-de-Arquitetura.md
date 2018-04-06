|    Data    | Versão | Modificação | Autor |
|:----------:|:------:|:--:|:---------------:|
| 03/04/2018 | 1.0 | Inicializa o documento com a estrutura básica e completa | Guilherme Lacerda e Ícaro Oliveira |
------------------------------------
# Sumário

>[1. Introdução](#1-introdução)

>[2. Representação da Arquitetura](#2-representação-da-arquitetura)

>[3. Metas e Restrições de Arquitetura](#3-metas-e-restrições-de-arquitetura)

>[4. Visão e Casos de Uso](#4-visão-de-casos-de-uso)

>[5. Visão Lógica](#5-visão-lógica)

------------------------------------

# 1. Introdução

&emsp;&emsp; O objetivo desse documento é apresentar e detalhar a arquitetura que será utilizada na plataforma _Mamid_. Dessa maneira, visa-se atingir um entendimento mútuo entre os desenvolvedores do projeto, de forma que seja entendida a estrutura utilizada para desenvolver o _software_, além das consequências que a escolha de tal arquitetura implica.

## 1.1. Finalidade

&emsp;&emsp; Este documento visa estabelecer de forma clara as especificidades sobre as decisões arquiteturais para que as consequências diminuam os riscos e que todo o time consiga evoluir e manter o _software_. O desenvolvedor que ler esse documento obterá uma visão geral de como esse software está estruturado, assim como os casos de uso abordados.

## 1.2. Escopo

&emsp;&emsp; O _Mamid_ é uma plataforma projetada para a comercialização de artefatos de tecnologia. Ele busca auxiliar e facilitar na busca e na venda desses produtos.

&emsp;&emsp; Este documento especificará a arquitetura utilizada no projeto, visando uma padronização para as decisões que serão tomadas durante o desenvolvimento da plataforma, de forma a maximizar, assim, a objetividade do desenvolvimento.

&emsp;&emsp; O documento afetará toda a construção do programa: casos de uso e histórias de usuário, diagramas de classe, casos de teste, todo o prosseguimento do projeto tomará como base as arquiteturas aqui descritas.

# 2. Representação da Arquitetura
&emsp;&emsp; O modelo arquitetural adotado pelo _framework_ _Rails_, ou seja, _MVC_, consiste em três partes ou camadas: _Model_, _View_ e _Controller_.

&emsp;&emsp; 1. _MODEL_ : Contém dados ou informações sobre a aplicação, além do estado da mesma, juntamente com as regras do negócio, ou seja, representa os dados do sistema a partir de informações abstraídos do mundo real.;

&emsp;&emsp; 2. _VIEW_ : Interface da aplicação, renderizando formulários, páginas, informações, etc. É passiva, ou seja, não faz processamento lógico dos dados.

&emsp;&emsp; 3. _CONTROLLER_ : Realiza operações ou manipulações nos dados/informações interagindo com a _Model_ e interpretando os eventos realizados na _View_. Dessa maneira, essa camada é responsável por fazer a interação entre o usuário e o sistema.

![](https://i.stack.imgur.com/Sf2OQ.png)


# 3. Metas e Restrições de Arquitetura

&emsp;&emsp; Quanto as metas, pode-se dizer:

&emsp;&emsp;O _framework_ _Rails_ promove alguns princípios, sendo um deles _DRY_ ("_Don't Repeat Yourself_”) este sugere que o desenvolvedor não escreva o mesmo código diversas vezes, de maneira à minimizar o trabalho e a redundância no código, a aplicação _Mamid_ deve priorizar esse principio em sua arquitetura.

&emsp;&emsp; A aplicação _Mamid_ toma decisões arquiteturais baseadas no _REST, REST_(“Representational State Transfer”) é um apanhado de princípios que definem como os padrões da Web devem ser aplicados, tais como atribuir uma identidade (_ID_) a todas as classes, usar métodos padronizados, representação múltipla de recursos, etc.

&emsp;&emsp; O Rails valoriza _Convention Over Configuration_ isso permite que o tempo de desenvolvimento seja reduzido, com padrões para nomes de classes, etc. A aplicação tem como meta seguir as convenções arquiteturais do _framework rails_.

&emsp;&emsp; No que se refere a usabilidade, a proposta é que a aplicação seja intuitiva, de maneira que o usuário tenha facilidade ao usar o sistema.

&emsp;&emsp; Dentro de Segurança, objetiva-se que a aplicação deva oferecer certa segurança ao usuário quanto aos seus dados pessoais. Também é necessário que seja ofertado a persistência dos dados armazenados, bem como manter a integridade dos mesmos.

&emsp;&emsp; A arquitetura _MVC_ facilita a manutenibilidade de código, estabelecendo padrões, que possibilita a possível inclusão de novas funcionalidades e correções.

&emsp;&emsp;Objetiva-se que a aplicação deva ser capaz de rodar em diversas plataformas.

# 4. Visão de Casos de Uso e de História de Usuário

* [Especificações de Caso de Uso](https://github.com/Desenho-1-2018-G-6/docs/wiki/Especifica%C3%A7%C3%A3o-de-Caso-de-Uso)

* [User Stories](https://github.com/Desenho-1-2018-G-6/docs/wiki/User-Stories)

# 5. Visão Lógica

## 5.1 Visão Geral

&emsp;&emsp;O diagrama de pacotes do projeto é dividido da seguinte maneira:

![diagramadepacotes](https://user-images.githubusercontent.com/26297247/38399796-e874b962-3922-11e8-9b64-2f24b656d317.jpeg)

&emsp;&emsp;1 – _App_ : Nessa pasta está localizado o núcleo do projeto, englobando as pastas da _Model_, View e Controller.

&emsp;&emsp;2 – _DB_ : Nessa pasta esta localizado arquivos de configuração relacionados ao banco de dados alem das _migrations_ que são representações das tabelas.

&emsp;&emsp;3 – _Config_ : O foco dessa pasta é a configuração geral das aplicações. As rotas e o banco de dados utilizado são exemplos de configurações que essa pasta definem.

&emsp;&emsp;4 – _Test_ : Nessa pasta estão localizados os testes que serão realizados para a validação da plataforma. Os testes estão divididos de maneira que existem validações para os três núcleos do projeto, ou seja, a _MVC_(_Model – View – Controller_).

## 5.2. Pacotes de Design Significativos no Ponto de Vista da Arquitetura

### 5.2.1 _View_ (Visão)
&emsp;&emsp;É a parte visual do sistema onde acontece a interação do usuário com o sistema. Em rails ela inclui arquivos .html.erb que são templates que definem a forma como os dados serão exibidos para o usuário.

### 5.2.2 _Model_ (Modelo)
&emsp;&emsp;Essa pasta tem como objetivo a abstração das entidades do mundo real utilizadas na plataforma. Por exemplo, um usuário no Mamid deverá possuir inúmeros campos obrigatórios, como nome, CEP e e-mail. Dessa maneira, essa pasta é responsável por armazenar a definição de uma entidade que faz a representação desse membro no sistema. As _models_ também são responsáveis pela comunicação com o banco de dados.

### 5.2.3 _Controller_ (Controladora)
&emsp;&emsp;Essa pasta tem como objetivo fazer a conexão entre a _view_ e a _model_, de maneira que são utilizados métodos para fazer tal interação. Por exemplo, um _login_ é realizado na _view_, passando pelo método correspondente à tal ação na _controller_ e finalmente chegando até a _model_, que fará a conexão com o banco de dados. Por padrão, cada controladora tem o padrão "_controller_" no final do arquivo.

### 5.2.4 _Database_ (Banco de Dados)
&emsp;&emsp;O pacote _database_ tem o schema que é uma imagem do estado atual do banco, além de arquivos de configurações do banco. O pacote também _database_ contém as _migrations_, que controlam o versionamento do estado das tabelas do banco.

### 5.2.5 _Test_ (Teste)
&emsp;&emsp;Contém arquivos de teste que serão usados em todo programa para realizar testes de aplicação e de controles de aplicação, como por exemplo os testes no _login_ para ter certeza de que nenhum usuário será cadastrado incorretamente etc.
