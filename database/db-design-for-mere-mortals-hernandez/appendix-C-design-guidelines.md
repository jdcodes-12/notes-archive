# DB Design | Appendix C: Design Guidelines

## Design Guidelines for Databases

### Defining and Establishing Field-Specific Business Rules
1. Select a table
2. Review each field and determine if the field needs constraints
3. Determine necessary business rules for the field
4. Establish business rules by modifying the field specification elements
5. Determine what actions test the rule
6. Record the rule on a Business Rule Specifications sheet

### Defining and Establishing Relationship-Specific Business Rules
1. Select a relationship
2. Review the relationship & determin whether it requires constraints
3. Define necessary business rules for the relationship
4. Establish buiness rules by modifying relationship characteristics
5. Determine what actions will test the rule
6. Record on the Business Rule Specficiations Sheet

### Creating Candidate Key
1. Cannot be a multi-part field
2. Must contain unique values
3. Cannot contain `NULL` values
4. Values cannot cause a breach of org's security or privacy rules
5. Values cannot be option in whole or in part
6. Use minimum number of fields to establishing uniqueness
7. Values must unique & exclusively define each record in a table
8. Value must exclusively identify the value of each field within a given record
9. Value only modified in rare or extreme cases

### Creating Foreign Key
1. Has same name as the primary key from which it is copied
2. Uses a replica of the field specs of the primary key it was copied
3. Draws values from the primary key it references

### Creating Primary Key
1. Cannot be multipart field
2. Must contain unique values
3. Cannot contain `NULL` values
4. Values cannot create a break of org's security or privacy rules
5. Cannot be optional value (in whole or part)
6. Use minimum number of fileds to establish uniqueness
7. Must uniquely and exclusively define unqiueness
8. Must exclusively identify each field within a given record
9. Value only modifed in rare or extreme cases

#### Rules for Establishing Primary Keys
1. Each table MUST have one - and only one - primary key
2. Each primary key in the DB must be unique
   - No two tables should have the same primary key (unless subset table)

### Creating the Ideal Field
1. represents a distinct characteristic of the entity
2. contains only a single value
3. cannot be deconstructued into smaller components
4. does not contain a calculated or concatenated valued
5. unique within the entire database structure
6. retains majority of its characteristics when appearn in more than 1 table

### Creating an Ideal Table
1. represnts a single entity (an object or an event)
2. has a primary key
3. does not contain multi-part or mulit-valued fields
4. does not contain calculated fields
5. does not contain unnecessary duplicate fields
6. contains absolute minimum amount of redundant data

### Field-Level Integiry
- Field-level integrity enstures:
  - identity & purpose of a field is clear
  - all tables which a field exists on is properly identified
  - field definitions are consistent throughout the DB
  - value of a field are consistent and valid
  - modifications, comparisons, and operations that can apply to a field are clearly defined and documented

### Composing Field Description
1. Accurately identify the field & clearly define its purpose
2. Write clear and succint statemnet
3. Refrain from renaming or restating the field name
4. Avoid using technical terms, acronyms, or abbreviations
5. Do not include implementation-specific information
6. Do not make description dependant on description of another field
7. Do not use exampels

### Guidelines for Composing a Table Description
1. Accurately define the table
2. Explain why the table is important to the organization
3. Statement is clear and succient
4. Do not include implemenation-specfici information ("how", "where")
5. Do not make description depend on another table
6. Do not use examples

### Guidelines for Creating Field Names
1. unique, descriptive, meaningful names (according to org's use)
2. accurately and clearly identify the name (no ambiguity)
3. use minimum number of words neccessary to convey meaning
4. no acronyms; use abbreviations sparingly
5. Do not use words that could confuse meaning of the field name
6. Do not use name that implicit or explicitly ID more than one field
7. Use singlar form on the field name

### Guidelines for Creating Table Names
1. unique, descriptive, and meaningful name (according to org's use)
2. accurately and clearly identify the Entity
3. use minimum number of words neccessary to convey meaning
4. dont use words that convey physical characteristics
5. dont use acronyms or abbreviations
6. Do not proper names or names that will restrict data entry
7. Do not try to ID more than one entity per table
8. Use plural form of the name

### Identifying Relationships
1. Select a pair of tables & find the junction between them
2. Find entry point of table A
3. Find entry point of table B
4. Determine relationship type (1:1, 1:N, M:N)
5. Diagram the relationship
6. Cross out both entries on the matrix

### Identifying View Requirements
1. Review interview notes from users & management
2. Review data entry, report, and presentation samples gathered
3. Exaim tables & subjects the above items represent
4. Analyze table relationships
5. Study business rules

### Mission Statements
- A well written mission statement is:
  1. succint & defines clear purpose of the database
  2. avoid uncessary statements or details
  3. avoids phrases or sentences that dscribe specific tasks
  4. make sense to the DB developer (you) & those using the DB

### Mission Objectives
- A well written mission objective is:
  1. declartive sentence that defines a general task
  2. not cluttered with uneccessary details
  3. expressed in general terms
  4. succint and to the point; not ambiguous
  5. makes sense to those the DB is being designed for

### Relationship-Level Integrity
- Ensure:
  1. connections between two tables (or key fields) is sound
  2. inserting new records into each table is meaningful
  3. able to delete existing record without side effects in the DB
  4. meaningful limit on # of records that can be interraled within a arelationship

### Resolving a Multivalued Field
1. Remove field from table & use it as basis for a new table
  - rename field if needed (according to field naming guidelines)
2. Take PK of origin table & place into new table structure
  - serve as part of the tables *composite PK*
  - serve as a FK to help establish relationships between origin table
3. Use appropriate name, type, and description for new table
4. Add to Final Table List

### Table-Level Integrity
- Ensures:
  - no duplicate records in a table
  - PK exclusively defines each record in the table
  - every PK is unique across the DB
  - PK values are not null
