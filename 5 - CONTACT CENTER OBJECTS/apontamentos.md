# CHAPTER 5 - CONTACT CENTER OBJECTS

## 5.1 Learning Objectives


After completing this chapter, you should be able to do the following:

1- Describe Contact Center Objects, such as persons, agent groups, agent skills, places, place groups, and access groups.

2 - Make changes to basic Contact Center Objects, such as persons, agent groups, and skills.

3- Navigate basic objects in Genesys Administrator Extension.



Depois de concluir este capítulo, você deve ser capaz de fazer o seguinte:

1- Descreva os objetos do Contact Center, como pessoas, grupos de agentes, habilidades de agentes, locais, grupos de locais e grupos de acesso.

2 - Faça alterações nos objetos básicos do Contact Center, como pessoas, grupos de agentes e habilidades.

3- Navegue pelos objetos básicos no Genesys Administrator Extension.

## 5.2 Contact Center Data(Dados do Contact Center)



For Genesys to perform well, you must provide specifics about your contact center. Genesys software will be configured to integrate with the hardware and other resources 
available in your contact center. This enables Genesys software to interact with the switch, make routing decisions, provide contact center reporting, and perform other
functions.

We begin this lesson with an introduction to the terms related to a switch in a contact center. The terms listed on the next page are defined in the context in which 
Genesys uses them. Keep in mind, the switch you are using in your Genesys implementation may use different terms.

Para que a Genesys tenha um bom desempenho, você deve fornecer detalhes sobre seu contact center. O software Genesys será configurado para integração com o hardware e
outros recursos disponíveis em seu contact center. Isso permite que o software Genesys interaja com o switch, tome decisões de roteamento, forneça relatórios de contact 
center e execute outras funções.

Começamos esta lição com uma introdução aos termos relacionados a um switch em um contact center. Os termos listados na próxima página são definidos no contexto em que 
a Genesys os utiliza. Lembre-se de que o switch que você está usando na implementação do Genesys pode usar termos diferentes.

![image](https://user-images.githubusercontent.com/52088444/157496023-a9d7ca0d-7552-468d-a75c-fadef4d09f2d.png)

## 5.3 Configuration Objects


Genesys uses the term configuration object to indicate a certain resource or part of the Genesys system that must be defined in GAX using the Configuration Manager 
window. These are also sometimes referred to as contact center objects.

Genesys uses configuration objects to define the Genesys system, as well as the equipment and resources in the contact center. Equipment and resources available in 
the contact center can be managed by Genesys if they are defined in Genesys terms. This means you must create a configuration object to represent each resource in your 
contact center.

Genesys usa o termo objeto de configuração para indicar um determinado recurso ou parte do sistema Genesys que deve ser definido no GAX usando a janela Configuration Manager.
Às vezes, eles também são chamados de objetos do contact center.

A Genesys usa objetos de configuração para definir o sistema Genesys, bem como os equipamentos e recursos do contact center. Os equipamentos e recursos disponíveis no
contact center podem ser gerenciados pela Genesys se forem definidos nos termos da Genesys.
Isso significa que você deve criar um objeto de configuração para representar cada recurso em seu contact center.

Examples:


- Every extension, queue, and routing point in your switch must be created as a DN object.
- Every agent in your contact center must be created as a Person object.
- Every Genesys software component must be created as an Application object.

Exemplos:


- Cada ramal, fila e ponto de roteamento em seu switch deve ser criado como um objeto DN.
- Cada agente em seu contact center deve ser criado como um objeto Pessoa.
- Todo componente de software Genesys deve ser criado como um objeto Aplicativo.

## 5.4 Logging in for Voice Calls

To accept voice calls in the Contact Center, an agent login process typically involves the following:
Para aceitar chamadas de voz no Contact Center, um processo de login de agente geralmente envolve o seguinte:

- Agent login code (ID) is specified
- Switch authenticates the code
- Agent makes the phone set ready

- O código de login do agente (ID) é especificado
- Switch autentica o código
- Agente deixa o telefone pronto

![image](https://user-images.githubusercontent.com/52088444/157670278-577a63b2-28ff-4063-8875-e4413e89ceda.png)


**Automatic call distributor(ACD)Um sistema automatizado de distribuição de chamadas, conhecido como distribuidor automático de chamadas, é um dispositivo de telefonia que atende e distribui as chamadas recebidas para um grupo específico de terminais ou agentes dentro de uma organização.**

The agent login is the code that an agent enters into the telephone set or Agent Desktop to log in to an ACD Queue on the switch. Once the switch receives the code, it verifies the existence of the code and that the code is not currently in-use. If the code entered by the agent is valid and available, the switch associates the agent’s extension with one or more queues (as programmed in the switch) and allows the phone set to receive calls from those queues.

Once the agent is logged in, the agent must make the phone set ready to receive calls. Usually, the agent can accomplish this by clicking a button or selecting a menu choice in the Agent Desktop.

O login do agente é o código que um agente insere no telefone ou no Agent Desktop para fazer login em uma fila ACD na central. Depois que o switch recebe o código, ele verifica a existência do código e se o código não está em uso no momento. Se o código inserido pelo agente for válido e disponível, a central associa o ramal do agente a uma ou mais filas (conforme programado na central) e permite que o telefone receba chamadas dessas filas.

Uma vez que o agente está conectado, o agente deve deixar o telefone pronto para receber chamadas. Normalmente, o agente pode fazer isso clicando em um botão ou selecionando uma opção de menu no Agent Desktop.

## 5.5 The Switch
![image](https://user-images.githubusercontent.com/52088444/157670840-e5e4c1e1-fc01-4c27-86f3-d028e44def9f.png)

Genesys uses the term DNs to describe any of the points on the switch, as demonstrated in the preceding image.
A Genesys usa o termo DNs para descrever qualquer um dos pontos no switch, conforme demonstrado na imagem anterior.

**Terminology and Definitions**
![image](https://user-images.githubusercontent.com/52088444/157678407-7780ef72-c516-415f-a62e-85960900fe2c.png)
![image](https://user-images.githubusercontent.com/52088444/157678445-d22fadbd-c6bd-4ee6-900a-261c9fff5a68.png)


![image](https://user-images.githubusercontent.com/52088444/157678148-20fdddf7-8a74-4853-a523-242e6a9e88e2.png)
![image](https://user-images.githubusercontent.com/52088444/157678180-dacc3edb-4640-4f1a-a3e6-2677589c9770.png)




