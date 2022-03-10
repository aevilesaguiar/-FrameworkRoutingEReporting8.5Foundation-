# CHAPTER 5 - CONTACT CENTER OBJECTS

## 5.1 Learning Objectives


After completing this chapter, you should be able to do the following:

1- Describe Contact Center Objects, such as persons, agent groups, agent skills, places, place groups, and access groups.

2 - Make changes to basic Contact Center Objects, such as persons, agent groups, and skills.

3- Navigate basic objects in Genesys Administrator Extension.



Depois de concluir este capítulo, você deve ser capaz de fazer o seguinte:

1- Descreva os objetos do Contact Center, como pessoas, grupos de agentes, habilidades de agentes, locais, grupos de locais e grupos de acesso.

2 - Faça alterações nos objetos básicos do Contact Center, como pessoas, grupos de agentes e habilidades.

3- Navegue pelos objetos básicos no Genesys Administrator Extension.

## 5.2 Contact Center Data(Dados do Contact Center)



For Genesys to perform well, you must provide specifics about your contact center. Genesys software will be configured to integrate with the hardware and other resources 
available in your contact center. This enables Genesys software to interact with the switch, make routing decisions, provide contact center reporting, and perform other
functions.

We begin this lesson with an introduction to the terms related to a switch in a contact center. The terms listed on the next page are defined in the context in which 
Genesys uses them. Keep in mind, the switch you are using in your Genesys implementation may use different terms.

Para que a Genesys tenha um bom desempenho, você deve fornecer detalhes sobre seu contact center. O software Genesys será configurado para integração com o hardware e
outros recursos disponíveis em seu contact center. Isso permite que o software Genesys interaja com o switch, tome decisões de roteamento, forneça relatórios de contact 
center e execute outras funções.

Começamos esta lição com uma introdução aos termos relacionados a um switch em um contact center. Os termos listados na próxima página são definidos no contexto em que 
a Genesys os utiliza. Lembre-se de que o switch que você está usando na implementação do Genesys pode usar termos diferentes.

