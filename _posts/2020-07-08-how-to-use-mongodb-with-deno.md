---
title: "How to Use MongoDB with Deno"
categories: [Deno]
tags: [Deno, MongoDB]
---

## How to Use MongoDB with Deno

1) Visit 'Third Party Modules' page of 'Done' Website (<https://deno.land/x>).
![Deno_Third_Party_Modules_Page](https://user-images.githubusercontent.com/32950391/86941383-dfb4e300-c111-11ea-9e2c-e65b13658322.JPG)

2) Enter **'mongo'** on the 'Search Input Box' and press 'Enter'.
3) Click **'mongo'** link.
![Search_Mongo_and_Click_Mongo_Link](https://user-images.githubusercontent.com/32950391/86942133-cb251a80-c112-11ea-80c4-22bb8e30f066.JPG)

3) Run **'deno command'** when you want to ren deno_mongo.
```
deno run --allow-net --allow-write --allow-read --allow-plugin --unstable xxx.ts
```

4) Examples of codes
* ##Import## Mongo module.
```javascript
import { MongoClient } from "https://deno.land/x/mongo@v0.8.0/mod.ts";
```

* Connection
```javascript
const client = new MongoClient();
client.connectionWithUri("mongodb://localhost:27017");
```

* Defining schema interface
```javascript
interface UserSchema {
    _id: { $oid: string };
    username: string;
    password: string;
};
```

* DB & Schema
```javascript
const db = client.database("test");
const users = db.collection<UserSchema>("users");
```

* insert
```javascript
const insertId = await users.insertOne({
    username: "user1",
    password: "pass1",
});
```

* insertMany
```javascript
const insertIds = await users.insertMany([
    {
        username: "user1",
        password: "pass1",
    },
    {
        username: "user2",
        password: "pass2",
    },
]);
```

* findOne
```javascript
const user1 = await users.findOne({ _id: insertId });
// Returns:
// { _id: { $oid: "<oid>" }, username: "user1", password: "pass1" }
```

* find
```javascript
const all_users = await users.find({ username: { $ne: null }});
```

* find by ObjectId
```javascript
const user1_id = await users.findOne(
    { _id: { "$oid": "<oid>" }},
);
```

* count
```javascript
const count = await users.count({ username: { $ne: null } });
```

* aggregation
```javascript
const docs = await users.aggregate([
    { $match: { username: "many" } },
    { $group: { _id: "$username", total: { $sum: 1 } } },
]);
```

* updateOne
```javascript
const { matchedCount, modifiedCount, upsertedId } = await users.updateOne(
    { username: { $ne: null } },
    { $set: { username: "USERNAME" } },
);
```

* updateMany
```javascript
const { matchedCount, modifiedCount, upsertedId } = await users.updateMany(
    { username: { $ne: null } },
    { $set: { username: "USERNAME" } },
);
```

* deleteOne
```javascript
const deleteCount = await users.deleteOne({ _id: insertId });
```

* deleteMany
```javascript
const deleteCount2 = await users.deleteMany({ username: "test" });
```


# References
---
Deno. deno_mongo. Retrieved July 8, 2020, from <https://deno.land/x/mongo>
---