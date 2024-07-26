### Prompts

Prompt: What is the command to start the mongo server? 

Ans: brew services start mongodb-community@7.0


Prompt: What is the command to connect to the mongo shell?

Ans: mongosh

Prompt: What is the command for listing all mongo databases?

Ans: show dbs

Prompt: What command would you use to create a database called burgers?

Ans: use burgers

Prompt: What command would you use to add the collection burger to your burgers database?

Ans: db.burger.insertOne

Prompt: What is the command for listing all collections in a database?

Ans: show collections

Prompt: What query would find all burgers with a beef patty?

Ans: db.burgers.find({ patty: "beef" })

Prompt: What query would find a burger by it's ObjectId?

Ans: db.burgers.find({ _id: ObjectId(ID Here)})

Prompt: What query would find all burgers with ketchup as a topping?

Ans: db.burgers.find({ toppings: "ketchup" })

Prompt: What query would find all burgers with either a turkey or veggie patty?

Ans: db.burgers.find({ patty: { $in: ["turkey", "veggie"] } })

Prompt: What query would find all burgers with a beef patty and cheese?

Ans: db.burgers.find({ patty: "beef", cheese: true })

Prompt: What query would find all burgers with a beef patty and ketchup as a topping?

Ans: db.burgers.find({ patty: "beef", toppings: "ketchup" })

Prompt: What query would find all burgers with a beef patty and both onions and pickles as toppings?

Ans: db.burgers.find({patty: "beef", toppings: { $all: ["onions", "pickles"]} })

Prompt: What query would find burgers with either a turkey patty or cheese?

Ans: db.burgers.find({ $or: [{ patty: "turkey" },{ cheese: true }]})


### Update

## Prompts

Prompt: What query would update one burger by it's ObjectId, setting it's "patty" to "pork"?

Ans: db.burgers.updateOne({ _id: ObjectId("yourObjectIdHere") },{ $set: { patty:"pork" } })

Prompt: What query would update all burgers with beef paddies to have cheese? (i.e. set "cheese" to true)

Ans: db.burgers.updateMany({ patty: "beef" },{ $set: { cheese: true } })

### Delete

## Prompts

Prompt: What query would delete a burger by it's ObjectId?

Ans: db.burgers.deleteOne({ _id: ObjectId("ObjectIdHere") })

Prompt: What query would delete all veggie burgers?

Ans: db.burgers.deleteMany({ patty: "veggie" })


Prompt: What query would delete all burgers with pickles on them?

Ans: db.burgers.deleteMany({ toppings: "pickles" })


