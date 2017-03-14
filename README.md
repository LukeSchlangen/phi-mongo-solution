# phi-mongo-solution

```
db.getCollection('orders').find({})

Create a collection named orders.


Insert at least 3 documents that represent an order. IMPORTANT: See section below for fields.
Find a single order document, any order document.
db.getCollection('orders').findOne({});
Find all orders and make them look pretty.
db.orders.find().pretty();
Find all orders with an orderDate that is prior to 1/1/2016.
db.orders.find({orderDate: { $lt: new Date('2016-01-01') }});
Find all orders with an orderDate that is after 1/1/2016.
db.orders.find({orderDate: { $gt: new Date('2016-01-01') }});
Find orders with lineItems that have a quantity that is less than 50, but greater than 5. HINT: Look at $and and dot notation.
db.orders.find({
                $and: [
                        {'lineItems.quantity': {$lt: 2}},
                        {'lineItems.quantity': {$gt: 0}}
                ]
              });
Update one of your line items to 42.99. HINT: Look at dot notation
db.orders.update({_id: ObjectId("58c84537d23a652cb011141c")},
        {$set: {'lineItems.0.thingPrice': 79.99}});

Remove one of your orders.
db.orders.deleteOne({"_id" : ObjectId("58c84537d23a652cb011141e")});
```
