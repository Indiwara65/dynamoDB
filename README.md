# dynamoDB
* dynamoDB is a fully managed serverless DB offered by AWS.
* dynamoDB is made up of tables and is a NoSQL database.
* Each table must have a partition key (unique) and optionally a sort key (both key combinations must be unique).
* Each row in a table is an item with a maximum size of 400kB.
* Partition key and the sort key (if present) are mandetory fileds for a item in a table.
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
