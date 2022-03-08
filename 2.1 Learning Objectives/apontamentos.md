# CHAPTER 2 - INTRODUCTION TO GENESYS FRAMEWORK, ROUTING, AND REPORTING

## Depois de concluir este capítulo, você deve ser capaz de fazer o seguinte:

1 - Descrever a arquitetura em camadas do framework.
2 -Descrever as principais funções das camadas do framework.
3 -Descrever o roteamento Genesys.
4 -Descrever o Genesys Reporting.


## 2.2 Framework Layered Architecture(Arquitetura em camadas de estrutura)

Genesys Framework is the foundation for all Genesys Multicloud CX based interaction management systems.
O Genesys Framework é a base para todos os sistemas de gerenciamento de interação baseados em Genesys Multicloud CX. 

![image](https://user-images.githubusercontent.com/52088444/157244500-c25ecf57-ae17-4297-897a-548b543c1c17.png)

O Genesys Framework consiste em um grande número de componentes especializados. Para facilitar a compreensão da finalidade desses diversos componentes,
podemos agrupá-los em “camadas” de acordo com o tipo de funcionalidade que fornecem. Cada camada é responsável por algumas das principais funções exigidas 
pela Plataforma Genesys.

- Configuration Layer—distributes configuration information to the entire platform(distribui informações de configuração para toda a plataforma.)

- Management Layer—manages logging of all server processes and allows management and monitoring of solutions(gerencia o registro de todos os processos do servidor e permite
o gerenciamento e o monitoramento de soluções.).

- User Interaction Layer—provides a comprehensive user interface to configure, monitor, and control the management environment(fornece uma interface de usuário abrangente para 
configurar, monitorar e controlar o ambiente de gerenciamento.).

- Media Layer—provides software translation between the platform and the various external network interfaces, such as telephone switches, IVRs, and corporate email servers
(fornece tradução de software entre a plataforma e as várias interfaces de rede externas, como centrais telefônicas, IVRs e servidores de e-mail corporativos.).

- Services Layer—calculates statistics and provides resource status(calcula estatísticas e fornece o status do recurso.).

O Management Framework fornece as seguintes funções de administração: Configuração, Controle de Acesso, Controle de Solução, Processamento de Alarmes, 
Solução de Problemas e Gerenciamento de Falhas.
Management Framework provides you with the following administration functions: Configuration, Access Control, Solution Control, Alarm Processing, 
Troubleshooting, and Fault Management.

## 2.3 Configuration Layer

Functions of Configuration Layer:

O Configuration Layer (Camada de Configuração) processa e armazena os dados do contact center exigidos pela Genesys Solutions para trabalhar em um ambiente específico.

PBXs, computadores host, aplicativos de servidor, etc. compõem o ambiente do contact center. Habilidades, agentes e afins constituem os recursos disponíveis.

Essa Layer(camada) também controla o acesso do usuário às funções e dados da solução. Para resumir, O Configuration Layer (Camada de Configuração)  fornece três 
funções principais para as soluções Framework e Genesys: Configuração, Controle de Acesso e Reconfiguração e Notificação Dinâmicas(Configuration, Access Control,
and Dynamic Reconfiguration and Notification.)

![image](https://user-images.githubusercontent.com/52088444/157245963-cca8dd79-1b9f-4e03-a19b-77f3a9bb3f64.png)

**Configuration**

The Configuration Layer centralizes the processing and storage of all of the configuration data required for Genesys Solutions to work within a particular environment. Users can enter contact center data in one location, and the Configuration Layer will send the changes to the rest of Genesys. This helps to ensure consistency, reliability, and integrity of the data.    

A camada de configuração centraliza o processamento e armazenamento de todos os dados de configuração necessários para que a Genesys Solutions funcione em um ambiente específico. Os usuários podem inserir os dados do contact center em um local, e a camada de configuração enviará as alterações para o restante da Genesys. Isso ajuda a garantir consistência, confiabilidade e integridade dos dados.

**Access Control**

The Configuration Layer enables system administrators to set and verify users’ permissions for access to solution functions and data.
A Camada de Configuração permite que os administradores do sistema definam e verifiquem as permissões dos usuários para acesso às funções e dados da solução.


**Dynamic Reconfiguration and Notification**


Changes made to the configuration during runtime are typically propagated throughout the Genesys system without the need to restart applications. In some rare, well-documented cases, dynamic change propagation and notification does not occur and a restart of the application is required.

Changes made to the configuration during runtime are typically propagated throughout the Genesys system without the need to restart applications. In some rare, well-documented cases, dynamic change propagation and notification does not occur and a restart of the application is required.

## 2.4 Management Layer

Functions of Management Layer:

The Management Layer provides a kind of centralized mission control.
A camada de gerenciamento fornece um tipo de controle de missão centralizado.

![image](https://user-images.githubusercontent.com/52088444/157246705-1527dd8d-c6a5-4b7e-8ad1-e93d9382b284.png)

**Solution Control**

The Management Layer manages startup, monitoring, and shutdown of applications and solutions.
A camada de gerenciamento gerencia a inicialização, monitoramento e desligamento de aplicativos e soluções.

**Alarm Processing**

The Management Layer defines and detects conditions critical to solution operation. Alarms are triggered by log events and other conditions. Alarm reactions provide administrative alerts and application fault management.
A camada de gerenciamento define e detecta condições críticas para a operação da solução. Os alarmes são acionados por eventos de log e outras condições. As reações de alarme fornecem alertas administrativos e gerenciamento de falhas do aplicativo.


**Log Events Interface**

The Management Layer hosts a user-oriented, unified logging system with advanced storage, sorting, and viewing capabilities.
A camada de gerenciamento hospeda um sistema de registro unificado e orientado ao usuário com recursos avançados de armazenamento, classificação e visualização.

**Fault Handling**

The Management Layer detects and corrects situations that might cause problems for solution operation. Fault Handling encompasses the ability to switch processing to a standby application or auto-restart a failed application, among other functions.
A camada de gerenciamento detecta e corrige situações que podem causar problemas para a operação da solução. O Tratamento de Falhas abrange a capacidade de alternar o processamento para um aplicativo em espera ou reiniciar automaticamente um aplicativo com falha, entre outras funções.



## 2.5 User Interaction Layer


Functions of User Interaction Layer

The User Interaction Layer provides centralized web-based functionality and interfaces for:

-Configuring, monitoring, and controlling applications and solutions in the environment. 
- Deploying Genesys Installation packages.

A camada de interação do usuário fornece funcionalidades e interfaces centralizadas baseadas na Web para:

-Configuração, monitoramento e controle de aplicações e soluções no ambiente.
- Implantação de pacotes de instalação do Genesys.

![image](https://user-images.githubusercontent.com/52088444/157247731-4a9f7792-8a14-48aa-858e-df7208b33d4d.png)

**Configuration and Monitoring**

Making configuration changes to the environment and resources also the ability to control applications and solutions.
Fazer alterações de configuração no ambiente e nos recursos também permite controlar aplicativos e soluções.

**Deployment**

Installing Genesys components to any computer on the network using the Genesys Deployment Agent (a Management Layer component).

The User Interaction Layer consists of two components, Genesys Administrator Extension (GAX) and Genesys Administrator (GA), that are
both deployed on a Web server and can be accessed using a Web browser. This layer provides a comprehensive user interface to configure, 
monitor, and control your Genesys environment.
Instalação de componentes Genesys em qualquer computador da rede usando o Genesys Deployment Agent (um componente da camada de gerenciamento).

A camada de interação do usuário consiste em dois componentes, Genesys Administrator Extension (GAX) e Genesys Administrator (GA), que são 
implantados em um servidor da Web e podem ser acessados usando um navegador da Web. Essa camada fornece uma interface de usuário abrangente para configurar, 
monitorar e controlar seu ambiente Genesys.


## 2.6 Media Layer

Functions of Media Layer

The Media Layer serves as the center of any Genesys system, receiving and distributing messages as directed by the other components. The Media Layer enables solutions to communicate with a variety of media including traditional telephony systems, voice over IP, email, instant messaging, and the Web. This layer also provides the mechanism for the attached data distribution within and across solutions.

A camada de mídia serve como o centro de qualquer sistema Genesys, recebendo e distribuindo mensagens conforme orientado pelos outros componentes. A camada de mídia permite que as soluções se comuniquem com uma variedade de mídias, incluindo sistemas de telefonia tradicionais, voz sobre IP, e-mail, mensagens instantâneas e a Web. Essa camada também fornece o mecanismo para a distribuição de dados anexados dentro e entre soluções.

![image](https://user-images.githubusercontent.com/52088444/157258959-eee9bd04-6271-4a23-9616-a949a7c4094e.png)

**External Interfaces(Interfaces externas)**

The Media Layer allows communication with a variety of telephony and multimedia systems. This allows the Genesys solutions to have control over customer interactions.
A camada de mídia permite a comunicação com uma variedade de sistemas de telefonia e multimídia. Isso permite que as soluções Genesys tenham controle sobre as interações com o cliente.

**Interaction Tracking(Acompanhamento de interação)**

The Media Layer tracks interactions that are in process. For example, for the life of a call, it maintains call information such as connection ID (a unique identifier), Automatic Number Identification (ANI), Dialed Number Identification (DNIS), and custom attached data.

A camada de mídia rastreia as interações que estão em processo. Por exemplo, durante a vida de uma chamada, ele mantém informações da chamada, como ID de conexão (um identificador exclusivo), Identificação Automática de Número (ANI), Identificação de Número Discado (DNIS) e dados anexados personalizados.

**Attached Data Distribution(Attached Data Distribution)**

The Media Layer supports the distribution of data attached to interactions within and across solutions. Attached data enables screen pop and intelligent transfers. In addition, routing decisions can be made based on attached data.

A camada de mídia suporta a distribuição de dados anexados a interações dentro e entre soluções. Os dados anexados permitem o pop-up da tela e transferências inteligentes. Além disso, as decisões de roteamento podem ser tomadas com base nos dados anexados.



## 2.7 Services Layer



Functions of Services Layer

The Services Layer generates statistical and status data used for interaction processing and contact center reporting.

A Camada de Serviços gera dados estatísticos e de status usados para processamento de interação e relatórios do contact center.

![image](https://user-images.githubusercontent.com/52088444/157259820-94357cd3-7b75-464f-a89a-5a9656764e2f.png)


**Compilation of Statistics and Object Status(Compilação de Estatísticas e Status do Objeto)**

Stat Server collects statistics and calculates the status of contact center objects (Agents, Places, DNs, and their groups).
O Stat Server coleta estatísticas e calcula o status dos objetos do contact center (Agentes, Locais, DNs e seus grupos).

calcule o tempo médio de espera
Calcule quanto tempo o agente está pronto

![image](https://user-images.githubusercontent.com/52088444/157260821-bb1751ca-cf31-4c97-8bfa-0c185c0c94a4.png)


## 2.8 Genesys Framework Review

Let’s review the functional examples of each layer.

![image](https://user-images.githubusercontent.com/52088444/157260995-c8a06a04-23c2-4c1f-a7f2-c07d0e4fda46.png)

- Camada de Configuração(Configuration Layer): Processe e armazene os dados do contact center
- Camada de gerenciamento(Managment Layer): gerencie aplicativos Genesys
- Camada de interação do usuário(User Interaction Layer): Implanta, provisiona e gerencia objetos Genesys.
- Media Layer(Media Layer): interface externa que cria e mantém o objeto de chamada
- Camada de Serviços(Services Layer): Calcula estatísticas e fornece status de recursos


The five layers of the Genesys Framework provide the above functionalities whether you are executing routing or outbound campaigns. These layers use telephony-only or multimedia or implement a multi-site global enterprise or a single center startup to function. The framework supports interactions with different physical switches and different media concurrently across sites.

All of these components of the Genesys Platform and the Genesys Solution Suite are used together to resolve Contact Center concerns such as managing across the enterprise and using existing switch hardware. The centralized management generates alarms and reactions so system administrators are aware of failures that affect the Genesys Platform, such as disconnection or errors in the application, and enables them to immediately address the issue, minimizing the impact of possible downtime. The availability of customer data and the ability to attach, distribute, and edit it promotes improved first call resolution numbers and supports your efforts to provide excellent customer support.

As cinco camadas do Genesys Framework fornecem as funcionalidades acima, quer você esteja executando campanhas de roteamento ou de saída. Essas camadas usam apenas telefonia ou multimídia ou implementam uma empresa global de vários locais ou uma inicialização de centro único para funcionar. A estrutura oferece suporte a interações com diferentes switches físicos e diferentes mídias simultaneamente nos sites.

Todos esses componentes da Plataforma Genesys e do Genesys Solution Suite são usados ​​juntos para resolver problemas do Contact Center, como gerenciamento em toda a empresa e uso de hardware de switch existente. O gerenciamento centralizado gera alarmes e reações para que os administradores do sistema estejam cientes das falhas que afetam a Plataforma Genesys, como desconexão ou erros na aplicação, e permite que eles resolvam o problema imediatamente, minimizando o impacto de possíveis paralisações. A disponibilidade dos dados do cliente e a capacidade de anexá-los, distribuí-los e editá-los promovem números de resolução de primeira chamada aprimorados e apoiam seus esforços para fornecer excelente suporte ao cliente.

![image](https://user-images.githubusercontent.com/52088444/157263781-aeab98dd-1e5d-4e78-83ca-c58e9c3cefd1.png)

O Genesys Routing and Reporting também usa o Genesys Framework.

## 2.9 Routing

Para muitas organizações, as mudanças nos requisitos de atendimento ao cliente exigem novos recursos que criam uma experiência de usuário melhor, mais eficaz e recompensadora. Um fator crítico para o sucesso é o roteamento inteligente, a capacidade de direcionar a interação do cliente para o recurso correto, independentemente do canal ou fonte de interação, e manter automaticamente o histórico de relacionamento com o cliente e as informações do último agente em qualquer chamada transferida.

**Contact Center Challenges**


- How to select the best agent to serve any given customer service request

- How to manage remote agents at branch offices, outsourcers, and homes

- How to coordinate different types of customer interactions

- How to manage distributed sites

**Desafios do Contact Center**


-Como selecionar o melhor agente para atender qualquer solicitação de atendimento ao cliente

- Como gerenciar agentes remotos em filiais, terceirizados e residências

- Como coordenar diferentes tipos de interações com o cliente

- Como gerenciar sites distribuídos

![image](https://user-images.githubusercontent.com/52088444/157264841-59687897-171d-446e-bed3-ff34ee3c11f6.png)

**Routing Challenges**

Routing can be challenging with disjointed resources such as agents and information. Many of the following challenges face call centers today:

- Selecting a proper agent to serve any given customer service request
- Managing remote agents at branch offices, outsourcers, and homes
- Incorporating contact centers in different locations
- Coordinating different types of customer interactions
- Leveraging enterprise resources outside contact centers
- Tracking, collecting, and reporting all customer interactions
- Utilizing enterprise databases to support customer interactions
- Measuring and managing overall customer service performance

O roteamento pode ser desafiador com recursos desconexos, como agentes e informações. Muitos dos seguintes desafios enfrentam os call centers hoje:

- Selecionar um agente adequado para atender a qualquer solicitação de atendimento ao cliente
- Gerenciamento de agentes remotos em filiais, terceirizados e residências
- Incorporação de contact centers em diferentes locais
- Coordenar diferentes tipos de interação com o cliente
- Alavancando os recursos da empresa fora dos contact centers
- Rastreamento, coleta e relatório de todas as interações com o cliente
- Utilização de bancos de dados corporativos para apoiar as interações com o cliente
- Medir e gerenciar o desempenho geral do serviço ao cliente

## Getting to Know Genesys Universal Routing(Conhecendo o Genesys Universal Routing)

Universal Routing is a part of the Genesys Platform that provides the core interaction management functionality.
O Roteamento Universal é uma parte da Plataforma Genesys que fornece a principal funcionalidade de gerenciamento de interação.

![image](https://user-images.githubusercontent.com/52088444/157265466-64ca0cb9-173e-4fbd-9885-0e697613d064.png)

In the simplest terms, routing is the process of sending an interaction to a target. Examples include directing an incoming telephone call or an incoming email to an agent.

In practice, many steps must be taken between the arrival of an interaction and the selection and use of a target. Not all interactions should go to the same target, choices must be made in order to determine the best target for each interaction.

Each choice-point is an opportunity to make a decision based on the current situation with the goal of getting the interaction delivered to the right target.

At a high level, Genesys Universal Routing incorporates three key areas for routing decisions: Customer, interaction, and resources. All routing can be designed and developed according to specific business rules and objectives. Using the customer/account info/segment, interaction types, and various kinds of resource availability, a wide variety of routing strategies are formed to meet the business needs and goals of the enterprise.

Em termos mais simples, roteamento é o processo de enviar uma interação para um destino. Os exemplos incluem direcionar uma chamada telefônica recebida ou um e-mail recebido para um agente.

Na prática, muitos passos devem ser dados entre a chegada de uma interação e a seleção e uso de um alvo. Nem todas as interações devem ir para o mesmo alvo, escolhas devem ser feitas para determinar o melhor alvo para cada interação.

Cada ponto de escolha é uma oportunidade de tomar uma decisão com base na situação atual com o objetivo de entregar a interação ao alvo certo.

Em alto nível, o Genesys Universal Routing incorpora três áreas principais para decisões de roteamento: Cliente, interação e recursos. Todo roteamento pode ser projetado e desenvolvido de acordo com regras e objetivos de negócios específicos. Usando as informações/segmentos do cliente/conta, tipos de interação e vários tipos de disponibilidade de recursos, uma ampla variedade de estratégias de roteamento é formada para atender às necessidades e objetivos de negócios da empresa.

## 2.10 Genesys Routing Capabilities(Recursos de Roteamento Genesys)

**Genesys Universal Routing:**

- Optimizes resources for customer service operations.
- Minimizes cost of transfer by matching best resources.
- Enhances customer experience and improves agent productivity.

- Otimiza recursos para operações de atendimento ao cliente.
- Minimiza o custo de transferência combinando os melhores recursos.
- Melhora a experiência do cliente e melhora a produtividade do agente.

**Flexible routing applications are developed to meet business needs and objectives:**
Os aplicativos de roteamento flexíveis são desenvolvidos para atender às necessidades e objetivos de negócios:

- **Database-driven routing** –provides routing based on an enterprise’s customer database information, such as a customer’s account status or call history.
- **Skills-based routing**–finds an agent who has the proper skills to assist the customer effectively, such as a customer’s preferred language.
- **Service-level routing**–enables interactions to be routed according to specified service-level requirements for service types and customer segmentation. For example, a business might have two service-level requirements: 90% of interactions received from premier customers must be answered in 10 seconds and 80% of all interactions must be answered in 20 seconds.
    - Universal Routing Server can expand or contract the number of agents available to maintain these service-level requirements.
    - This type of routing also supports a more advanced form of skills-based routing, which rates a skill or skill set according to its importance level.
- **Statistical routing**–allows you to route interactions based on the value of a statistic. The following are commonly used statistics:

    - StatAgentLoading is used for distributing interactions among agents evenly within an agent group. This predefined statistic can be used to select an agent based on two criteria: Least number of busy DNs and longest time in Ready state.
    - StatAgentOccupancy is used for distributing interactions among agents fairly within a group in a voice contact center. This predefined statistic can be used as agent selection criteria in an agent surplus scenario.

- **Relationship** -based routing–takes personalization to another level by enabling your most valuable customers to reach specific agents or groups of agents based on assignment or last-contact metrics.

- **Multi-site routing** –supports routing across the contact center. Multiple sites—and all available agent resources—serve as one virtual contact center. Interactions are routed according to business criteria and best available agent, regardless of location. Genesys T-Servers support switches that transfer interactions between sites, so you can route interactions to contact centers at different sites and between different departments at different sites. This results in reduced administrative expense and increased workforce flexibility.

- **Multimedia routing** –enables the routing of multiple types of interactions, such as email, chat, and SMS within a contact center. Routing applications can control automatic email receipts and email replies according to content analysis rules, which learn to respond specifically to your customer base.

- **Business priority routing** –encompasses additional selection criteria that Genesys can consider when routing interactions including priority, interaction age, “What-If” wait time, and service objective risk factor.



