
## 3.1 Persons/Users

Users can be created, configured, and administered using Genesys Administrator.

Os usuários podem ser criados, configurados e administrados usando o Genesys Administrator.

## 3.2 Creating Configuration Objects

You can define all configuration objects in the Genesys Administrator.

Você pode definir todos os objetos de configuração no Genesys Administrator.

## 3.3 Basics of Configuring Objects

Genesys Administrator can be used to define and configure objects.

If using GA, objects are defined and configured under the PROVISIONING tab.

Genesys Administrator (GA): Provisioning


O Genesys Administrator pode ser usado para definir e configurar objetos.

Se estiver usando GA, os objetos são definidos e configurados na guia PROVISIONING.

Administrador Genesys (GA): Provisionamento

To locate and manage your configuration objects using Genesys Administrator, navigate to the PROVISIONING tab. Here you will see the object types organized under folders, 
such as Accounts.

Para localizar e gerenciar seus objetos de configuração usando o Genesys Administrator, navegue até a guia PROVISIONING. Aqui você verá os tipos de objetos organizados em pastas,
como Contas.

![image](https://user-images.githubusercontent.com/52088444/157984640-47769c44-6492-4f93-b878-c13da107acc5.png)


Select the object types (folder) you wish to configure first. For example, if you want to configure Skills, click Accounts. The specific object types are shown within the folder. For example, to choose Skills, you would first go to the Accounts folder and then to Skills.

Selecione os tipos de objeto (pasta) que deseja configurar primeiro. Por exemplo, se você deseja configurar Habilidades, clique em Contas. Os tipos de objetos específicos são mostrados na pasta. Por exemplo, para escolher Habilidades, você deve ir primeiro para a pasta Contas e depois para Habilidades.

![image](https://user-images.githubusercontent.com/52088444/157984842-0937ea78-1ec6-45ab-9eee-7dac6aba40a7.png)

**Managing Objects(Gerenciando objetos)**

GA is used for managing objects in your Contact Center. This interfaces allow the creation, modification, and deletion of objects.

O GA é usado para gerenciar objetos em seu Contact Center. Essas interfaces permitem a criação, modificação e exclusão de objetos.

## 3.4 Creating a New Skill

**Genesys Administrator**

To create a Mandarin skill in GA, you would navigate to PROVISIONING > Accounts > Skills and then click New. Next, you would type in the Name Mandarin and then click Save and Close.

**Administrador Genesys**

Para criar uma habilidade de mandarim no GA, navegue até PROVISIONING > Accounts > Skills e clique em New. Em seguida, você digitaria o nome mandarim e, em seguida, clicaria em Salvar e fechar.

![image](https://user-images.githubusercontent.com/52088444/157984969-1b99d524-df5a-4ed6-a049-c5ca670235b8.png)

## 3.5 Creating a New Agent Group

Agent Groups can be created in Genesys Administrator. You must specify the desired Name for the agent group. This name can be referenced as a routing target and also for gathering reporting statistics.

Grupos de agentes podem ser criados no Genesys Administrator. Você deve especificar o Nome desejado para o grupo de agentes. Esse nome pode ser referenciado como destino de roteamento e também para coletar estatísticas de relatórios.

![image](https://user-images.githubusercontent.com/52088444/157985042-f9596155-d405-4205-b74c-84430678ca19.png)


Another option for creating new Agents is using Genesys Administrator. You will notice that creating a new Agent in Genesys Administrator feels very similar to creating a new Agent in Genesys Administrator Extension. The steps and folders are the same, but the interfaces look a little different. 

When you create a new User, there are common properties shared by both Agents and
Non-agents. 

To configure the new agent, navigate to PROVISIONING > Accounts > Users > New and complete the Configuration and Member of tabs of the User General section:

-Employee ID—Uniquely defines the person within the Genesys system. This is mandatory. The Human Resources team often provides Employee IDs.
- Username—Refers to the log in the person is assigned to gain access to Genesys GUI applications such as the Genesys Agent Desktop or custom soft phone applications. This is mandatory.
- Password—The password the person is assigned for Genesys GUI access.
- Member of Access Group–Determines what a user can and can't do (permissions) within an application based on which access groups the user is a member. Access groups are groups of users who need to have the same set of permissions for configuration objects in Genesys. Genesys provides four standard Access Groups: Agents, Supervisors, Managers, and Administrators. You can also create custom Access Groups. Further configuration is necessary. See the External Authentication Reference Guide for more details.
-  State Enabled—Defines whether or not the employee’s status is active. 
- Agent—Defines whether or not the person is an agent. When creating a new Person object in Configuration Manager, this flag is selected by default. If you are creating a non-agent Person object, you must clear this checkbox.

Outra opção para criar novos Agentes é usar o Genesys Administrator. Você notará que a criação de um novo agente no Genesys Administrator é muito semelhante à criação de um novo agente no Genesys Administrator Extension. As etapas e pastas são as mesmas, mas as interfaces parecem um pouco diferentes.

Quando você cria um novo usuário, há propriedades comuns compartilhadas por agentes e
Não agentes.

Para configurar o novo agente, navegue até PROVISIONING > Accounts > Users > New e complete as guias Configuration e Member of da seção User General:

-Employee ID—Define exclusivamente a pessoa dentro do sistema Genesys. Isso é obrigatório. A equipe de Recursos Humanos geralmente fornece IDs de funcionários.
- Nome de usuário—Refere-se ao login que a pessoa está designada para obter acesso aos aplicativos Genesys GUI, como o Genesys Agent Desktop ou aplicativos de softphone personalizados. Isso é obrigatório.
- Senha — A senha atribuída à pessoa para acesso ao Genesys GUI.
- Membro do grupo de acesso – determina o que um usuário pode e não pode fazer (permissões) em um aplicativo com base em quais grupos de acesso o usuário é membro. Grupos de acesso são grupos de usuários que precisam ter o mesmo conjunto de permissões para objetos de configuração no Genesys. A Genesys oferece quatro grupos de acesso padrão: Agentes, Supervisores, Gerentes e Administradores. Você também pode criar grupos de acesso personalizados. É necessária uma configuração adicional. Consulte o Guia de Referência de Autenticação Externa para obter mais detalhes.
- Estado Ativado—Define se o status do funcionário está ativo ou não.
- Agente—Define se a pessoa é ou não um agente. Ao criar um novo objeto Person no Configuration Manager, esse sinalizador é selecionado por padrão. Se você estiver criando um objeto Person não agente, deverá desmarcar esta caixa de seleção.

![image](https://user-images.githubusercontent.com/52088444/157985428-c42f53f7-585f-4d4b-80b2-5435d571a6cf.png)

Since the new user will be an agent, you must next configure the following extra 
Agent properties: 

 - Default Place—It's used only in rare cases that can’t work with Places (when a real-time association with a Place cannot be established through the login procedure).
- Capacity Rule—It's a script that limits the number and media type of interactions that can be distributed to this User. For example, one voice and two emails (see the Resource Capacity Planning Guide). These can be assigned at the level of the Agent, Place, and Tenant. 
- Agent Checkbox–Make sure this box is checked for an agent. 

Como o novo usuário será um agente, você deve configurar o seguinte extra
Propriedades do agente:

- Local padrão—É usado apenas em casos raros que não podem funcionar com locais (quando uma associação em tempo real com um local não pode ser estabelecida por meio do procedimento de login).
- Regra de Capacidade—É um script que limita o número e o tipo de mídia de interações que podem ser distribuídas a este Usuário. Por exemplo, uma voz e dois e-mails (consulte o Resource Capacity Planning Guide). Eles podem ser atribuídos no nível do Agente, Local e Locatário.
- Caixa de seleção do agente – certifique-se de que esta caixa esteja marcada para um agente.

![image](https://user-images.githubusercontent.com/52088444/157985740-4b913487-2027-4242-b779-0524a9e46289.png)


**Skills**—A complete description of each agent’s skill set enables complex routing decisions. Skills are defined in the Skills folder. They are selected and given Level values in this tab.

     1 - Click the drop-down arrow next to Agent Info, and you will see Skill Levels. Click Add.
     2 -Under Skills, click the search icon to browse the list of existing skills and select one or enter the name of a new skill you wish to add.
     3 - Assign a level from 1 to 10. 
     4 - Click OK.

**Habilidades**—Uma descrição completa do conjunto de habilidades de cada agente permite decisões de roteamento complexas. As habilidades são definidas na pasta Habilidades. Eles são selecionados e recebem valores de Nível nesta guia.

      1 - Clique na seta suspensa ao lado de Informações do Agente e você verá os Níveis de Habilidade. Clique em Adicionar.
      2 - Em Habilidades, clique no ícone de pesquisa para navegar na lista de habilidades existentes e selecione uma ou digite o nome de uma nova habilidade que deseja adicionar.
      3 - Atribua um nível de 1 a 10.
      4 - Clique em OK.

 **Agent Logins**—Each telephony agent has a Login ID which enables authorization on the switch. An agent can have more than one Login ID (from one or more switches), but you cannot assign a single Agent Login to more than one agent.

     1 - Click Add next to Agent Logins.
     2 -Under Agent Login, click the search icon to browse the Agent Logins already configured on the switches in your environment. Select an Agent Login from the list.
     3 -Click OK.

**Agent Logins**—Cada agente de telefonia tem um Login ID que permite a autorização no switch. Um agente pode ter mais de um ID de login (de uma ou mais centrais), mas você não pode atribuir um único login de agente a mais de um agente.

      1 - Clique em Adicionar ao lado de Logins de agente.
      2 - Em Agent Login, clique no ícone de pesquisa para navegar pelos Agent Logins já configurados nos switches do seu ambiente. Selecione um logon de agente na lista.
      3 -Clique em OK.

![image](https://user-images.githubusercontent.com/52088444/157986004-aaa24af8-ed59-493b-82a8-f060a142f493.png)

To add the agent to an access group, click the Member Of tab, click Add, and then select an Access Group. 

Para adicionar o agente a um grupo de acesso, clique na guia Membro de, clique em Adicionar e selecione um Grupo de acesso.