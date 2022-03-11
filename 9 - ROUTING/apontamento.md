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
Oportunidades de venda cruzada(Cross-sale) e up-sale que podem ser maximizadas. A retenção e fidelização de clientes também mostram melhorias quando o cliente tem uma experiência melhor.

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

