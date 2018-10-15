# Getting Started

Il progetto si basa sull'utilizzo dei seguenti tools:

- Spring Tool Suite 3.9.5
- Maven 3.5.4
- Tomcat 9.0.10
- Java 8 
- Spring Initializer 1.5.16

### Java

[![image](https://image.ibb.co/bz1VZU/en.png)](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
Java 8 version.

Download package depending on your OS System and install. After that:
  - add JAVA_HOME to environment variables pointing to JDK folder and add to PATH variable
  - add JRE_HOME to environment variables pointing to JRE folder and add to PATH variable
  
### Apache Maven

[![image](https://image.ibb.co/bz1VZU/en.png)](https://maven.apache.org/download.cgi)
Maven 3.5.4 version.

Download package depending on your OS System and install. After that:
  - add M2_HOME to environment variables pointing to Maven folder and add to PATH variable
  
### Maven settings
Maven `settings.xml` file is inside maven conf folder. Here you can change global configurations and add for example proxy settings. If you want to override global settings you can create inside your local `~/.m2` folder a copy of the global `settings.xml` file and edit this one. 
```xml
<proxy>
    <id>sopra_http</id>
    <active>true</active>
    <protocol>http</protocol>
    <host>miln.proxy.corp.sopra</host>
    <port>8080</port>
    <nonProxyHosts>local.net|some.host.com</nonProxyHosts>
</proxy>
<proxy>
    <id>sopra_https</id>
     <active>true</active>
     <protocol>https</protocol>
     <host>miln.proxy.corp.sopra</host>
     <port>8080</port>
     <nonProxyHosts>local.net|some.host.com</nonProxyHosts>
</proxy>  
```
### Apache Tomcat

[![image](https://image.ibb.co/bz1VZU/en.png)](https://archive.apache.org/dist/tomcat/tomcat-9/)
Tomcat 9.0.10 version.

Download package depending on your OS System and install. After that:
  - add CATALINA_HOME to environment variables pointing to Maven folder and add to PATH variable 
Run startup.bat
Go to localhost:8080 to verify the correct installation
  
### Spring Tool Suite

[![image](https://image.ibb.co/bz1VZU/en.png)](https://spring.io/blog/2018/07/05/spring-tool-suite-3-9-5-released)
Spring Tool Suite 3.9.5 version.

Download package depending on your OS System and install. After that:
  - Start your IDE
  - Add a new Server (Tomcat)
  - Set up proxies if necessary.
  
### Spring Boot Inizializer

 [![image](https://image.ibb.co/jgPaZU/1_O68_Lb_Dv_D5_Dcsnez73_M7v4_Q.png)](https://start.spring.io/)
  
  - Select an useful name and artifact_id for your project.
  - Add dependencies.
  - Click on Generate Project to download your project.
  - Copy the files in your workspace
  - Import the project as Maven project
  
  
  ### Now you are ready to start!




# app fornitori

### Secondo l'analisi delle specifiche richieste si propongono i seguenti diagrammi:

### ER:
![image](https://image.ibb.co/e1r1M9/ER.png)

### UML:
![image](https://image.ibb.co/bFsDZU/UML.png)

### Use Case:
![image](https://image.ibb.co/hLvT19/UseCase.png)

### PUNTI SALIENTI:
- PM e ASSISTANT:accesso con le credenziali aziendali (Single-Sign-On)

- ASSISTANT: può invitare uno o più providers

- PROVIDER: se riceve un invito può registrarsi attraverso un form. 
A registrazione avvenuta il provider riceverà una password temporanea da personalizzare

- PM: può creare una CAMPAIGN di reclutamento.
All'atto della creazione può selezionare una lista di providers*

- PROVIDER: Se indicato come provider all'atto di creazione di una CAMPAIGN riceve un email di notifica.

- PROVIDER: Può registrare un PROFILE inserendone i dati e allegando un CV.

- PROVIDER: Può associare un PROFILE ad una CAMPAIGN.

- PM: Quando un PROFILE viene associato alla propria CAMPAIGN riceve una email di notifica.

- PM: Può approvare o meno i PROFILE inviati dai PROVIDERS.

- PM: Può chiudere una CAMPAIGN.
All'atto della chiusura i PROVIDERS associati alla campaign e gli ASSISTANT riceveranno una email di notifica.
Nella mail sarà presente una lista dei PROFILE idonei e le indicazioni su come procedere per l'offerta.

### Workflow:

![image](https://image.ibb.co/gFwnip/Git-Flow-Workflow.png)

Si procederà staccando il branch DEVELOP da MASTER, per ogni FEATURE verrà staccato un apposito BRANCH che verrà opportunamente
pushato su DEVELOP al termine dello sviluppo della stessa. Prima di ogni release il progetto verrà pushato su TEST dove verranno
identificati e corretti eventuali bug. Quando la fase di test verrà completata con successo si procederà pushando su MASTER.

NOTES:
*Un futuro sviluppo dovrà prevedere un ranking per i providers con priorità di notifica.


