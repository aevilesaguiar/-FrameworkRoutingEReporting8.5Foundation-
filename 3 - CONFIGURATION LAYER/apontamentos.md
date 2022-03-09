## 3.1 Learning Objectives( 3.1 Learning Objective)


Depois de concluir este capítulo, você deve ser capaz de fazer o seguinte:

- Recupere as principais funções da Configuration Layer (Camada de Configuração).

- Descreva o  Configuration Server.(Servidor de Configuração).

- Explicar os tipos de instalação (Single-Site, Multi-Site e Multi-Tenant).

- Descrever Permissões.

- Descrever o controle de acesso baseado em função( role-based access control.).


## 3.2 Review Functions of Configuration Layer

**Functions of Configuration Layer**


- Centralized configuration

- Access control

- Dynamic reconfiguration and notification

Examples:

-Creating and storing agents

-Creating groups

-Associating agents with groups

- Configuração centralizada

- Controle de acesso

- Reconfiguração dinâmica e notificação

Exemplos:

-Criação e armazenamento de agentes

-Criando grupos

-Associar agentes a grupos


The Configuration Layer processes and stores the contact center data required by Genesys Solutions to work in a particular environment.

PBXs, host computers, server applications, etc. comprise the contact center environment.
Skills, agents, etc., are the available resources within the contact center.

This layer also controls user access to solution functions and data. To summarize, the Configuration Layer provides two key functions to the Framework and the Genesys solutions: Configuration and Access Control.

A Camada de Configuração processa e armazena os dados do contact center exigidos pela Genesys Solutions para trabalhar em um ambiente específico.

PBXs, computadores host, aplicativos de servidor, etc. compõem o ambiente do contact center.
Habilidades, agentes, etc., são os recursos disponíveis dentro do contact center.

Essa camada também controla o acesso do usuário às funções e dados da solução. Para resumir, a Camada de Configuração fornece duas funções principais para as soluções Framework e Genesys: Configuração e Controle de Acesso.

**Configuration**

The Configuration Layer centralizes the processing and storage of all the configuration data required for Genesys Solutions to work within a particular environment. Users can enter contact center data in one location and the Configuration Layer will send the changes to the rest of Genesys. This helps to ensure consistency, reliability, and integrity of the data.    

A camada de configuração centraliza o processamento e armazenamento de todos os dados de configuração necessários para que a Genesys Solutions funcione em um ambiente específico. Os usuários podem inserir os dados do contact center em um local e a camada de configuração enviará as alterações para o restante da Genesys. Isso ajuda a garantir consistência, confiabilidade e integridade dos dados.

**Access Control**

A Camada de Configuração permite que os administradores do sistema definam e verifiquem as permissões dos usuários para acesso às funções e dados da solução.

**Dynamic Reconfiguration and Notification(Reconfiguração e Notificação Dinâmica)**

Changes made to the configuration during runtime are typically propagated throughout the Genesys system without the need to restart applications. In some rare well-documented cases, dynamic change propagation and notification does not occur and a restart of the application is required.

As alterações feitas na configuração durante o tempo de execução normalmente são propagadas por todo o sistema Genesys sem a necessidade de reiniciar os aplicativos. Em alguns casos raros e bem documentados, a propagação e a notificação de alterações dinâmicas não ocorrem e é necessário reiniciar o aplicativo.

## 3.3 Most Components Connect to Configuration Server(A maioria dos componentes se conecta ao servidor de configuração)**

