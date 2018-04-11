|    Data    | Versão |                                         Modificação                                        |                Autor                |
|:----------:|:------:|:----------------------------------------------------------------------------------------:|:-----------------------------------:|
| 01/04/2018 | 1.0 | Estrutura básica do projeto | Lucas Malta |

# Plano de Gerência e configuração de software

## 1. Introdução
Neste documento, será descrito o planejamento dos principais itens relevantes em relação a Gerência de Configuração do Projeto, com o objetivo de apresentar as ferramentas utilizadas na configuração do projeto além dos padrões de organização e nomenclatura a serem utilizados.

## 2. Itens de configuração
Os itens de configuração desse projeto podem ser definidos como:
- Documentação - Arquivos textuais contendo descrições, definições e planejamentos a respeito do projeto, além de relatórios de reuniões e fluxos de projeto.
- Código - Artefato resultante da execução do projeto. São compostos por um conjunto de arquivos de textos distintos, que podem variar entre HTML, CSS e scripts no geral.

### 3. Ferramentas

| Ferramenta | Versão | Descrição |
|:----------:|:------:|:---------:|
| Ruby | 2.3.3 | Linguagem de programação utilizada para o projeto |
| Rails | 5.0.0.1 | Framework para o desenvolvimento do servidor/front do projeto|
| Docker | 3.0 | Aplicação utilizada para configuração de ambiente padrão|

### 4. Políticas

#### 4.1 Políticas de branches
O repositório conterá duas branches principais: master e development. A branch master será definida como a versão mais atualizada e estável do projeto, enquanto a development conterá funcionalidades já testadas, mas em estágio de revisão. Para o desenvolvimento de cada funcionalidade, uma branch nova deverá ser criada, e a mesma será integrada à development quando finalizada. O nome da branch deve conter a identificação da issue que remete a mesma. Ex: [cadastro-de-cliente-#9]()

 Nenhum integrante tem a permissão de realizar commits diretamente à master/development.

#### 4.2 Políticas de commits
Os commits devem ser atômicos, objetivando uma breve explicação sobre o que foi adicionado/removido/modificado. Mensagens sucintas e em inglês. Quando houver trabalho em conjunto (pairing/super pairing), evitar o uso do push force. Caso o mesmo seja necessário, verificar o motivo e avaliar com os integrantes trabalhando na mesma branch.

#### 4.3 Política de Pull requests
Todos os pull requests devem ser validados por ao menos dois integrantes que não participaram do desenvolvimento da funcionalidade. Além disso, é primordial que todas as funcionalidades estejam testadas e a build esteja passando. Após a aprovação, ocorre o merge entre a branch em questão com a development. Ao final da sprint, todas as mudanças da development testadas e estáveis passam para a master.

#### 4.5 Política de Issues
As issues do projeto focam em definir quais histórias de usuário existem, quais já foram/estão sendo/serão desenvolvidas. Elas também devem conter labels para melhor identificação das mesmas.
