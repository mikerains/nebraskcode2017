# Advanced EF 201-301

Clayton Terry, Keyhole Software

# Alternatives:
- Dapper: fast data puling
- OrmLite: fast joins
- NoSQL: Mongo, Elastic Search

I always forget about the setup crap such as
onModelVCreating(DbModelBuilder modelBuilder) {
  modelBuilder.Configuration.Add(new InvoiceMap());
  // ...
}


## My notes, not part of presentation ...


[EF Core](https://docs.microsoft.com/en-us/ef/core/)

[EF Core InMemory DB](https://docs.microsoft.com/en-us/ef/core/providers/in-memory/)

[rEVERSE poco gENERATOR](https://github.com/sjh37/EntityFramework-Reverse-POCO-Code-First-Generator)

