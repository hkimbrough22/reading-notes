# Code 301 - Reading Notes

## API
<!-- https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design -->
1. What does REST stand for?
    - Representational State Transfer
2. REST APIs are designed around a ____.
    - Resources.
3. What is an identifer of a resource? Give an example.
    - URI for a customer order: `https://adventure-works.com/orders/1`
4. What are the most common HTTP verbs?
    - GET, POST, PUT, PATCH, and DELETE.
5. What should the URIs be based on?
    - When possible, resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource).
6. Give an example of a good URI.
    - `https://adventure-works.com/orders`
7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
    - An API that requires a client application to send multiple requests to find all of the data that it requires.
    - It is not good.
8. What status code does a successful GET request return?
    - 200
9. What status code does an unsuccessful GET request return?
    - 404
10. What status code does a successful POST request return?
    - 200, 201, 204
11. What status code does a successful DELETE request return?
    - 204

## Thing I want to know more about

- All of the common verbs. How to use them correctly.
- Just generally more familiarity with APIs.

[BACK TO HOME](../README.md)