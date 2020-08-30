# mongodb-tx

## MongoDB Docs
- [Transactions@docs](https://docs.mongodb.com/manual/core/transactions/)
> With distributed transactions, transactions can be used 
across multiple operations, collections, databases, documents, and shards.

- [MongoDB Transactions: Your very First Transaction with MongoDB 4.0; 2018](https://dzone.com/articles/mongodb-transactions-your-very-first-transaction-w)
> MongoDB 4.0 implements snapshot isolation for the transactions.

## Specifications
- [mongodb/specifications/transactions](https://github.com/mongodb/specifications/tree/master/source/transactions)

## Protocols
- [Section 5 of Paper MongoDB@VLDB2019]()

## Jepsen Testing
- [MongoDB 4.2.6; Kyle Kingsbury; 2020-05-15](https://jepsen.io/analyses/mongodb-4.2.6)
> Jepsen evaluated MongoDB version 4.2.6, 
and found that even at the strongest levels of read and write concern, 
it failed to preserve snapshot isolation.