# Database Design | Chapter 3: Terminology

## Relational Database Terminology

### Value Related
1. Data
  - static values that are stored inside the database
  - static because it doesn't change until it is purposeful modified
  - meaningless by itself; needs to be processed to make "information"

2. Information
  - the derived meaning of some processed data
  - can be presented in various forms (e.g. paper, digital, etc.)
  - what is retrieved from the database (e.g. the results of Query)

3. Null
  - represents missing or unknown value
    - DOES NOT represent zero or empty string (one or more blank spaces)
  - `NULL` can be caused when:
    - values are forgotten when input to the DB (missing values)
    - a value is truly unknown during the data entry type (unknown values)
  - negatively affects the return value for math expression & aggregates

### Structure Related
1. Table
  - also called "relation"
  - stores the collection of all records for a given entity/subject
  - the main data structure within a database
  - field order & record order has no importance (unless purposely sorted)
  - contains a primary key to uniquely identify the table
  - stores data about an obejct (user, etc.) or event (transactions, etc.)
    - for events: represents something that happens at a specific point and time
    - for objects: represents characteristics about that object 

2. Data Table
  - most commonly used table
  - stores atomic data values which are processed to make information
  - dynamic data 
    - a database user can insert, delete, modify, or process the data
  - often used directly

3. Validation Table
  - stores data specifically for mainintaing data integrity
  - contains data such as:
    - city names
    - skill categories
    - product codes
    - project identifiers, etc.
  - static data
    - data rarely changes
  - often used indirectly to validate value that are entered into a *data table*

4. Field
  - smallest structure in the database
  - represents a characteristic of the entity/subject
  - also called "attribute"
  - the place data is actually stored in
  - should contain *one and only one* piece of data to follow good design
  - example of bad fields:
    1. multipart/compsite field: contains 2+ distinct items within a value
    2. multivalued: contains multiple instances of the same type of value
    3. calculated: contains the result of some math express or joining text

5. Record
  - represents a unique instance of entity/subject of the table
  - also called "tuple" or "entry"
  - a set of fields in a table (value of field can be `NULL` or not null)
 
6. View
  - "virtual" table composed of fields from one or more other tables (base tables)
  - draws data from base tables rather than storing it's own data
  - DB only stores the structure of a view (so it can be reused later) & no data
  - advantages:
    1. enable users to work with data from multiple tables simultaneously
    2. prevent certain users from viewing or manipulating fields
    3. increase security via restricting access to sensitive data
    4. can enhance data integrity (called a "validation view" when used this way)

7. Keys
  - special fields within a table that determine the tables purpose
  - primary key
    - used to uniquely identify a record
    - can be a single or set of fields within a table
      - called "composite key" when 2+ fields used for identification
    - primary key *value*: identifies a single record in the database
    - primary key *field*: identifies a given table throughout the database 
    - enforces **table-level** integrity

  - foregin key:
    - a reference to a primary key of an external table
    - used to establish relationships between tables
    - help ensure **relationship-level** integrity
      - protects against the "orphaned record" problem
    - foreign key values MUST match the referencing primary key's value
      - gaurantee that data data responds to the record in the external table
  
8. Index
  - physical structure used to improve data processing (querying, etc.)
  - DOES NOT affect logical structure of the database

### Relationship Related
1. Relationship
  - also known as "cardinality"
  - occurs when data in table A can be associated to data in table B in some way
  - can be established via:
    - keys (primary & foreign)
    - linking tables (also known as associative table)
  - enable the creation of multi-table Views
  - crucial to data integrity because:
    1. reduces redundant data
    2. removes duplicate data

2. One-to-One Relationship (1:1)
  - single record in table A relates to only one record in table B, and vice versa
  - parent-child relationship
  - to establish:
    1. find the primary key of the "parent" table
    2. make a foreign key in the "child" table that references the parent's PK 

3. One-to-Many Relationship (1:N)
  - single record in table A can relate to multiple records in table B
  - mutliple records in table B can relate to only one record in table A
  - parent-child relationship:
    - `parent`: the table on the "one" record side
    - `child`: the table on the "multiple" record side
  -  to establish:
    1. find primary key of "parent" table
    2. make a foreign key in the "child table", referencing the parent's PK
  - elimates data duplication & keeps redudancy to a minimum

4. Many-to-Many Relationship (N:N)
  - single record in table A can relate to many records in table B, vice-versa.
  - relationship established by using a *linking table*
    - helps ensure CRUD operations of the related data
    - make it easier to associate records from two external tables
  - to make a linking table:
    1. find primary key of table A
    2. find primary key of table B
    3. create a new table that consist of PK of A and PK of B.
      - forms the composite primary key of the linking table
      - separately, these keys act as foreign keys to external table A and B
  - poorly design many-to-many relations severly affect data-integrity

5. Table Participation
  - describes the a table's importance/significance within a specific relationship
  - mandatory: before entering data into table B, must enter into a value into A
  - optional: not required to enter records into A before entering into table B

6. Degree of Participation
  - determines the minimum number of records a table must have associated w/ a single record in the related table 
  - determines the max num records a given table is allowed to have associated with a single record in the related table

### Integrity Related
1. Field Specifcation
  - known as "domain"
  - represents the aspects of a field (general, physical, logical)
    - general: 
      - metadata about the field (field name, description, parent table, etc.)
    - physical:
      - determines how a field is to be built & represented to the person using it
      - concerned with:
        1. data type of field
        2. length of field
        3. display format of field
    - logical:
      - determines the values the field can store
      - sets constraints such as:
        - if the field is required or can be null
        - acceptable range of values
        - any default values

2. Data Integrity
  - refers to the validity, consistency, and accuracy of the data in a database
  - high data-inegirty relates to higher accuracy of retrieved information!!
  - DO NOT neglecit, overlook, or underestimate data ingerity during design
    - leads to very hard to detect & correct errors (inaccurate data, etc.)

3. Table-Level Integrity
  - also known as "entity integrity"
  - ensures that:
    - no duplicate records w/in a table
    - fields are unique and can never be NULL (unless explcitly allowed)
   
4. Field-Level Integrity
  - also known as "domain integrity"
  - ensures that:
    - structure of every field is sound
    - the values in each field are valid, accurate, and consistent
    - fields of same type (i.e. Dog, City, etc.) are used throughout database

5. Relationship-Level Integrity
  - also known as "referential integrity"
  - ensures that:
    - relation between a pair of tables is sound
    - records within relations are synchronized whenver data is changed (insert, delete, updated)

6. Business Rules Integrity
  - imposees restrictions or limitations on the database according to business needs, regulations, etc.
  - during design process, clearly defined business rules can:
    - determine table structure
    - determine the relationships that can exist between tables
    - values which can be stored in fields
    - type of particiation & degree of particiation within relationships
    - type of synchonization used for relationshio-level integrity in certain relationships
