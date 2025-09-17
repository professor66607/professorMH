**Create \& Use Database**



use myDatabase



**Drop Database**



db.dropDatabase()



**Create Collection**



db.createCollection("students")



**show collections**



show collections



**Insert Sample Data**



db.students.insertMany(\[

&nbsp;  { name: "Alice", age: 21, course: "Math" },

&nbsp;  { name: "Bob", age: 22, course: "Physics" },

&nbsp;  { name: "Charlie", age: 20, course: "Chemistry" }

])



**Display Collection Data**



db.students.find()



**Drop Collection**



db.students.drop()



**Insert**



db.students.insertOne({ name: "David", age: 23, course: "Biology" })



db.students.insertMany(\[

&nbsp;  { name: "Emma", age: 24, course: "CS" },

&nbsp;  { name: "Frank", age: 21, course: "Math" }

])



**Find**



db.students.find()

db.students.findOne({ name: "Alice" })



// updateOne

db.students.updateOne(

&nbsp;  { name: "Alice" },

&nbsp;  { $set: { course: "Statistics" } }

)



**Update**



// updateMany

db.students.updateMany(

&nbsp;  { course: "Math" },

&nbsp;  { $set: { level: "Beginner" } }

)



// updateMany

db.students.updateMany(

   { course: "Math" },

   { $unset: { level: "Beginner" } }

)





// using push

db.students.updateOne(

   { name: "Yashwanth" },

   { $push: { hobbies: "football" } }

)



db.students.updateOne(

   { name: "Yashwanth" },

   { $pull: { hobbies: "football" } }

)



 **deleteOne**



db.student.deleteOne({name:"Yashu"})



 **delete many** 



db.student.deleteOne({})





**Field Operations**





// Add new field

db.students.updateOne({ name: "Bob" }, { $set: { grade: "A" } })



// Remove a field

db.students.updateOne({ name: "Bob" }, { $unset: { grade: "" } })



// Push value into array

db.students.updateOne({ name: "Charlie" }, { $push: { hobbies: "Reading" } })



// Remove value from array

db.students.updateOne({ name: "Charlie" }, { $pull: { hobbies: "Reading" } })



**Delete**



db.students.deleteOne({ name: "David" })

db.students.deleteMany({ course: "Math" })



**Practical 3: Aggregation**



**Insert Sample Data**



db.marks.insertMany(\[

&nbsp;  { student: "Alice", score: 85 },

&nbsp;  { student: "Bob", score: 90 },

&nbsp;  { student: "Charlie", score: 78 },

&nbsp;  { student: "David", score: 92 },

&nbsp;  { student: "Emma", score: 88 }

])



**Sum, Avg, Min, Max**



db.marks.aggregate(\[

&nbsp;  {

&nbsp;    $group: {

&nbsp;      \_id: null,

&nbsp;      total: { $sum: "$score" },

&nbsp;      avgScore: { $avg: "$score" },

&nbsp;      minScore: { $min: "$score" },

&nbsp;      maxScore: { $max: "$score" }

&nbsp;    }

&nbsp;  }

])





**Push \& addToSet**



db.orders.insertMany(\[

&nbsp;  { customer: "John", product: "Banana" },

&nbsp;  { customer: "John", product: "Apple" },

&nbsp;  { customer: "John", product: "Banana" },

&nbsp;  { customer: "Mary", product: "Orange" }

])



db.orders.aggregate(\[

&nbsp;  { $group: { \_id: "$customer", items: { $push: "$product" } } }

])



// addToSet (removes duplicates)

db.orders.aggregate(\[

&nbsp;  { $group: { \_id: "$customer", items: { $addToSet: "$product" } } }

])





**REPLICATION**



db.students.aggregate(\[

&nbsp;  { $match: {} },            // match everything

&nbsp;  { $out: {db:"students\_copy",coll:"stCopy"}}  // write into a new collection

])





**A) Creating JSON**



studentTest> db.st.insertMany(\[

&nbsp; {name:"sahil", age:19, course:"bscit", subjects:\["AI","AWP","NGT"]},

&nbsp; {name:"munnawar", age:21, course:"cs", subjects:\["AI","AWP","NGT"]},

&nbsp; {name:"salman", age:26, course:"aviation", subjects:\["atc","arch","maths"]},

&nbsp; {name:"sufi", age:33, course:"bsc", subjects:\["AI","AWP","NGT"]}

])



**B) Parsing JSON**



1\. Show all documents (pretty print)

studentTest> db.st.find().pretty()



**2. Find by name**



studentTest> db.st.find({name:"sahil"})



**3. Find with condition (age less than 20)**



studentTest> db.st.find({age:{$lt:20}})



**4. Find by subject (where subject contains "AI")**



studentTest> db.st.find({subjects:"AI"})



