|    Data    | Versão | Modificação | Autor |
|:----------:|:------:|:--:|:---------------:|
| 03/04/2018 | 1.0 | Inicializa o documento com a estrutura básica e completa | Guilherme Lacerda, Guilherme Augusto e Thalisson Melo |

# Sumário

>[1. Introdução](#1-introdução)

>[2. Legendas](#2-legendas)

>[3. Diagrama de Classes](#3-diagrama-de-classes)

# 1. Introdução

&emsp;&emsp; A Linguagem de modelagem unificada ajuda a modelar diversos subconjuntos de diagramas, incluindo diagramas de comportamento, diagramas de interação e diagramas de estrutura. Os diagramas de classe são um tipo de diagrama da estrutura porque descrevem o que deve estar presente no sistema a ser modelado.

&emsp;&emsp; O diagrama de classe é parte central da UML. Ele representa as principais finalidades da UML pois separa os elementos de design da codificação do sistema.

# 2. Legendas

&emsp;&emsp; Para a representação das classes, foi usado um retângulo (desenho semelhante a de uma tabela) com três campos. O primeiro campo aborda o nome da classe, descrito em _UpperCamelCase_. Logo em seguida, estão descritos os atributos pertecentes àquela classe, com seus respectivos tipos. Por último, são listados os métodos que irão compor a classe.

&emsp;&emsp; Tendo em vista que as classes possuem algumas relações, utilizamos da agregação, composição e da herança.

* <b>Agregação:</b> É um tipo especial de associação onde tenta-se demonstrar que as informações de um objeto (chamado objeto-todo) precisam ser complementados pelas informações contidas em um ou mais objetos de outra classe (chamados objetos-parte); conhecemos como todo/parte.

&emsp;&emsp; É uma relação forte, mas não tanto quanto a Composição. Pois a parte existe sem a parte/todo.

* <b>Composição:</b> A composição representa um vínculo forte entre duas classes, ou seja, uma classe FILHA só faz sentido se uma classe PAI existir. Se a classe PAI for apagada, a classe FILHA automaticamente deixará de existir.

* <b>Herança:</b> Um dos grandes diferenciais da programação orientada a objetos em relação a outros paradigmas de programação que também permitem a definição de estruturas e operações sobre essas estruturas estão no conceito de herança, mecanismo através do quais definições existentes podem ser facilmente estendidas.

# 3. Diagrama de Classes

![Diagrama de Classes](https://github.com/Desenho-1-2018-G-6/docs/blob/master/Diagrama_de_Classes/Diagrama%20de%20classe.jpg?raw=true)
