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
Web Front End->>Data Store: historical data request
Data Store->>Web Front End: historical data
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

The kids write a Control System that starts subbed to a simulation with a visualisation that it subbed to the simulation too. runs at 60  times speed. 

The fake tank can be attached to the control data of one of the simulated tanks.

A control system can then be subbed to the fake tank measurements and really take over.



```mermaid



```

```mermaid

C4Context
		title System Context diagram for Internet Banking System
		Enterprise_Boundary(b0, "BankBoundary0") {
		  Person(customerA, "Banking Customer A", "A customer of the bank, with personal bank accounts.")
		  Person(customerB, "Banking Customer B")
		  Person_Ext(customerC, "Banking Customer C", "desc")
  
		  Person(customerD, "Banking Customer D", "A customer of the bank, <br/> with personal bank accounts.")
  
		  System(SystemAA, "Internet Banking System", "Allows customers to view information about their bank accounts, and make payments.")
  
		  Enterprise_Boundary(b1, "BankBoundary") {
  
			SystemDb_Ext(SystemE, "Mainframe Banking System", "Stores all of the core banking information about customers, accounts, transactions, etc.")
  
			System_Boundary(b2, "BankBoundary2") {
			  System(SystemA, "Banking System A")
			  System(SystemB, "Banking System B", "A system of the bank, with personal bank accounts. next line.")
			}
  
			System_Ext(SystemC, "E-mail system", "The internal Microsoft Exchange e-mail system.")
			SystemDb(SystemD, "Banking System D Database", "A system of the bank, with personal bank accounts.")
  
			Boundary(b3, "BankBoundary3", "boundary") {
			  SystemQueue(SystemF, "Banking System F Queue", "A system of the bank.")
			  SystemQueue_Ext(SystemG, "Banking System G Queue", "A system of the bank, with personal bank accounts.")
			}
		  }
		}
  
		BiRel(customerA, SystemAA, "Uses")
		BiRel(SystemAA, SystemE, "Uses")
		Rel(SystemAA, SystemC, "Sends e-mails", "SMTP")
		Rel(SystemC, customerA, "Sends e-mails to")
  
		UpdateLayoutConfig($c4ShapeInRow="3", $c4BoundaryInRow="1")


```
