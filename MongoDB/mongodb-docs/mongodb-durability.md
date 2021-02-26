# mongodb-durability

- [Term: Durable](https://docs.mongodb.com/manual/reference/glossary/#term-durable)
> A write operation is durable when it will persist *across* a shutdown (or crash) and restart of one or more server processes. 
> - For a single `mongod` server, a write operation is considered durable when it has been written to the server’s journal file. 
> - For a replica set, a write operation is considered durable once the write operation is durable on a majority of voting nodes; i.e. written to a majority of voting nodes’ journals.

## Articles
- [(May 7, 2017; brandur) The long road to Mongo's durability](https://brandur.org/fragments/mongo-durability)
> About `write concern` and `journaling`

- [(Sep 13, 2018; InfoQ) 14 Things I Wish I’d Known When Starting with MongoDB](https://www.infoq.com/articles/Starting-With-MongoDB/)
> the "Using fast writes" section; talking about `journaling`

- [(Quora) How durable is MongoDB?](https://www.quora.com/How-durable-is-MongoDB)
> talking about "possible failure scenarios"

- [Understanding durability & write safety in MongoDB (Aug 26, 2014; Dharshan Rangegowda; DZone)](https://dzone.com/articles/understanding-durability-write)
> 

> Written with [StackEdit](https://stackedit.io/).
