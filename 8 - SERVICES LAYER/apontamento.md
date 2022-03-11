## 8.1 Learning Objectives

After completing this chapter, you should be able to do the following: 

1 - Recall major functions of the Services Layer.
2 - Describe the Stat Server..


Depois de concluir este capítulo, você deve ser capaz de fazer o seguinte:

1 - Relembre as principais funções da Camada de Serviços.
2 - Descreva o Servidor Estatístico.

## 8.2 Review Functions of Services Layer(Revisar Funções da Camada de Serviços)

Services Layer Functionality

- Compilation of statistics and object status

The Services layer converts events related to managing single interactions and non-interaction into statistical data, which is then used for interaction processing for routing and monitoring contact center resources for reporting.

Examples:

1- Inbound Interaction on a Queue will calculate how many total calls and how many waiting calls.

2- Interaction on an Extension will calculate time spent ringing and answered.

3 -  Resources such as Agent and AgentGroup monitoring its current status.

This responsible component is known as Stat Server.


Funcionalidade da camada de serviços

- Compilação de estatísticas e status de objetos

A camada de Serviços converte eventos relacionados ao gerenciamento de interações únicas e não interação em dados estatísticos, que são então usados ​​para processamento de interação para roteamento e monitoramento de recursos do contact center para relatórios.

Exemplos:

1- A interação de entrada em uma fila calculará quantas chamadas totais e quantas chamadas em espera.

2- A interação em um ramal calculará o tempo gasto para ligar e atender.

3 - Recursos como Agent e AgentGroup monitorando seu status atual.

Este componente responsável é conhecido como Stat Server.

## 8.3 Stat Server(Servidor de Estatísticas)



8.3 Stat Server


Stat Server tracks information about the contact center. Stat Server also converts the data accumulated for DNs, agents, agent groups, and non-telephony-specific object types such as voice interactions, email, and chat sessions, into statistically useful information and passes these calculations to other software applications that request data. 

Collected data is converted into useful information to be used by Contact Center applications, such as the following:

- Universal Routing Server (URS) and Orchestration Server (ORS)
- Solution Reporting


O Stat Server rastreia informações sobre o contact center. O Stat Server também converte os dados acumulados para DNs, agentes, grupos de agentes e tipos de objetos não específicos de telefonia, como interações de voz, e-mail e sessões de bate-papo, em informações estatisticamente úteis e passa esses cálculos para outros aplicativos de software que solicitam dados.

Os dados coletados são convertidos em informações úteis a serem utilizadas pelos aplicativos do Contact Center, como:

- Servidor de Roteamento Universal (URS) e Servidor de Orquestração (ORS)
- Relatório de soluções

![image](https://user-images.githubusercontent.com/52088444/157884671-e6ae7924-66fd-4306-bf59-7ab781a74a2f.png)

Managers are provided with a wide range of information to maximize the efficiency and flexibility of the contact center.


Os gerentes recebem uma ampla gama de informações para maximizar a eficiência e a flexibilidade do contact center.


## 8.4 Linking Agent and Place  


Stat Server links the place and agent together. This is important for status and statistics. If the extension is busy, the agent is busy. If the agent sets their status to Not Ready, that extension is not ready.


O Stat Server vincula o local e o agente. Isso é importante para status e estatísticas. Se o ramal estiver ocupado, o agente estará ocupado. Se o agente definir seu status como Não pronto, esse ramal não estará pronto.

![image](https://user-images.githubusercontent.com/52088444/157885188-d92cfaf2-b30c-4689-bce6-5ecc78e9f48a.png)

An agent logs into a place using the agent desktop such as Workspace. Based on the configuration, there can be an agent login associated with the agent and there can be an extension associated with the place. That information can be communicated to a switch to log an agent login code into an extension.

Um agente efetua login em um local usando a área de trabalho do agente, como o Workspace. Com base na configuração, pode haver um login de agente associado ao agente e pode haver um ramal associado ao local. Essas informações podem ser comunicadas a um switch para registrar um código de login do agente em um ramal.

**Obs:This is specific to a traditional voice environment. Agents and places are still used in non-voice environments, without agent logins and extensions.**

**Isso é específico para um ambiente de voz tradicional. Agentes e locais ainda são usados ​​em ambientes sem voz, sem logins e ramais de agentes.**

## 8.5 Learning Summary

Now that you have completed this chapter, you should be able to do the following: 

1 - Recall major functions of the Services Layer.

2 - Describe the Stat Server.


Agora que você concluiu este capítulo, você deve ser capaz de fazer o seguinte:

1 - Relembre as principais funções da Camada de Serviços.

2 - Descreva o Stat Server.


## 8.6 Learning check

Question
01/04
Stat Server tracks information about the contact center.

True (verdade)

false


Question
02/04
Services Layer provides status of agent to the Configuration Layer.

True

False(correta)

Question
03/04
Routing and reporting use the Services Layer for statistics.

True(verdade)

False

Question
04/04
Which functions apply to the Services Layer?

Interaction tracking

Database connectivity

Dynamic reconfiguration and notification

Attached data distribution

Alarm processing 

Log events interface

Fault handling

Configuration

Access control

External interfaces

Compilation of statistics and object status(verdade)

Solution control