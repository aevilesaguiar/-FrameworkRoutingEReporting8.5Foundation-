
## A.2 User Interaction Layer—GA

## 2.1 Accessing with a Web Browser(Acessando com um navegador da Web)

GA is a Web application which is accessed using a Web browser.

GA é um aplicativo da Web que é acessado usando um navegador da Web.

![image](https://user-images.githubusercontent.com/52088444/157937200-33a3080b-87be-4ee1-9728-8a2a7721337d.png)


Supported browsers are Microsoft Internet Explorer (10.x or 11.x), Mozilla Firefox (5 or higher), Safari (6 or higher), or Chrome (8 or higher).

Os navegadores suportados são Microsoft Internet Explorer (10.x ou 11.x), Mozilla Firefox (5 ou superior), Safari (6 ou superior) ou Chrome (8 ou superior).

## 2.2 Logging In

![image](https://user-images.githubusercontent.com/52088444/157948364-521ab789-5419-4e8e-828d-13d0cd01a645.png)

GA makes a connection to the Configuration Server to authenticate the user logging in.

**Logging into GA**

Open a web browser, such as Internet Explorer or Mozilla Firefox, and go to the URL (web site address) that your administrator provides for accessing Genesys Administrator. Enter your assigned Username and Password, then click Log In. You may also need to fill in values for Application, Host Name, and Port. These would be provided to you by your system administrator and tell Genesys Administrator how to contact your Configuration Server:

- Application—Name of Configuration Manager Application object with which it is associated
- Host Name—Name of computer on which Configuration Server runs 
-  Port—Number of communication port that client applications use to connect to the Configuration Server

O GA faz uma conexão com o Servidor de Configuração para autenticar o login do usuário.

**Entrando no GA**

Abra um navegador da web, como o Internet Explorer ou o Mozilla Firefox, e vá para a URL (endereço do site) que seu administrador fornece para acessar o Genesys Administrator. Digite seu nome de usuário e senha atribuídos e clique em Login. Você também pode precisar preencher valores para Aplicativo, Nome do Host e Porta. Eles serão fornecidos a você pelo administrador do sistema e informarão ao Administrador da Genesys como entrar em contato com o servidor de configuração:

- Aplicativo—Nome do objeto Aplicativo do Configuration Manager ao qual está associado
- Nome do host—Nome do computador no qual o Configuration Server é executado
- Porta—Número da porta de comunicação que os aplicativos cliente usam para se conectar ao Servidor de Configuração

## 2.3 User Interface: Headers(Interface do usuário: cabeçalhos)

![image](https://user-images.githubusercontent.com/52088444/157948925-34c3678f-50d5-4042-8e3f-15c29a5a88bf.png)

## Genesys Administrator

The Genesys Administrator header contains (on the left) three tabs, each corresponding to a major functional module:

- Monitoring—The Monitoring tab enables you to monitor the overall operations and specific elements of your contact center.
- Provisioning—The Provisioning tab enables you to configure the objects and perform other tasks to provision your system.
- Operations—The Operations tab enables you to set up the operations in your contact center and perform other tasks related to its operation.

The same functionality is available in both Genesys Administrator Extension and  Genesys Administrator.

Example:

To monitor your environment, view an application status or an active alarm, you would use Dashboard in Genesys Administrator Extension. You would use Monitoring in  Genesys Administrator. 

The same functionality is present in both interfaces, just indifferently labeled modules.


## Administrador Genesys

O cabeçalho Genesys Administrator contém (à esquerda) três guias, cada uma correspondendo a um módulo funcional principal:

- Monitoramento—A guia Monitoramento permite monitorar as operações gerais e elementos específicos do seu contact center.
- Provisionamento—A guia Provisionamento permite configurar os objetos e realizar outras tarefas para provisionar seu sistema.
- Operações—A guia Operações permite que você configure as operações em seu contact center e execute outras tarefas relacionadas à sua operação.

A mesma funcionalidade está disponível no Genesys Administrator Extension e no Genesys Administrator.

Exemplo:

Para monitorar seu ambiente, visualizar o status de um aplicativo ou um alarme ativo, você usaria o Dashboard no Genesys Administrator Extension. Você usaria o Monitoring no Genesys Administrator.

A mesma funcionalidade está presente em ambas as interfaces, apenas módulos rotulados de forma indiferente.

## 2.4 Breadcrumbs

Genesys configuration objects are in folders. (Folder names may be specific to your contact center).

Os objetos de configuração do Genesys estão em pastas. (Os nomes das pastas podem ser específicos do seu contact center).

![image](https://user-images.githubusercontent.com/52088444/157950696-6077fb52-99b1-43c0-9cae-b8effe43cb12.png)


Breadcrumbs are located directly beneath the tabs. This navigation path (hence the term breadcrumbs) shows the tab/menu selections that brought you to the currently active part of the interface. You can also select any entry in this path to go directly to that part of the interface. Home is the Configuration Manager home.

Breadcrumbs  estão localizadas diretamente abaixo das guias. Este caminho de navegação (daí o termo breadcrumbs) mostra as seleções de guia/menu que levaram você à parte ativa da interface no momento. Você também pode selecionar qualquer entrada neste caminho para ir diretamente para essa parte da interface. Home é a casa do Configuration Manager.

## 2.5 Tenant(Locatário)

This list appears only in multi-tenant configuration environments.
Essa lista aparece apenas em ambientes de configuração multilocatário.

![image](https://user-images.githubusercontent.com/52088444/157951112-e4609add-1cc7-4e37-8e6a-12cd728913c0.png)

Use this list to select the objects that are used by all tenants in the Environment, or only those belonging to a specific Tenant. A Multi-Tenant environment is the one in which several companies are using the same set of Genesys software, each company is referred to as a Tenant.

Use esta lista para selecionar os objetos que são usados por todos os locatários no ambiente ou apenas aqueles que pertencem a um locatário específico. Um ambiente Multi-Tenant é aquele em que várias empresas estão usando o mesmo conjunto de software Genesys, cada empresa é chamada de Tenant.

##   2.6 Online Help

GA has context-sensitive Online Help. The help topic is automatically provided based on the action you are performing. Online Help has well-documented information on functions and options. You can also search for a specific topic. To get Help, click on the question mark found in the header.

O GA tem ajuda online sensível ao contexto. O tópico de ajuda é fornecido automaticamente com base na ação que você está executando. A Ajuda Online tem informações bem documentadas sobre funções e opções. Você também pode pesquisar um tópico específico. Para obter ajuda, clique no ponto de interrogação encontrado no cabeçalho.

![image](https://user-images.githubusercontent.com/52088444/157951523-4fff21a3-9bb8-4e96-be3b-14a9a0af7641.png)

## 2.7 User Tools and Preferences

GA enables you to customize the interface to suit your personal preferences. These preferences take effect each time that you, or anyone using your login credentials, logs into Genesys Administrator from any browser.

O GA permite que você personalize a interface de acordo com suas preferências pessoais. Essas preferências entram em vigor sempre que você, ou qualquer pessoa usando suas credenciais de login, fizer login no Genesys Administrator a partir de qualquer navegador.

GA—To open the User Tools and Preferences menu, click on Preferences button (shaped like a gear) in the Header Bar. 

GA allows you to customize the interface to suit your personal preferences. These preferences take effect each time that you, or anyone using your login credentials, logs into Genesys Administrator from any browser. 

Log out–Click the Log out option on the Genesys Administrator Header to exit the application, as shown in the following image. 

Click the Tools and Preferences button (shaped like a gear) to access the Preferences menu.

GA—Para abrir o menu Ferramentas e Preferências do Usuário, clique no botão Preferências (em forma de engrenagem) na Barra de Cabeçalho.

O GA permite que você personalize a interface de acordo com suas preferências pessoais. Essas preferências entram em vigor sempre que você, ou qualquer pessoa usando suas credenciais de login, fizer login no Genesys Administrator a partir de qualquer navegador.

Logout–Clique na opção Logout no Genesys Administrator Header para sair do aplicativo, conforme mostrado na imagem a seguir.

Clique no botão Ferramentas e Preferências (em forma de engrenagem) para acessar o menu Preferências.

![image](https://user-images.githubusercontent.com/52088444/157951818-7b58a68b-8be6-4bf7-80cb-6c71be75d6da.png)

**General Tab—Start Up Page**

In the general tab, click in the Startup page field that you see, in the preceding image. Next, select the view that you want to display when you first log in, as defined by selections in the main tabs and the Navigation panel. 

For example, if you use GA most often to configure applications, you can choose to display the list of applications (Provisioning tab > Environment > Applications) when you log in. The drop-down box contains all possible views currently defined in GA, represented by their navigation paths (breadcrumbs). The default is MONITORING > Environment > Dashboard (the Monitoring Dashboard).

In the Expand tasks panel automatically field, the checkbox is selected to have the Tasks panel expand automatically if there are tasks associated with the objects currently in view.
 
In the Show breadcrumbs field, the checkbox is selected to have the breadcrumbs appear in the Header.

**Guia Geral—Página Inicial**

Na guia geral, clique no campo Página de inicialização que você vê na imagem anterior. Em seguida, selecione a visualização que deseja exibir ao efetuar login pela primeira vez, conforme definido pelas seleções nas guias principais e no painel Navegação.

Por exemplo, se você usa o GA com mais frequência para configurar aplicativos, pode optar por exibir a lista de aplicativos (guia Provisionamento > Ambiente > Aplicativos) ao efetuar login. A caixa suspensa contém todas as visualizações possíveis atualmente definidas no GA, representadas pelos seus caminhos de navegação (breadcrumbs). O padrão é MONITORAMENTO > Ambiente > Painel (o Painel de Monitoramento).

No campo Expandir painel de tarefas automaticamente, a caixa de seleção é marcada para que o painel Tarefas seja expandido automaticamente se houver tarefas associadas aos objetos atualmente em exibição.
 
No campo Mostrar trilhas, a caixa de seleção é marcada para que as trilhas apareçam no cabeçalho.

**Monitoring/Environment(monitoramento/ambiente)**

![image](https://user-images.githubusercontent.com/52088444/157952291-0535990a-a223-4fde-97e5-a718c0145356.png)

In the Monitoring/Environment tab, shown in the preceding image, you can define the refresh interval for automatic refresh of certain displays (such as the Dashboard and the list of active alarms). Valid values are 5 to 600 seconds. The default value of the refresh interval is 20 seconds. To disable the automatic refresh, clear the checkbox.

Na guia Monitoring/Environment, mostrada na imagem anterior, você pode definir o intervalo de atualização para atualização automática de determinados displays (como o Dashboard e a lista de alarmes ativos). Os valores válidos são de 5 a 600 segundos. O valor padrão do intervalo de atualização é 20 segundos. Para desabilitar a atualização automática, desmarque a caixa de seleção.

**Provisioning**

In the Provisioning tab, shown in the following image, select the checkbox if you want to show the hidden options on the Options tab. The checkbox is not selected by default.

**Provisionamento**

Na guia Provisionamento, mostrada na imagem a seguir, marque a caixa de seleção se desejar mostrar as opções ocultas na guia Opções. A caixa de seleção não está marcada por padrão

![image](https://user-images.githubusercontent.com/52088444/157952723-9bcb8ee9-2bb9-451d-98b5-4df7850a1e7b.png)

**Change Your Password**

If you want to change your password, you can do so on the Password tab. Your Username, First and Last name, and Email address are displayed to remind you of the account for which you are changing the password. You will need to enter your old password, type in your new password twice, then save.

**Mude sua senha**

Se você quiser alterar sua senha, poderá fazê-lo na guia Senha. Seu nome de usuário, nome e sobrenome e endereço de e-mail são exibidos para lembrá-lo da conta para a qual você está alterando a senha. Você precisará digitar sua senha antiga, digite sua nova senha duas vezes e salve.

obs:The user’s password is encrypted within Genesys Administrator (as well as in the configuration Database). Transport of encrypted passwords between the Configuration Server and clients is secure.

obs:A senha do usuário é criptografada no Genesys Administrator (assim como no banco de dados de configuração). O transporte de senhas criptografadas entre o Servidor de Configuração e os clientes é seguro.

