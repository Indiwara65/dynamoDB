# dynamoDB
* dynamoDB is a fully managed serverless DB offered by AWS.
* dynamoDB is made up of tables and is a NoSQL database.
* Each table must have a partition key (unique) and optionally a sort key (both key combinations must be unique).
* Each row in a table is an item with a maximum size of 400kB.
* Partition key and the sort key (if present) are mandetory fileds for a item in a table.
* Same field cannot be both the partition key and the sort key.
* **Data Types** -
    1. Scalar Types
          + String - text - "name":"Bob"
          + Number - integer and float - "price":15.92
          + Boolean - true/false - "booked":true
          + Binary - base64 encoded binary
          + Null - null
    2. Document Types
         + List - list of values - "names":[ "Bob" , "Jane", "Ella"]
         + Map - JSON like objects - "data" : {"name":"Bob", "age":20}
    3. Set Types
         + Sting Set - set of string values - "name":{"Bob" , "Jane", "Ella"}
         + Number Set - set of numbers - "numbers" : {10, 20, 30}
## Query vs Scan    
* Query is very efficient compared to Scan.
* Scan reads all the content in the table and then sort them out.
* Query is always prefered over Scan.
* Scan can be used to read all records in a table or to sort fileds that are not partition or sort keys.
## Conditions     
#### Partition Key
- Only condition that can be used is equal to.
-  .eq(value)
#### Sort Keys  
- .eq(value) - Key('job_id').eq('JOB#001')
- .lt(value) - Key('part_id').lt('PART#005')
- .gt(value) - Key('part_id').gt('PART#005')
- .lte(value) - Key('part_id').lte('PART#005')
- .gte(value) - Key('part_id').gte('PART#005')
- .begins_with(value) - Key('part_id').begins_with('PART#')
- .between(value) - Key('part_id').between('PART#001', 'PART#010')
#### Other Fields            
* All conditions used for sort keys can be used but are inefficient.
#### Multiple Conditions
* AND - Key('user_id').eq('user_1') & Attr('username').eq('James')
* OR - Key('user_id).eq('user_1') | Key('user_id).eq('user_2') | Key('user_id').eq('user_3')
## GSI - Global Secondary Index

## LSI - Local Secondary Index





