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
-  o gerenciamento e o monitoramento de soluções.).

- User Interaction Layer—provides a comprehensive user interface to configure, monitor, and control the management environment(fornece uma interface de usuário abrangente para 
- configurar, monitorar e controlar o ambiente de gerenciamento.).

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
