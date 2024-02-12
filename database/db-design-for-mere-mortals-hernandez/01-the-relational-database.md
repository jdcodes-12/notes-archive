# DB Design | The Relational Database

## Types of Databases
`OLTP`: online-transaction processing
  - collect, modify, and maintain data on a daily basis
  - "operational database"
    - constantly changes
    - data reflects "up-to-the-minute" information
  - often used in:
    - hospitals & clinics
    - manufacturing companies
    - retail organizations

`OLAP`: online-analytics processing
  - "analytics database"
  - good for:
    - tracking trends in data
    - viewing statistics over long-period of times
    - making tactical or strategic business projections
  - stores static data (i.e. data rarley changes over time)
  - reflects a "point-in-time" snapshot of data
  - often used in:
    - chemical labs
    - geological companies
    - marketing analysis firms
  - main data source comes from the operational datases (OLTP_

## Early Database Models

### The Hierarchical Database
- Tree based hierarchy of data (parent/child relationships)

### The Network Database
- Relies on Nodes & Set Structures

## The Relational Database Model
- Proposed by Dr. Edagar F. Codd (IBM research scientist)

- Based on set theory & first-order predicate logic (math)

- Stores data in `relations`, which user preceives as tables

- Relationship types:
  - one to one (1:1)
  - one to many (1:n)
  - many to many (n:n)

- Relationships made via matching shared values in among tables
- Uses SQL to create, modify, and retrieve data

### Advantages of Relational Database
1. Built-in multilevel data integrity
2. Logical and physical data independence from DB applications
3. Guaranteed data consistency and accurcy
4. Easy data retrieval

