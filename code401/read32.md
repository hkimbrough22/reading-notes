# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 32 -->

[comment]: <> (https://hackernoon.com/what-is-serverless-architecture-what-are-its-pros-and-cons-cc4b804022e9)

[comment]: <> (https://aws.amazon.com/amplify/)

[comment]: <> (https://docs.amplify.aws/cli/graphql-transformer/overview/)
## Serverless Architecture
### Why?
With all of that infrastructure heavy lifting out of the way - implementing, maintaining, debugging, and monitoring - we really can focus on the business goals our applications serve.

### What is it?
Serverless is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers. A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider.

Serverless applications are event-driven, cloud-based systems where application development rely solely on a combination of third-party services, client-side logic and cloud-hosted remote procedure calls (Functions as a Service - FaaS).

FaaS is an implementation of Serverless architectures where engineers can deploy an individual function or a piece of business logic.

![Traditional versus Serverless](https://hackernoon.com/hn-images/1*x_v5NRC3TTMt1MaYl1gMUg.jpeg)

A Serverless solution consists of a web server, Lambda functions (FaaS), security token service (STS), user authentication and database.

![Serverless Example](https://hackernoon.com/hn-images/1*TIrjN7EjLUVJmJ6YvHR7Dg.png)


[BACK TO HOME](../README.md)