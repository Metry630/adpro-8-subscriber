a. What is AMQP?

AMQP, or Advanced Message Queuing Protocol, is a messaging protocol designed to facilitate communication between client applications and message brokers. It ensures reliability, efficiency, and flexibility in handling messaging tasks.

b. What does "guest:guest@localhost:5672" signify? What is the first "guest," and what is the second "guest," and what is "localhost:5672" used for?

In "guest:guest@localhost:5672," the first "guest" signifies the username, while the second "guest" denotes the password for accessing the RabbitMQ server. "localhost:5672" represents the address of the RabbitMQ server, with the default port being 5672.
![Screen Shot 2024-04-23 at 12.10.07.png](img%2FScreen%20Shot%202024-04-23%20at%2012.10.07.png)
The spikes indicate the message rates of how many messages are sent within a time interval. Because the publisher sends messages to the message broker the spikes appear.

![Screen Shot 2024-04-23 at 12.56.36.png](img%2FScreen%20Shot%202024-04-23%20at%2012.56.36.png)
![Screen Shot 2024-04-23 at 12.58.46.png](img%2FScreen%20Shot%202024-04-23%20at%2012.58.46.png)

In the image, it's clear that each subscriber gets different data when the publisher sends a lot of data to the message queue. This happens because each subscriber works like its own app, so they grab data from the message queue separately. Once data is taken from the queue, the message disappears, and other apps can't use it.

Also, I think improving the performance of subscriber apps can be done by making them multithreading, so they can handle many publisher events at once.

