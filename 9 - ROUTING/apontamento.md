## 9.1 Learning Objectives (objetivos de aprendizagem)


After completing this chapter, you should be able to do the following: 

1 - Recall Genesys Routing.

2 - Describe ORS and URS.

3 -  Describe Composer.

4 - Explain a Simple Routing Scenario.

5 - Describe the use of Parameter groups with Routing.

6 - Use GAX to set values in Parameter groups.



Depois de concluir este capítulo, você deve ser capaz de fazer o seguinte:

1 - Recupere o roteamento Genesys.

2 - Descrever ORS e URS.

3 - Descreva o Composer.

4 - Explique um cenário de roteamento simples.

5 - Descrever o uso de Grupos de Parâmetros com Roteamento.

6 - Use GAX para definir valores em grupos de parâmetros.


## 9.2 Routing: Interactions and Tasks(Roteamento: Interações e Tarefas)


Universal Routing is a part of the Genesys Platform that provides the core interaction management functionality.

Universal Routing can direct interactions from a wide variety of platforms, such as toll-free carrier switches, premise PBXs or ACDs, IVRs, IP PBXs, email servers, web servers, and workflow servers. It can handle pure-voice, multimedia, and blended environments, enabling routing of each media type based on appropriate criteria.

In the simplest terms, routing is the process of sending an interaction to a target, for example, directing an incoming telephone call or an incoming email to an agent.


O (Roteamento Universal) Universal Routing é uma parte da Plataforma Genesys que fornece a principal funcionalidade de gerenciamento de interação.

O Universal Routing pode direcionar as interações de uma ampla variedade de plataformas, como comutadores de operadora gratuita, PBXs ou ACDs locais, IVRs, PBXs IP, servidores de e-mail, servidores web e servidores de fluxo de trabalho. Ele pode lidar com ambientes de voz pura, multimídia e combinados, permitindo o roteamento de cada tipo de mídia com base em critérios apropriados.


Em termos mais simples, roteamento é o processo de enviar uma interação para um alvo, por exemplo, direcionar uma chamada telefônica ou um e-mail para um agente.

