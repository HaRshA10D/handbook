# Database

What is a distirbuted system?

> A collection of independent computers appear to it's user as one computer.

#### Three charectaristics

* They operate concurrently
* They can fail independently
* They don't share a global clock

Examples are explained in 
#### Three Topics

* Storage
* Computation
* Messaging


### Storage


#### Scale - 1

Most common case, simple and works well

> postgres

**single master**

It exist on one host and all reads and writes happen on one instance.

#### Scale - 2

* reads are less costlier than writes
* Read trafic increases
* Strong consistency

**read replication**

* Reads happen on replicas
* Writes happen to leader
* Broken consistency due to replication lag, stale reads can happen
* Eventual consistency
* Can scale reads by adding more and more replicas

#### Scale - 3

Writes increased so single leader can't handle

**sharding**

* Multiple shards with their replicas
* Broken data model, can't join tables

#### Scale - 4

Reads are not performing properly

**indexes**

* Try tuning indexes by adding new ones and removing not needed ones
* Join on indexes and improve queries

**denormalize**

* Increase redundancy for performance
* Breaks the purpose of relational model
* ALmost immporal

#### Scale - 5

When the tables are denormalized, why not go with a non relational database

>cassandra 

**consistent hashing**

**replication**


### Consistency problem

R+W>N

Then system is consistent.


### CAP theorem

---

c - consistency

a - availability

p - partition tolerence
