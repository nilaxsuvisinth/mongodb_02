# mongodb_02

**1. Create a Database called customers.**
```
use customers
```

**2. Create a collection called customerdetails.**
```
db.createCollection("customerdetails")
```

**3. Insert all documents into the collection named   customerdetails.**
```
db.customerdetails.insertMany([{name:"John",age:25,gender:"Male",city:"New york"},{name:"Emily",age:22,gender:"Female",city:"London"},{name:"Daniel",age:28,gender:"Male",city:"Sydney"},{name:"Sophia",age:24,gender:"Female",city:"Paris"},{name:"William",age:26,gender:"Male",city:"Chicago"},{name:"Olivia",age:23,gender:"Female",city:"Los Angeles"},{name:"Benjamin",age:27,gender:"Male",city:"Toronto"},{name:"Mila",age:29,gender:"Female",city:"Berlin"},{name:"James",age:30,gender:"Male",city:"Tokyo"}])
```

**4. Retrieve all documents from the collection and sort the results by the “age” field    in ascending order.**
```
db.customerdetails.find().sort({age:1}).pretty()
```

**5. Count the number of females.**
```
db.customerdetails.countDocuments({gender:"Female"})
```

**6.Insert one document into the customerdetails collection.**
```
db.customerdetails.insertOne({name:"Vijay",age:49,gender:"Male",city:"Chennai"})
```

**7. Update city=SriLanka to John.**
```
db.customerdetails.update({name:"John"},{$set:{city:"SriLanka"}},{upsert:true})
```













