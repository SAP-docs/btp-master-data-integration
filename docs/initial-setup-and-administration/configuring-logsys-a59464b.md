<!-- loioa59464b050bf408cb4e9268f60038d24 -->

# Configuring logSys



<a name="loioa59464b050bf408cb4e9268f60038d24__purpose-of-logsys"/>

## Purpose of `logSys` 

Sets the `logSys` attribute of the client.

It is used when returning the logical system of the last significant writer on the SAP Master Data Integration Events API. If a client is the last significant writer, the value of its `logSys` attribute is the one returned by the Events API.

When a client is deleted, the value of its `logSys` attribute is no longer accessible on the Events API.



<a name="loioa59464b050bf408cb4e9268f60038d24__how-to-configure-logsys"/>

## How to configure `logSys` 

> ### Note:  
> You should only configure `logSys` if the documentation of the connected application demands it.

To configure the `logSys` , open the SAP BTP cockpit, and navigate to the service instance that is used to connect your application.

View and update attributes as follows:

1.  Navigate to the service instance.

2.  Select **... -\> View Parameters** to view the current attribute configuration of the service instance.

3.  Copy the JSON object with the current state of attributes.

4.  Select **... -\> Update** . Paste the existing JSON object and add, update, or remove the relevant attributes. Note that the update operation does not patch the existing configuration, it replaces the full state of configuration. Therefore, it is important to provide all relevant attributes in the update operation.


Add the following attribute to configure the `logSys` .

```
"logSys": "<logicalSystem>"
```

The `logSys` attribute has to meet the following constraints:

-   A length of up to 10 characters.


