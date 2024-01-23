<!-- loioa59464b050bf408cb4e9268f60038d24 -->

# Configuring logSys



<a name="loioa59464b050bf408cb4e9268f60038d24__purpose-of-logsys"/>

## `logSys` Purpose of

`logSys` Sets theattribute of the client.

`logSys` It is used when returning the logical system of the last significant writer on the SAP Master Data Integration Events API. If a client is the last significant writer, the value of itsattribute is the one returned by the Events API.

`logSys` When a client is deleted, the value of itsattribute is no longer accessible on the Events API.



<a name="loioa59464b050bf408cb4e9268f60038d24__how-to-configure-logsys"/>

## `logSys` How to configure

> ### Note:  
> `logSys` You should only configureif the documentation of the connected application demands it.

`logSys` To configure the, open the SAP BTP cockpit, and navigate to the service instance that is used to connect your application.

View and update attributes as follows:

`logSys` Add the following attribute to configure the.

`logSys` Theattribute has to meet the following constraints:

1.  Navigate to the service instance.

2.  **... -\> View Parameters** Selectto view the current attribute configuration of the service instance.

3.  Copy the JSON object with the current state of attributes.

4.  **... -\> Update** Select. Paste the existing JSON object and add, update, or remove the relevant attributes. Note that the update operation does not patch the existing configuration, it replaces the full state of configuration. Therefore, it is important to provide all relevant attributes in the update operation.


```
"logSys": "<logicalSystem>"
```

-   A length of up to 10 characters.


