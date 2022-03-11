
## 10.1 Learning Objectives

After completing this chapter, you should be able to do the following: 

1 - Recall Genesys Solution Reporting.

2 - Describe Pulse.

3 - Navigate the Pulse interface.

4 - Describe the Analytical Reporting Historical Solution.


Depois de concluir este capítulo, você deve ser capaz de fazer o seguinte:

1 - Recupere o Relatório da Solução Genesys.

2 - Descreva o Pulso.

3 - Navegue na interface do Pulse.

4 - Descrever a Solução Histórica do Relatório Analítico.


## 10.2 Solution Reporting(Relatório de Solução)


Genesys Platform provides Solution Reporting:

- Pulse: Real-time reports

Genesys Pulse is an application that offers at-a-glance views of real-time contact center statistics on dashboards within the user interface. The stat server provides real-time data and information about interactions that the objects can handle. It also gives non-interaction-related data about objects themselves (for example, agent status).

Genesys Pulse is your gateway for monitoring your contact center to meet your business needs better.


A Plataforma Genesys fornece Relatórios de Soluções:

- Pulso: relatórios em tempo real

O Genesys Pulse é um aplicativo que oferece visualizações rápidas das estatísticas do contact center em tempo real em painéis na interface do usuário. O Stat Server (servidor de estatísticas) fornece dados e informações em tempo real sobre as interações que os objetos podem manipular. Ele também fornece dados não relacionados à interação sobre os próprios objetos (por exemplo, status do agente).

O Genesys Pulse é seu gateway para monitorar seu contact center para atender melhor às suas necessidades de negócios.

