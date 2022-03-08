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

