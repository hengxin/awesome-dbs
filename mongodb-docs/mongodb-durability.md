# mongodb-durability

- [Term: Durable](https://docs.mongodb.com/manual/reference/glossary/#term-durable)
> A write operation is durable when it will persist *across* a shutdown (or crash) and restart of one or more server processes. 
> - For a single `mongod` server, a write operation is considered durable when it has been written to the server’s journal file. 
> - For a replica set, a write operation is considered durable once the write operation is durable on a majority of voting nodes; i.e. written to a majority of voting nodes’ journals.



> Written with [StackEdit](https://stackedit.io/).