![image](https://user-images.githubusercontent.com/52088444/157496023-a9d7ca0d-7552-468d-a75c-fadef4d09f2d.png)

## 5.3 Configuration Objects


Genesys uses the term configuration object to indicate a certain resource or part of the Genesys system that must be defined in GAX using the Configuration Manager 
window. These are also sometimes referred to as contact center objects.

Genesys uses configuration objects to define the Genesys system, as well as the equipment and resources in the contact center. Equipment and resources available in 
the contact center can be managed by Genesys if they are defined in Genesys terms. This means you must create a configuration object to represent each resource in your 
contact center.

Genesys usa o termo objeto de configuração para indicar um determinado recurso ou parte do sistema Genesys que deve ser definido no GAX usando a janela Configuration Manager.
Às vezes, eles também são chamados de objetos do contact center.

A Genesys usa objetos de configuração para definir o sistema Genesys, bem como os equipamentos e recursos do contact center. Os equipamentos e recursos disponíveis no
contact center podem ser gerenciados pela Genesys se forem definidos nos termos da Genesys.
Isso significa que você deve criar um objeto de configuração para representar cada recurso em seu contact center.

Examples:


- Every extension, queue, and routing point in your switch must be created as a DN object.
- Every agent in your contact center must be created as a Person object.
- Every Genesys software component must be created as an Application object.

Exemplos:


- Cada ramal, fila e ponto de roteamento em seu switch deve ser criado como um objeto DN.
- Cada agente em seu contact center deve ser criado como um objeto Pessoa.
- Todo componente de software Genesys deve ser criado como um objeto Aplicativo.

## 5.4 Logging in for Voice Calls

To accept voice calls in the Contact Center, an agent login process typically involves the following:
Para aceitar chamadas de voz no Contact Center, um processo de login de agente geralmente envolve o seguinte:

- Agent login code (ID) is specified
- Switch authenticates the code
- Agent makes the phone set ready

- O código de login do agente (ID) é especificado
- Switch autentica o código
- Agente deixa o telefone pronto

![image](https://user-images.githubusercontent.com/52088444/157670278-577a63b2-28ff-4063-8875-e4413e89ceda.png)


**Automatic call distributor(ACD)Um sistema automatizado de distribuição de chamadas, conhecido como distribuidor automático de chamadas, é um dispositivo de telefonia que atende e distribui as chamadas recebidas para um grupo específico de terminais ou agentes dentro de uma organização.**

The agent login is the code that an agent enters into the telephone set or Agent Desktop to log in to an ACD Queue on the switch. Once the switch receives the code, it verifies the existence of the code and that the code is not currently in-use. If the code entered by the agent is valid and available, the switch associates the agent’s extension with one or more queues (as programmed in the switch) and allows the phone set to receive calls from those queues.

Once the agent is logged in, the agent must make the phone set ready to receive calls. Usually, the agent can accomplish this by clicking a button or selecting a menu choice in the Agent Desktop.

O login do agente é o código que um agente insere no telefone ou no Agent Desktop para fazer login em uma fila ACD na central. Depois que o switch recebe o código, ele verifica a existência do código e se o código não está em uso no momento. Se o código inserido pelo agente for válido e disponível, a central associa o ramal do agente a uma ou mais filas (conforme programado na central) e permite que o telefone receba chamadas dessas filas.

Uma vez que o agente está conectado, o agente deve deixar o telefone pronto para receber chamadas. Normalmente, o agente pode fazer isso clicando em um botão ou selecionando uma opção de menu no Agent Desktop.

## 5.5 The Switch
![image](https://user-images.githubusercontent.com/52088444/157670840-e5e4c1e1-fc01-4c27-86f3-d028e44def9f.png)

Genesys uses the term DNs to describe any of the points on the switch, as demonstrated in the preceding image.
A Genesys usa o termo DNs para descrever qualquer um dos pontos no switch, conforme demonstrado na imagem anterior.

**Terminology and Definitions**
![image](https://user-images.githubusercontent.com/52088444/157678407-7780ef72-c516-415f-a62e-85960900fe2c.png)
![image](https://user-images.githubusercontent.com/52088444/157678445-d22fadbd-c6bd-4ee6-900a-261c9fff5a68.png)


![image](https://user-images.githubusercontent.com/52088444/157678148-20fdddf7-8a74-4853-a523-242e6a9e88e2.png)
![image](https://user-images.githubusercontent.com/52088444/157678180-dacc3edb-4640-4f1a-a3e6-2677589c9770.png)


## 5.6 Places and Place Groups(Places and Place Groups)

A Place is a physical location that consists of a telephone with one or more extensions together with a workstation (computer) running an agent application. This agent place consists of a phone and a workstation.

Um Local(Place) é um local físico que consiste em um telefone com um ou mais ramais junto com uma estação de trabalho (computador) executando um aplicativo de agente. Este local de agente consiste em um telefone e uma estação de trabalho.

DNs are associated with places for the following reasons:

- Interactions destined for a particular agent can be routed to the phone set on the agent’s desk.
- Multiple interaction types (calls, emails, chats, etc.) can be associated with one particular workstation (or desk).

Os DNs são associados a locais pelos seguintes motivos:

- As interações destinadas a um determinado agente podem ser roteadas para o telefone na mesa do agente.
- Vários tipos de interação (chamadas, e-mails, chats, etc.) podem ser associados a uma determinada estação de trabalho (ou mesa).

![image](https://user-images.githubusercontent.com/52088444/157679618-84301237-421e-4dd8-a2e9-bdb895c4decc.png)

When a place is defined in the configuration database, it is good practice to name it according to the DN (and switch) associated with that place.

Quando um local é definido no banco de dados de configuração, é uma boa prática nomeá-lo de acordo com o DN (e switch) associado a esse local.

Example:

Name a place which is linked to DN 6001 on the Chicago switch as [6001_Chicago].

An agent can only be logged in at one place at a time and no more than one agent can be logged in at a particular place. When creating a place to represent a desk, you associate the phone set that sits on the desk with that place. Multiple DNs can be associated with a single place.

If an agent uses a hard phone to log in, Genesys associates the agent with a place based on the DN to which the agent logged in. If Genesys decides a call should be routed to that specific agent, it knows the place and DN (Extension or ACD Position) to which the call should be delivered.

Furthermore, in some versions, multiple interaction types can be associated with a particular workstation. For example, one agent can log in for voice, email, and chat. Any calls, emails, or chat requests for this agent are routed to the agent’s phone or workstation, based on the DNs associated with the place.

Places can be grouped by location as seen here (ChicagoPlaces) into a Place Group. 

![image](https://user-images.githubusercontent.com/52088444/157680177-1094956f-c69c-4ea1-a39e-912cbae9ed9e.png)


Place Groups are a collection of places (locations) used for monitoring, reporting, and routing purposes.

Exemplo:

Nomeie um local vinculado ao DN 6001 no switch Chicago como [6001_Chicago].

Um agente só pode estar conectado em um local por vez e não mais de um agente pode estar conectado em um determinado local. Ao criar um local para representar uma mesa, você associa o telefone que fica sobre a mesa com esse local. Vários DNs podem ser associados a um único local.

Se um agente usa um hard phone para fazer login, a Genesys associa o agente a um local com base no DN ao qual o agente efetuou login. ou Posição ACD) para a qual a chamada deve ser entregue.

Além disso, em algumas versões, vários tipos de interação podem ser associados a uma determinada estação de trabalho. Por exemplo, um agente pode fazer login para voz, e-mail e bate-papo. Quaisquer chamadas, e-mails ou solicitações de bate-papo para este agente são roteados para o telefone ou estação de trabalho do agente, com base nos DNs associados ao local.

Locais podem ser agrupados por localização como visto aqui (ChicagoPlaces) em um Grupo de Locais.

Grupos de Locais são uma coleção de locais (locais) usados ​​para fins de monitoramento, geração de relatórios e roteamento.



## 5.7 Persons/Users


Users are the people in the contact center who work with Genesys software. Users are either agents or non-agents.

- Agents interact with customers using phone, email, chat, and other means of communication.
- Non-agents use Genesys software for administrative or supervisory functions, not customer interactions. For example, contact center managers and system administrators are non-agents.

Users can be created, configured, and administered using GAX.

Os usuários são as pessoas do contact center que trabalham com o software Genesys. Os usuários são agentes ou não agentes.

- Os agentes interagem com os clientes por telefone, e-mail, chat e outros meios de comunicação.
- Os não agentes usam o software Genesys para funções administrativas ou de supervisão, não para interações com clientes. Por exemplo, gerentes de contact center e administradores de sistema não são agentes.

Os usuários podem ser criados, configurados e administrados usando o GAX.


**Common Properties**

There are common properties that must exist whether you are an agent or a non-agent:

- Employee ID—Uniquely identifies the person within the Genesys system. This is a required value. The Human Resources team often provides Employee IDs.


- Username—Refers to the login credential that the person is assigned to gain access to Genesys GUI applications, such as the Genesys Agent Desktop application. This is a required value.


- Password—Protects an agent's account against unauthorized access to a Genesys GUI.


- Member of Access Group—Determines what a user can do (permissions) within Genesys, based on which access groups the user is a member. Access groups are groups of users who need the same set of permissions of configuration objects in Genesys. Genesys provides three standard access groups for users: Users, Administrators, and Super Administrators. You can also create custom access groups.


**Propriedades comuns**

Existem propriedades comuns que devem existir seja você um agente ou um não agente:

- ID do funcionário—Identifica exclusivamente a pessoa dentro do sistema Genesys. Este é um valor obrigatório. A equipe de Recursos Humanos geralmente fornece IDs de funcionários.


- Nome de usuário — Refere-se à credencial de login atribuída à pessoa para obter acesso aos aplicativos Genesys GUI, como o aplicativo Genesys Agent Desktop. Este é um valor obrigatório.


- Senha—Protege a conta de um agente contra acesso não autorizado a uma GUI Genesys.


- Membro do grupo de acesso—Determina o que um usuário pode fazer (permissões) dentro da Genesys, com base em quais grupos de acesso o usuário é membro. Grupos de acesso são grupos de usuários que precisam do mesmo conjunto de permissões de objetos de configuração no Genesys. A Genesys oferece três grupos de acesso padrão para usuários: Usuários, Administradores e Superadministradores. Você também pode criar grupos de acesso personalizados.


![image](https://user-images.githubusercontent.com/52088444/157680841-31a56fcc-c21d-41b1-9b3b-639d6e1d9fcf.png)

**Agent Properties**

Users who are created as agents can have additional information such as the following:

- Agent checkbox—Defines whether a person is an agent. When creating a new person object, this flag is selected by default. If you create a non-agent person object, you must clear this checkbox.
- Agent logins—A login ID that enables authorization on the switch. An agent can have more than one login ID (from one or more switches), but you cannot assign a single agent login to more than one agent.
- Default place—Used only in rare cases that can’t work with places (when a real-time association with a place cannot be established through the login procedure).
- Skills—A complete description of each agent’s skill set enables complex routing decisions. Skills are defined in the Skills folder. They are selected and given level values in this tab.


Tipos de tradução
Tradução de textos

DETECTAR IDIOMA

INGLÊS

PORTUGUÊS

ESPANHOL

PORTUGUÊS

INGLÊS

ESPANHOL
Texto de origem
Users who are created as agents can have additional information such as the following:

- Agent checkbox—Defines whether a person is an agent. When creating a new person object, this flag is selected by default. If you create a non-agent person object, you must clear this checkbox.
- Agent logins—A login ID that enables authorization on the switch. An agent can have more than one login ID (from one or more switches), but you cannot assign a single agent login to more than one agent.
- Default place—Used only in rare cases that can’t work with places (when a real-time association with a place cannot be established through the login procedure).
- Skills—A complete description of each agent’s skill set enables complex routing decisions. Skills are defined in the Skills folder. They are selected and given level values in this tab.
Users who are created as agents can have additional information such as the following:

- Agent checkbox—Defines whether a person is an agent. When creating a new person object, this flag is selected by default. If you create a non-agent person object, you must clear this checkbox.
- Agent logins—A login ID that enables authorization on the switch. An agent can have more than one login ID (from one or more switches), but you cannot assign a single agent login to more than one agent.
- Default place—Used only in rare cases that can’t work with places (when a real-time association with a place cannot be established through the login procedure).
- Skills—A complete description of each agent’s skill set enables complex routing decisions. Skills are defined in the Skills folder. They are selected and given level values in this tab.


Os usuários criados como agentes podem ter informações adicionais, como:

- Caixa de seleção Agente—Define se uma pessoa é um agente. Ao criar um novo objeto de pessoa, esse sinalizador é selecionado por padrão. Se você criar um objeto de pessoa não agente, deverá desmarcar essa caixa de seleção.
- Logins do agente — Um ID de login que permite a autorização no switch. Um agente pode ter mais de um ID de logon (de uma ou mais centrais), mas você não pode atribuir um único logon de agente a mais de um agente.
- Local padrão—Usado apenas em casos raros que não podem trabalhar com locais (quando uma associação em tempo real com um local não pode ser estabelecida por meio do procedimento de login).
- Habilidades—Uma descrição completa do conjunto de habilidades de cada agente permite decisões de roteamento complexas. As habilidades são definidas na pasta Habilidades. Eles são selecionados e recebem valores de nível nesta guia. 

![image](https://user-images.githubusercontent.com/52088444/157681303-e1484309-194d-48f8-b100-d847d96dd7c3.png)

**Agents and Skills**

Skills define a quality or ability that an agent possesses which can be used as criteria for routing interactions. Skills are assigned to each agent and are given a level value. The skill levels indicate the agent’s proficiency in that skill. Routing decisions can then be made based on the assigned skills.

As habilidades definem uma qualidade ou habilidade que um agente possui que pode ser usada como critério para interações de roteamento. As habilidades são atribuídas a cada agente e recebem um valor de nível. Os níveis de habilidade indicam a proficiência do agente nessa habilidade. As decisões de roteamento podem ser tomadas com base nas habilidades atribuídas.

![image](https://user-images.githubusercontent.com/52088444/157681442-7299fdac-39b5-4d5d-b6db-ff8b95cf6210.png)


Examples:
- Languages: English and Spanish
- Categories of product knowledge: Mortgages, Investments, and Billing
- Ability to handle a certain category of customer: PlatinumCustomers, GoldCustomers, and NewAccounts

Exemplos:
- Idiomas: Inglês e Espanhol
- Categorias de conhecimento do produto: Hipotecas, Investimentos e Faturamento
- Capacidade de lidar com uma determinada categoria de cliente: PlatinumCustomers, GoldCustomers e NewAccounts

**Agents and Agent Groups**

An Agent Group is a collection of agents. Agent groups are used for monitoring, routing, and reporting. One of the benefits of grouping agents is that contact center activity can be monitored in relation to groups. This high-level view can help a contact center manager or supervisor to monitor activity at a glance. Another benefit is the use of groups as routing targets.

Um grupo de agentes é uma coleção de agentes. Os grupos de agentes são usados para monitoramento, roteamento e relatórios. Um dos benefícios de agrupar agentes é que a atividade do contact center pode ser monitorada em relação aos grupos. Essa visão de alto nível pode ajudar um gerente ou supervisor de contact center a monitorar a atividade rapidamente. Outro benefício é o uso de grupos como destinos de roteamento.

![image](https://user-images.githubusercontent.com/52088444/157681782-da28bb0a-9210-4dff-9eb5-56dd2335fc7e.png)

Example:

You could route to the Billing agent group (regardless of location) or route to the ChicagoAgents.

Exemplo:

Você pode rotear para o grupo de agentes de cobrança (independentemente do local) ou rotear para os ChicagoAgents.

**Routing and Reporting**

Interactions are typically routed to Agent Groups and Skills.

The contact center is the central point of any organization from which all customer contacts are managed. Valuable information about customers is routed to the appropriate people, contacts are tracked, and data is gathered for reporting. All interactions are routed through the contact center. Typically, this includes voice interactions and multimedia (email, chat, etc.).

Customer data is gathered from switches and IVRs (voice interactions) or other media servers (email, chat, etc.) and is used to supply information to the agent. This data can also be used in the decision-making process on how to route the interactions.

As interações geralmente são roteadas para Grupos de Agentes e Habilidades.

O contact center é o ponto central de qualquer organização a partir do qual todos os contatos com os clientes são gerenciados. Informações valiosas sobre os clientes são roteadas para as pessoas apropriadas, os contatos são rastreados e os dados são coletados para relatórios. Todas as interações são roteadas pelo contact center. Normalmente, isso inclui interações de voz e multimídia (e-mail, bate-papo etc.).

Os dados do cliente são coletados de switches e IVRs (interações de voz) ou outros servidores de mídia (e-mail, chat, etc.) e são usados para fornecer informações ao agente. Esses dados também podem ser usados no processo de tomada de decisão sobre como rotear as interações.

Interactions are typically routed to groups and skills. When deciding which call should be sent to an agent and which call can wait, some things to consider are the following:
- Agent skills
- Agent groups
- Current contact center load
- Customer’s priority

As interações geralmente são direcionadas para grupos e habilidades. Ao decidir qual chamada deve ser enviada a um agente e qual chamada pode esperar, algumas coisas a serem consideradas são as seguintes:
- Habilidades do agente
- Grupos de agentes
- Carga atual do contact center
- Prioridade do cliente

You want to make sure that the contact center is configured with logical and accurate groups and skills in order to make your routing decisions easier and more effective. The goal is to maximize the profitability of the enterprise. 

Interactions are typically monitored for real-time and historical reporting.

Você quer ter certeza de que o contact center está configurado com grupos e habilidades lógicas e precisas para tornar suas decisões de roteamento mais fáceis e eficazes. O objetivo é maximizar a lucratividade do empreendimento.

As interações são normalmente monitoradas para relatórios históricos e em tempo real.

## 5.8 Contact Center Object Summary(Resumo do Objeto do Contact Center)

![image](https://user-images.githubusercontent.com/52088444/157682548-849aa770-1e5c-4ff9-a611-7f459072f8a3.png)

![image](https://user-images.githubusercontent.com/52088444/157682592-e419b6e9-167e-4045-b8e9-aaeea9a5fe65.png)

![image](https://user-images.githubusercontent.com/52088444/157682636-8b8c81ea-b59c-4436-8e70-7b4d452a6869.png)

![image](https://user-images.githubusercontent.com/52088444/157682699-1bf00050-2e67-43e3-91b4-7b46256fcd82.png)

![image](https://user-images.githubusercontent.com/52088444/157682763-33e81735-5410-4921-8e34-bf9b0e9047f6.png)

![image](https://user-images.githubusercontent.com/52088444/157682811-93e50e77-a2fe-4a94-9b58-fa87baab7e63.png)

One of the primary reasons for companies to choose CTI involves the types of targets they can select. As a general rule, the switch knows about DNs (e.g., extensions) and agent logins, and – occasionally – agents themselves. Genesys broadens the scope of possible targets to include skill levels, agent groups, places, and place groups.

The Genesys system is aware of all the possible targets at all the available sites. For example, Genesys can select the best available agent in the Mortgage group in Chicago or Milan.

Because the switch can only send a telephone call to an actual DN, Genesys must specify a DN in its target selection. For example, if Genesys selects a particular user as the target because that agent possesses a skill at a particular level, Genesys must supply a DN to the switch by which that user can receive the call. In the switch, a DN is associated with an agent login ID when the agent logs in.

Genesys links the agent with their place. All associated Genesys objects are then associated with specific DNs in the switch.

The Place object represents an agent’s desk with all the associated DNs – extension and ACD Position (where applicable).

The Agent (User) object represents the agent with skills and one or more agent logins. This enables Genesys to track agents, their skills, places, agent groups, and place groups for reporting, routing, and other Genesys solutions across multiple sites and for all 
interaction types.


Uma das principais razões para as empresas escolherem o CTI envolve os tipos de alvos que podem selecionar. Como regra geral, a central conhece DNs (por exemplo, ramais) e logins de agentes e – ocasionalmente – os próprios agentes. A Genesys amplia o escopo de possíveis alvos para incluir níveis de habilidade, grupos de agentes, locais e grupos de locais.

O sistema Genesys está ciente de todos os alvos possíveis em todos os sites disponíveis. Por exemplo, a Genesys pode selecionar o melhor agente disponível no grupo Mortgage em Chicago ou Milão.

Como o switch só pode enviar uma chamada telefônica para um DN real, a Genesys deve especificar um DN em sua seleção de destino. Por exemplo, se a Genesys selecionar um usuário específico como destino porque esse agente possui uma habilidade em um determinado nível, a Genesys deverá fornecer um DN à central pela qual esse usuário possa receber a chamada. No switch, um DN é associado a uma ID de logon do agente quando o agente efetua logon.

A Genesys vincula o agente ao seu local. Todos os objetos Genesys associados são então associados a DNs específicos no switch.

O objeto Place representa a mesa de um agente com todos os DNs associados – ramal e Posição ACD (quando aplicável).

O objeto Agente (Usuário) representa o agente com habilidades e um ou mais logins de agente. Isso permite que a Genesys rastreie os agentes, suas habilidades, locais, grupos de agentes e grupos de locais para relatórios, roteamento e outras soluções da Genesys em vários locais e para todos
tipos de interação.

**Configurable Resources**

Once the switch is in place, you can configure the following resources in your contact center:
Assim que o switch estiver instalado, você poderá configurar os seguintes recursos em seu contact center:

![image](https://user-images.githubusercontent.com/52088444/157683268-d9e5f4c1-0573-4696-b16b-2809d67b5ac8.png)

![image](https://user-images.githubusercontent.com/52088444/157683909-5eb5e673-aa5a-45d6-8e1c-443dd229f537.png)

![image](https://user-images.githubusercontent.com/52088444/157683978-60e9d7bc-578f-4c7d-81ac-e54add35cff1.png)

**Agent Login Objects**

When you create a new agent login, you must configure the following objects in the General tab:
Ao criar um novo login de agente, você deve configurar os seguintes objetos na guia Geral:

![image](https://user-images.githubusercontent.com/52088444/157684515-e725111a-e999-481b-a1e7-634015c20849.png)


![image](https://user-images.githubusercontent.com/52088444/157684584-55c1b088-971b-43ff-9679-c4c58e11c499.png)

## 5.9 Creating Configuration Objects

You can define all configuration objects in Genesys Administrator Extension.

This includes DNs, People, Skills, Hosts, Genesys Applications, and others. When you define a configuration object in Genesys Administrator Extension, the Configuration Server pushes the information about that object to all the other Genesys servers and the Configuration Database.

Você pode definir todos os objetos de configuração no Genesys Administrator Extension.

Isso inclui DNs, Pessoas, Habilidades, Hosts, Aplicativos Genesys e outros. Quando você define um objeto de configuração no Genesys Administrator Extension, o servidor de configuração envia as informações sobre esse objeto para todos os outros servidores Genesys e o banco de dados de configuração.

![image](https://user-images.githubusercontent.com/52088444/157684764-a4365148-99af-4fb3-b5a9-c000f51c989d.png)


In this way, the Configuration Server provides two important functions:
- Makes it possible for any of the Genesys servers to immediately find out about configuration objects
- Facilitates storing configuration data permanently by sending the data to the Configuration Database

Desta forma, o Configuration Server oferece duas funções importantes:
- Possibilita que qualquer um dos servidores Genesys descubra imediatamente sobre objetos de configuração
- Facilita o armazenamento de dados de configuração permanentemente enviando os dados para o Banco de Dados de Configuração


## 5.10 Basics of Configuring Objects(Noções básicas de configuração de objetos)

Genesys Administrator Extension can be used to define and configure objects. When you define objects in GAX, they are immediately pushed to Configuration Server and are seen in Genesys Administrator (or if defined in GA, the reverse is true) and all other Genesys applications.

Genesys Administrator Extension pode ser usado para definir e configurar objetos. Quando você define objetos no GAX, eles são imediatamente enviados para o Configuration Server e são vistos no Genesys Administrator (ou se definido no GA, o inverso é verdadeiro) e em todos os outros aplicativos Genesys.

![image](https://user-images.githubusercontent.com/52088444/157685146-32170618-b881-423c-9e00-60cfb2b9f75e.png)

In GAX, objects are defined and configured under the Configuration menu.
No GAX, os objetos são definidos e configurados no menu Configuração.

**GAX Configuration**

You can locate and manage your configuration objects using the Configuration tab on the Genesys Administration Extension header. It shows different configuration object types organized under different headings.

Você pode localizar e gerenciar seus objetos de configuração usando a guia Configuration no cabeçalho Genesys Administration Extension. Ele mostra diferentes tipos de objetos de configuração organizados em diferentes títulos.

![image](https://user-images.githubusercontent.com/52088444/157685397-f3b6d234-7d22-4c9d-b7de-cb9860b35b38.png)

The specific object types are listed within the object headings. For example, for skills, you would first go to the object heading Accounts and then to Skills. 
Os tipos de objetos específicos são listados nos títulos dos objetos. Por exemplo, para habilidades, você iria primeiro para o título de objeto Contas e depois para Habilidades.

![image](https://user-images.githubusercontent.com/52088444/157685686-71a60cf8-79c8-407e-be1c-749fb930e8da.png)

**Managing Objects**

GAX is used for managing objects in your contact center. The GAX interface allows the creation, modification, and deletion of objects.
GAX é usado para gerenciar objetos em seu contact center. A interface GAX permite a criação, modificação e exclusão de objetos.

To create a new object: 
- Navigate to the location containing the type of object you want to create. For example, to create a new skill in GAX, you would go to Configuration > Accounts > Skills. 
- Click the New button to start configuring a new object of that type. (You may also select an existing object and edit its properties.)

Para criar um novo objeto:
- Navegue até o local que contém o tipo de objeto que deseja criar. Por exemplo, para criar uma nova habilidade no GAX, vá para Configuração > Contas > Habilidades.
- Clique no botão Novo para começar a configurar um novo objeto desse tipo. (Você também pode selecionar um objeto existente e editar suas propriedades.)

![image](https://user-images.githubusercontent.com/52088444/157686046-87f5004e-0e4f-4fb6-9581-76fc215c9f79.png)

## 5.11 Creating a New Skill

A complete description of each agent’s skill set enables complex routing decisions. 

When you create a new skill, configure the properties in the General tab of the skill. The only property you must fill in is the name. Notice the red asterisk indicating that the property requires a value.

Uma descrição completa do conjunto de habilidades de cada agente permite decisões de roteamento complexas.

Ao criar uma nova habilidade, configure as propriedades na guia Geral da habilidade. A única propriedade que você deve preencher é o nome. Observe o asterisco vermelho indicando que a propriedade requer um valor.
![image](https://user-images.githubusercontent.com/52088444/157686259-b1b52365-0dfe-41a9-9cf4-6d5d85b9f36d.png)

- Name refers to the name of the skill you enter.
- State Enabled defines whether or not the skill is active.

- Name refers to the name of the skill you enter.
- State Enabled defines whether or not the skill is active.

Por padrão, todos os objetos de configuração do Genesys estão habilitados – a propriedade State Enabled está marcada. Você pode tornar um objeto inativo no sistema Genesys desmarcando a caixa de seleção State Enabled.

Etapas para criar uma habilidade no idioma mandarim no GAX

1- Navegue até Configuração > Contas > Habilidades.

2- Clique em Novo.

3- No campo Nome, digite Mandarim.

4- Clique em Salvar.

![image](https://user-images.githubusercontent.com/52088444/157686591-c23445ed-1058-4c44-b9b1-9e6cc9ce4c79.png)

## 5.12 Making Changes to Agent Group(5.12 Making Changes to Agent Group)

An Agent Group is a collection of agents. One of the benefits of grouping agents is that contact center activity can be monitored in relation to groups. This high-level view can help a contact center manager or supervisor to monitor activity at a glance. Another benefit is the use of groups as routing targets.

For example, you could route to the Bankers agent group (regardless of location) or route to the Chicago_Places.

Agent Groups can be created in Genesys Administrator Extension. You must specify the desired name for the agent group. This name can be referenced as a routing target and also for gathering reporting statistics.

Um grupo de agentes é uma coleção de agentes. Um dos benefícios de agrupar agentes é que a atividade do contact center pode ser monitorada em relação aos grupos. Essa visão de alto nível pode ajudar um gerente ou supervisor de contact center a monitorar a atividade rapidamente. Outro benefício é o uso de grupos como destinos de roteamento.

Por exemplo, você pode rotear para o grupo de agentes Bankers (independentemente do local) ou rotear para Chicago_Places.

Grupos de agentes podem ser criados no Genesys Administrator Extension. Você deve especificar o nome desejado para o grupo de agentes. Esse nome pode ser referenciado como destino de roteamento e também para coletar estatísticas de relatórios.

![image](https://user-images.githubusercontent.com/52088444/157686863-95f55867-f038-412d-851a-24e714300992.png)

Use the tabs to access more properties of the object. Clicking the Agents tab displays the agents that have been added to the agent group. In the example shown, the Agent Group has two members—AAgent and MAngelou.

Use as guias para acessar mais propriedades do objeto. Clicar na guia Agentes exibe os agentes que foram adicionados ao grupo de agentes. No exemplo mostrado, o Grupo de Agentes tem dois membros—AAgent e MAngelou.

![image](https://user-images.githubusercontent.com/52088444/157687173-b08cffd5-d689-4a9e-8318-02e4a7b9b9fe.png)

Para um novo grupo de agentes, a guia Agentes é onde você adiciona agentes como membros do grupo de agentes. Um agente pode pertencer a zero, um ou até vários grupos de agentes.
![image](https://user-images.githubusercontent.com/52088444/157687322-246b12c1-3605-473e-9ca5-3969f67bb6c5.png)

## 5.13 Making Changes to Agents


In this chapter, let’s look at the two different ways to create agents:
- GAX - Configuration Manager
- GAX - Agents View
- 

Neste capítulo, vamos ver as duas maneiras diferentes de criar agentes:
- GAX - Gerenciador de configuração
- GAX - Visualização de Agentes

![image](https://user-images.githubusercontent.com/52088444/157687688-faec25a8-cae0-4404-af9a-77191122bebb.png)

One option for creating new agents is the GAX–Configuration Manager. This interface provides a more detailed view of objects.

When you create a new user, you must configure the common properties shared by both agents and non-agents.

To configure the new agent, navigate to Configuration > Accounts > Persons > New and complete the General and Member of tabs of the New Properties section.

- Employee ID–Uniquely identifies the person within the Genesys system. This is a required value. The Human Resources team often provides employee IDs.
- Username–Refers to the login credential that the person is assigned to gain access to Genesys GUI applications such as the Genesys Agent Desktop application. This is a required value.
- Password–Protects the user's account against unauthorized access to a Genesys GUI.
- Member of Access Group–Determines what a user can and cannot do (permissions) within Genesys platform, based on which access groups the user is a member. Access groups are groups of users who need to have the same set of permissions of configuration objects in Genesys. Genesys provides three standard Access Groups for users: Users, Administrators, and Super Administrators. You can also create custom Access Groups.
- State Enabled–Defines whether or not the employee’s status is active.
- Agent–Defines whether or not the person is an agent. When creating a new person object in the Configuration Manager, this flag is selected by default. If you create a non-agent person object, you must clear this checkbox. Once the new user is saved, this option cannot be changed.

Uma opção para criar novos agentes é o GAX–Configuration Manager. Essa interface fornece uma visão mais detalhada dos objetos.

Ao criar um novo usuário, você deve configurar as propriedades comuns compartilhadas por agentes e não agentes.

Para configurar o novo agente, navegue até Configuração > Contas > Pessoas > Novo e preencha as guias Geral e Membro da seção Novas propriedades.

- ID do funcionário – identifica exclusivamente a pessoa dentro do sistema Genesys. Este é um valor obrigatório. A equipe de Recursos Humanos geralmente fornece IDs de funcionários.
- Nome de usuário – Refere-se à credencial de login atribuída à pessoa para obter acesso aos aplicativos Genesys GUI, como o aplicativo Genesys Agent Desktop. Este é um valor obrigatório.
- Senha – Protege a conta do usuário contra acesso não autorizado a uma GUI Genesys.
- Membro do Grupo de Acesso – Determina o que um usuário pode e não pode fazer (permissões) na plataforma Genesys, com base em quais grupos de acesso o usuário é membro. Grupos de acesso são grupos de usuários que precisam ter o mesmo conjunto de permissões de objetos de configuração no Genesys. A Genesys fornece três grupos de acesso padrão para usuários: usuários, administradores e superadministradores. Você também pode criar grupos de acesso personalizados.
- Estado Ativado – Define se o status do funcionário está ativo ou não.
- Agente – Define se a pessoa é ou não um agente. Ao criar um novo objeto de pessoa no Configuration Manager, esse sinalizador é selecionado por padrão. Se você criar um objeto de pessoa não agente, deverá desmarcar essa caixa de seleção. Depois que o novo usuário for salvo, essa opção não poderá ser alterada.

![image](https://user-images.githubusercontent.com/52088444/157688097-38b39865-997b-41a0-bf15-99ef5b735c80.png)

Specify the appropriate access group to assign a set of permissions. Click the Member Of tab, click Add, and select an appropriate Access Group. Administrators define the access groups and the permissions they represent. In this example, the agent is now a member of the Users access group.

Especifique o grupo de acesso apropriado para atribuir um conjunto de permissões. Clique na guia Membro de, clique em Adicionar e selecione um grupo de acesso apropriado. Os administradores definem os grupos de acesso e as permissões que eles representam. Neste exemplo, o agente agora é membro do grupo de acesso Usuários.

![image](https://user-images.githubusercontent.com/52088444/157688296-371c6daf-070d-4a78-9638-f68004f149f6.png)

![image](https://user-images.githubusercontent.com/52088444/157688351-8054e938-65c0-4fdf-9fe4-3aa34e6cb383.png)

Because the new user will be an agent, you can configure the following extra agent properties:

- Default Place–Used only in rare cases that can’t work with places (when a real-time association with a place cannot be established through the login procedure.)

- Capacity Rule–A script which limits the number and media type of interactions that can be distributed to this user. For example, one voice and two emails. (See the Resource Capacity Planning Guide.) These can be assigned at the level of the agent, place, and tenant.

Como o novo usuário será um agente, você pode configurar as seguintes propriedades extras do agente:

- Local padrão – Usado apenas em casos raros que não podem trabalhar com locais (quando uma associação em tempo real com um local não pode ser estabelecida por meio do procedimento de login).

- Regra de Capacidade – Um script que limita o número e o tipo de mídia de interações que podem ser distribuídas para este usuário. Por exemplo, uma voz e dois e-mails. (Consulte o Resource Capacity Planning Guide.) Eles podem ser atribuídos no nível do agente, local e locatário.

![image](https://user-images.githubusercontent.com/52088444/157691354-91b5f2ec-bb2a-4cb5-8452-a3fbce1a1e1e.png)

Skills–A complete description of each agent’s skill set enables complex routing decisions. Skills are defined in the Skills folder. They are selected and given level values in this tab.

Click the Skills tab and select Add.
Under Skills, click the folder icon to browse the list of existing skills and select one or enter the name of a new skill you wish to add.
Assign a level from 1 to 10.
Click OK.


Habilidades – Uma descrição completa do conjunto de habilidades de cada agente permite decisões de roteamento complexas. As habilidades são definidas na pasta Habilidades. Eles são selecionados e recebem valores de nível nesta guia.

Clique na guia Habilidades e selecione Adicionar.
Em Habilidades, clique no ícone de pasta para navegar na lista de habilidades existentes e selecione uma ou digite o nome de uma nova habilidade que deseja adicionar.
Atribua um nível de 1 a 10.
Clique OK.

![image](https://user-images.githubusercontent.com/52088444/157691500-723fac8a-06ca-48a6-9d70-e5648d53f20d.png)

Agent Logins–Each telephony agent has a login ID which enables authorization on the switch. An agent can have more than one Login ID (from one or more switches), but you cannot assign a single agent login to more than one agent.

Click the Agent Logins tab and select Add.
Under Agent Login, click the folder icon to browse the agent logins already configured on the switches in your environment. Select an agent login from the list.
Click OK.

- Agent Checkbox–Make sure this box is checked for an agent.

You can also edit existing agents. In the person's window, select the checkbox next to the agent you want to edit and click the Edit button at the top of the screen. This opens the details of the person and allows you to make any required changes.

754 / 5.000
Resultados de tradução
Logins do Agente – Cada agente de telefonia possui um ID de login que permite a autorização no switch. Um agente pode ter mais de um ID de login (de uma ou mais centrais), mas você não pode atribuir um único login de agente a mais de um agente.

Clique na guia Logins de agente e selecione Adicionar.
Em Login do Agente, clique no ícone da pasta para navegar pelos logins do agente já configurados nos switches em seu ambiente. Selecione um logon de agente na lista.
Clique OK.

- Caixa de seleção do agente – certifique-se de que esta caixa esteja marcada para um agente.

Você também pode editar os agentes existentes. Na janela da pessoa, marque a caixa de seleção ao lado do agente que deseja editar e clique no botão Editar na parte superior da tela. Isso abre os detalhes da pessoa e permite que você faça as alterações necessárias. 

![image](https://user-images.githubusercontent.com/52088444/157691669-e91dc142-2d16-4c20-af65-c2f5f346e722.png)

![image](https://user-images.githubusercontent.com/52088444/157691713-4eeb910f-66f7-4eba-9427-89516d4cb597.png)

There is an additional option found in GAX: Agents View. This option doesn’t provide the same detailed view of the agent as the Configuration Manager, but it does allow for fast creation, modification, and deletion of agents. If the agent's view is not available, it can be turned on in the System Preferences. The preferences also determine the access group used for new agents added here.

Depending on your assigned access at work, this may be the only page you have access to for creating agents.

To create an agent in the Agents screen in GAX, you navigate to Agents View then, click Add. 

Existe uma opção adicional encontrada no GAX: Visualização de Agentes. Essa opção não fornece a mesma visão detalhada do agente que o Configuration Manager, mas permite a criação, modificação e exclusão rápidas de agentes. Se a visualização do agente não estiver disponível, ela poderá ser ativada nas Preferências do Sistema. As preferências também determinam o grupo de acesso usado para novos agentes adicionados aqui.

Dependendo do seu acesso atribuído no trabalho, esta pode ser a única página à qual você tem acesso para criar agentes.

Para criar um agente na tela Agentes no GAX, navegue até a Visualização de agentes e clique em Adicionar.

![image](https://user-images.githubusercontent.com/52088444/157691856-ef96744e-58ba-4c66-8294-a8442e0a287b.png)

First, enter the required common properties for the user information:

- Username, First Name, Last Name, and Password. The Username must be unique within the Genesys system. It will be used for logging in to interfaces.

Primeiro, insira as propriedades comuns necessárias para as informações do usuário:

- Nome de usuário, nome, sobrenome e senha. O nome de usuário deve ser exclusivo no sistema Genesys. Ele será usado para fazer login nas interfaces.

![image](https://user-images.githubusercontent.com/52088444/157692041-237883f0-222a-41f6-8dd2-fffd0f1205f4.png)

Next, configure the agent properties:

![image](https://user-images.githubusercontent.com/52088444/157692086-2cd18fe8-d40b-4d3d-a72c-2cf41db403bb.png)

For Place, click on the folder icon and select a place. This enables you to specify a default place to be used when the agent logs into an agent desktop.

For Agent Logins, click the + to open a new window. Click the folder icon to browse the list. Select the agent’s assigned agent login for the switch or click the + and create the necessary new agent login.

Para Local, clique no ícone da pasta e selecione um local. Isso permite que você especifique um local padrão a ser usado quando o agente efetuar login em um desktop do agente.

Para Logins de Agente, clique no + para abrir uma nova janela. Clique no ícone da pasta para navegar na lista. Selecione o logon de agente atribuído ao agente para o switch ou clique em + e crie o novo logon de agente necessário.

![image](https://user-images.githubusercontent.com/52088444/157692182-8be9f175-a290-4669-90af-24efe3023e7d.png)

For Number/DNs, click the + to open the new window and click the folder icon to browse the list or click the + and create a new DN. By selecting a default place, the associated DNs will be set here.

For Skills, select the checkbox next to the skill you wish to assign to your agent and enter a rating. If you wish to create a new skill, type the name of the skill you want to add in the search box and press Enter. Select the checkbox next to the newly added skill and enter a rating for that agent.

For Agent Groups, select the checkbox next to any group you want to assign to your agent.

Para Número/DNs, clique no + para abrir a nova janela e clique no ícone de pasta para navegar na lista ou clique no + e crie um novo DN. Ao selecionar um local padrão, os DNs associados serão definidos aqui.

Para Habilidades, marque a caixa de seleção ao lado da habilidade que deseja atribuir ao seu agente e insira uma classificação. Se você deseja criar uma nova habilidade, digite o nome da habilidade que deseja adicionar na caixa de pesquisa e pressione Enter. Marque a caixa de seleção ao lado da habilidade recém-adicionada e insira uma classificação para esse agente.

Para Grupos de agentes, marque a caixa de seleção ao lado de qualquer grupo que você deseja atribuir ao seu agente.

![image](https://user-images.githubusercontent.com/52088444/157692309-64ac6932-6152-4239-988e-f0bf040812b1.png)

After an agent has been added, they will be listed in the Agents view. By hovering the mouse over the row or selecting anywhere in the row, three tools appear at the far right to Disable, Clone, or Edit the agent. Disable prevents the agent object from being used such as to log in. Clone creates a new agent with the same initial properties. Edit lets you change the highlighted agent.

Depois que um agente for adicionado, ele será listado na visualização Agentes. Ao passar o mouse sobre a linha ou selecionar qualquer lugar na linha, três ferramentas aparecem na extrema direita para Desativar, Clonar ou Editar o agente. Desabilitar impede que o objeto do agente seja usado como para efetuar login. Clone cria um novo agente com as mesmas propriedades iniciais. Editar permite alterar o agente destacado.

![image](https://user-images.githubusercontent.com/52088444/157692395-855ed7cf-6b9e-460a-bead-4fc34d139b69.png)


This provides the ability to import a file which can be used to create and modify various configuration objects.

The import process can create new objects as well as build relationships between objects. For example, during the creation of a set of agents, the agents can be assigned Skills, put into Agent Groups, and have their Access Group set. In general, when using the import or export process to build relationships, the referenced objects should be created in advance.

Isso fornece a capacidade de importar um arquivo que pode ser usado para criar e modificar vários objetos de configuração.

O processo de importação pode criar novos objetos, bem como construir relacionamentos entre objetos. Por exemplo, durante a criação de um conjunto de agentes, os agentes podem receber Habilidades, colocados em Grupos de Agentes e ter seu Grupo de Acesso definido. Em geral, ao usar o processo de importação ou exportação para construir relacionamentos, os objetos referenciados devem ser criados antecipadamente.
