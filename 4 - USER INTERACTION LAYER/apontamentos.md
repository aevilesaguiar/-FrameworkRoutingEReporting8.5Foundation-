## Learning Objectives

After completing this chapter, you should be able to do the following: 

1- Recall major functions of the User Interaction Layer.

2 - Describe GAX.

3- Describe the major sections of GAX.

4- Observe different levels of access in GAX.

5-Change user passwords using GAX.

Depois de concluir este capítulo, você deve ser capaz de fazer o seguinte:

1- Recupere as principais funções da camada de interação do usuário.

2 - Descreva o GAX.

3- Descreva as principais seções do GAX.

4- Observe os diferentes níveis de acesso no GAX.

5-Alterar senhas de usuários usando GAX.


## 4.2 Review Functions of User Interaction Layer

**Functions of User Interaction Layer**

Functions of User Interaction Layer

The User Interaction Layer provides centralized web-based functionality and interfaces for the following:

- Configure, monitor, and control applications and solutions.
- Deploy Genesys installation packages on any host.
- Control access based on roles.

Funções da camada de interação do usuário

A camada de interação do usuário fornece funcionalidades e interfaces centralizadas baseadas na web para o seguinte:
- Configurar, monitorar e controlar aplicativos e soluções.
- Implante pacotes de instalação do Genesys em qualquer host.
- Controle de acesso baseado em funções.

**Examples:**

- Create agents.

- View alarms.

- Monitor applications (started, stopped).

The GA has similar functionality to GAX but will be primarily used on the Genesys Multicloud CX Outbound Solution to manage and operate Outbound Campaigns and calling lists.

Exemplos:

- Criar agentes.

- Ver alarmes.

- Monitorar aplicativos (iniciados, parados).

O GA tem funcionalidade semelhante ao GAX, mas será usado principalmente na solução de saída Genesys Multicloud CX para gerenciar e operar campanhas de saída
e listas de chamadas.

## 4.3 The Bigger Picture

User Interaction Layer:
- Connects to Configuration Server
- Logs in
- Controls access
- Provides information

Genesys Administrator Extension and Genesys Administrator are both used to monitor, configure, and manage the day-to-day operations of your contact center. 
The contact center objects are categorized and presented in both of these Web-based interfaces. There are similarities and differences. Both Genesys Administrator 
Extension (which is the newer interface) and Genesys Administrator can be used together in an implementation. You will be learning GAX interface in this class.

Camada de interação do usuário:
- Conecta-se ao servidor de configuração
- Entra
- Controla o acesso
- Fornecem informações

Genesys Administrator Extension e Genesys Administrator são usados para monitorar, configurar e gerenciar as operações diárias do seu contact center. 
Os objetos do contact center são categorizados e apresentados em ambas as interfaces baseadas na Web. Existem semelhanças e diferenças. Tanto o Genesys Administrator
Extension (que é a interface mais recente) quanto o Genesys Administrator podem ser usados juntos em uma implementação. Você aprenderá a interface GAX nesta aula.

