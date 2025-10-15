# 🧠 MongoDB Practicals

## 📘 Practical 1: MongoDB Basics

### 1️⃣ Create and Drop Database
```javascript
// Create or switch to a database
use aryan    

// Create a collection
db.createCollection("user")

// Drop the current database
db.dropDatabase()
```

---

### 2️⃣ Create, Display, and Drop Collection
```javascript
// Use a database
use sy

// Insert a document
db.user.insert({ "name": "aryan", "age": 18 })

// Show all collections
show collections

// Display all documents
db.user.find()

// Drop a collection
db.user.drop()

// Verify drop
show collections
```

---

### 3️⃣ Insert, Update, and Delete Documents
```javascript
// Use database
use ty

// Insert multiple documents
db.product.insert({ "name": "xyz", "age": 12 })
db.product.insert({ "name": "xyz1", "age": 13 })
db.product.insert({ "name": "xyz2", "age": 12 })

// Update a document
db.product.update(
   { "name": "xyz" },
   { $set: { "age": 25, "COD": "YES" } }
)

// Display all documents
db.product.find()

// Remove a document
db.product.remove({ "name": "xyz" })

// Verify deletion
db.product.find()
```

---

## 📗 Practical 2: Simple Queries in MongoDB

```javascript
// Display all documents
db.product.find()

// Find with a condition
db.product.find({
  $where: function() {
    return (this.name == "aryan");
  }
})
```

---

## 📙 Practical 3: Implementing Aggregation

### a) Using `$sum`, `$avg`, `$min`, and `$max` Expressions
```javascript
db.school.insert([
  { _id: 100, name: "komal", age: 18, roll: 1, gender: "female" },
  { _id: 101, name: "stud1", age: 8,  roll: 2, gender: "male" },
  { _id: 102, name: "stud2", age: 28, roll: 3, gender: "female" },
  { _id: 103, name: "stud3", age: 19, roll: 4, gender: "male" },
  { _id: 104, name: "stud4", age: 20, roll: 5, gender: "male" },
  { _id: 105, name: "stud5", age: 25, roll: 6, gender: "male" }
])

db.school.find()

// Sum of students by gender
db.school.aggregate([
  { $group: { _id: "$gender", Total: { $sum: 1 } } }
])

// Maximum age by gender
db.school.aggregate([
  { $group: { _id: "$gender", MaxAge: { $max: "$age" } } }
])

// Minimum age by gender
db.school.aggregate([
  { $group: { _id: "$gender", MinAge: { $min: "$age" } } }
])

// Average age by gender
db.school.aggregate([
  { $group: { _id: "$gender", AvgAge: { $avg: "$age" } } }
])
```

---

### b) `$first` and `$last` Expressions
```javascript
db.school.aggregate([
  {
    $group: {
      _id: null,
      first: { $first: "$$ROOT" },
      last: { $last: "$$ROOT" }
    }
  }
])
```

---

### c) `$push` and `$addToSet` Expressions
```javascript
// Push adds a value even if duplicate
db.school.updateOne(
  { name: "komal" },
  { $push: { roll: 80 } }
)

// AddToSet adds only if value is unique
db.school.updateOne(
  { name: "komal" },
  { $addToSet: { "june": 13 } }
)
```

---

## ✅ Summary

| Task | Command Used |
|------|---------------|
| Create Database | `use <dbname>` |
| Create Collection | `db.createCollection()` |
| Insert Document | `db.<collection>.insert()` |
| Update Document | `db.<collection>.update()` |
| Delete Document | `db.<collection>.remove()` |
| Drop Database | `db.dropDatabase()` |
| Aggregation | `db.<collection>.aggregate()` |

---

📌 **Author:** Aryan  
📅 **Course:** MongoDB Basics  
🏫 **Institution:** (Add your college name if needed)
