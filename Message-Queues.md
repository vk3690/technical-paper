# Technical paper
# MESSAGING QUEUES

A message queue is an asynchronous service to service communication used in a serverless and microservices architecture. The queue is like a buffer or temporary storage where the messages are stored. Once these messages are processed they are deleted from the buffer, every message is processed only once and by a single consumer. These messages are arranged based on the FIFO (first in first out), where the first message that entered queue is processed first. Every queue has a queue manager, which manages and maintains the queue. A message in the queue can be of various forms like XML, text, bytes. These messages are added to the queue explicitly by the sender to receiver.

   ![block diagram of queue](https://i.stack.imgur.com/1Oq0A.png)





## Why use Message Queues

### Better Performance

They provide asynchronous communication between two systems, where these systems would only interact with queue, but not with each other. At any point, any producer can add a message to the queue without waiting for them to be processed. On the other side consumer only process the messages only when they are available. So, no system is waiting for others to respond which gradually improves performance of the both the applications.

### Reliability

Queues make data persistence across the internet .when one part of the system faces failure or goes offline the messages are still in the queue. The remaining part of the system that is functioning can still interact with the queue and process the messages and update themselves.

### Scalability
messaging queues can be scaled according to traffic between producer and consumer. A queue can get longer when the system faces peak workload and shrink when the workload is low. These shrinking and growing queues help in managing messages and processing them efficiently.



## Messaging Queue Tools

Messaging queues services are provided by many companies, these companies provide these services to clients with their developed tools. Here are some of the tools, which are developed by individual companies.

* Mulesoft anypoint platform

* IBM Mq

* Azure scheduler

* Apache Kafka

* TIBCO Rendezvous

* Rabbit Mq

* IBM cloud Pak for integration

* Google cloud pub/sub

* Apache Active Mq

* Amazon Mq

* Alibaba message services

## Enterprise Message Bus

A message bus provides one or more Applications to communicate through messages with one or more applications. Unlike in messaging queues where it is based on FIFO, message bus may not follow the same order. A subscriber may come and go without the knowledge of the message producer.

   ![working of bus](https://i.stack.imgur.com/5PkJy.gif) 

Let application A be a message sender, which communicates messages to application B through a message bus, later application C can be configured to listen to the message bus and can take actions based on the messages of A. The configuration is done without the knowledge of application A.
Message bus works based on subscribe/publish model when a sender sends messages in message bus any application or receiver subscribed to that kind of messages can listen to them and take actions and update. This approach allows the application to follow the open/closed principle, where they are open to future changes while remaining closed for additional modifications.

### References
* [https://aws.amazon.com/message-queue/](https://aws.amazon.com/message-queue/)

* [https://www.youtube.com/watch?v=ZwZvQIuX0AU](https://www.youtube.com/watch?v=ZwZvQIuX0AU)

* [https://stackoverflow.com/questions/7793927/message-queue-vs-message-bus-what-are-the-differences](https://stackoverflow.com/questions/7793927/message-queue-vs-message-bus-what-are-the-differences)

* [https://www.youtube.com/watch?v=oUJbuFMyBDk](https://www.youtube.com/watch?v=oUJbuFMyBDk)

* [https://www.youtube.com/watch?v=5-Rq4-PZlew](https://www.youtube.com/watch?v=5-Rq4-PZlew)
