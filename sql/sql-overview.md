# Learning SQL | Basics -> Intermediate

## Terminology

### General Terms
- `database`: set of related information
- `database system`: computerized data storage & retrieval mechanisms

### Databse System Terms
- `optimizer`: determines the most efficient way to execute SQL queries
- `optimizer hints`: influence the way the optimizer determines the query 

### Relational Database Terms
- `entity`: something of interest to a DB user (i.e. customer, account, etc.)
- `table`: set of rows - either in memory (nonpersistent) or on permanent storage
- `column`: individual piece of data stored in a table
- `row`: set of columns that describe an entity (also. "record")
- `result set`: non-persistent table, usually a result of a SQL query
- `primary key`: 1+ columns used to uniquely identify a row within a table
- `foreign key`: 1+ columns used to identify a single row from another table
- `persistant table`: a table that is stored permanentaly on some storage device
- `non-persistant table`: a table stored within memory
- `normalization`: refinding a DB to ensure data is independant and in one place

### SQL Terms
- `schema statements`: used to define the shape and constraints of a table
- `data statements`: used to manipulate the data within a schema (i.e. table)
- `transactions statement`: use to being, end, and roll-back transactions
- `subquery`: a query inside another query. Used to generate temp tables.

## SQL Language

### Data Types
> Common datatypes across all Database Management System vendors (e.g. Oracle
> Microsoft, MySQL, PostgreSQL, etc.). To get the most udpated information for you
> current SQL vendor, it is best to reference their updated documentation.

### Chatacter Types
- `varchar(n)`: variable string of max length of `n` characters
  - not right-padded with space characters
  - amount of bytes used will vary

- `char(n)`: fixed-length string of size `n`.
  - right-padded with space characters until upper limit `n` is hit
  - always consume the same about of bytes

- Character Sets
  - determinet the letters/symbols that can be stored within the DB or column
  - `multibyte set`: a character set which one symbol takes up more than 1 byte
  - `singlebyte set`: a character set which one symbol takes only 1 byte to store


### Numeric Types (MySQL)
> Database Management Systems can store numeric dasta - integers and floats. Below
> are the numeric type associated with MySQL. Check the docs of the vendor you are
> using to see which numeric types it utilizies.

- MySQL Integer Types
  - `Tinyint`
  - `Smallint`
  - `Mediumint`
  - `Int`
  - `Bigint`

- MySQL Floating-Point Types:
  - `Float(precision, scale)`
  - `Double(precision, scale)`

- Side notes:
  - `precision`: the total number of digits to the left and right of deicmal point
  - `scale`: the totoal number of digits allowed to the right of the decimal point

### Temporal Types (MySQL)

- Datetime Formatters:
  - `%a`: short weekday name (i.e. Sun, Mon, etc.)
  - `%b`: short month name (i.e. Jan, Feb, etc.)
  - `%c`: numeric month (i.e. 1, 2, 3, etc.) 
  - `%d`: numeric day of month (00..31)
  - `%f`: number of microseconds (000_000..999_999)
  - `%H`: hour of day, in 24-hour format (00..23)
  - `%h`: hour of day, in 12-hour format (01..12)
  - `%i`: minutes within hour (00..59)
  - `%j`: day of year (001..365)
  - `%M`: full month name (i.e. January..December)
  - `%m`: numeric month
  - `%p`: AM or PM
  - `%s`: number of seconds (00..59)
  - `%W`: full weekday name (Sunday..Saturday)
  - `%w`: numeric day of week (0=Sunday..6=Satruday)
  - `%Y`: four-digit year (i.e. 2042)

## Understanding SQL Queries

### Common Query Operators
- `select`: initiates a query, determines which columns to use in result set
- `from`: determines which table to use & how to join tables
- `where`: filter unwanted rows based on some condition
- `group by`: group rows by common column values
- `having`: filter unwanted groups based on some condition
- `order by`: sort row of final result set by one or more columns
- `distinct`: remove duplicates

### From Clauses
