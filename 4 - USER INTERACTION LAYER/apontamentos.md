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


## 4.7 Breadcrumbs

Genesys configuration objects are in folders. (Folder names may be specific to your contact center.)
Os objetos de configuração do Genesys estão em pastas. (Os nomes das pastas podem ser específicos do seu contact center.)

![image](https://user-images.githubusercontent.com/52088444/157460480-d2def49c-4272-4ce7-be4e-de114bc5fb73.png)

Breadcrumbs are located directly beneath the tabs. This navigation path shows the tab/menu selections that brought you to the currently active part of the interface. You can also select any entry in this path to go directly to that part of the interface. Home is the Configuration Manager home.

Breadcrumbs  estão localizadas diretamente abaixo das guias. Este caminho de navegação mostra as seleções de guia/menu que o levaram à parte ativa da interface no momento. Você também pode selecionar qualquer entrada neste caminho para ir diretamente para essa parte da interface. Home é a casa do Configuration Manager.

## 4.8 Tenant

This list appears only in multi-tenant configuration environments.
Essa lista aparece apenas em ambientes de configuração multilocatário.

![image](https://user-images.githubusercontent.com/52088444/157463244-57086838-e96c-46a7-a796-0b0896143234.png)

Use this list to select the objects that are used by all tenants in the environment or only those belonging to a specific tenant. A multi-tenant environment is one in which several companies are using the same set of Genesys software, where each company is referred to as a tenant.

Use esta lista para selecionar os objetos que são usados ​​por todos os locatários no ambiente ou apenas aqueles que pertencem a um locatário específico. Um ambiente multilocatário é aquele em que várias empresas estão usando o mesmo conjunto de software Genesys, em que cada empresa é chamada de locatário.

## 4.9 Online Help

GAX has context-sensitive online help. The help topic is automatically provided based on the action you are performing. Online help has well-documented information on functions and options. You can also search for a specific topic. To access Help, click the question mark found on the header.

GAX tem ajuda online sensível ao contexto. O tópico de ajuda é fornecido automaticamente com base na ação que você está executando. A ajuda online tem informações bem documentadas sobre funções e opções. Você também pode pesquisar um tópico específico. Para acessar a Ajuda, clique no ponto de interrogação encontrado no cabeçalho.

Online help may require a Support Login. Contact Genesys Customer Care for more information.
A ajuda online pode exigir um Login de Suporte. Entre em contato com o Atendimento ao cliente da Genesys para obter mais informações.

![image](https://user-images.githubusercontent.com/52088444/157463830-7d46cfb5-46fa-4b18-a48d-1ab045bce566.png)

## 4.10 User Tools and Preferences(Ferramentas e preferências do usuário)

GAX enables you to customize the interface to suit your personal preferences. These preferences take effect each time you log in to GAX from any web browser.
O GAX permite que você personalize a interface para atender às suas preferências pessoais. Essas preferências entram em vigor sempre que você faz login no GAX a partir de qualquer navegador da web.


![image](https://user-images.githubusercontent.com/52088444/157464234-f4559953-60a0-4d95-8b2b-feb0a5b0e9e7.png)


To open the User Tools and Preferences menu, click your username in the Header bar. The User Tools and Preferences menu contains the following options:


- About
- Change Password
- User Preferences
- System Preferences
- Set Current Page as Home
- Log Out

Para abrir o menu Ferramentas e preferências do usuário, clique no seu nome de usuário na barra de cabeçalho. O menu Ferramentas e preferências do usuário contém as seguintes opções:


- Sobre
- Mudar senha
- Preferências de usuário
- Preferências do Sistema
- Definir a página atual como inicial
- Sair

**Para abrir o menu Ferramentas e preferências do usuário, clique no seu nome de usuário na barra de cabeçalho. O menu Ferramentas e preferências do usuário contém as seguintes opções:


- Sobre
- Mudar senha
- Preferências de usuário
- Preferências do Sistema
- Definir a página atual como inicial

**About**

You can click the About option to view information about your installation and about the Configuration Server to which you are connected.
Você pode clicar na opção Sobre para visualizar informações sobre sua instalação e sobre o Servidor de Configuração ao qual você está conectado.

![image](https://user-images.githubusercontent.com/52088444/157464689-f84511c5-cc14-4ddd-9701-9dbc57c82960.png)

**Set Current Page as Home(Definir a página atual como inicial)**

The Set Current Page as Home option is also found under the GAX User Tools and Preferences menu. You can choose the Set Current Page as Home option to use the currently displayed page as the home page for your GAX user account. 

A opção Definir página atual como página inicial também é encontrada no menu Ferramentas e preferências do usuário GAX. Você pode escolher a opção Definir página atual como inicial para usar a página exibida no momento como a página inicial da sua conta de usuário GAX.

**Change Password**

Using GAX, you can change your password with the Change Password menu option. To access this option, go to the User Tools and Preferences menu on the Header bar and click Change Password. The current user’s login name is then displayed. You are required to enter your existing password and enter the new password twice. 

Your password change for the application takes effect the next time you log in.


Usando o GAX, você pode alterar sua senha com a opção de menu Alterar senha. Para acessar esta opção, vá para o menu Ferramentas e Preferências do Usuário na barra de Cabeçalho e clique em Alterar Senha. O nome de login do usuário atual é então exibido. Você deve digitar sua senha existente e digitar a nova senha duas vezes.

Sua alteração de senha para o aplicativo entrará em vigor na próxima vez que você efetuar login.

![image](https://user-images.githubusercontent.com/52088444/157465186-71a96cdd-829e-4eca-bd06-1e0d4e977f6e.png)

The user’s password is encrypted within GAX (as well as in GA and the Configuration Database). Transport of encrypted passwords between Configuration Server and clients is secure.

A senha do usuário é criptografada no GAX (assim como no GA e no banco de dados de configuração). O transporte de senhas criptografadas entre o Configuration Server e os clientes é seguro.

**User Preferences**

In GAX, the User Preferences drop-down list contains the following preferences:

- **Advanced**—Lets you set the level of logging detail for the GAX log file (Debug, Info, Warning, Error, or Off to turn off logging).

**Locale**—Lets you set your individual user preferences for language, date format, start of week (Sunday or Monday), number format, and time zone.

No GAX, a lista suspensa User Preferences contém as seguintes preferências:

- **Avançado**—Permite definir o nível de detalhes de registro para o arquivo de registro GAX (Depuração, Informações, Aviso, Erro ou Desativado para desativar o registro).

- **Locale**—Permite que você defina suas preferências de usuário individuais para idioma, formato de data, início de semana (domingo ou segunda-feira), formato de número e fuso horário.

- **Gerenciador de Configuração** —Permite definir as preferências de exibição do Gerenciador de Configuração (Mostrar DBID, Mostrar Recente e Número máximo de itens recentes a serem exibidos).
- **Configuration Manager** —Lets you set the display preferences for Configuration Manager (Show DBID, Show Recent, and Maximum number of recent items to display).

![image](https://user-images.githubusercontent.com/52088444/157465787-ae2bdb31-431b-4b75-aebf-b3d9de1962ba.png)

Be sure to click Save after changing any of the user preferences.
Certifique-se de clicar em Salvar após alterar qualquer uma das preferências do usuário.

**System Preferences**

In GAX, the System Preferences drop-down list contains three options – Throttling, Locale, and Agent Management.
No GAX, a lista suspensa System Preferences contém três opções – Throttling, Locale e Agent Management.

**Throttling(limitação)**

Throttling lets you set the number of simultaneous changes that are sent to the Configuration Server. Change the Bulk Update Batch Size field to specify how many bulk updates for configuration objects can be executed simultaneously. The default value is 300.

A value of 0 indicates that there will be no throttling of changes for configuration objects (all requested operations will be sent to the Configuration Server without delay). You can enter 0 or any positive integer in this field.

A limitação permite definir o número de alterações simultâneas que são enviadas ao Configuration Server. Altere o campo Tamanho do lote de atualização em massa para especificar quantas atualizações em massa para objetos de configuração podem ser executadas simultaneamente. O valor padrão é 300.

Um valor de 0 indica que não haverá limitação de alterações para objetos de configuração (todas as operações solicitadas serão enviadas ao Configuration Server sem demora). Você pode inserir 0 ou qualquer número inteiro positivo neste campo.

**Locale**

Locale lets you set your overall GAX preferences for language, date format, start of week (Sunday or Monday), number format, and time zone.
A localidade permite que você defina suas preferências gerais do GAX para idioma, formato de data, início da semana (domingo ou segunda-feira), formato de número e fuso horário.

![image](https://user-images.githubusercontent.com/52088444/157466849-215f5322-246d-486b-89ee-901a988cd80d.png)

**Agent Management(Gerenciamento de Agentes)**

Agent Management

Agent Management lets you choose whether the Agents window is displayed using the Cloud layout or Premise layout. If you select Hidden, the Agent menu is not displayed on the GAX header and then there is no option to add agents using the Agent window. 

When you change this option you must log off and log back in to see your changes take effect. By default, the Agents menu is hidden.


O Gerenciamento de Agentes permite que você escolha se a janela Agentes é exibida usando o layout Cloud ou o layout Premise. Se você selecionar Oculto, o menu Agente não será exibido no cabeçalho GAX e não haverá opção para adicionar agentes usando a janela Agente.

Ao alterar esta opção, você deve fazer logoff e fazer login novamente para ver suas alterações entrarem em vigor. Por padrão, o menu Agentes fica oculto.

![image](https://user-images.githubusercontent.com/52088444/157467158-81ff6811-50a4-4654-9c0a-fcde2a63e88c.png)

Settings in the User Preferences menu take precedence over settings in the System Preferences menu.

For example, if the System Preferences language setting is English (US) and the User Preferences language setting is different, GAX uses the User Preferences language setting.

As configurações no menu Preferências do usuário têm precedência sobre as configurações no menu Preferências do sistema.

Por exemplo, se a configuração de idioma das Preferências do sistema for Inglês (EUA) e a configuração de idioma das Preferências do usuário for diferente, o GAX usará a configuração de idioma das Preferências do usuário.

## 4.11 Security Based on Login

Roles and Permissions affect what you can see and what you can do when you log on to GAX.
For example, if you have two different users—each with a different set of permissions and roles—when each user logs on, they would see a different interface in GAX that would allow them to do different things.

One user with fewer permissions and a restricted role would see only the Dashboard option on the GAX Header, as shown in the following image.

Funções e permissões afetam o que você pode ver e o que pode fazer ao fazer logon no GAX.
Por exemplo, se você tiver dois usuários diferentes, cada um com um conjunto diferente de permissões e funções, quando cada usuário fizer logon, eles verão uma interface diferente no GAX que permitirá que eles façam coisas diferentes.

![image](https://user-images.githubusercontent.com/52088444/157468551-3e9d0f88-e4e8-47cc-aaeb-0579bd1a2582.png)

The other user who has more permissions would have access to all of the options on the GAX header, as shown in the following image.
O outro usuário que tiver mais permissões teria acesso a todas as opções do cabeçalho GAX, conforme mostrado na imagem a seguir.

![image](https://user-images.githubusercontent.com/52088444/157468658-1542588c-0e5c-4b11-95d7-ff233386edb7.png)

The interface can also vary based on implementation. It may appear differently in your own work environment than it does in the classroom.
A interface também pode variar com base na implementação. Pode parecer diferente em seu próprio ambiente de trabalho do que na sala de aula.

## 4.12 Learning Summary(Resumo de aprendizagem)

Now that you have completed this chapter, you should be able to do the following: 
 1 - Recall major functions of the User Interaction Layer.
2 - Describe GAX.
3 - Describe the major sections of GAX.
4 - Observe different levels of access in GAX.
5 - Change user passwords using GAX.


Agora que você concluiu este capítulo, você deve ser capaz de fazer o seguinte:
 1 - Recupere as principais funções da camada de interação do usuário.
2 - Descreva o GAX.
3 - Descreva as principais seções do GAX.
4 - Observe os diferentes níveis de acesso no GAX.
5 - Altere as senhas dos usuários usando GAX.


