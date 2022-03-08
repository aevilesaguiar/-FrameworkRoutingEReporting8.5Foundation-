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


