# Management Layer—GA

## 4.1 Dashboard

GA has a Dashboard which provides a central monitoring location for your contact center. You can locate the Dashboard in the following locations:

**GA**

- Navegue até MONITORAMENTO > Ambiente > Painel


![image](https://user-images.githubusercontent.com/52088444/157986236-5b14adbc-04e4-42fe-96fe-ba78a1aa64ab.png)



## 4.2 Monitoring Your Environment

Each Genesys server application exists in the configuration database where it is assigned to a host. Solution Control Server monitors and allows Management Layer to control the Genesys applications. Using Genesys Administrator, you can view individual applications and entire solutions on all hosts.

![image](https://user-images.githubusercontent.com/52088444/157986333-10fce91a-210d-4a34-bce1-4c1128cb6152.png)


**Alarm Processing**

Alarms are displayed in Genesys Administrator. 

Each alarm can be associated with an automatic reaction (e.g., send an email/page, restart an application, send an SNMP trap). Wizards are available to assist in configuring alarms and reactions. Alarms stay in the system until canceled by other specified events or cleared.

Os alarmes são exibidos no Genesys Administrator.

Cada alarme pode ser associado a uma reação automática (por exemplo, enviar um e-mail/página, reiniciar um aplicativo, enviar uma interceptação SNMP). Assistentes estão disponíveis para auxiliar na configuração de alarmes e reações. Os alarmes permanecem no sistema até serem cancelados por outros eventos especificados ou apagados.

## 4.3 GA Environment Monitoring

You can also monitor your system using Genesys Administrator. It allows you to monitor the system as a whole, all of the objects that make up your system, and logs and alarms generated throughout your system.

Você também pode monitorar seu sistema usando o Genesys Administrator. Ele permite que você monitore o sistema como um todo, todos os objetos que compõem seu sistema, e os logs e alarmes gerados em todo o seu sistema.

**High-Level Overview of Environment(Visão geral de alto nível do ambiente)**

![image](https://user-images.githubusercontent.com/52088444/157986664-ab18a100-f952-418a-b93c-45294fca9cbf.png)

The Monitoring tab provides the following monitoring possibilities:

- Dashboard—A high-level summary of all operations.
- Active Alarms—A summary of active alarms, from which you can select and investigate any that are of special interest.
- Centralized Log—A summary of logs, from which you can select and investigate any that are of special interest.

A guia Monitoramento oferece as seguintes possibilidades de monitoramento:

- Dashboard—Um resumo de alto nível de todas as operações.
- Alarmes ativos—Um resumo dos alarmes ativos, a partir do qual você pode selecionar e investigar qualquer um que seja de interesse especial.
- Log Centralizado—Um resumo dos logs, a partir do qual você pode selecionar e investigar qualquer um que seja de interesse especial.

**Active Alarms(alarmes ativos)**

The next two images show an example of active alarms in GA.

As próximas duas imagens mostram um exemplo de alarmes ativos no GA.

![image](https://user-images.githubusercontent.com/52088444/157986879-7f41b304-3094-4ad7-8afb-592bf7f5c670.png)

![image](https://user-images.githubusercontent.com/52088444/157986946-83e4af82-870b-4667-8fc8-98c8c9e49c07.png)

When there is an active alarm present, you can click the arrow next to the Alarm Condition in the list of alarms and you will see more details about the Alarm Condition.

Quando houver um alarme ativo presente, você pode clicar na seta ao lado da Condição de Alarme na lista de alarmes e verá mais detalhes sobre a Condição de Alarme.

