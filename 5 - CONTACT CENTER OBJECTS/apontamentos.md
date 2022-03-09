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
