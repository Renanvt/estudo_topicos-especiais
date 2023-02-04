[👈 ](https://github.com/Renanvt/topicos-especiais)

# Tópicos

[ Refatoração ]( #refatoração)

# Refatoração

Uma **Refatoração** é uma transformação que preserva comportamento.

Uma **Refatoração** é uma alteração feita na estrutura interna do software para torná-lo mais fácil de ser entendido e menos custoso de ser modificado sem alterar seu comportamento observável.

**Refatoração** é a mudança de um código fonte, na estrutura interna do software, visando melhorar o entendimento e a manutenibilidade sem alterar seu comportamento e suas funções externas. 

A **Refatoração** surgiu quando alguns desenvolvedores foram analisar seus códigos para alterar ou incluir novas funcionalidades, e notaram que os códigos já existentes estavam em grande parte desestruturados, trechos repetidos e de difícil compreensão e manutenção.

Razões para refatorar um código:

![Imgur](https://i.imgur.com/ffQDP0T.png)

### Código legível por humano
 
- Ao escrever códigos, devemos produzir um método que seja legível por humanos. 

- Para exemplificar, seguem dois códigos que produzem a mesma data:

![Imgur](https://i.imgur.com/1UPjOxu.png)


### Refatorar x Reescrever 

![Imgur](https://i.imgur.com/WlK55iW.png)

**Refatoração** é tornar o software mais fácil de entender e modificar. 

**Refatoração** não altera o comportamento observável do software. Esse ainda executa a mesma função de antes. Qualquer usuário, seja ele um usuário final ou outro programador, não é capaz de dizer que algo mudou


## Quando refatorar?

A refatoração pode surgir pode surgir em dois momentos:
 
- Para melhorar o código existente 
- Quando temos que jogar fora e começar do zero.

Três vezes você refatora: 

**Refatore quando acrescentar funções**
**Refatore quando precisar consertar uma falha**
**Refatore enquanto revisa o código**

## Refatoração – Maus Cheiros no código


O fato de você saber como a Refatoração funciona, não significa que sabe quando usá-la. 

Decidir quando parar a Refatoração é tão importante quanto saber a sua mecânica. 

Para isso, temos um **catálogo de “maus cheiros”** -> para ser usado quando não estiver certo sobre a Refatoração a ser feita. 

Este **catálogo** ajuda a:
Identificar o que o desenvolvedor está sentido
Identificar e detectar o mau cheiro no código 
Apontar a direção certa, quando for realizar a Refatoração.

## Refatoração – Catálogo de Maus Cheiros no código

**Código duplicado mostrando desperdício**: se você vir o mesmo código em mais de um lugar, ele está duplicado e com certeza seu sistema ficará melhor se você encontrar um meio de unificá-los.

**Método longo**: quanto maior for o procedimento, mais difícil é entendê-lo. 

**Classe grande**: quando uma classe tenta fazer muita coisa, ela frequentemente tem variáveis de instância demais. 

**Lista de parâmetros longa**: se a lista de parâmetros for longa demais ou as alterações frequentes demais, você precisa repensar sua estrutura de dependência.

**Alteração divergente**: quando uma classe é frequentemente alterada de diferentes maneiras por diferentes razões.

**Cirurgia com rifle**: quando, cada vez que executa uma mudança, tem que fazer muitas alterações pequenas em muitas classes diferentes.

**Inveja dos dados**: um indício clássico de problema é um método que parece mais interessado em uma classe diferente daquela na qual ele se encontra. O foco mais comum da inveja são os dados. 

**Grupos de dados**: os dados tendem a ser como crianças gostam de ficar em grupos. Agrupamento de dados que perambulam juntos, na verdade, deveriam ser criados no seu próprio objeto.

**Comandos Switch**: um dos fenômenos mais óbvios do código orientado a objetos é sua comparativa falta de comandos switch (ou case). O problema com os comandos switch é essencialmente o da duplicação. 

**Hierarquias paralelas de herança**: cada vez que você cria uma subclasse de uma determinada classe, tem também que criar uma subclasse de outra. 

**Classe ociosa**: uma classe que não esteja fazendo o suficiente para se pagar deve ser eliminada

**Generalidade Especulativa**: pode ser identificada quando os únicos usuários de um método ou classe forma os casos de teste. 

**Campo Temporário**: às vezes você encontra um objeto no qual uma variável de instância recebe um valor apenas em determinadas circunstâncias. 

**Cadeias de Mensagens**: Você se depara com cadeias de mensagens quando um cliente pede um objeto para outro objeto, ao qual o cliente pede então outro objeto, ao qual o cliente pede então outro objeto e assim por diante. 

**Intermediário**: você olha uma interface de uma classe e descobre que metade dos métodos delegam para outra classe.

**Intimidade inadequada**: às vezes as classes se tornam íntimas demais e gastam tempo demais sondando as partes privadas das outras. Classes íntimas demais precisam ser separadas. 

**Herança recusada**: Subclasses conseguem herdar métodos e dados de seus pais, mas e se não quiserem ou precisarem do que lhes é dados? Elas recebem todos estes ótimos presentes e escolhem apenas alguns para brincar. Isso significa que a hierarquia está errada.

**Comentários**: não se preocupe, pode usar comentários no seu código, eles não cheiros ruins. São considerados cheiro doce, pois muitas vezes são usados como desodorantes. Pois é com muita frequência que se vê códigos cheios de comentários e percebe que eles estão lá porque o código é ruim.

**Refatoração** pode apresentar riscos se aplicada da forma errada, como:

- Atraso do projeto
- Introdução de falhas no sistema
- Tornar o código ilegível e não modificável. 

Portanto é uma **mudança que deve ser efetuada com cuidado.**

## Catálogo de Refatoração para Padrões

Segundo Fowler (2004, p. 95):

“Este catalogo não é de forma alguma completo ou fechado, mas deve **fornecer uma base solida** para o seu **próprio trabalho de refatoração**”.

- Vamos falar sobre o **formato de refatorações** criado por Fowler.

- **Formato de Refatorações**: trata-se de um formato padrão, em que cada refatoração representa cinco partes.

Formato das Refatorações:

![Imgur](https://i.imgur.com/zVezRui.png)

## Catálogo de Técnicas de Refatoração para Padrões


As técnicas de Refatoração, são diferentes padrões que se dividem em categorias:

- Compondo Métodos
- Movendo Recursos Entre Objetos
- Simplificando Expressões Condicionais
- Tornado as Chamadas de Métodos Mais Simples
- Organizando Dados
- Lidando com Generalização

**Compondo Métodos**: esta categoria agrupa técnicas que são utilizadas para a composição de métodos para empacotar códigos apropriadamente, ajudando a reduzir o acoplamento e a sua complexidade. 

![Imgur](https://i.imgur.com/PA0DnQX.png)

Exemplo Compondo Métodos -> Extrair Método: constitui-se em dividir o método grande em pequenos fragmentos. 

![Imgur](https://i.imgur.com/amVibv6.png)

**Movendo Recursos Entre Objetos**: uma das decisões mais fundamentais, no projeto orientado a objetos é onde colocar as responsabilidades”. E a refatoração é usada para redefinir essas decisões fundamentais. 

![Imgur](https://i.imgur.com/Il9rm1C.png)

**Movendo Recursos Entre Objetos -> Mover método**: se um método está usando ou sendo usado por mais recursos de outra classe do que a classe na qual ele está definido, **crie um novo método** com o corpo similar e transforme o método antigo em uma simples delegação ou remova completamente. 

![Imgur](https://i.imgur.com/vHmQSMl.png)


**Exemplo Movendo Recursos Entre Objetos -> Mover método**: se um método está usando ou sendo usado por mais recursos de outra classe do que a classe na qual ele está definido, **crie um novo método** com o corpo similar e transforme o método antigo em uma simples delegação ou remova completamente. 

![Imgur](https://i.imgur.com/Z8y1sRu.png)

**Exemplo Movendo Recursos Entre Objetos -> Extrair Classe**: se você tem uma classe fazendo um trabalho que deveria ser feito por duas, crie uma nova classe e mova os campos e métodos pertinentes da classe antiga para a nova. 

![Imgur](https://i.imgur.com/MsAdOcV.png)

**Simplificando Expressões Condicionais**: a lógica condicional pode ser refatorada e regra básica é "quebra” de uma expressão condicional em partes. Isso é importante porque separa a lógica variante dos detalhes do que ocorre.

![Imgur](https://i.imgur.com/fnNJttY.png)

**Exemplo Simplificando Expressões Condicionais -> Decompor condicional**: de uma estrutura condicional complicada (if-then-else), extraia métodos da condição, da parte após o then e da parte após o else.

![Imgur](https://i.imgur.com/Tpr2CO6.png)

**Tornado as Chamadas de Métodos Mais Simples**: este conjunto de refatorações explora a utilização da refatoração para tornar as interfaces mais diretas; produzindo interfaces que sejam mais fáceis de entender e usar.

![Imgur](https://i.imgur.com/fVFkS79.png)

**Exemplo Tornado as Chamadas de Métodos Mais Simples -> Renomear Método**: se você tem um nome de um método que não revela seu propósito, altere o nome do método.

![Imgur](https://i.imgur.com/QlhNqzb.png)

**Organizando Dados:**  é um conjunto de técnicas de refatorações que são extremamente úteis e que tornam mais fácil o tratamento de dados, utilizando linguagem de programação orientada a objetos, que podem permitir a definição de novos tipos que vão além do que pode ser feito com os tipos de dados simples das linguagens tradicionais.

![Imgur](https://i.imgur.com/pSKa10h.png)

**Exemplo Organizando Dados -> Auto-encapsular campo**: se você está acessando um campo diretamente, mas o acoplamento a esse campo está se tornando inadequado, então crie métodos de acesso ao campo e use apenas estes métodos para acessar o campo.

![Imgur](https://i.imgur.com/guNAW6S.png)

**Lidando com Generalização**: generalizações produzem seu próprio lote de refatorações, a maior parte delas lidando com a movimentação de métodos por uma hierarquia de herança.

![Imgur](https://i.imgur.com/qoiLXzF.png)

**Exemplo Lidando com Generalização -> Subir Campo na Hierarquia**: você tem duas subclasses que tem o mesmo campo, então mova o campo para a superclasse.

![Imgur](https://i.imgur.com/U7QDCHh.png)

# [👆 TÓPICOS](#tópicos)