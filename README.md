# Grubdash: Backend/API

![Alt text](grubdash-header.jpg)

## A demonstration of backend work and RESTful API implementation.
This project sets up a RESTful API, as well as uses custom validation functions, route handlers, and specific API endpoints I created. Note: This repository only contains backend server-side/API code and is meant to only demonstrate backend development. This repository does not include any front-end elements nor is it meant to be interpreted as a full-stack application.


## Concepts and Tools used throughout the implementation of this project include:

### RESTful design principles
A robust API should give clear direction for API developers and consumers. It should be easy for the people who are using it to make sense of it. Accordingly, the API's design should be simple, predictable, and consistent. One way to ensure a robust API design is by following RESTful design principles when creating your API.

REST, which stands for representational state transfer, is a software architecture style. REST is a set of constraints for building web APIs. A RESTful API server provides access to resources. A client, like the browser or another server, can then access and change the resources.

### Major error types and handling
Another key feature of a robust API is its error-handling approach. When building RESTful APIs using Express, or any other framework or library, validation checks are always necessary as a best practice. And it's always important to return an error response to the client, so that the client can stay informed on why their request isn't working.

However, as the API grows in size and complexity, handling every possible error and returning a response for every validation check can quickly become tedious; it can make it difficult to quickly grasp what the code is doing. Having a centralized error-handling approach can simplify the code.

### Organizing Express code
Besides following RESTful design principles and having centralized error handling, a robust API is built on top of well-organized and well-structured code. Like all software projects, Express APIs tend to get larger and more complex over time. The more files that you have in the project, the more important that the file organization becomes. The files need to be organized in a way that makes it easy to find and modify existing code, and to add new code in a location consistent with the existing code. An example of advanced organization is by using ideas like:

- **Group-by-resource structure:** A file organization structure in which any code that handles requests to a resource is stored in a folder with the same name as the resource, regardless of the URL to that resource.

- **Controller files:** A file that defines and exports the route handler functions and is responsible for managing the state of a single resource in an API.

- **Express router:** A modular middleware and routing system that can be attached to an Express app

### Passing data on the response
There is a special ```locals``` property on the response that can be used to share variables scoped to the request. The ```locals``` property is an object where you can add properties that will be available only during that request-response cycle. Once the request-response cycle ends (meaning that the response has been sent to the client), the ```locals``` object is deleted.