![image](https://user-images.githubusercontent.com/52088444/157887916-dba7e0b2-acbc-4159-a8b0-c6356ea8c677.png)

In practice, many steps must be taken between the arrival of an interaction, the selection and use of a target. Not all interactions should go to the same target, choices must be made in order to determine the best target for each interaction.

Each choice-point is an opportunity to make a decision based on the current situation—with the goal of getting the interaction delivered to the right target.

At a high level, Genesys Universal Routing incorporates three key areas for routing decisions:
- Customer
- Interaction
- Resources

All routing can be designed and developed according to specific business rules and objectives.


Na prática, muitos passos devem ser dados entre a chegada de uma interação, a seleção e o uso de um alvo. Nem todas as interações devem ir para o mesmo alvo, escolhas devem ser feitas para determinar o melhor alvo para cada interação.

Cada ponto de escolha é uma oportunidade de tomar uma decisão com base na situação atual – com o objetivo de entregar a interação ao alvo certo.

Em alto nível, o Genesys Universal Routing incorpora três áreas principais para decisões de roteamento:

- Cliente
- Interação
- Recursos

Todo roteamento pode ser projetado e desenvolvido de acordo com regras e objetivos de negócios específicos.


## 9.3 Universal Routing Based on the Genesys Platform(Roteamento Universal Baseado na Plataforma Genesys)


The business benefits of Genesys Universal Routing include improving customer satisfaction with more first call resolutions and less wait time. Customers experience less frustration because intelligent routing provides their specific information to the agent responding to their interaction. 

Results: 
Cross-sale and up-sale opportunities that can be maximized. Customer retention and loyalty also show improvements when the customer has a better experience.


Os benefícios comerciais do Genesys Universal Routing incluem a melhoria da satisfação do cliente com mais resoluções na primeira chamada e menos tempo de espera. Os clientes ficam menos frustrados porque o roteamento inteligente fornece suas informações específicas ao agente que responde à sua interação.

Resultados:
Oportunidades de venda cruzada(Cross-sale) e incentivar o cliente up-sale(Upselling é uma técnica de vendas em que um vendedor convida o cliente a comprar itens, atualizações ou outros complementos mais caros para gerar mais receita.) que podem ser maximizadas. A retenção e fidelização de clientes também mostram melhorias quando o cliente tem uma experiência melhor.

![image](https://user-images.githubusercontent.com/52088444/157888830-02635de7-b745-4480-a341-0f52d2cc9a4d.png)

Database-driven routing provides routing based on an enterprise’s customer database information, such as a customer’s account status or call history.

- Skills-based routing finds an agent who has the proper skills to assist the customer effectively, such as a preferred customer language choice.

- Service-level routing enables interactions to be routed according to specified service-level requirements for service types and customer segmentation. For example, a business might have two service-level requirements:

90% of interactions received from premier customers must be answered in 10 seconds.
80% of all interactions must be answered in 20 seconds.

O roteamento baseado em banco de dados fornece roteamento com base nas informações do banco de dados de clientes de uma empresa, como o status da conta de um cliente ou o histórico de chamadas.

- O roteamento baseado em habilidades encontra um agente que tenha as habilidades adequadas para ajudar o cliente de forma eficaz, como uma escolha de idioma preferencial do cliente.

- O roteamento de nível de serviço permite que as interações sejam roteadas de acordo com os requisitos de nível de serviço especificados para tipos de serviço e segmentação de clientes. Por exemplo, uma empresa pode ter dois requisitos de nível de serviço:

90% das interações recebidas de clientes premier devem ser respondidas em 10 segundos.
80% de todas as interações devem ser respondidas em 20 segundos.

## 9.4 What are Targets?(O que são Metas?)


A routing target is the configured object to which a routing application routes an interaction. In most routing applications, there is more than one target. For example, the Customer Service or Technical Support agent group, or queue 6602, may all be targets.


Um routing target (destino de roteamento) é o objeto configurado para o qual um aplicativo de roteamento roteia uma interação. Na maioria dos aplicativos de roteamento, há mais de um destino. Por exemplo, o grupo de agentes de Atendimento ao Cliente ou Suporte Técnico, ou a fila 6602, podem ser alvos.

ALVOS SÃO OBJETOS CONFIGURADOS, TAIS COMO:

![image](https://user-images.githubusercontent.com/52088444/157889452-1180dc96-199a-4c96-9ba7-689b990448ec.png)

Categories of target types include ACD Queues, Agents, Agent Groups, Places, Place Groups, Skills, and Routing Points. You may see these target types identified by abbreviations within Genesys. 

All objects are maintained using GAX, including information about DNs, queues, places, agents, and their skills and groupings.

GAX is the key to routing. It is the tool for developing the objects commonly required in routing strategies as well as provisioning a routing application to run on a specific Route Point.

As categorias de target types(tipos de destino) incluem Filas ACD, Agentes, Grupos de Agentes, Locais, Grupos de Locais, Habilidades e Pontos de Roteamento. Você pode ver esses tipos de destino identificados por abreviações no Genesys.

Todos os objetos são mantidos usando GAX, incluindo informações sobre DNs, filas, locais, agentes e suas habilidades e agrupamentos.

GAX é a chave para o roteamento. É a ferramenta para desenvolver os objetos normalmente necessários em estratégias de roteamento, bem como fornecer um aplicativo de roteamento para ser executado em um Route Point(ponto de rota) específico.

##  9.5 Example of Routing Application Logic(Exemplo de Lógica de Aplicação de Roteamento)


Each step in the following flowchart represents one stage or state that the interaction passes through during the decision-making process in routing. At each step, an action is performed and feedback on that action determines what step the interaction transitions to next.
 
For example, after an interaction arrives, information can be gathered such as information to identify the customer. Then, based on the product they have and their support level, the interaction could be handled differently such as being given a different priority or routed to different agents. Finally, the ideal target is specified. If that target is not available, the requirements can be relaxed to get the customer to a less ideal but available target in a 
timely manner.


Cada etapa no fluxograma a seguir representa um estágio ou estado pelo qual a interação passa durante o processo de tomada de decisão no roteamento. Em cada etapa, uma ação é executada e o feedback sobre essa ação determina para qual etapa a interação passa para a próxima.
 
Por exemplo, depois que uma interação chega, informações podem ser coletadas, como informações para identificar o cliente. Então, com base no produto que eles têm e em seu nível de suporte, a interação pode ser tratada de maneira diferente, como receber uma prioridade diferente ou roteada para diferentes agentes. Finalmente, o alvo ideal é especificado. Se essa meta não estiver disponível, os requisitos podem ser relaxados para levar o cliente a uma meta menos ideal, mas disponível em um
maneira oportuna.

![image](https://user-images.githubusercontent.com/52088444/157890427-c46c4961-9d45-46d3-96e7-37a54c27ec69.png)

![image](https://user-images.githubusercontent.com/52088444/157890541-35fd455e-2e95-4f52-8f3c-28aa68630481.png)


![image](https://user-images.githubusercontent.com/52088444/157890643-5a240148-0aa1-42b1-9f42-75cf62ad33b9.png)

![image](https://user-images.githubusercontent.com/52088444/157912162-24a2b761-aad2-44ea-a01c-3c87c5a31d40.png)

This concept is what powers our Genesys Routing Solution and allows for different, complex and powerful routing applications to be built to deliver the right interaction to the right resource at the right time.

Esse conceito é o que impulsiona nossa solução de roteamento Genesys e permite que aplicativos de roteamento diferentes, complexos e poderosos sejam criados para fornecer a interação certa para o recurso certo no momento certo.


##  9.6 Genesy Routing Components

A routing application is a set of decisions and instructions that tells the Genesys Routing Solution how to handle and where to direct interactions under different circumstances. 

Think of a routing application as a structured set of choice-points, each of which analyzes some aspect of the current interaction. The data that a strategy uses to analyze an interaction includes facts related to the interaction itself, the customer initiating the interaction, the state of the contact center, the particular point in time, and so on. 

At any given choice-point, only one of several possible outcomes can be optimal. Routing determines which outcome is optimal and sends the interaction along a specified route accordingly.

Routing includes a set of components that will enables intelligent distribution of interactions throughout the enterprise, those components are the following:


Um aplicativo de roteamento é um conjunto de decisões e instruções que informam à Genesys Routing Solution como lidar e para onde direcionar as interações em diferentes circunstâncias.

Pense em um aplicativo de roteamento como um conjunto estruturado de pontos de escolha, cada um dos quais analisa algum aspecto da interação atual. Os dados que uma estratégia usa para analisar uma interação incluem fatos relacionados à própria interação, o cliente que iniciou a interação, o estado do contact center, o momento específico e assim por diante.

Em qualquer ponto de escolha, apenas um dos vários resultados possíveis pode ser ótimo. O roteamento determina qual resultado é ideal e envia a interação ao longo de uma rota especificada de acordo.

O roteamento inclui um conjunto de componentes que permitirá a distribuição inteligente de interações em toda a empresa, esses componentes são os seguintes:


**Composer**

Composer is Genesys’ consolidated application development tool that uses the State Chart XML (SCXML) industry standard development language to create routing applications:

O Composer é uma ferramenta consolidada de desenvolvimento de aplicativos da Genesys que usa a linguagem de desenvolvimento padrão do setor State Chart XML (SCXML) para criar aplicativos de roteamento:

- SCXML

   - Open Standard
   - XML-based markup language

- Stored on a Web Application Server

The following image presents an example of a routing application built in Composer.


- SCXML

   - Padrão Aberto
   - Linguagem de marcação baseada em XML

- Armazenado em um servidor de aplicativos da Web

A imagem a seguir apresenta um exemplo de um aplicativo de roteamento criado no Composer.


![image](https://user-images.githubusercontent.com/52088444/157914349-ee8edb25-e011-4adc-a257-8a624efc9485.png)


**obs:If you have already used Universal Routing’s Interaction Routing Designer to build routing strategies, you will find similarities with Composer. Composer is an open system that uses a non-proprietary language called SCXML to build routing applications.**


**Se você já usou o Interaction Routing Designer do Universal Routing para criar estratégias de roteamento, encontrará semelhanças com o Composer. O Composer é um sistema aberto que usa uma linguagem não proprietária chamada SCXML para construir aplicativos de roteamento.**

**ORS**


The routing application is stored as SCXML (open standard). Orchestration Server (ORS) is responsible for executing the (SCXML) code and providing the data needed for more advanced routing flexibility. Some logic gets delegated to URS, whose responsibility is to provide a necessary routing service to the Orchestration Server.

- Store as SCXML (open standard)

- Executed by ORS

- Some logic delegated to URS



O aplicativo de roteamento é armazenado como SCXML (padrão aberto). O Orchestration Server (ORS) é responsável por executar o código (SCXML) e fornecer os dados necessários para uma flexibilidade de roteamento mais avançada. Alguma lógica é delegada ao URS, cuja responsabilidade é fornecer um serviço de roteamento necessário ao Orchestration Server.

- Armazenar como SCXML (padrão aberto)

- Executado por ORS

- Alguma lógica delegada ao URS



**URS**

Universal Routing Server (URS) is the routing engine that provides services to the Orchestration Server and selects the target. Universal Routing Server relies on the stat server for status and statistics about targets. It is responsible for verifying whether the targets are ready and available, and selecting a specific member of a targeted group to be sent an interaction.

- URS is a Routing engine that runs strategic target-seeking algorithms for each inbound interaction.
- It is capable of delivering over 100 calls per second.
- It is also known as “Router”.



O Universal Routing Server (URS) é o mecanismo de roteamento que fornece serviços ao Orchestration Server e seleciona o destino. O Universal Routing Server depende do Stat Server(servidor de estatísticas) para status e estatísticas sobre destinos. Ele é responsável por verificar se os alvos estão prontos e disponíveis e selecionar um membro específico de um grupo alvo para receber uma interação.

- URS é um mecanismo de roteamento que executa algoritmos estratégicos de busca de alvos para cada interação de entrada.
- É capaz de entregar mais de 100 chamadas por segundo.
- Também é conhecido como “Roteador”.

## 9.7 Routing in Action

 Let's now apply and observe an example of a Routing application and see the Genesys Routing Solution in action.

 
Vamos agora aplicar e observar um exemplo de um aplicativo de roteamento e ver a solução de roteamento Genesys em ação.


**Genesys Beyond Training Contact Center Scenario(Cenário de Contact Center Genesys Beyond Training)**

A customer wants to contact the Genesys Beyond training company for a specific service and for further information around their product offerings. They have been presented a contact number to call the company on a 1-800 6671, which is a dedicated service for Engage Customers only.

The system performs IVR options playing corresponding messages. The customer selects an option from a menu. Genesys Routing will take these collected digits and map them to a target, which is an agent skill using a Virtual Agent Group (VAG) expression. If no skilled agents are available, the target expands to the overflow which is represented by ACD Queue 6602.

The Agents will then be presented by a screen-pop displaying attach data on their desktops. This shows the department and product data. The customer data will also be included where applicable. (Check diagram in Business flow section.).


Um cliente deseja entrar em contato com a empresa de treinamento Genesys Beyond para obter um serviço específico e obter mais informações sobre suas ofertas de produtos. Eles receberam um número de contato para ligar para a empresa no número 1-800 6671, que é um serviço dedicado apenas para clientes do Engage.

O sistema executa as opções IVR reproduzindo as mensagens correspondentes. O cliente seleciona uma opção de um menu. O Genesys Routing pegará esses dígitos coletados e os mapeará para um destino, que é uma habilidade do agente usando uma expressão de Grupo de Agentes Virtuais (VAG). Se nenhum agente qualificado estiver disponível, o destino se expandirá para o estouro que é representado pela ACD Queue 6602.

**Business Flow(Fluxo de negócios)**


The flow below describes the use case from the perspective of the caller and contact center agent. The following diagram shows the business flow of the use case.

O fluxo abaixo descreve o caso de uso da perspectiva do chamador e do agente do contact center. O diagrama a seguir mostra o fluxo de negócios do caso de uso.

![image](https://user-images.githubusercontent.com/52088444/157916680-c811539b-3d8a-4e02-98d8-4cb05631057d.png)

## 9.8 OPM

Contact centers would like to provide users the ability to change routing information quickly and easily. Genesys provides Operational Parameter Management(OPM)—modifying routing information to react quickly to the needed changes.

Os centros de contato gostariam de fornecer aos usuários a capacidade de alterar as informações de roteamento de forma rápida e fácil. A Genesys fornece Operational Parameter Management (OPM)—modificando as informações de roteamento para reagir rapidamente às mudanças necessárias.


Use GAX to change these values: 

- Announcements
- Open hours
- Target
- Agent screen pop
- Emergencies


Use GAX para alterar estes valores:

- Anúncios
- Horário de funcionamento
- Alvo
- Tela pop do agente
- Emergências

**Operational Parameter Management Examples(OPM)**

There are numerous routing items that you can change in GAX. You can change announcements or music files to be played by Media Server, open and close times, holidays, targets, attached data for agent screen pop, skill levels, and so forth.

Example:

You can change open and close times for the Accounts department and set the announcement that will play when the department is closed (Accounts Close Announcement). In this example, a routing application has been configured to get this information and check if the current time is between the open and close time. If it is, the routing application routes the call to an agent. If the current time is outside of the open and close time, the routing application sends the call to the Media Server for the closed announcement.


Existem vários itens de roteiro que podem ser alterados no GAX. Você pode alterar anúncios ou arquivos de música a serem reproduzidos pelo Media Server, horários de abertura e fechamento, feriados, alvos, dados anexados para pop de tela do agente, níveis de habilidade e assim por diante.

Exemplo:

Você pode alterar os horários de abertura e fechamento do departamento de contas e definir o anúncio que será reproduzido quando o departamento for fechado (Anúncio de fechamento de contas). Neste exemplo, um aplicativo de roteamento foi configurado para obter essas informações e verificar se o horário atual está entre o horário de abertura e fechamento. Se for, o aplicativo de roteamento roteará a chamada para um agente. Se o horário atual estiver fora do horário de abertura e fechamento, o aplicativo de roteamento enviará a chamada ao Media Server para o anúncio fechado.

**Routing Parameters**

A routing application receives the routing information that you have changed in the GAX. Composer users must configure the corresponding application to receive and act on the routing information changed in GAX.

- GAX provides role-based administration to display only the information that a specific user needs.
- GAX provides data validation for operational parameters after they have been set up.
- The receiving routing application must be configured to accept the data that has been changed in the GAX.


Parâmetros de roteamento

Um aplicativo de roteamento recebe as informações de roteamento que você alterou no GAX. Os usuários do Composer devem configurar o aplicativo correspondente para receber e atuar nas informações de roteamento alteradas no GAX.

- GAX fornece administração baseada em função para exibir apenas as informações que um usuário específico precisa.
- GAX fornece validação de dados para parâmetros operacionais depois de configurados.
- O aplicativo de roteamento de recebimento deve ser configurado para aceitar os dados que foram alterados no GAX.

![image](https://user-images.githubusercontent.com/52088444/157919004-efa44f99-2143-42c4-bdc4-a1062b920369.png)

![image](https://user-images.githubusercontent.com/52088444/157919383-87f0eb41-a5d5-4b7b-a3a8-be0099d9e9af.png)


##  9.9 Configuring Operational Parameter Management(Configurando o Gerenciamento de Parâmetro Operacional)

In Genesys Administrator Extension, the Routing Parameters menu provides operational parameter management.

There are three Operational Parameters menu options:

-  Parameters—You specify individual items that a routing application or voice application will use. Genesys Rules System uses operational parameters to facilitate greater business agility.
- Group Templates—You group the individual items together (Parameters).
- Parameter Groups—You specify values for all the items (Parameters) in the Parameter Group Template.

No Genesys Administrator Extension, o menu Routing Parameters fornece gerenciamento de parâmetros operacionais.

Existem três opções de menu de Parâmetros Operacionais:

- Parâmetros—Você especifica itens individuais que um aplicativo de roteamento ou um aplicativo de voz usará. O Genesys Rules System usa parâmetros operacionais para facilitar uma maior agilidade nos negócios.
- Modelos de grupo—Você agrupa os itens individuais (Parâmetros).
- Grupos de Parâmetros—Você especifica valores para todos os itens (Parâmetros) no Modelo de Grupo de Parâmetros.


## 9.10 Parameter Groups

Parameter Groups are the sets of Operational Parameters that are associated with a routing application. They are first deployed as Parameter Group Templates. When needed, you can use this screen to assign values to the Operational Parameters. 

When ORS executes a routing application, the values of the Operational Parameters in the associated Parameter Group are incorporated into the call flow.

Grupos de Parâmetros são os conjuntos de Parâmetros Operacionais associados a um aplicativo de roteamento. Eles são implantados primeiro como modelos de grupo de parâmetros. Quando necessário, você pode usar esta tela para atribuir valores aos Parâmetros Operacionais.

Quando o ORS executa um aplicativo de roteamento, os valores dos Parâmetros Operacionais no Grupo de Parâmetros associado são incorporados ao fluxo de chamadas.

![image](https://user-images.githubusercontent.com/52088444/157921054-dae115a8-963e-454d-bd37-37415343b62c.png)



## 9.11 Learning Summary

Now that you have completed this chapter, you should be able to do the following: 

1 - Recall Genesys Routing.

2 - Describe ORS and URS.
3 - Describe Composer.

4 - Explain a Simple Routing Scenario. 

5 - Describe the use of Parameter groups with Routing.

6 - Use GAX to set values in Parameter Groups.


## 9.11 Resumo de Aprendizagem

Agora que você concluiu este capítulo, você deve ser capaz de fazer o seguinte:

1 - Recupere o roteamento Genesys.

2 - Descrever ORS e URS.
3 - Descreva o Compositor.

4 - Explique um cenário de roteamento simples.

5 - Descrever o uso de Grupos de Parâmetros com Roteamento.

6 - Use GAX para definir valores em Grupos de Parâmetros.

## 9.12 Learning Check


Question
01/03
Genesys Composer is an Eclipse-based development environment that supports the development of routing applications (SCXML).

True( VERDADEIRO)

False


Question
02/03
Universal Routing Server is the routing engine that runs strategic target-seeking algorithms for inbound interactions.

True (VERDADEIRO)

False


Question
03/03
Orchestration Server is responsible for executing SCXML based logic.

True(VERDADEIRO)

False