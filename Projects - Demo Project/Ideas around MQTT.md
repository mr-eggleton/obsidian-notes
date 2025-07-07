
```mermaid
sequenceDiagram
Real Fish Tank -->> Broker: measurements
Broker-->>Data Store: measurements
Web Front End->>Data Store: measurement data request
Data Store->>Web Front End: measurement data
Web Front End-->>Broker: range data request
Broker-->>Web Front End: range data
Web Front End-->>Broker: range data change
Broker-->>Web Front End: range data
Broker-->>Control System : range data
Control System-->>Broker : range data
Broker-->>Real Fish Tank: control data
Broker-->>Web Front End: control data
```

