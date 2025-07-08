## Real Fish Tank System

```mermaid
sequenceDiagram
Real Fish Tank -->> Broker: measurements
Broker-->>Control System : measurements
Broker-->>Display : measurements
Control System-->>Broker : control data
Broker-->>Real Fish Tank: control data
Broker-->>Web Front End: control data
Broker-->>Data Store: measurements
Broker-->>Display: control data
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
Broker-->>Display: control data
```

But because of Pub/Sub we can use other arrangements for demos etc.

The kids write a Control System that starts subbed to a simulation with a visualisation that it subbed to the simulation too. runs at 60  times speed

The fake tank can be attached to the outputs of one of the simulated tanks.

A control system can then be subbed to the fake tank measurements and really take over.
