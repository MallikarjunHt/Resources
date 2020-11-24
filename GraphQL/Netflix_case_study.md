# How Netflix Scales its API with GraphQL Federation

* Netflix is known for its loosely coupled and highly scalable microservice architecture.
* Independent services allow for evolving at different paces and scaling independently.
* Yet they add complexity for use cases that span multiple services.
* Rather than exposing 100s of microservices to UI developers, Netflix offers a unified API aggregation layer at the edge.

>UI developers love the simplicity of working with one conceptual API for a large domain. Back-end developers love the decoupling and resilience offered by the API layer. 

* Netflix has developed a federated GraphQL platform to power the API layer.

##  Studio Edge
![Content Lifecycle](https://miro.medium.com/max/700/0*tF6eYngRkxpxmVus)

