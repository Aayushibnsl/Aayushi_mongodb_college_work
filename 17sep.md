Registration> use("Registration")
switched to db Registration

Registration> db.createCollection("product")
{ ok: 1 }

Registration> show collections
product

Registration> db.product.insertOne({
...     productId: 1,
...     name: "Sample Product",
...     category: "Electronics",
...     price: 15000,
...     quantity: 1,
...     isActive: true
... })
{
  acknowledged: true,
  insertedId: ObjectId("...")
}

Registration> db.product.find()
[
  {
    _id: ObjectId("..."),
    productId: 1,
    name: 'Sample Product',
    category: 'Electronics',
    price: 15000,
    quantity: 1,
    isActive: true
  }
]

Registration> db.product.countDocuments()
1

Registration> db.product.getIndexes()
[
  {
    v: 2,
    key: { _id: 1 },
    name: '_id_'
  }
]

Registration> db.product.createIndex({ price: 1 })
price_1

Registration> db.product.createIndex({ category: 1, price: -1 })
category_1_price_-1

Registration> db.product.createIndex({ tags: 1 })
tags_1

Registration> db.product.createIndex({ description: "text" })
description_text

Registration> db.product.createIndex({ productId: "hashed" })
productId_hashed

Registration> db.product.createIndex({ location: "2dsphere" })
location_2dsphere

Registration> db.product.createIndex({ email: 1 }, { unique: true, sparse: true })
email_1

Registration> db.product.createIndex({ email: 1 }, { partialFilterExpression: { isActive: true } })
email_1

Registration> db.product.createIndex({ "$**": 1 })
$**_1

Registration> db.product.getIndexes()
[
  {
    v: 2,
    key: { _id: 1 },
    name: '_id_'
  },
  {
    v: 2,
    key: { price: 1 },
    name: 'price_1'
  },
  {
    v: 2,
    key: { category: 1, price: -1 },
    name: 'category_1_price_-1'
  },
  {
    v: 2,
    key: { tags: 1 },
    name: 'tags_1'
  },
  {
    v: 2,
    key: { _fts: 'text', _ftsx: 1 },
    name: 'description_text'
  },
  {
    v: 2,
    key: { productId: 'hashed' },
    name: 'productId_hashed'
  },
  {
    v: 2,
    key: { location: '2dsphere' },
    name: 'location_2dsphere'
  },
  {
    v: 2,
    key: { email: 1 },
    name: 'email_1',
    unique: true,
    sparse: true
  },
  {
    v: 2,
    key: { email: 1 },
    name: 'email_1',
    partialFilterExpression: { isActive: true }
  },
  {
    v: 2,
    key: { '$**': 1 },
    name: '$**_1'
  }
]
