# technical-paper
# MESSAGING QUEUES

Message queue is asynchronous service to service communication used in server less and micro services architecture . The queue is like a buffer or temporary storage where the messages are stored . Once these messages are processed they are deleted from the buffer  , every message is processed only once and bt a single consumer . These messages are arranged based on the FIFO (first in first out) ,where the first message that entered queue is processed first . Every queue has a queue manager ,which manages and maintains the queue. A message in the queue can be of various forms like xml , text, byets. These messages are added to the queue explicitly by sender to receiver .

![block diagram of queue](https://i.stack.imgur.com/1Oq0A.png)





## Why use Message Queues

**Better Performance:**

They provide asynchronous communication between two systems, where these systems  would only interact with  queue , but not with each other . At any point any producer can add  message to queue without waiting for them to be processed . On the other side  consumer only process the messages only when they are available. So ,no system is waiting for other to respond which gradually improves performance.

**Reliability:**

Queues make data persistence across the internet .when one part of the system face failure or gone offline the messages are still in the queue. The remaining part of system that is functioning can still interact with queue and process the messages and update themselves.

**Scalability:**

Messaging queues can be scaled according to traffic between producer and consumer. Queue can get longer when the system faces peak workload  and shrink when workload is low. These shrinking and growing of queue helps in managing messages and processing them efficiently .




### Messaging Queue Tools

Messaging queues services are provided by many companies ,these companies provides these services to clients with their own developed tools . Here are the some of the tools ,which are developed by individual company .


.Mulesoft anypoint platform

.IBM Mq

.Azure scheduler

.Aphache Kafka

.TIBCO Rendezvous

.Rabbit Mq

.IBM cloud Pak for integration

.Google cloud pub/sub

.Apache Active Mq

.Amazon Mq

.Alibaba message services

## Enterprise Message Bus

A message bus provides one or more Applications to communicate messages to one or more applications . Unlike in messaging queues where it is based on fifo , message bus may not follow same order . A subscriber may come and go without the knowledge of message  producer .

![working of bus](https://i.stack.imgur.com/5PkJy.gif) 

Let an application  A be a message sender , which communicates messages to application B through message bus , later an application C can be configured to listen to message bus and can take actions based on the messages of  A. The configuration is done without the knowledge of application A . Message bus works based on subscribe / publish model , when a sender sends messages in message bus any application or receiver subscribed to that kind of messages can listen to them and take actions and update .  This approach allows application to follow open / closed  principle ,where they are open to future changes while remaining closed for additional modifiactions.