![image](https://user-images.githubusercontent.com/52088444/157922654-530ca05a-b40b-4869-bde2-2cbe46b0b4b4.png)

## 10.3 Real-Time Reporting

Contact center managers and supervisors can most effectively manage a contact center when they have the information they need to make speedy decisions.

Real-time reporting

With Real-time reporting, you can know:

-  What is happening now?
-  How many calls are waiting in Queue?
-  How many agents are in a “Not Ready” state?
-  What is the feedback to any changes you make immediately?
-  Has assigning more agents to Inbound queues caused the number of calls waiting in queue to decrease? If so, by how much?


Os gerentes e supervisores do contact center podem gerenciar um contact center com mais eficiência quando têm as informações necessárias para tomar decisões rápidas.

**Relatórios em tempo real**

Com relatórios em tempo real, você pode saber:

- O que está acontecendo agora?
- Quantas chamadas estão esperando na fila?
- Quantos agentes estão no estado “Não pronto” "NOT READY"?
- Qual é o feedback para quaisquer mudanças que você faz imediatamente?
- A atribuição de mais agentes às filas de entrada fez com que o número de chamadas em espera na fila diminuísse? Se assim for, por quanto? 

## 10.4 Genesys Pulse

Genesys Pulse is a widget-driven, graphical user application. It enables at-a-glance views of real-time contact center statistics such as agents, agent groups, queues, and more.

Genesys Pulse é um aplicativo de usuário gráfico orientado por widget. Ele permite visualizações rápidas das estatísticas do contact center em tempo real, como agentes, grupos de agentes, filas e muito mais.

![image](https://user-images.githubusercontent.com/52088444/157923798-0afef5ba-d437-4279-a507-a180763993a6.png)


**Widget(ferramenta)**

A widget is an individual element of the dashboard created by applying a template to a set of reporting objects. A widget can have a regular (small view) and an Extended View.

Um widget é um elemento individual do painel criado pela aplicação de um modelo a um conjunto de objetos de relatório. Um widget pode ter uma visualização normal (pequena) e uma visualização estendida.

**Widget Extended View(Visualização Estendida do Widget)**

Extended View allows you to expand the widget and examine more details about the statistics you are tracking. To open the extended view, click the ellipsis at the top of the widget and click Expand to tab.

A Exibição Estendida permite expandir o widget e examinar mais detalhes sobre as estatísticas que você está acompanhando. Para abrir a visualização estendida, clique nas reticências na parte superior do widget e clique em Expandir para guia.

The widget opens in extended view and you have the ability to observe and change your view on-demand.

When you hover your mouse over the data displayed in the extended view widget, a pop-up appears containing more detailed information, as demonstrated in the following image.

O widget abre em exibição estendida e você tem a capacidade de observar e alterar sua exibição sob demanda.

Quando você passa o mouse sobre os dados exibidos no widget de exibição estendida, um pop-up aparece contendo informações mais detalhadas, conforme demonstrado na imagem a seguir.

![image](https://user-images.githubusercontent.com/52088444/157924166-743ede6c-6935-4fc0-9622-59fdaa9cd29d.png)

Clicking the icons in the top right-hand corner changes the display of the extended view widget as follows:

Clicar nos ícones no canto superior direito altera a exibição do widget de visualização estendida da seguinte forma:

![image](https://user-images.githubusercontent.com/52088444/157924250-327e59b0-cebc-45b8-b789-653f8d9896dd.png)

You can select and change the objects which are to be displayed in the extended view widget, as follows:

- All objects - Select that checkbox.
- Individual objects - Click the radio button next to each object name.

You also have the ability to change the statistic that is displayed in the extended view widget. Use the statistic dropdown box to select the statistic you want to appear in the widget.


Você pode selecionar e alterar os objetos que devem ser exibidos no widget de visualização estendida, da seguinte forma:

- Todos os objetos - Marque essa caixa de seleção.
- Objetos individuais - Clique no botão de rádio ao lado do nome de cada objeto.

Você também pode alterar a estatística exibida no widget de exibição estendida. Use a caixa suspensa de estatísticas para selecionar a estatística que deseja que apareça no widget.

![image](https://user-images.githubusercontent.com/52088444/157924394-a604329b-14f4-44e3-aba6-c8c171a1516c.png)


To close the extended view and return to the regular (small) widget view, click the ellipsis at the top of the widget, as demonstrated in the following image, and click Close.


Para fechar a visualização estendida e retornar à visualização de widget normal (pequena), clique nas reticências na parte superior do widget, conforme demonstrado na imagem a seguir, e clique em Fechar.

![image](https://user-images.githubusercontent.com/52088444/157924488-9145ceed-18f5-4086-9634-22ffe1d2a938.png)

## 10.5 Where Do You Find Pulse?(Onde você encontra o Pulse?)

Genesys Pulse can be started only in a standalone mode. Genesys Pulse version 9.0.0 cannot be used as a plugin of GAX (in earlier versions of the product the Pulse was part of the GAX interface).


O Genesys Pulse pode ser iniciado apenas em modo autônomo. O Genesys Pulse versão 9.0.0 não pode ser usado como plugin do GAX (nas versões anteriores do produto o Pulse fazia parte da interface GAX).

![image](https://user-images.githubusercontent.com/52088444/157924689-f77b390f-1a74-45ab-bb66-e9b8fdf96082.png)

##  10.6 Pulse Dashboard/Wallboard Displays(Monitores de painel/wallboard de pulso)

Pulse uses dashboards and wallboards to display real-time reports within different types of widgets so that you can monitor your contact center to suit your needs. 

- Dashboards are for personal use, and provide drill-down reports, and contain more detail than wallboards.
- Wallboards can broadcast information on a large screen for a team of people.

O Pulse usa painéis e wallboards para exibir relatórios em tempo real em diferentes tipos de widgets, para que você possa monitorar seu contact center para atender às suas necessidades.

- Os painéis são para uso pessoal e fornecem relatórios detalhados e contêm mais detalhes do que os painéis de parede.
- Wallboards podem transmitir informações em uma tela grande para uma equipe de pessoas.

**Dashboard**
![image](https://user-images.githubusercontent.com/52088444/157924959-cd73da2e-7de0-41d9-93de-185ba0ead1e8.png)


**Wallboard**
![image](https://user-images.githubusercontent.com/52088444/157925008-d9ef2e7a-e9a2-40cb-8f0e-024c81ba181e.png)

**Types of Dashboards(Tipos de painéis)**

- Default Dashboard—Same standard dashboard for all users.

- Custom Dashboard—Specific to an individual user (if roles allow).

A user with the necessary permissions creates and saves the Default Dashboard. Roles control where you can make any changes to customize the dashboard.

- Dashboard padrão—Mesmo painel padrão para todos os usuários.

- Dashboard personalizado — Específico para um usuário individual (se as funções permitirem).

Um usuário com as permissões necessárias cria e salva o Dashboard Padrão. As funções controlam onde você pode fazer alterações para personalizar o Dashboard.


**Dashboard samples( amostras de Dashboard**

Here are some examples of real-time reports models you can use and display on your dashboard depending on the business decisions.

Aqui estão alguns exemplos de modelos de relatórios em tempo real que você pode usar e exibir em seu painel, dependendo das decisões de negócios.

**Sales team lead dashboard(Painel de liderança da equipe de vendas)**

![image](https://user-images.githubusercontent.com/52088444/157925513-6f51cd76-51e2-4dfb-a4b3-e0f2f9bb8cfb.png)

![image](https://user-images.githubusercontent.com/52088444/157925544-284106f6-b3d1-4c46-8957-71b63f1f4aeb.png)

![image](https://user-images.githubusercontent.com/52088444/157925616-03d30bee-f2e1-4c25-9dca-2e8daa9e3e4b.png)

## 10.7 Pulse Widget Displays

The Pulse Dashboard is made up of widgets. The widgets display charts that provide an at-a-glance view of what is happening in your contact center. 

- List—Display the statistics in a list. Can be switched to recent past line graph.
- Donut—Display the headline stat in a donut comparing configuration objects.
- Grid—Display showing data in rows and columns.
- KPI—Display a series of stats in a set of panels that the user can click through or have auto-play for the headline configuration object.
- Line—Display three objects with the Headline type Statistics or up to three statistics with the Headline type Object. Compare the trend of calls answered by each agent.
- Alert—Display alerts from widgets on specified dashboards or wallboards. Alerts can be deactivated (and reactivated later) or snoozed (the default snooze timeout is 15 minutes).
- Text—Display broadcast information to the audience. The text widget can be displayed as a news feed ticker and edited by Administrators.

O Pulse Dashboard é composto de widgets. Os widgets exibem gráficos que fornecem uma visão rápida do que está acontecendo em seu contact center.

- Lista—Exibe as estatísticas em uma lista. Pode ser alternado para o gráfico de linhas do passado recente.
- Donut—Exibe a estatística do título em um donut comparando objetos de configuração.
- Grade—Exibição mostrando dados em linhas e colunas.
- KPI—Exibe uma série de estatísticas em um conjunto de painéis que o usuário pode clicar ou reproduzir automaticamente para o objeto de configuração do título.
- Linha—Exibe três objetos com as Estatísticas do tipo Título ou até três estatísticas com o Objeto do tipo Título. Compare a tendência das chamadas atendidas por cada agente.
- Alerta—Exibe alertas de widgets em painéis ou wallboards especificados. Os alertas podem ser desativados (e reativados posteriormente) ou adiados (o tempo limite de adiamento padrão é de 15 minutos).
- Texto—Exibe informações de transmissão para o público. O widget de texto pode ser exibido como um ticker de feed de notícias e editado pelos Administradores.

![image](https://user-images.githubusercontent.com/52088444/157925953-0f566bf0-d16b-457f-8908-83a42bbf0534.png)
![image](https://user-images.githubusercontent.com/52088444/157925997-7c084f63-acac-416c-8893-db2cd90a1f30.png)
![image](https://user-images.githubusercontent.com/52088444/157926074-4376257e-7ee8-4567-b76b-983ba6bffa26.png)

## 10.8 Reporting in Action

Let us now observe an example of a Pulse Dashboard/Wallboard and see the Genesys Reporting Solution in action. 

Genesys Beyond Training Contact Center Scenario

The Contact Center Management team wants to view real-time specific statistics and status about Engage customer business and agents handling them. Using Genesys Pulse the team can access the dashboards and wallboard configured with specific widgets to know various stats such as:

- Business data
- AgentGroup performances
- Agent KPI's
- Queue data

511 / 5.000
Resultados de tradução
Vamos agora observar um exemplo de um Pulse Dashboard/Wallboard e ver a Genesys Reporting Solution em ação.

Cenário de Contact Center Genesys Beyond Training

A equipe de gerenciamento do Contact Center deseja visualizar estatísticas e status específicos em tempo real sobre os negócios dos clientes do Engage e os agentes que os tratam. Usando o Genesys Pulse a equipe pode acessar os dashboards e wallboard configurados com widgets específicos para conhecer diversas estatísticas como:

- Dados comerciais
- Performances do AgentGroup
- KPIs do agente
- Dados da fila 

## 10.9 Analytical Reporting Historical Solution(Solução histórica de relatórios analíticos)

Solution Reporting is included with the Genesys Platform, whereas Analytical Reporting involves an additional purchase.

**Solution Reporting**

Genesys Solution Reporting is a powerful tool for viewing and analyzing contact center performance, enabling you to improve enterprise efficiency. It consists of two products:
- Pulse

**Pulse** 

Pulse enables at-a-glance views of real-time contact center statistics. Pulse allows you to monitor the pulse of the contact center using dashboards to view agents, agent groups, queues, and more in real time.

O Solution Reporting está incluído na Plataforma Genesys, enquanto o Analytical Reporting envolve uma compra adicional.

**Relatório de solução**

O Genesys Solution Reporting é uma ferramenta poderosa para visualizar e analisar o desempenho do contact center, permitindo que você melhore a eficiência da empresa. É composto por dois produtos:
- Pulso

**Pulso**

O Pulse permite visualizações rápidas das estatísticas do contact center em tempo real. O Pulse permite monitorar o pulso do contact center usando painéis para visualizar agentes, grupos de agentes, filas e muito mais em tempo real.

**Performance Management Suite
(Analytical Reporting)**

Performance Management is an add-on to the Genesys Platform and provides sophisticated ad-hoc business intelligence. It is based on detailed events directly from Media Layer. Performance Management includes the premier Genesys reporting solutions of:
- Info Mart
- MicroStrategy Suite (GCXI)

**Suite de gerenciamento de desempenho
(Relatório Analítico)**

O Performance Management é um complemento da Genesys Platform e fornece inteligência de negócios ad-hoc sofisticada. É baseado em eventos detalhados diretamente do Media Layer. O Performance Management inclui as principais soluções de relatórios da Genesys de:
- Info Mart
- MicroStrategy Suite (GCXI)


**obs:Existing customers with Infomart may have SAP Business objects Enterprise suite using Interactive Insight (GII2).**
**Clientes existentes com Infomart podem ter SAP Business objects Enterprise suite usando Interactive Insight (GII2).**

![image](https://user-images.githubusercontent.com/52088444/157927288-733f1b84-0f6f-4608-8590-f37bb77698f0.png)

- foco operacional
- gestão de desempenho

## 10.10 Genesys Info Mart

** Genesys Info Mart**

Genesys Info Mart uses an ETL process. ETL is the acronym for Extract the data, Transform the data into useful chunks, and Load the data into the report viewing component. 

Genesys Info Mart provides a consistent and flexible structure for collecting contact center analytics data and sorting it to provide insights to business users. Info Mart data can be used to create reports, feed analytical applications, or create executive dashboards. Info Mart aggregates granular historical data using available Media Layer components (T-Server, SIP Server, Interaction Server) and not Stat Server for data collection.

Genesys Info Mart produces a Data Mart that you can use for contact center historical reporting. Genesys Info Mart includes a server component, administration GUI, and database. 

The Genesys Info Mart server runs a set of predefined jobs that execute extract, transform, and load (ETL) processes to:

- Extract data that has been gathered by Interaction Concentrator from data sources such as Configuration Server, T-Server, and Interaction Server.
- Genesys Info Mart stores this low-level interaction data in the Info Mart database.
- Transforms the low-level interaction data and loads it into the Info Mart database.

Genesys Info Mart can also be configured to host an aggregation engine that aggregates or re-aggregates the data, and populates Aggregate tables in the Info Mart database. 

You can query the database using Structured Query Language (SQL), to obtain results that enable you to examine the data in detail, identify patterns, and predict trends for your organization.

** Genesys Info Mart**

Genesys Info Mart usa um processo ETL. ETL é o acrônimo para Extrair os dados, Transformar os dados em partes úteis e Carregar os dados no componente de visualização de relatórios.

O Genesys Info Mart fornece uma estrutura consistente e flexível para coletar dados analíticos do contact center e classificá-los para fornecer insights aos usuários de negócios. Os dados do Info Mart podem ser usados ​​para criar relatórios, alimentar aplicativos analíticos ou criar painéis executivos. O Info Mart agrega dados históricos granulares usando os componentes Media Layer disponíveis (T-Server, SIP Server, Interaction Server) e não o Stat Server para coleta de dados.

O Genesys Info Mart produz um Data Mart que você pode usar para relatórios históricos do contact center. O Genesys Info Mart inclui um componente de servidor, GUI de administração e banco de dados.

O servidor Genesys Info Mart executa um conjunto de tarefas predefinidas que executam processos de extração, transformação e carregamento (ETL) para:

- Extraia dados que foram coletados pelo Interaction Concentrator de fontes de dados, como Configuration Server, T-Server e Interaction Server.
- O Genesys Info Mart armazena esses dados de interação de baixo nível no banco de dados do Info Mart.
- Transforma os dados de interação de baixo nível e os carrega no banco de dados do Info Mart.

O Genesys Info Mart também pode ser configurado para hospedar um mecanismo de agregação que agrega ou reagrega os dados e preenche as tabelas Agregadas no banco de dados do Info Mart.

Você pode consultar o banco de dados usando a Linguagem de Consulta Estruturada (SQL), para obter resultados que permitem examinar os dados em detalhes, identificar padrões e prever tendências para sua organização.

## 10.11 Learning Summary

Now that you have completed this chapter, you should be able to do the following: 

1- Recall Genesys Solution Reporting.

2 - Describe Pulse.

3- Navigate the Pulse interface.

4-  Describe the Analytical Reporting Historical Solution.



## 10.11 Resumo de Aprendizagem

Agora que você concluiu este capítulo, você deve ser capaz de fazer o seguinte:

1- Recupere os Relatórios da Solução Genesys.

2 - Descreva o Pulso.

3- Navegue pela interface do Pulse.

4- Descrever a Solução Histórica do Relatório Analítico.