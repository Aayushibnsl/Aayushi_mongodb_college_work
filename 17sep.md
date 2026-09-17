use("Registration")

db.createCollection("product")

show collections

db.product.insertOne({
    productId: 1,
    name: "Sample Product",
    category: "Electronics",
    price: 15000,
    quantity: 1,
    isActive: true
})

db.product.find()

db.product.countDocuments()

db.product.getIndexes()

db.product.createIndex({ price: 1 })

db.product.createIndex({ category: 1, price: -1 })

db.product.createIndex({ tags: 1 })

db.product.createIndex({ description: "text" })

db.product.createIndex({ productId: "hashed" })

db.product.createIndex({ location: "2dsphere" })

db.product.createIndex({ email: 1 }, { unique: true, sparse: true })

db.product.createIndex({ email: 1 }, { partialFilterExpression: { isActive: true } })

db.product.createIndex({ "$**": 1 })

db.product.getIndexes()
