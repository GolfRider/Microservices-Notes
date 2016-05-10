### Microservices-Notes
Notes on Microservices based System Design &amp; Architecture

  1. Microservices based system is actually a Distributed System
  2. Distributed Systems comes with their unique complexities
  3. Embrace Failure,rather than preventing it (Let it crash approach)
  4. Isolation: Isolate services by transaction boundaries/bounded context/business features
  5. So it doesn't has to be small, but it has to be of the right (optimal/minimal) size 
  6. Asynchronous messaging/computation/communication (non-blocking calls) is essential for scalability/resilience
  7. Much thought has to be spent on communication interfaces than the service's internal implementation - In any System Design
  8. The hard+interesting things exist in-between the services
  9. Refactoring a Monolith into micro-services/building microservices from scratch 
                          : Service Transaction Boundaries play a major role
  10. Do only ONE thing well:  Services should be highly focussed, follow the UNIX philosophy
                               Should have Single Responsibility  
  11. Autonomous services
  12. Services Owns their Data/State
  13. Embrace Polyglot Systems+DB (Can have multiple tech stacks depending on the use case)
  14. Standard Communication Protocols: JSON (Data format),HTTP/REST(Sync Transport), Websockets (Async Messaging/Streaming)
  15. Immutablity: Represent States/Events/DTO as immutable objects
  16. CQRS : Separate Read & Write Queries for both Persistence/Queries
             Avoid Updates/Deletes on Data (Only CR of CRUD)
             Optimize Write & Optimize Read separately as they are 2 different system-concerns
             Enables better performance,reduced locks
  17. Read Side usually needs more scalability
  18. Eventually Consistency should be embraced
  19. There is no atomic-style Distributed Transactions, things can fail at any stage
  20. Use compensating action for rollbacks
  21. Isolation: Each service can be managed,deployed & scaled independently
  22. Build Services-By-Services
  23. Realize business use-cases as workflows comprising of mutliple micro-services
  23. Operational+Deployment+Test efficiency, Conitnuous Integration
  24. Increases lot of operational overhead, so best practices/processes should be in place
      otherwise things can get pretty messy
  25. Avoid the temptation of having a GLOBAL-CONSISTENT VIEW of the system
  26. Java/Scala Frameworks:    Spring Cloud (Pivotal)
                                Lagom (LightBend,formerly Typesafe)

  
