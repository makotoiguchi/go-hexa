# Studying Hexagonal Architecture in Golang

## ref

  - Arquitetura Hexagonal em Golang
    <https://youtu.be/wYyHZL1r7dQ?si=Bhv13cRjEtbULo3Z>


## Domain Layer

`Presentation -> Application -> Domain`

Domain layer contains business logic and types.

It should be Agnostic:
  - no external depdencies
  - it should not depend on any framework (JSON/BSON/SQL tags, bindings, specific data primitives, etc)

This layer should define data models and structures that represents business entities and concepts.


## Domain Objects

Consider that the Domain object is the Original object, the Reference object.
Any other representation of the same information should be created from the Domain object.

For example: 
  - Domain object --> Postgres entity
  - Domain object --> MongDB entity
  - Domain object --> RabbitMQ entity


--------------------

## Application Layer

All input data will arrive at the Application through a Port, coming from an Adapter.
All output data will be sent by the Application through a Port, to an Adapter.
Data will received and sent in Domain data model format.
No external data model should be used by Application.


--------------------

## Adapter Layer

### Input - through Use case

May receive data from different requestors/invokers and needs to convert it to Domain data model format before invoking Application (defined by the Use Case Interface).
Response will be returned by the Application in Domain data model format. Data should be converted to requestor/invoker expected format before replying to it.


### Outpout - through Port

Will receive data from the Application in Domain data model format and needs to convert it to the external resource specific format.

