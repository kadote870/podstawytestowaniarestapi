# Case study: Keys blacklist tests

```mermaid
stateDiagram-v2
direction LR

state MONOLIT{
    Blacklist
    Storage
    Offer_Creator
    Final_Offer
}

```

```mermaid
stateDiagram-v2
direction LR

state Offer_Creator{
    Key
}

state Key_Logistic_Service {
    Blacklist
    Storage
}

Key --> Blacklist
Blacklist --> Storage
Storage --> Final_Offer
```