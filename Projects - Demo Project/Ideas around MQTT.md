## Real Fish Tank System

```mermaid
sequenceDiagram
Real Fish Tank -->> Broker: measurements
Broker-->>Control System : measurements
Control System-->>Broker : control data
Broker-->>Real Fish Tank: control data
Broker-->>Web Front End: control data
Broker-->>Data Store: measurements
Web Front End->>Data Store: measurement data request
Data Store->>Web Front End: measurement data
Web Front End-->>Broker: range data request
Broker-->>Web Front End: range data
Web Front End-->>Broker: range data change
Broker-->>Web Front End: range data
Broker-->>Control System : range data
Control System-->>Broker : control data
Broker-->>Real Fish Tank: control data
Broker-->>Web Front End: control data
```

But because of Pub Sub we can use other arrangements for demos etc.

The kids write a Control System that starts subbed to a simulation with a visualisation that it subbed to the simulation too. runs at 60  timespeed*
