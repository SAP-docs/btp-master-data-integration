<!-- loio923c184197354734bfb4b94cd2143eac -->

# Support for Initial Loads

SAP Master Data Integration service maintains a database of master data records for the landscape.Applications exchange messages with Master Data Integration to keep their local copies of the master data in sync. The initial load functionality of the service supports two different use cases:

1.  **Initial \(up\)load** : Applications that modify and create master data records can load their local master data records into Master Data Integration as part of the initial upload. This is done to populate the central database in Master Data Integration. Applications using this functionality are producing clients.

2.  **Initial \(down\)load** : Applications receive their initial copy of master data records from Master Data Integration. Applications using this functionality are consuming clients.


Consuming clients can get a copy of the master data centrally from the Master Data Integration service without affecting existing integration scenarios. This decoupling eliminates the need to integrate with multiple different applications of a landscape.

After performing an initial load, applications transition to a continuous synchronization with Master Data Integration. Refer to [Synchronization of Master Data](synchronization-of-master-data-20db337.md) for more details.

