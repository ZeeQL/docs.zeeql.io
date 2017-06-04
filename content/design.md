# ZeeQL Framework Design

> Work in progress. Stay tuned.

ZeeQL is a Swift ORM / database access library primarily inspired by EOF,
and in consequence CoreData. Adding some ActiveRecord ideas.

The basic setup is that Access has two levels of abstraction:
- adaptor  level (`Adaptor`,  `AdaptorChannel`)
- database level (`Database`, `DatabaseChannel`, `DatabaseDataSource`)

In general it is recommended to write a Model or a Model pattern, and then
use the DatabaseDataSource to fetch mapped objects.
However, for simple SQL you can also do that in rather convenient ways at the
adaptor level.

Important: to inject raw SQL you don't have to go down to adaptor level. You
have various ways to embed SQL in the model and thats the recommended way to
do it. [Raw SQL Injection Notes](embedsql.md).


### Adaptor Level

The adaptor level is a relatively thin wrapper around the client libs, e.g.
Apache DBD, which provides some convenience methods, model reflection etc.

TBD: document


### Database Level

TBD: document
