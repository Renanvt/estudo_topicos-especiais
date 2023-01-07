# Tópicos

[Reutilização de Software](#reutilização-de-software)

[Reutilização de Componentes, Padrões e Frameworks](#reutilização-de-componentes-padrões-e-frameworks)

[Reutilização com Framework](#reutilização-com-frameworks)

[Engenharia de Software Baseada em Componentes](#engenharia-de-software-baseada-em-componentes)

[ A evolução da Reutilização de Software ](#a-evolução-da-reutilização-de-software)

# Reutilização de Software

Os desenvolvedores de software tem buscado por soluções que datam desde quando surgiu o termo Engenharia de Software.

Dentre as ideias estudadas: tem-se a **reutilização** de unidades de software resultantes da decomposição de software.

A noção de reutilização é antiga e teve inicio desde os tempos em que as pessoas começaram a encontrar soluções consistentes para problemas. 

**Qual a motivação?** 

Na ideia de que uma vez encontrada a solução, esta poderia ser aplicada a novos problemas.

Na literatura podemos encontrar várias definições para reuso. Vamos conhecer algumas delas:

**Reutilização** é o uso de qualquer informação disponível que um desenvolvedor pode necessitar no processo de criação de software (Freeman, 1987).

**Reutilização** é a capacidade de um item de software, previamente desenvolvido, ser usado novamente ou usado repetidamente em parte ou todo, com ou sem modificação (Cooper, 1994).

**Reutilização** de software é o processo de criar sistemas de software a partir de softwares existentes ao invés de construí-los do zero (Krueger, 1992).

**Evolução histórica**

![Imgur](https://i.imgur.com/c4p762E.png)

![Imgur](https://i.imgur.com/WbIpWYK.png)

## Vantagens e Desvantagens da Reutilização de Software
A mais óbvia: redução dos custos globais de desenvolvimento

![Imgur](https://i.imgur.com/0mTF5oH.png)

Dificuldades da Reutilização 

![Imgur](https://i.imgur.com/mCiGF4L.png)

Para uma efetiva reutilização, é importante que se atenda a alguns requisitos:

1. Existência de uma biblioteca (ou repositório de componentes) Ex.: component source, jars;

2. Garantia de que o componente se comportará conforme foi especificado e que serão confiáveis;

3. Existência de documentação que ajude a compreendê-los e adotá-los. 

# [👆 TÓPICOS](#tópicos)

# Reutilização de Componentes, Padrões e Frameworks

Uma vez que a **Reutilização** pode ocorrer em diferentes níveis de abstração, cabe apresentar a definição de componentes, padrões e frameworks  e e como pode ser visto a reutilização em cada um destes:

- Reutilização de Componentes

- Reutilização com Padrões de Projeto

- Reutilização com Frameworks

Um componente é uma unidade de software independente, que encapsula, dentro de si, seu projeto e implementação e oferece serviços, por meio de interfaces bem definidas para o meio externo.

- Interfaces de componentes

- Notação gráfica

- COTS (commercial off the shelf)

- Documentação de componentes

- Arquitetura de software

- Comentários interessantes sobre componentes

**Cada interface consiste**: serviços especificados, mediante uma ou mais operações, sendo cada uma delas separadamente identificadas e especificadas de acordo com seus parâmetros de entrada, saída e tipos estabelecidos. 

Essas definições constituem o que é conhecido como **assinatura da interface**.

As interfaces podem ser de dois tipos: 

- **Interfaces fornecidas** (provided interfaces) : definem os serviços oferecidos pelo componente por meio de operações.

- **Interfaces requeridas** (required interfaces): referem aos serviços que o componente necessita de outros componentes por meio da interface requerida de um com a interface fornecida de outro.

## Reutilização de Componentes - Interfaces

### Notação gráfica

Uso de notação UML (Unified Modeling Language) para pacotes e interfaces. 

A evolução da notação UML inseriu a representação de interfaces requeridas e providas conforme ilustra a figura 

-**Exemplo**:  componente **Pedido** que provê as interfaces **Alocação de Itens** e **Rastreamento**.  

- Por outro lado, **Pessoa, Fatura, Item Disponível** são interfaces requeridas.

![Imgur](https://i.imgur.com/bzuqOxc.png)

**COTS (Commercial Off-the-Shelf)**

- Além de projeto e especificação de componentes para aplicações organizacionais, existe também um interesse por **componentes comerciais** ou **componentes COTS** (commercial off the shelf). 

- Isto envolve pesquisas em formas de produzir, empacotar, regulamentar e selecionar componentes para produzir sistemas a partir de componentes comerciais existentes. 

- Em muitos sistemas construídos o **principal desafio** é utilizar o **máximo** de **componentes** comerciais de software.  
    Exemplos de componentes comerciais incluem: navegadores (Web Browsers), servidores HTTP, ORB, Middleware orientado a mensagens dentre outros.

**Reuso de produtos COTS**:  preocupado com o reuso de sistemas de prateleira em grande escala. 

**Fornecem uma grande funcionalidade**: reduzir, radicalmente, os custos e o tempo de desenvolvimento. 

Os sistemas podem ser desenvolvidos por meio da configuração de um único **produto genérico COTS ou integrando** dois ou mais produtos COTS. 

Os conhecidos sistemas ERP (Enterprise Resource Planning) são exemplos de reuso COTS em grande escala.

**Materialização de componentes prontos:** 
- Reutilização de componente já utilizado pela organização

- Aquisição de componentes a partir de catálogos de terceiros

## Reutilização com Padrões de Projeto

Inicialmente definir padrões de projeto para então entendermos a reutilização com padrões. 


**Definição**:

- Um **padrão** descreve um problema que ocorre repetidamente no nosso ambiente, descrevendo a essência de uma solução para este problema, de forma que pode-se usar esta solução milhares de vezes, sem fazê-lo da mesma forma duas vezes. (ALEXANDER et al.,  1977).

- Um **padrão** de software nomeia, motiva e explica uma solução genérica a um problema recorrente que surge em uma situação específica. Ele descreve o problema, a solução, quando é aplicável e quais as consequências de seu uso. (GAMMA et al., 2002, p. 395)

Os padrões, no contexto de desenvolvimento de software, são denominados **design patterns**. 

**Objetivo**: descrever soluções para problemas recorrentes no desenvolvimento de software. 

Com **design patterns** a busca é pelo reuso de solução e não apenas de código.

Os **design patterns** têm foco nas fases de projeto e implementação.  Também podem ser encontrados **padrões de análise** que são artefatos de alto nível.

Os seguintes **fatores** têm contribuído para **motivar o uso de design patterns** em projetos:

**Redução de tempo e custo** de desenvolvimento  consequentemente, aumentar a produtividade.
**Evitar falhas** (os componentes foram previamente testados).
**Interoperabilidade**: componentes de diferentes origens podem compartilhar e trocar informações.
Aumenta a possibilidade de **reutilização de boas soluções** para problemas frequentes.
Os padrões surgem com a **experiência prática**.
**Experiência de especialistas** pode ser **compartilhada com novatos**

Todo **design pattern** possui, basicamente,  os seguintes elementos:

- **Nome** [descreve a essência do padrão, deve ser curto e expressivo]
- **Problema** [descreve a intenção e objetivo]
- **Contexto** [define a configuração inicial, antes do padrão]
- **Forças** [destaca a motivação pelo seu uso]
- **Solução**
 	Estrutura [apresenta a organização estática do padrão]
  	Participantes [classes e objetos]
  	Dinâmica [define o comportamento]
 	Implementação
  	Variantes [apresenta especializações da solução]
- **Exemplos**
- **Contexto resultante**
- **Padrões relacionados**
- **Usos conhecidos**

Os padrões de projeto variam na sua granularidade e no seu nível de abstração. 

Existem muitos -> necessitamos de uma maneira de organizá-los.  A classificação ajuda a aprender os padrões mais rapidamente, bem como direcionar esforços na descoberta de novos.

Os padrões podem ter finalidade de criação, estrutural ou comportamental. 

- **Criação**: se preocupam com o processo de criação de objetos. 

- **Estruturais**: lidam com a composição de classes ou de objetos. 

- **Comportamentais**: caracterizam as maneiras pelas quais classes ou objetos interagem e distribuem responsabilidades.

**Catálogo de  Gof (Gang of four)**

A catalogação constitui-se em uma das primeiras iniciativas e foi estruturada de acordo com a finalidade e o escopo de cada um dos padrões.

![Imgur](https://i.imgur.com/fxbUtrz.png)

**Uma vez que você tem acesso a um conjunto de diversos padrões, vem a pergunta: como faço para usar  um padrão?** 

Algumas diretrizes que podem te ajudar a nortear o uso:

- **Leia** o **padrão por inteiro** (para obter uma visão geral).
- **Estude** as seções de descrição do **problema** e do **padrão**.
- **Olhe** exemplos de código do padrão.
- **Escolha** nomes para os participantes do padrão que tenham sentido no contexto da sua aplicação.
- **Defina** as classes.
- **Defina** nomes específicos da aplicação para as operações no padrão.
- **Implemente** as operações para apoiar as responsabilidades e colaborações presentes.

Além da classificação (Gof) -> temos uma **lista de padrões**, conhecida como **POSA** (Pattern oriented software architecture). 

Os padrões são agrupados conforme as seguintes categorias:

**Padrões arquiteturais**: expressam um esquema de organização estrutural e fundamental para um sistema. São conjuntos de subsistemas pré-definidos, especificando seus relacionamentos e as regras para a sua organização.

**Padrões de projeto**: refinam os subsistemas ou componentes de um sistema, descrevendo uma estrutura que constitui uma solução para um problema de projeto.

**Idioma**: são padrões específicos para uma linguagem de programação. Descrevem a forma de implementar um aspecto particular de um componente usando características de uma linguagem específica.

# [👆 TÓPICOS](#tópicos)

# Reutilização com Frameworks

Um **framework** é um conjunto cooperativo de classes que tornam um projeto reutilizável para uma classe específica de software. 

Um **framework** fornece uma orientação arquitetural através da divisão do projeto em classes abstratas e definindo as suas responsabilidades e colaborações. 
 
Para Martins (2005):

- **Framework**: projeto de um subsistema (ou arquitetura de software semi-definida) constituído de um conjunto de componentes individuais e das interconexões entre eles.

- **Frameworks** criam uma infraestrutura pré-fabricada para o desenvolvimento de aplicações de um domínio específico.

- Uma aplicação pode ser construída a partir da integração de vários **frameworks**.

Um framework podem ser identificados:

**Hot spots**: constituem-se em partes do framework que são projetados para serem genéricos e, podem ser adaptados às necessidades da aplicação.

**Frozen spots**: definem a arquitetura geral da aplicação, seus componentes e os relacionamentos entre eles. Eles permanecem fixos em todas as instanciações do framework.

Conforme o modo de estender um **framework** tem-se os seguintes tipos:

**Framework caixa branca**: usuários desenvolvem implementações para as classes abstratas fornecidas, que funcionam como *pontos adaptáveis*, bem como o código específico para a aplicação.

**Framework caixa preta**: contém todas as possíveis alternativas para todos os seus pontos adaptáveis. 

Os **frameworks** de aplicação são classificados de acordo com seu contexto da seguinte forma:

- **Framework de infraestrutura de sistema**: são frameworks utilizados como sistemas operacionais.

- **Frameworks de integração e comunicação (middleware)**: são frameworks utilizados para integrar aplicações e componentes distribuídos, como por exemplo os ORBs (Object Request Broker).

- **Framework de aplicações**: são frameworks que tem no domínio de aplicações. 

# [👆 TÓPICOS](#tópicos)

# Engenharia de Software Baseada em Componentes

O desenvolvimento de software baseado em reutilização é visto como um ciclo contínuo de aprendizagem influenciado por atividades da **Engenharia de domínio (ED)**.

**Objetivo da ED**: possibilita que *características comuns e variáveis* possam ser identificadas e modeladas com base em um processo previamente definido. 

Os **artefatos gerados pela ED** (modelos de domínio, arquiteturas de componentes, casos de uso, dentre outros) podem ser instanciados para uma aplicação específica do domínio. A esta instanciação se dá o nome de Engenharia de Aplicação (EA). 

- **ED provê um conjunto de artefatos “para” reutilização**

- **EA constrói aplicações “com” base na reutilização de artefatos providos pela ED**

Um conceito importante que surge é o que se refere a **Engenharia de Software Baseada em Componentes** (ESBC) ou component based software engineering (CBSE do inglês). 

**ESBC** é uma abordagem para desenvolvimento de sistemas de software com base no reuso de componentes.

Metodologias de Desenvolvimento Baseado em Componentes (DBC): 
- **UML Components**
- **Catalysis** 
- **Kobra** 

**UML Components**:  é constituído dos seguintes Workflows:
 
**Requirements Workflow** ( Workflow Requisitos)

São elaborados os seguintes modelos: 
- (i) **Modelo conceitual** das informações que existem no domínio do problema.
- (ii) **Diagrama com os tipos do negócio** (e seus relacionamentos) que precisam ser mantidos pelo software.
- (iii) **Diagrama de casos de uso** do software.

**UML Components**:  é constituído dos seguintes Workflows:
  
b) **Specification Workflow** (Workflow Especificação)

Tem como **entrada**: um modelo de caso de uso e um modelo conceitual de negócios vindos do workflow de requisitos. 

c) **Provisioning Workflow** ( Workflow  Provisão/Fornecimento)

 Determina quais componentes construir ou comprar.

d) **Assembly Workflow** (Workflow de Montagem)

- Deve ocorrer a correta composição dos componentes. 

- Coloca-se todos os componentes juntos com o software existente e uma adequada interface com o usuário para formar uma aplicação executável que vai ao encontro das necessidades de um negócio.
 
e)  **Test Workflow** (Workflow Teste)
 
f)   **Deployment Workflow** (Workflow Entrega)

## Catalysis 

método DBC que apresenta conceitos importantes para o desenvolvimento de software baseado em componentes. 

Cobre:  **todas as fases**, desde a **especificação** dos componentes até sua **implementação** para reutilização

- Busca **solucionar problemas**: elimina **gaps** entre as fases, estabelecer um **vocabulário comum**, **rastreamento** de requisitos, semântica para verificar **consistência**, níveis de **granularidade** e **refinamento, distinção entre modelos** do domínio, modelos do sistema e arquitetura e **reuso** em **todas as fases** do ciclo de vida


Os princípios fundamentais são:

- **Construção de um modelo de domínio** do sistema: com base em tipos, objetos e ações que enfatiza a independência entre o domínio, a solução de software e a sua implementação.

- **Forte ênfase nos conceitos de abstração e refinamento** para representar os relacionamentos essenciais entre os artefatos do sistema obtidos durante o processo de desenvolvimento. 

- **Procedimentos** e **diagramas** que apoiam o particionamento do sistema, o projeto e a conexão dos componentes.

- **Forte articulação do processo de desenvolvimento** com os conceitos de arquitetura de software, padrões e frameworks.

- Uso de **ciclo de vida rápido, iterativo e incremental**.

Modelos elaborados quando se adota Catalysis:

- **Especificação de requisitos**: entende o contexto do sistema, a arquitetura e os requisitos funcionais e gerar o Modelo do domínio. 

- **Especificação de sistema**: descreve o comportamento externo do sistema através do modelo de domínio do problema. Gera cenários, modelo de tipos e especificação de operações.

- **Projeto da arquitetura**: separa os componentes arquiteturais técnicos dos de aplicação e os seus conectores para se alcançar os objetivos de projeto.  

- **Projeto interno de componentes**: projetar interfaces e classes para cada componente, construir e testar.  Gera-se a especificação de classes e interface.

O **Catalysis** identifica os pacotes como a unidade de decomposição de mais alto nível.  Esses pacotes podem ser obtidos pela **análise** e **refinamento** do modelo de negócios

O método propõe algumas técnicas de particionamento desses pacotes e do sistema:
 
- **Divisão vertical**: visa refletir o fato de que usuários diferentes têm visões diferentes de um sistema ou negócio.

- **Divisão horizontal**: visa organizar os pacotes em camadas horizontais desde as ações de mais alto nível até as de infraestrutura.

- **Domínios diferentes**: visam separar domínios de funcionalidades diferentes, como interface com o usuário, persistência ou subdomínios do próprio problema.

## Kobra

- **Objetivo**: tornar os **componentes** de um sistema de software o foco do processo de desenvolvimento. 

- Adota a **estratégia de linha de produtos** para a criação, manutenção e implantação de componentes. 

- Utiliza uma **visão de componentes** que são descritos em uma representação baseada em UML que expressa suas características e relacionamentos.

- Permite que a estrutura e o comportamento dos sistemas possam ser **descritos independente de tecnologia**.

- Por tratar de linha de produtos, a abordagem **Kobra** utiliza o conceito de **framework genérico** e **reutilizável** que é utilizado para instanciar aplicações. 

Cada componente nesta abordagem é dividido em duas partes: 

- **Especificação**:  que descreve as características externamente visíveis do componente (isto é, os requisitos)

- **Realização**: que descreve como o componente satisfaz essas características em termos de interações com outros componentes, descrevendo inclusive o projeto interno

# [👆 TÓPICOS](#tópicos)

# A evolução da Reutilização de Software

No decorrer dos últimos anos percebeu-se um esforço, por parte de estudiosos da área, para tornar a **reutilização** uma realidade cada vez mais presente na vida de desenvolvedores. 

 Assim, tivemos as vertentes: 

- **Linha de Produtos de Software**
- **Ecossistemas de Software**

**Linha de Produtos de Software (LPS) ou Família de Aplicações**: envolve um conjunto de aplicações similares dentro de um domínio.  

Uma família de sistemas que compartilham **características** ou **especificações** comuns que satisfazem estratégias de mercado ou a um domínio de aplicação ou a uma missão.

Família de Produtos:
- Características Comuns
- Características Variáveis

![Imgur](https://i.imgur.com/4bMJJST.png)

As três atividades essenciais da construção de uma linha de produto são: 

- **Desenvolvimento de ativos centrais** (Engenharia de Domínio): os ativos centrais constituem-se nas **partes** a serem **reutilizadas** entre os produtos da família.

- **Desenvolvimento de produtos** (Engenharia de Aplicação): construção de produtos utilizando os ativos centrais.

- **Gerenciada LPS**: atividades que gerenciam a implantação e manutenção de LPS.


**Ecossistemas de Software**: um sistema de software representa uma combinação de software, hardware e “peopleware”, constituída sobre um ambiente comum, isto é, uma plataforma. 

Um conjunto de elementos configura os **ECOSs**: 

1. Atores envolvidos dentro e fora da organização
2. O produto de software principal
3. A plataforma de apoio ao software 
4. Os ativos de ECOS

**Exemplo real de ECOS:**

Ambiente do iPhone onde os atores são a empresa Apple, os usuários, os desenvolvedores da Apple, os desenvolvedores externos de aplicativos, e o iOS é a tecnologia de software central deste ECOS. 

- Para compreender os processos envolvidos nos ECOSs é necessário compreender sua estrutura **->** que elementos são formados e o que significam para o ECOS.


- **Ativos de software** são artefatos produzidos ou adquiridos e armazenados por uma organização.

- **Ativos de ECOS** representam os produtos do ECOS, podendo ser ativos reutizáveis  de software (componentes, serviços, aplicações) e necessidades. 

- Uma **plataforma de ECOS** pode ter apoio de uma biblioteca de ativos, responsável por gerenciar o seu ciclo de vida. 

- **Ativos de software**: em geral, também podem ser considerados ativos reutilizáveis. 

- Estes **ativos reutilizáveis** podem ser criados **dentro** da organização ou serem trazidos de **fora** da organização, ou mesmo do ECOS.



