# CST8915 Lab 8 : Deploying and Managing the Algonquin Pet Store (On Steroids)

**Student Name**: Joshua Chen

**Student ID**: 041280453

**Course**: CST8915 Full-stack Cloud-native Development

**Semester**: Winter 2026

---

## Demo Video

https://youtu.be/W_z5dqSRD4g

---

## Repositories

Store-Front : https://github.com/JChen-AC/store-front-L8

Store-Admin : https://github.com/JChen-AC/store-admin-L8

Order-Service: https://github.com/JChen-AC/order-service-L8

Product-Service: https://github.com/JChen-AC/product-service-L8

Makeline-Service: https://github.com/JChen-AC/makeline-service-L8

AI-Service : https://github.com/JChen-AC/ai-service-L8

Virtual Customer: https://github.com/JChen-AC/virtual-customer-L8

Virtual Worker: https://github.com/JChen-AC/virtual-worker-L8

---

## Technical Explanations

### Modification to MongoDB 

ChatGPT and Claude was used to help research and set up the persistence storage. 


### Modification to RabbitMQ

ChatGPT and Claude was used to help research and set up the persistence storage. 

First the order-service was updated to have the sender send durable and persistent messages. 

Second update the deployment file to use a volumeClaimTemplate setting the AccessMode to ReadWriteOnce and add storage. 

### Replacement services: 
#### Self=hosted MongoDB
The self-hosted MongoDB could be replaced win Azure CosmoDB. This is a fully managed No-SQL Database service offered by Azure. As such it offers easy scalalibility, backups and availability through its different options. The Purpose of Azure CosmoDB is to provide a managed No-SQL Database.

#### Rabbit MQ 
The self-hosted Rabbit-MQ can be replaced with Azure Service Bus. This is a filly managed message handling service offered by Azure. Its purpose is to handle events through a queue, similar to what Rabbit-MQ does. It is a good fit for the service as it is easily scalable, available and automatically comes with persistent storage. As in the configuration you can set up redundancy and availability zones to ensure that it is always available. 



---