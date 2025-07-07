
```mermaid
sequenceDiagram
Real Fish Tank -->> Broker: measurements
Broker-->>Data Store: measurements
Web Front End->>Data Store: measurement data request
Data Store->>Web Front End: measurement data
Web Front End->>Data Store: control data request
Data Store->>Web Front End: control data
Web Front End->>Broker: control data change
Broker->>Web Front End: control data


```