![image](https://user-images.githubusercontent.com/52088444/157313753-240261c4-8174-4a0d-8c36-ebe930653170.png)

O Configuration Server fornece acesso centralizado ao Configuration Database. O acesso aos dados é baseado em permissões que os administradores podem conceder a qualquer usuário para qualquer objeto de configuração. O Configuration Server também mantém a integridade lógica dos dados de configuração e notifica os aplicativos sobre as alterações feitas nos dados.

Os clientes do Configuration Server, como o T-Server, não serão iniciados a menos que se conectem com sucesso ao Configuration Server. Isso ocorre principalmente porque a maioria dos aplicativos não pode executar nenhuma função essencial sem acesso aos dados de configuração. Os componentes pertencentes às demais camadas do Framework se conectam ao Configuration Server para obter informações sobre sua configuração. Componentes para roteamento, relatórios(reporting) e outras soluções também se conectam ao  Configuration Server.(Servidor de Configuração).
Os componentes não precisam permanecer conectados ao Configuration Server(Servidor de Configuração).para permanecerem operacionais. (Eles continuarão trabalhando com os dados de configuração que já leram em sua própria memória.) Em uma reconexão, eles receberão dados de configuração novos e/ou alterados que o Configuration Server mantém em um log de histórico para essa finalidade.

## Configuration Types


Existem três tipos principais de configuração de estrutura para escolher, dependendo dos requisitos de negócios: Single-Site, Multi-Site e Multi-Tenant.

**Site único versus vários sites**
**Single-Site Versus Multi-Site**


- Single-Site—This is the most basic configuration. A single-site contains all Genesys applications. Ownership of the environment, resources, administration, and utilization belongs to a single user.
- 
- Multi-Site—In a multi-site configuration, the environment is distributed. This can be viewed as multiple single-sites that are linked and able to pass contacts with user data between sites. Ownership of the environment, resources, administration, and utilization belongs to a single user.


- Single-Site—Esta é a configuração mais básica. Um único site contém todos os aplicativos Genesys. A propriedade do ambiente, recursos, administração e utilização pertence a um único usuário.

- Multi-Site—Em uma configuração multi-site, o ambiente é distribuído. Isso pode ser visto como vários sites únicos vinculados e capazes de passar contatos com dados do usuário entre sites. A propriedade do ambiente, recursos, administração e utilização pertence a um único usuário.

![image](https://user-images.githubusercontent.com/52088444/157447954-705ee15c-a017-4949-b04e-b9c1912e89a3.png)


A configuração de vários sites é o tipo mais comum.

**Multi-Tenant Configuration**

Multi-Tenant Configuration

A tenant is a single corporate entity with its own business goals, agents, strategies, switch configurations, etc. 

In a multi-tenant configuration, each client’s resources can be separately maintained in the same configuration database. All interactions can be managed by the same set of software components (Environment) using resources dedicated to each client.


Um locatário é uma única entidade corporativa com seus próprios objetivos de negócios, agentes, estratégias, configurações de switch, etc.

Em uma configuração multilocatário, os recursos de cada cliente podem ser mantidos separadamente no mesmo banco de dados de configuração. Todas as interações podem ser gerenciadas pelo mesmo conjunto de componentes de software (Ambiente) utilizando recursos dedicados a cada cliente.

Example:

A corporation that maintains a large contact center and sells its CTI services to a number of different corporate clients is demonstrated in the Multi-Tenant diagram below.

Uma corporação que mantém um grande contact center e vende seus serviços de CTI para vários clientes corporativos diferentes é demonstrada no diagrama Multi-Tenant abaixo.

![image](https://user-images.githubusercontent.com/52088444/157448329-804a575b-509f-4e91-b943-82b0858eb4a5.png)

The multi-tenant configurations can have a single physical location or can be distributed across multiple sites.

Genesys now recommends multi-tenant configurations for all implementations, even for just one company

As configurações de vários locatários podem ter um único local físico ou podem ser distribuídas em vários sites.

A Genesys agora recomenda configurações multilocatário para todas as implementações, mesmo para apenas uma empresa

## 3.5 Configuration Layer Provides Centralized Security(Configuration Layer Fornece Segurança Centralizada)

The security mechanism implemented in the Configuration Server allows the system administrator to define the level of access to any object as a whole for each valid user account. The access privileges of valid user accounts define what the user can and cannot do within the application. This section describes the various mechanisms in place, to ensure that the data is accessed only by authorized users.

O mecanismo de segurança implementado no Configuration Server permite ao administrador do sistema definir o nível de acesso a qualquer objeto como um todo para cada conta de usuário válida. Os privilégios de acesso de contas de usuário válidas definem o que o usuário pode e não pode fazer dentro do aplicativo. Esta seção descreve os vários mecanismos em vigor, para garantir que os dados sejam acessados ​​apenas por usuários autorizados.

There are two levels of security settings:

- Permissions—Controls access to configuration data (can be set per object/folder)(
Permissões—Controla o acesso aos dados de configuração (pode ser definido por objeto/pasta).

- Role-Based Access—Controls which functions or items are visible within graphical interfaces.
- Acesso Baseado em Função—Controla quais funções ou itens são visíveis nas interfaces gráficas.

**Permissions**

User authorization is provided by the combination of a set of elementary permissions as shown in the following table. This security mechanism implemented in the Configuration Server allows the system administrator to define the level of access for any account with respect to any object separately.

A autorização do usuário é fornecida pela combinação de um conjunto de permissões elementares, conforme mostrado na tabela a seguir. Este mecanismo de segurança implementado no Configuration Server permite que o administrador do sistema defina o nível de acesso para qualquer conta em relação a qualquer objeto separadamente.

![image](https://user-images.githubusercontent.com/52088444/157449206-89248113-81d6-4faf-87e7-1fefcdece0d6.png)


The access permissions of authenticated user accounts define what the user can and cannot do within the application.
As permissões de acesso de contas de usuário autenticadas definem o que o usuário pode e não pode fazer dentro do aplicativo.

![image](https://user-images.githubusercontent.com/52088444/157449400-55bf20c8-67e4-4bde-a3c8-b909e3516860.png)

**Role-Based Access**

Roles are a functionality-based security feature for graphical interfaces (Genesys Administrator, Genesys Administrator Extension, Workspace Desktop Edition, etc.). They control the features of the graphical interface that a user can access. The system administrator (or a designated individual) defines GUI access functionality and in some cases what can be done (viewed, modified, deleted) to the objects. They are application-specific and must be defined for each application that supports them.

As funções são um recurso de segurança baseado em funcionalidade para interfaces gráficas (Genesys Administrator, Genesys Administrator Extension, Workspace Desktop Edition, etc.). Eles controlam os recursos da interface gráfica que um usuário pode acessar. O administrador do sistema (ou um indivíduo designado) define a funcionalidade de acesso à GUI e, em alguns casos, o que pode ser feito (visualizado, modificado, excluído) para os objetos. Eles são específicos do aplicativo e devem ser definidos para cada aplicativo que os suporta.

Role Example:

Assume that you are assigned a role which grants you the privilege to access all of the features of Workspace. Another agent is assigned a role with fewer privileges in the Workspace application. When you log in, you will see a different Workspace interface as shown in the example below. While you can view all the available options, you will notice that a few sections are hidden from the other agent.

Suponha que você recebeu uma função que concede a você o privilégio de acessar todos os recursos do Workspace. Outro agente é atribuído a uma função com menos privilégios no aplicativo Workspace. Ao fazer login, você verá uma interface de área de trabalho diferente, conforme mostrado no exemplo abaixo. Embora você possa visualizar todas as opções disponíveis, você notará que algumas seções estão ocultas do outro agente.

![image](https://user-images.githubusercontent.com/52088444/157449875-89ff9a07-e431-4e93-88cb-13e8305bbafd.png)

##  3.6 Learning Summary

Now that you have completed this chapter, you should be able to do the following: 

1 -  Recall major functions of the Configuration Layer.

2 - Describe the Configuration Server.

3 - Explain the installation types (Single-Site, Multi-Site, and Multi-Tenant).

4 - Describe Permissions.

5- Describe role-based access control.


Agora que você concluiu este capítulo, você deve ser capaz de fazer o seguinte:

1 - Recupere as principais funções da Camada de Configuração.

2 - Descreva o Servidor de Configuração.

3 - Explique os tipos de instalação (Single-Site, Multi-Site e Multi-Tenant).

4 - Descreva as Permissões.

5- Descrever o controle de acesso baseado em função.

## 3.7 Learning Check


Question
01/06
Select all functions that apply to the Configuration Layer.
- Access control
- Dynamic reconfiguration and notification
- Configuration

Question
02/06
Permissions control access to the specific features in graphical interfaces. (FALSE)

Question
03/06
The three major types of Genesys installations are: Single-site, Multi-site,
and Multi-tenant.(VERDADEIRO)

Question
04/06
A tenant is a single corporate entity with its own business goals, agents, strategies, switch configurations, etc.(VERDADEIRO)


Question
05/06
What is the function of Configuration Server? 

Maintains the logical integrity of configuration data (VERDADEIRO)

Monitor and control applications  

Tracks call information within the Contact Center  

Question
06/06
Which component provides central repository for all configuration data?

Configuration Server 

Config DB (VERDADEIRO)

Stat Server
