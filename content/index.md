# ZeeQL Documentation

**ZeeQL** is a Swift ORM / database access library primarily inspired by EOF,
and in consequence CoreData, adding some ActiveRecord concepts. 
The framework is self contained and doesn't have any 3rd party dependencies. 
It comes with a SQLite3 driver builtin, and APR as well as a standalone
PostgreSQL driver as optional modules.

The framework can be used in either server side Swift applications or in client
applications (iOS or macOS apps).
It is not quite there yet, but could potentially serve as a pure Swift CoreData
replacement that doesn't just work w/ SQLite3 but with other servers as well.

### Provides Choices

Use raw SQL queries in a typesafe way:

```swift
try adaptor.select("SELECT name, count FROM pets") {
  ( name: String, count: Int) in
  print("\(name): #\(count)")
}
```

Use full object fetches, and prefetch relationships:

```swift
let objects = try datasource.fetchObjects(
  Person
    .where(Person.e.login.like("he*"))
    .limit(10)
    .prefetch(Person.e.addresses)
    .order(by: Person.e.login)
)
```

Or partial object fetches, which still provide most of the neat stuff
while avoiding fetching full objects all the time:

```swift
let partials = try db
  .select(Person.e.firstname, from: Persons.self)
   .where(Person.e.login.like("he*"))
   .order(by: Person.e.login)
)
```

Declare your models in neat code (either typesafe, or by using names),
or fetch them from the database information schema,
or design them with the Xcode CoreData modeler.


### WORK IN PROGRESS, STAY TUNED

ZeeQL is still being prepared. Please stay tuned for the release. 
If you want to stay up to date, subscribe to the 
[ZeeQL Blog](http://zeeql.io/blog/).
