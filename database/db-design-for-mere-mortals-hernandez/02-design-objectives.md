# Database Design | Chapter 2: Design Objectives

## Why Be Concerned with Database Design?
- Crucial for data consistency, integrity, and accuracy
- Poorly design DB:
  - can lead to inaccurate information (most detrimental)
    - may affect the company's bottom line severly
  - can make the table hard to query
  - more efficient data stroage
  - can lead to easier maintenance & management

- Logical Database Design
  - describe shape, size, and necessary systems for the DB
  - addresses information & operational needs of the business
  
- Physical Implementation
  - created once you have the logical design (via RDBMS)
  - can use design tools to reduce time of creating tables

- End-User Applications
  - creating apps to interact with the newly implemented DB
 
## The Importance of Theory
- Relational DB Model:
  - based on set theory & first-order predicate logic
    - guarantees data accuracy

## Advantages of Learning Good Design
- Learning good DB design methodology:
1. provides skills to design a structurally sound DB
2. provides set of techiniques to guide through design process
3. reduce the number of re-iterations of making the DB
4. make the DB design process easier and shorter
5. enable more effective use of the underlying RDBMS

## Obejctives of Good Design
- A good DB design:
  1. supports required & ad hoc information retrieval
  2. table constructed properly & efficiently
    - tables concerned with a single entity
    - tables composed of atributed describing the one entity
    - keep redudnant data to an absolute minimum
    - table is referend throughout DB via unique value (keys)
  3. data integrity imposed at field, table, relationship levels
    - the levels of intergrity help guarantee data accuracy
  4. supports business rules relevant to the organization
    - must provide meaningful, accurate and valid info
  5. lend to future growth
    - easy to modify/expand as information requirements grow

## Benefits of Good Design
- Appling good design brings these advantages:
  1. DB structure easy to modify & maintain
    - updates to one table or field won't affect other tables or fields in a DB
  2. Data is easy to modify
    - changes to a field won't affect other values in the table
    - duplicates reduce to bare minimum
  3. Information is easy to retrieve
    - easier query creation beacuse:
      - tables are structured well
      - relationships are established well
  4. End-user apps are easy to develop & build
    - can focus more on app development & data processing

## Database Design Methods

- Traditional DB design includes:
  1. requirements analysis
  2. data modeling
  3. normalization

- Requirements Analysis
  - gathering the intended constraints and scope of the database
  - gathering informational and operational requirements of the data being collected

- Data modeling
  - logical reasoning about the data via creating Entity Relation Diagrams (ERDs)
  - thinking about:
    - tables needed
    - relationships among tables
    - giving attributes/fields to the entity
    - assigning keys:
      - primary: for establishing identity & data integrity
      - foreign: for establishing relationships between tables

## Normalization
- Normalization
  - happens after initial data modeling (sidenote: it's an on going process during design)
  - decompose large tables into smaller ones
  - aim to reduce redundant data & duplicate data
  - tables tested again 'Normal Forms'

- `normal form`: set of rules that can be used to test a table structure to insure soundness
  - First Normal Form  (1NF)
  - Second Normal Form (2NF)
  - Third Normal Form  (3NF)
  - Fourth Normal Form (4NF)
  - Fifth Normal Form  (5NF)
  - Boyce-Codd Normal Form
  - Domain/Key Normal Form
