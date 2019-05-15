# Dell Boomi
![afe57363.png](:storage\55ebc588-89d2-47d8-85f5-766bf38bea02\afe57363.png)

Its a iPass(Integration as a service too), having connectors for all data sources such as AWS, GCP, even local machines and server
with different protocol such as FTP, SFTP 
* It provides services for both on premise and cloud system


Now it is useful, since there are application specifics to modules such as Payroll and lets say attendance. Now these systems needs communicate with each other, hence a tool like Boomi comes in very handy

## Main Terms
**Atom/or dynamic runtime engines** -> Process running on machines/server that communicates with Source and target, real backbone of data integration

Now Atom is attached to integration process and also checks if there is any updates to it 
* It runs 247 on the machine/server
* It has connectivity to all of your source, target system and integration, basically runs the integration job
* can be attahed for environment, statging, production

**Component**
Such as functions, connectors, , APIS, certificates, connections
Now connections can be reutilised, making it easy to maintain and update and reference same database connection against multiple integration flows

**Connectors**
basically component specifiying from where to get data into and send data out of processes.



It has fields :-
* **Connector/Type** -> e.g. Disk, FTP
* **Action** -> Get, Send
* **Process** 
  * Single type of data to integrate between two or more systems 
  * It comes with start shape
  * has type - data, passthrough, no data

* **Connection**
  *  Machine Where atom is running
  *  
![4ea11bb8.png](:storage\55ebc588-89d2-47d8-85f5-766bf38bea02\beb2cd8f.png)

* **Documents**
  Files/records passing through every shape 
  * Document Properties
  You can use document properties to set things such as document name, document location etc

* **Stop Shape**
To end the integration flows, if your process goes into other branches, check option **continue processing other execution paths**
![c847f12d.png](:storage\55ebc588-89d2-47d8-85f5-766bf38bea02\c847f12d.png)


