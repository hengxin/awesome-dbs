## mongodb-consistency-models

## General Consistency Models
- [Consistency Models @ jepsen.io](https://jepsen.io/consistency#fn-1)

> Jepsen analyses the safety properties of distributed systems–most notably, 
identifying violations of consistency models.
But what are consistency models? 
What phenomena do they allow? 
What kind of consistency does a given program really need?
In this reference guide, we provide basic definitions, intuitive explanations, 
and theoretical underpinnings of various consistency models for engineers and academics alike.

- [Read Concerns @ mongodb-manual](https://docs.mongodb.com/manual/reference/read-concern/?_ga=2.214513239.1537524606.1571995321-1885120209.1571995321#readconcern-option)
- [Read Isolation, Consistency, and Recency @ mongodb-manual](https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#read-isolation-consistency-and-recency)

## Tunable Consistency Models

## Causal Consistency
- [Causal Consistency @ jepsen.io](https://jepsen.io/consistency/models/causal)
  - Convergent causal systems
  - Causal consistency is sticky available
  - Real-Time Causal
  - CausalVisibility + CausalArbitration + RVal
- [Causal Consistency and Read and Write Concerns @ mongodb-manual)](https://docs.mongodb.com/manual/core/causal-consistency-read-write-concerns/)