![image](https://user-images.githubusercontent.com/52088444/157455888-1e31c974-ba9d-4043-8907-b336d549bbf9.png)

## 4.4 GAX

GAX is a customized companion product from its GA.

- Next generation interface for configuring, monitoring, and controlling your Genesys environment
- Can be used in parallel with GA

Adds more flexibility and support for the additional platforms, along with an improved user interface.

Genesys Administrator Extension provides user-friendly interfaces that perform the following functionalities:

**Configuration Object Management**: Provides a user-friendly interface for users to create and manage configuration objects such as user accounts, agent groups, roles, Directory Numbers (DNs), and places.

**Operational Parameter Management**: Provides the ability to create a user-friendly interface with data validation that enables the management of operational parameters. These operational parameters can be used as input to routing applications that enable a business user to modify the behavior of routing without having to change the associated application. You can change the parameter in a safe and controlled manner without having to modify the routing application.


GAX é um produto complementar personalizado de seu GA.

- Interface de última geração para configurar, monitorar e controlar seu ambiente Genesys

- Pode ser usado em paralelo com GA

Adiciona mais flexibilidade e suporte para as plataformas adicionais, juntamente com uma interface de usuário aprimorada.

Genesys Administrator Extension fornece interfaces amigáveis ​​que executam as seguintes funcionalidades:

**Gerenciamento de objetos de configuração**: fornece uma interface amigável para que os usuários criem e gerenciem objetos de configuração, como contas de usuários, grupos de agentes, funções, números de diretório (DNs) e locais.

**Gerenciamento de Parâmetros Operacionais**: Oferece a capacidade de criar uma interface amigável com validação de dados que permite o gerenciamento de parâmetros operacionais. Esses parâmetros operacionais podem ser usados ​​como entrada para aplicativos de roteamento que permitem que um usuário de negócios modifique o comportamento do roteamento sem precisar alterar o aplicativo associado. Você pode alterar o parâmetro de maneira segura e controlada sem precisar modificar o aplicativo de roteamento.


Operational Parameter Management is covered in the Framework Routing & Reporting 8.5 Operation.

See the Genesys Administrator Extension 8.5 documentation for additional functionality not covered in this class.


O Gerenciamento de Parâmetros Operacionais é abordado no Framework Routing & Reporting 8.5 Operation.

Consulte a documentação do Genesys Administrator Extension 8.5 para obter funcionalidades adicionais não abordadas nesta classe.

## 4.5 Accessing with a Web Browser

GAX is a web-based interface that runs on a web application server.
GAX é uma interface baseada na web que é executada em um servidor de aplicativos da web.

Supported browsers are Microsoft Internet Explorer (10.x or 11.x), Mozilla Firefox (5 or higher), Safari (6 or higher), or Chrome (8 or higher).

GAX now uses an embedded Jetty instance as the Web application server. As a result, Tomcat is no longer required to use GAX. Previous releases required the third-party product Apache Tomcat.
O GAX agora usa uma instância Jetty incorporada como servidor de aplicativos da Web. Como resultado, o Tomcat não precisa mais usar o GAX. As versões anteriores exigiam o produto de terceiros Apache Tomcat.

**Jetty é um servidor HTTP e Servlet Container 100% escrito em Java. É o grande concorrente do Tomcat que ficou famoso por ter sido utilizado como o servlet container do JBoss antigamente. A grande vantagem do Jetty com relação ao Tomcat é a sua fácil configuração.**

**Logging In**

![image](https://user-images.githubusercontent.com/52088444/157457145-22483241-7b3b-4a89-a84d-b29accc1b34a.png)


**Logging into GAX**

![image](https://user-images.githubusercontent.com/52088444/157456736-eb7b38c1-18fc-4b35-a005-420089efd847.png)

GAX login makes a connection to Configuration Server to authenticate the user logging in.

Open a Web browser such as Internet Explorer or Mozilla Firefox, and go to the URL (Web site address) that your system administrator provides for accessing GAX. Enter your assigned username and password, then click the Log In button.


**Entrando no GAX**

O login do GAX faz uma conexão com o Configuration Server para autenticar o login do usuário.

Abra um navegador da Web, como o Internet Explorer ou o Mozilla Firefox, e vá para a URL (endereço do site) que o administrador do sistema fornece para acessar o GAX. Digite seu nome de usuário e senha atribuídos e clique no botão Login.

##  4.6 User Interface

![image](https://user-images.githubusercontent.com/52088444/157457462-1cac4b81-3cd5-47ee-88c5-4f1e0e056a2b.png)

The GAX header contains six tabs, each corresponding to a major functional module:

- **Dashboard** —Helps you to monitor your contact center. It shows a high-level summary of the current operations of your environment.

- **Agents**—Helps you to add, modify, and delete agents in your environment. This menu is only displayed when activated in the system preferences settings.

- **Configuration Manager**—Enables users to create and manage configuration objects such as users, agent groups, skills, access groups, roles, DNs, and places.

- **Routing Parameters**—Works in conjunction with a routing application, voice application (working with Genesys Voice Platform), or the Genesys Rules System to allow users to change routing information in GAX.

- **Administration**—Allows administrators to deploy Genesys products to remote locations.

- **Centralized Logs**—Allows users to access log events that are recorded in one central location for convenient access and solution-level troubleshooting.

O cabeçalho GAX contém seis guias, cada uma correspondendo a um módulo funcional principal:

- **Painel** —Ajuda você a monitorar seu contact center. Ele mostra um resumo de alto nível das operações atuais do seu ambiente.

- **Agentes**—Ajuda você a adicionar, modificar e excluir agentes em seu ambiente. Este menu só é exibido quando ativado nas configurações de preferências do sistema.

- **Gerenciador de configuração** — permite que os usuários criem e gerenciem objetos de configuração, como usuários, grupos de agentes, habilidades, grupos de acesso, funções, DNs e locais.

- **Parâmetros de roteamento**—Funciona em conjunto com um aplicativo de roteamento, um aplicativo de voz (trabalhando com a Genesys Voice Platform) ou o Genesys Rules System para permitir que os usuários alterem as informações de roteamento no GAX.

- **Administração**—Permite que os administradores implantem produtos Genesys em locais remotos.

- **Logs centralizados**—Permite que os usuários acessem eventos de log que são registrados em um local central para acesso conveniente e solução de problemas em nível de solução.
