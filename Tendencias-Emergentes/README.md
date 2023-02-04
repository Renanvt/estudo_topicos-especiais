# [👈 ](README.md)

[ Sistemas Distribuídos ](#sistemas-distribuídos)

[Arquitetura Orienta a Serviços - SOA](#arquitetura-orientada-a-serviço-soa)

[ Engenharia de Serviços ](#engenharia-de-serviços)

[Tendências Leves](#tendências-leves)

# Sistemas Distribuídos
A grande maioria dos grandes sistemas computacionais são **sistemas distribuídos**. 

Um **sistema distribuído** é um sistema que envolve vários computadores, diferente dos sistemas centralizados, em que todos os componentes do sistema executam em um único computador. 

Tanenbaum e Van Steen definem um sistema distribuído como sendo:

**"Um sistema distribuído é um conjunto de computadores independentes que se apresenta a seus usuários como um sistema único e coerente."** 

Essa definição tem vários aspectos importantes: 

- **Primeiro**:  um sistema distribuído consiste em componentes (isto é, computadores) autônomos. 

- **Segundo**: os usuários, sejam pessoas ou programas, acham que estão tratando com um único sistema. 


**Isto significa que, de um modo ou de outro, os componentes autônomos precisam colaborar e *como estabelecer essa colaboração* é o cerne do *desenvolvimento de sistemas distribuídos*** 

A definição de sistema distribuído para Coulouris et al (2013):

**Um sistema distribuído é aquele no qual os componentes localizados em computadores interligados em rede se comunicam e coordenam suas ações apenas passando mensagens.**

Essa definição nos leva a pensar de forma abrangente:

- Todos os sistemas com computadores interligados em rede podem ser distribuídos de maneira útil. 

- Se estão conectados por meio de uma rede, podem estar separados por qualquer distância, podendo estar em continentes separados, no mesmo edifício ou na mesma sala 

Podemos identificar as seguintes **vantagens** ao **utilizar a abordagem distribuída** de desenvolvimento de sistemas:

- **Compartilhamento de recursos**: um sistema distribuído permite o compartilhamento de recursos de hardware e software (impressoras), recursos de dados (como arquivos) e recursos com funcionalidade mais específica (como os mecanismos de busca).

- **Sistemas Abertos**: um sistema computacional é aberto quando ele pode ser estendido e reimplementado de várias maneiras. Um sistema distribuído pode ser ou não um sistema aberto. 

- **Concorrência**: serviços e aplicativos fornecem recursos que podem ser compartilhados pelos clientes em um sistema distribuído. Existe a possibilidade de que vários clientes tentem acessar um recurso compartilhado ao mesmo tempo.

- **Escalabilidade**: um sistema é descrito como escalável se permanece eficiente quando há um aumento significativo no número de recursos e no número de usuários.

- **Tratamento de Falhas**: as falhas em um sistema distribuído são parciais – isto é, alguns componentes falham, enquanto outros continuam funcionando. Portanto, o tratamento de falhas é particularmente difícil.

O **desejo de compartilhar recursos** é uma das principais motivação para se construir e usar **sistemas distribuídos** .

O termo “**recurso**” é bastante abstrato: caracteriza bem o conjunto de coisas que podem ser compartilhadas de maneira útil em um sistema de computadores interligados em rede, como: 
componentes de *hardware*, entidades definidas pelo *software*, como arquivos, bancos de dados e objetos de dados de todos os tipos. 

Os **sistemas distribuídos** são mais complexos e por isso difíceis de projetar, implementar e testar do que os sistemas centralizados

## Questões sobre Sistemas Distribuídos

**Complexidade**: surge porque é praticamente impossível ter um modelo de controle top-down desses sistemas. 

Pois muitas vezes, o sistema que fornece funcionalidades são sistemas independentes sem nenhuma autoridade sobre eles.

Portanto, essa é uma **imprevisibilidade** inerente à operação de sistemas distribuídos, a qual deve ser considerada pelo projetista do sistema.

Mas como lidar com esta imprevisibilidade? 
Devemos considerar nos sistemas distribuídos algumas questões mais importantes de projeto

Questões importantes de projeto:

![Imgur](https://i.imgur.com/9tm24Mv.png)

## Sistemas distribuídos abertos

São sistemas construídos de acordo com normas que são geralmente aceitas pela comunidade. 

Os componentes de qualquer fornecedor podem ser integrados ao sistema e podem interoperar com outros componentes do sistema. 

Os componentes de sistema devem ser desenvolvidos independentemente em qualquer linguagem de programação e, se estas estiverem em conformidade com as normas, funcionarão com outros componentes

## Modelos de Interação
 
Em um sistema distribuído existem dois tipos fundamentais de interação que podem ocorrer: 

- Interação procedural 
- Interação baseada em mensagens
 
**Interação procedural**: envolve um computador que chama um serviço conhecido oferecido por algum outro computador e (normalmente) esperando que esse serviço seja fornecido. 

![Imgur](https://i.imgur.com/Qb6v1JA.png)

**Interação baseada em mensagens**: envolve o computador ‘que envia’ que define as informações sobre o que é requerido em uma mensagem, que são enviadas para outro computador

![Imgur](https://i.imgur.com/yXyR1Qe.png)
Interação baseada em mensagens entre um garçom e o pessoal da cozinha 

## Middleware

Os componentes em um sistema distribuído podem ser implementados em diferentes linguagens de programação e podem ser executados em diferentes tipos de processador. 

Um sistema distribuído requer um software que possa gerenciar essas diversas partes e assegurar que elas podem se comunicar e trocar dados. 

O termo ‘**middleware**’ é usado para se referir a esse software — ele fica no meio, entre os componentes distribuídos do sistema. 

O **middleware** é implementado como um conjunto de bibliotecas que é instalado em cada computador distribuído, além de um sistema de run-time para gerenciar a comunicação.

É um software de uso geral geralmente comprado no mercado e que não é escrito especialmente por desenvolvedores de aplicações. 

**Exemplos de middleware**:

- Software para Gerenciamento de Comunicações com Bancos de Dados
- Gerenciadores de Transações
- Conversores de Dados
- Controladores de Comunicação


Middleware em um Sistema Distribuído 

![Imgur](https://i.imgur.com/ahfzcJm.png)

O middleware costuma fornecer dois tipos distintos de suporte em um sistema distribuído:

![Imgur](https://i.imgur.com/i15tewz.png)

## Padrões de arquitetura para sistemas distribuídos

Os projetistas de sistemas distribuídos precisam organizar seus projetos de sistema para encontrar um equilíbrio entre desempenho, confiança, proteção e capacidade de gerenciamento do sistema.  

Como não existe um modelo universal de organização de sistema distribuído surgiram vários padrões de arquitetura. 

Ao projetar um sistema distribuído, deve-se escolher um **padrão de arquitetura** que ofereça suporte aos requisitos não funcionais críticos de seu sistema.

Tem cinco **padrões de arquitetura** de sistemas distribuídos:
 

1. Arquitetura de mestre-escravo
2. Arquitetura cliente-servidor de duas camadas
3. Arquitetura cliente-servidor multicamadas 
4. Arquitetura distribuída de componentes
5. Arquitetura ponto-a-ponto

## 1. Arquitetura de mestre-escravo

Usadas em sistemas de tempo real em que tempos de resposta precisos de interação são requeridos e quando é importante cumprir os deadlines (prazos) de processamento. 

![Imgur](https://i.imgur.com/ChUi1rG.png)
Um sistema de gerenciamento de tráfego com uma arquitetura mestre-escravo . Fonte: Sommerville (2011)

## 2. Arquitetura cliente-servidor de duas camadas

Usada para sistemas cliente-servidor simples e em situações nas quais é importante centralizar o sistema por razões de proteção. Sistemas cliente-servidor tem a parte do sistema de aplicação que é executada no computador do usuário (o cliente) e tem a parte que é executada em um computador remoto (o servidor).  

![Imgur](https://i.imgur.com/qJnETB6.png)

Formas do Modelo de arquitetura cliente-servidor de duas camadas

![Imgur](https://i.imgur.com/GumxKqu.png)

## 3. Arquitetura cliente-servidor multicamadas

Usada quando existe um alto volume de transações a serem processadas pelo servidor. As diferentes camadas do sistema, apresentação, gerenciamento de dados, processamento de aplicação e banco de dados, são processos separados que podem ser executados em diferentes processadores.

![Imgur](https://i.imgur.com/0lGLua8.png)

## 4. Arquitetura distribuída de componentes

Usada quando recursos de diferentes sistemas e bancos de dados precisam ser combinados ou é usada como um modelo de implementação para sistemas cliente-servidor em várias camadas.

![Imgur](https://i.imgur.com/6cOfckU.png)

## 5. Arquitetura ponto-a-ponto 

Usada quando os clientes trocam informações localmente armazenadas e o papel do servidor é introduzir clientes uns aos outros.

![Imgur](https://i.imgur.com/yabDYPO.png)


- **Sistemas ponto-a-ponto (p2p - peer-to-peer)**: são sistemas descentralizados em que os processamentos  podem ser realizados por qualquer no na rede. 

Todo o sistema é projetado para aproveitar o poder computacional e o armazenamento disponível por meio de uma rede  potencialmente enorme de computadores.

Principal problema: questões de proteção e confiança. A comunicação ponto-a-ponto envolve abrir seu computador para direcionar as interações com outros pontos -> isso significa que esses sistemas poderiam, potencialmente, acessar qualquer um de seus recursos.

# [👆 TÓPICOS](#tópicos)


# Arquitetura Orientada a Serviço (SOA)

**Arquitetura Orientada a Serviço (SOA)**: são uma forma de desenvolvimento de sistemas distribuídos em que os componentes de sistema são serviços autônomos, executando em computadores geograficamente distribuídos. 

Os **serviços** são plataforma e implementados independentes de linguagem e da aplicação que o usa.  

Os sistemas de software podem ser construídos pela **composição de serviços locais** e **serviços externos** de provedores diferentes, com interação perfeita entre os serviços no sistema. 

Desde o surgimento do SOA, houve um **processo de padronização**: empresas de hardware e software estão comprometidas com esses padrões. 

O SOA não sofreu as incompatibilidades que costumam surgir com as inovações técnicas. 

![Imgur](https://i.imgur.com/gDQhYrg.png)

Padrões fundamentais criados para oferecer suporte aos Web Services.

**Os protocolos de Web Services**: cobrem todos os aspectos das SOA, desde os mecanismos básicos para troca de informações de serviço (SOAP) até os padrões de linguagem da programação. 

![Imgur](https://i.imgur.com/26qlhsP.png)

Os principais padrões para SOA de Web são:

![Imgur](https://i.imgur.com/Mxz6JNx.png)

- A arquitetura SOA são menos rígidas, onde as ligações de serviços podem mudar durante a sua execução. 

- Isso significa que uma versão diferente, mas equivalente, do serviço, pode ser executada em diferentes momentos. 

- Muitos sistemas são construídos exclusivamente para o uso de Web Services, e outros podem misturar os Web Services com componentes desenvolvidos localmente.

Como exemplo de como as aplicações que usam uma mistura de componentes e serviços podem ser organizadas. Considere o seguinte cenário: 

“Um **sistema de informações em um carro**  fornece aos motoristas informações sobre **clima, condições de trafego da estrada**, informações **locais**, e assim por diante. Ele é ligado ao radio do carro para que a informação seja entregue como um sinal em um canal de radio especifico. O carro é equipado com receptores GPS para descobrir sua posição, e, com base nessa posição, o sistema acessa uma gama de serviços de informação. Em seguida, as informações podem ser entregues na linguagem especificada pelo motorista”. 

Exemplo: sistema de informações de bordo baseado em serviços 

![Imgur](https://i.imgur.com/M00ufZm.png)

## Serviços como componentes reusáveis

- Um **serviço** pode ser definido como um componente de software de **baixo acoplamento, reusável**, que **encapsula** funcionalidade discreta, que pode ser distribuída e acessada por meio de programas.  

- O modelo de componentes é um conjunto de padrões associados com Web Services: pois os serviços são um desenvolvimento natural dos componentes de software.

Diferença entre um serviço e um componente: 

- Uma distinção fundamental entre um serviço e um componente de software, é que os **serviços devem ser independentes** e **fracamente acoplados**. 

- Os **serviços** se comunicam por meio de **troca de mensagens**, expressas em XML.  Essas **mensagens são distribuídas** usando protocolos-padrão de transporte de Internet (HTTP e TCP/IP). 

- Um **serviço** define o que precisa de outro serviço, definindo seus requisitos em uma mensagem e enviando-a a esse serviço. 

- O **serviço** passa a analisar a resposta para extrair as informações que são necessárias. 

Diferente dos componentes de software, os **serviços** não fazem uso de chamadas de procedimentos ou de métodos remotos para acessar a funcionalidade associada a outros serviços

Quando se usa um Web Service, precisa saber onde se encontra o serviço (sua URI – Uniform Resource Identifier) e os detalhes de sua interface. 

Estes **serviços** são descritos em uma descrição de serviço expressa em uma linguagem baseada em XML, chamada WSDL. 

A **especificação WSDL** define três aspectos de um Web Service: 

- O que faz o serviço.
- Como ele se comunica. 
- Onde o encontrar.

Aspectos de um Web Service:

![Imgur](https://i.imgur.com/E33YHNQ.png)

O modelo conceitual WSDL com os elementos de uma descrição de serviço, onde cada um é expresso em XML e pode ser fornecido em arquivos separados.

![Imgur](https://i.imgur.com/rPnau2J.png)

As partes da definição de serviço WSDL são:

![Imgur](https://i.imgur.com/2vdZioW.png)

A definição de **interface de serviço** não inclui quaisquer informações sobre a semântica do serviço ou suas características não funcionais, como desempenho e confiança e **isso é considerado um grande problema com WSDL ->**  pois ele é apenas uma simples descrição da assinatura de serviço, ou seja, somente as operações e seus parâmetros. 

**Planejar usar o serviço**:  necessário que se defina **o que o serviço** realmente vai fazer e **o que significa cada um dos diferentes campos** nas mensagens de entrada e saída. 

A **documentação** e os **nomes significativos** são importantes para que os leitores consigam compreender a funcionalidade oferecida do serviço.

# [👆 TÓPICOS](#tópicos)


# Engenharia de Serviços

A **Engenharia de Serviços** é o processo de desenvolvimento de serviços para reuso em aplicações orientadas a serviços.  

Os engenheiros de serviço precisam garantir que o serviço que vai ser oferecido represente uma abstração reusável que poderia ser usada em outros sistemas. 

A funcionalidade a ser projetada e desenvolvida deve ser útil e que assegure que o serviço seja robusto e confiável. 

O serviço deve ser documentado para que possa ser usado por outros usuários em potencial.

Temos três estágios lógicos no processo de Engenharia de Serviço:

![Imgur](https://i.imgur.com/g6Dth4I.png)

Processo de Engenharia de Serviços:

**Quando desenvolvemos um componente reusável**: podemos começar com um componente já existente e que já foi implementado e usado em outra aplicação. 

**Com o serviço é o mesmo**: podemos começar o processo com um serviço existente ou um componente que será convertido em um serviço.

![Imgur](https://i.imgur.com/6nbrjQ4.png)

- Os **serviços** devem **apoiar os processos de negócios**: as empresas possuem uma gama de processos com muitos serviços possíveis que podem ser implementados. 

- Para isso, é necessária a identificação de **serviço candidato**. 

- A **identificação de um serviço candidato**: envolve a compreensão e a análise dos processos de negócios da empresa. 

- **Após a análise**: passa-se a decidir quais serviços reusáveis podem ser implementados para dar suporte a esses processos da empresa.

- **Após a seleção dos serviços candidatos**: o próximo passo do processo de engenharia de serviço é projetar as interfaces de serviço. 

- **Depois de ter selecionado os serviços candidatos e projetado suas interfaces**: a fase final do processo de engenharia de serviço é a implementação de serviço. 

# [👆 TÓPICOS](#tópicos)


# Tendências Leves

Ao longo da história relativamente recente da Engenharia de Software muitos pesquisadores com a ajuda de profissionais desenvolveram **vários modelos de processo, métodos e ferramentas automatizadas** para apoiar a mudança na maneira como desenvolvemos software. 

Mas será que encontramos a "**solução mágica**" de desenvolver software grandes e complexos, sem confusão, enganos e atrasos? 

**Pela história**: ainda estamos buscando pela solução mágica.

**Novas tecnologias são introduzidas regularmente**: apresentadas como sendo a “solução” para muitos dos problemas que os engenheiros de software enfrentam e incorporadas nos projetos.

**Quando surgem novas tecnologias**: críticos do setor exageram na importância dessas **“novas” tecnologias de software**. 

Com isso os **especialistas de software** as adotam com entusiasmo, mas muitas vezes tendem a não produzir o resultado esperado, e, como consequência, a busca continua pela “solução”.

Mas quais seriam as **“grandes questões”** quando consideramos a **evolução da tecnologia?** 

Alguns desafios que enfrentamos ao tentarmos isolar tendências significativas em novas tecnologias:

- Que fatores determinam o sucesso de uma tendência?
- Qual é o ciclo de vida de uma tendência?
- Com que antecedência pode uma tendência bem-sucedida ser identificada?
- Quais os aspectos controláveis da evolução?

![Imgur](https://i.imgur.com/b0ZHQSN.png)

Evolução da tecnologia

- Já pensou em quão rápido uma tecnologia evolui? 

- Quando uma tecnologia bem-sucedida é introduzida: o conceito inicial transforma-se em um ciclo de vida da inovação razoavelmente previsível.

![Imgur](https://i.imgur.com/YVzgO0N.png)

O ciclo de vida da evolução da tecnologia possui as seguintes fases:
 
- **Avanço**: fase onde um problema é identificado e tentativas repetidas são realizadas em busca de uma solução viável.

- **Replicador**: fase onde o trabalho inicial de avançar é reproduzido e ganha um uso mais amplo.

- **Empirismo**: fase em que se leva à criação de regras que regem o uso da tecnologia.

- **Teoria**: fase onde o sucesso repetido leva a uma teoria de uso mais amplo. 

- **Automação**: fase onde são criadas as ferramentas de automatização.

- **Maturidade**: fase onde a tecnologia amadurece e passa a ser amplamente utilizada.

Muitas dessas **tendências tecnológicas nunca atingem a maturidade**. 

- A grande maioria das **tecnologias “promissoras”** no domínio da engenharia de software suscita um grande interesse por alguns anos e depois passa a ser usada por um grupo dedicado de usuários.

- Isso não significa que não tenham valor: mas que o caminho para o sucesso através da inovação é longo e difícil.

- Ao longo de suas carreiras, os **engenheiros de software enfrentam vários tipos de desafios**:   lidar com rápidas mudanças, incerteza e emergência, confiabilidade, diversidade e interdependência. 

**Mas, eles também passam por muitas oportunidades de fazer contribuições significativas a comunidade.**

**Gestão da Complexidade**: quando pensamos na **complexidade** que envolve o software, surgem algumas questões:

- Será que há uma maneira confiável de garantir que todas as conexões permitam que a informação flua adequadamente?

- Será que conseguimos gerenciar o fluxo de trabalho e ainda acompanhar o progresso?

- Será que há uma maneira de gerenciar e coordenar indivíduos que estão trabalhando em um projeto grande?

- Será que tem como analisar dezenas de milhares de requisitos, limitações e restrições de uma forma que garanta que todas as inconsistências e ambiguidades, omissões e erros sejam imediatamente encontrados e corrigidos?

- Será que tem como criar uma arquitetura de projeto que seja robusta o bastante para lidar com o sistema desse tamanho?

- Será que tem como os engenheiros de software estabelecer um sistema de controle de alterações que irá manipular centenas de milhares de alterações?

- Será que podemos realizar verificações e validações de modo significativo? Como testamos um sistema de 1 bilhão de linhas de código?

- O que acontecerá no futuro? Será que as abordagens atuais estarão a altura das tarefas a serem realizadas no futuro?
 
**Muitas dessas questões, somente no futuro poderão ser respondidas. **

## Software Aberto
 
Software aberto abrange inteligência ambiente, aplicações sensíveis ao contexto e computação generalizada. 

Software que é projeto para se adaptar a um ambiente que esteja em contínua mudança “auto organizando sua estrutura e auto adaptando seu comportamento.

## Requisitos emergentes

Em todo início de um projeto de software, há um levantamento de requisitos e uma análise com todos os envolvidos. 

Em muitos casos, os clientes raramente definem **requisitos “estáveis” no início do projeto**. 

Isto indica que os engenheiros de software não podem prever onde ocorrerão as ambiguidades e inconsistências do projeto. 

**Um fato comum a todos os projetos de software: os requisitos mudam.**


Para os softwares desenvolvido até hoje: a **fronteira** entre o sistema baseado em software e seu ambiente externo é **estável**.  

Mas para muitos da comunidade: esta **fronteira** pode **mudar**. 

**Esta mudança deve ocorrer de uma maneira controlada**: que permita que o software seja adaptado como parte de um ciclo de manutenção. 

Os **requisitos emergentes levam à mudança**, pela sua natureza.

**Como controlamos a evolução de um aplicativo ou sistema amplamente usado durante toda a sua vida útil?** 

**E que efeito isso tem sobre a maneira como projetamos software?**

- **Estas perguntas nos leva ao fato que**: conforme o número de alterações aumenta, a possibilidade de efeitos colaterais não desejados também aumenta. 

- Quando os sistemas complexos com requisitos emergentes se tornarem comum: isso será um grande motivo de preocupação. 

- Para isso, deve ser desenvolvido métodos e técnicas que ajudem a prever o impacto das mudanças neste sistema e com isso, moderando os efeitos colaterais indesejados.

## Mix de talentos

- E conforme o software fica mais complexo, a natureza de uma equipe de engenharia de software também muda. 

- As equipes se tornaram globais e a comunicações e colaboração e os requisitos emergentes (com o fluxo de mudanças resultantes) se tornarem a norma. 

- Cada equipe de software deve contribuir com talento criativo e habilidades técnicas para sua parte de um sistema complexo. 

- E o processo todo deve permitir que o resultado dessas ilhas de talento se combine efetivamente.

## Blocos básicos de software

Uma filosofia de Engenharia de Software é a necessidade de **reutilização** de código-fonte, de classes orientadas a objeto, de componentes e de padrões. 

Apesar de muitas **empresas terem feito progresso na tentativa de capturar conhecimento e reutilizar soluções aprovadas**:  ainda temos várias outras que continuam criar o software desde o início, pois acreditam no desejo de “**soluções únicas**”. 

Há também uma **tendência em adotar soluções de plataforma de software reutizavéis**:  que incorporam coleções de funcionalidades relacionadas, fornecidas em uma estrutura de software integrada.

## Rumos da tecnologia

Uma **tendência inegável**: os sistemas baseados em software sem dúvida se tornarão maiores e mais complexos com o passar do tempo. 

**Criar novas abordagens para lidar com esses sistemas**:  é um grande desafio para a engenharia de software


A seguir algumas características de sistemas que devem ser tratadas e consideradas pelos analistas e projetistas de engenharia de software para futuras aplicações:

![Imgur](https://i.imgur.com/k9zOutu.png)

![Imgur](https://i.imgur.com/zl7xhtd.png)

Para que essas e outras características do software possam ser gerenciadas: 

- Os analistas e projetistas devem desenvolver uma filosofia de engenharia de software distribuída e colaborativa mais eficaz.

- Melhores abordagens de requisitos de engenharia: uma abordagem mais robusta do desenvolvimento **motivado por modelo e melhores ferramentas de software.**

# [👆 TÓPICOS](#tópicos)































