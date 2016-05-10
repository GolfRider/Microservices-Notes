### Microservices-Notes
Notes on Microservices based System Design &amp; Architecture

  1. Microservices based system is actually a Distributed System
  2. Distributed Systems comes with their unique complexities
  3. Embrace Failure,rather than preventing it (Let it crash approach)
  4. Service Discovery: Clients discover servics via service discovery. Eg:Netflix Eureka,Zookeeper
  5. Configuration: Service Configuration externalized/versioned/centralized
                    Can be applied without restarting the services 
  6. Isolation: Isolate services by transaction boundaries/bounded context/business features
  7. So it doesn't has to be small, but it has to be of the right (optimal/minimal) size 
  8. Asynchronous messaging/computation/communication (non-blocking calls) is essential for scalability/resilience
  9. Much thought has to be spent on communication interfaces than the service's internal implementation - In any System Design
  10. The hard+interesting things exist in-between the services
  11. Refactoring a Monolith into micro-services/building microservices from scratch 
                          : Service Transaction Boundaries play a major role
  12. Do only ONE thing well:  Services should be highly focussed, follow the UNIX philosophy
                               Should have Single Responsibility  
  13. Autonomous services
  14. Services Owns their Data/State
  15. Embrace Polyglot Systems+DB (Can have multiple tech stacks depending on the use case)
  16. Standard Communication Protocols: JSON (Data format),HTTP/REST(Sync Transport), Websockets (Async Messaging/Streaming)
  17. Immutablity: Represent States/Events/DTO as immutable objects
  18. CQRS : Separate Read & Write Queries for both Persistence/Queries
             Avoid Updates/Deletes on Data (Only CR of CRUD)
             Optimize Write & Optimize Read separately as they are 2 different system-concerns
             Enables better performance,reduced locks
  19. Read Side usually needs more scalability
  20. Eventually Consistency should be embraced
  21. There is no atomic-style Distributed Transactions, things can fail at any stage
  22. Use compensating action for rollbacks
  23. Isolation: Each service can be managed,deployed & scaled independently
  24. Build Services-By-Services
  25. Realize business use-cases as workflows comprising of mutliple micro-services
  26. Operational+Deployment+Test efficiency, Conitnuous Integration
  27. Increases lot of operational overhead, so best practices/processes should be in place
      otherwise things can get pretty messy
  28. Avoid the temptation of having a GLOBAL-CONSISTENT VIEW of the system
  29. Java/Scala Frameworks:    Spring Cloud (Pivotal)
                                Lagom (LightBend,formerly Typesafe)

  30. Functional Programming Helps in distributed systems.
       Eg: Spark, Kafka, Akka etc
