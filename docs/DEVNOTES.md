# Collections

## Schema:
### employees table:

| _id | empNum | empIdent | companyId | name | role | email | phoneNum | password | vatId | ssNum | active | type |
|-----|--------|----------|-----------|------|------|-------|----------|----------|-------|-------|--------|------|
  
`empMovements` table

| _id | empId | time | action |
|-----|-------|------|--------|

`company` table

| _id | codeLetter | name | legalName | nif | ssNum | location |
|-----|------------|------|-----------|-----|-------|----------|

`logs`

| _id | empId | action | time | ip |
|-----|-------|--------|------|----|



## Type/Permissions Levels
`admin`: 
* Company Admin  

`hr`: 
* HR employees (allow salary and user management)

`accounting`: 
* Accounting/Treasury employees (allow finance movements)

`employee`:
* Employee page only
* Can edit:
    * Email, password
* Can see:
    * All financial documents and their dates (salaries, bonus, etc)
    * a
* Can request:
    * Vacations
    * Legal Documents

____________________________________________
# Routes
* /employee/*
    * Employee related stuff such as editing email password and checking the documents (salaries, etc)
* /accounting/*
    * Send invoices and accounting stuff (banking, etc)
* /hr/*
    * Salaries, approval of vacations, etc
