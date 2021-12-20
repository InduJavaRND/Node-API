
API-1: Login Page:
URL: http://localhost:4000/api/signin
Method: POST
Request: {
    "username": string,
    "password": string
}
Response {
    "authenticated": true
}
Sample Payload:
{
   "username":"cluemediator",
    "password": "123456"
}

API-2: New Register
URL: http://localhost:4000/api/signup
Method: POST
Request: {
    "name": string
    "username": string,
    "password": string,
    "email": string,
    "contact": string
}
Response {
    {
    "user": {
        "name": "123456",
        "username": "123456",
        "email": "cluemediator@gmail.com",
        "contact": "123456"
    }
}
Sample Payload:
{
 "name":"indu",
 "username":"Indu",
 "password":"1234",
 "email":"test@test.com",
 "contact": 25451236
}


API-3: Product details
URL: http://localhost:4000/api/productManagement/saveProduct
Method: POST
Request: {
    "productName":string,
    "price":string,
    "quantity":number,
    "vendor":string,
    "warranty":string
}
Response{
    {
    "product": {
        "productName": "Laptop",
        "price": "70000",
        "quantity": "1",
        "vendor": "zen computers",
        "warranty": "2 years"
    }
}
}
API3 - Sample request payload
{
    "productName":"mobile",
    "price":15000,
    "quantity":1,
    "vendor":"Zen computers",
    "warranty":"1 year"
}

API-4: Product management
URL: http://localhost:4000/api/productManagement/listProduct
Method: GET
Request: {}
Response: {
    "products":[
        {
            "productId":1,
            "productName":"computer",
            "price":70000,
            "quantity":1,
            "vendor":"Zen computers",
            "warranty":"1 year"
        },
        {
            "productId":2,
            "productName":"computer",
            "price":70000,
            "quantity":1,
            "vendor":"Zen computers",
            "warranty":"1 year"
        }
    ] 
}

API-5: Product details
URL: http://localhost:3000/api/productManagement/updateProduct/<productId>
Method: PATCH
Request: {
    "productName":string,
    "price":string,
    "quantity":number,
    "vendor":string,
    "warranty":string
}
Response{
    "productName":"computer",
    "price":70000,
    "quantity":1,
    "vendor":"Zen computers",
    "warranty":"1 year"
}
Sample Payload
{
    "productId": 2,
    "productName":" samsung mobile",
    "price":75000,
    "quantity":1,
    "vendor":"Zen computers",
    "warranty":"1 year"
}

API-6:  Delete Product details
URL: http://localhost:4000/api/productManagement/deleteproduct/<productId>
Method: DELETE
Request: {
    
}
Response{
    "success":true
}

Sample Payload:
{
    "productId": 3

}