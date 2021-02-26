# mongodb-driver

## Overview
- [MongoDB Drivers](https://docs.mongodb.com/ecosystem/drivers/)
A list of MongoDB drivers for various programming languages.

- [MongoDB Drivers Specs](https://docs.mongodb.com/ecosystem/drivers/specs/)
  - [read-write-concern.rst](https://github.com/mongodb/specifications/blob/master/source/read-write-concern/read-write-concern.rst)
  - [crud.rst](https://github.com/mongodb/specifications/tree/master/source/crud)
  - [server-write-commands.rst](https://github.com/mongodb/specifications/blob/master/source/server_write_commands.rst)
  > -  Method to do writes (insert/update/delete) that declares the write concern up front
  > -  Support for batch operations
  - [driver-sessions.rst](https://github.com/mongodb/specifications/blob/master/source/sessions/driver-sessions.rst)
    > This specification is limited to *how applications start and end sessions*. Other specifications define various ways in which sessions are used (e.g. *causally consistent reads, retryable writes, or transactions*).
  - [causal-consistency.rst](https://github.com/mongodb/specifications/blob/master/source/causal-consistency/causal-consistency.rst)
    > This spec builds upon the *Sessions Specification* to define how an application *requests* causal consistency* and how a driver interacts with the server to *implement* causal consistency.
  - [transactions.rst](https://github.com/mongodb/specifications/blob/master/source/transactions/transactions.rst)

## Drivers & Programming Languages
### C++
- [MongoDB C++ Driver](http://mongocxx.org/)

### Python
- [M220P: MongoDB for Python Developers](https://university.mongodb.com/courses/M220P/about)
  > This course will teach you how to use MongoDB as the database for a Python application. You'll play the role of a back-end developer for a Python application, and your job is to implement the application's communication with MongoDB.
 
 ### Java
 - [API Docs for MongoDB Java Driver](https://mongodb.github.io/mongo-java-driver/4.0/apidocs/mongodb-driver-sync/index.html)
