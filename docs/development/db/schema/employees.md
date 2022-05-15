# employees

### employees Collection:

| _id | empNum | companyId | name | role | email | phoneNum | password | vatId | ssNum | active | type |
|-----|--------|-----------|------|------|-------|----------|----------|-------|-------|--------|------|

* _id: Unique MongoDB document id (ObjectId)
* empNum: Company Letter +  Employee Number
* companyId: ObjectId for the Company on another collection
* name: Full legal name
* role: Role in the company
* email: Employee email (for notifications)
* phoneNum: Phone number in international format
* password: SHA256+Salt encrypted password
* vatId: Vat ID for Tax/IRS purposes
* ssNum: Social Security Number
* active: Does person still work at the company?
* type:
    * admin: Company IT Admin
    * hr: HR Employees
    * accounting: Accounting Employees
    * employee: A employee