# Histórico de Revisão

|    Data    | Versão |        Descrição        |       Autor     |
|:----------:|:------:|:-----------------------:|:---------------:|
| 06/04/2018 |  1.0   |  Criação da primeira versão   | Ícaro Oliveira e Guilherme Lacerda |

# PSM
&emsp;&emsp; A abordagem Practical Software and Systems Measurement (PSM) tem como alvo especificar uma série de práticas, ferramentas e serviços.

&emsp;&emsp; O PSM possui dois fortes alicerces:

* Definição estrutural das medidas que serão utilizadas;
* Política de medição e análise.

A modelagem básica do processo PSM é: 

![](https://i.imgur.com/Yyx7Hzf.png)

&emsp;&emsp; Para tal, essa modelagem será inserida no contexto das filosofias ágeis adotadas neste projeto. Tornando-se uma atividade paralela ao desenvolvimento e, como benefício, preservando a sua natureza cíclica conforme descrita na modelagem acima.

&emsp;&emsp; Deve-se também notar que o processo de qualidade e análise de métricas deve conter características enxutas, uma vez que uma grande quantidade de dados pode levar à perda de escopo e lentidão no processo.

# Métricas e política de medição

&emsp;&emsp; Uma vez que as metodologias adotadas evocam à importância do código, tornando essenciais o cuidado com todas as suas características. 

&emsp;&emsp; Tamanho: serão adotadas três métricas essenciais: AMLOC, LOC e NOM. Em relação a complexidade, o sistema por ser feito em linguagem orientada à objeto, tem-se a necessidade da verificação de coesão e acoplamento entre classes, LCOM (coesão) e CBO (acoplamento).

&emsp;&emsp; A medição será feita ao final de cada sprint e caso os indicadores acusem baixa qualidade, será aberta uma issue a ser resolvida na sprint seguinte.

## Testes Unitários
&emsp;&emsp;Para a verificação de funcionamento a nível de métodos por cada classe, serão realizados testes unitários, com meta inicial de 85% de cobertura. 

## Testes Funcionais
&emsp;&emsp;Serão realizados ciclos constantes de testes funcionais, pela dupla designada a realizar as histórias designadas em cada sprint. Durante o desenvolvimento da história, não serão formalizados bugs via issue.
 
&emsp;&emsp;Ao encontrarem erros em histórias já finalizadas, deverá ser aberta uma Issue seguindo o template:

* **[US(XX)]** *{Breve descrição do bug}*

* *(Obrigatório)* **Descrição:** *{Deverá conter uma descrição mais detalhada do erro}*

* *(Obrigatório)* **Caminho:** *{Como reproduzir o erro}*

* *(Obrigatório)* **Gravidade:** *{Travamento, Alta, Média, Baixa, Melhoria}*

* *(Obrigatório)* **Prioridade:** *{Alta, Média, Baixa}*

* *(Opcional)* **Evidência:** *{prints da tela}*

&emsp;&emsp;Os erros de gravidade Travamento (onde não há possibilidade nem ao menos de acessar a funcionalidade) e Alta deverão ser classificados com prioridade Alta e resolvidos na mesma sprint. Erros de gravidade Média deverão ser classificados com prioridade Alta ou Média, a depender do caso. Erros de gravidade Baixa ou Melhoria deverão ter prioridade Baixa.

&emsp;&emsp;Os bugs assim relatados deverão ser designados para os membros do grupo levando em conta a prioridade, gravidade e disponibilidade da equipe naquela sprint. 

# Ferramentas
&emsp;&emsp;Para o monitoramento e coleta de métricas, será utilizado o CodeClimate.

## Processo do Gerenciamento de Qualidade
### Métricas
  <img src="https://github.com/fga-gpp-mds/2017.1-Trezentos/wiki/images/produto.png"/>

### Testes unitários
  <img src="https://i.imgur.com/VwNuNaW.png" width="600" height="300" />

### Verificação e Validação de Testes Funcionais
  <img src="https://i.imgur.com/1AO2nIu.png" width="800" height="400" />
