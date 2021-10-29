# Mule 4 + GraphQL sample app

This is a sample Mule 4 app, with GraphQL implemented on top of it.

# Prerequisite 
Build this repo into a dependency using maven build and then include that dependency in this projects pom.xml :




# Information
This project creates three dummy rest apis as follows:

## Accounts REST api(dummy) :
![image](https://user-images.githubusercontent.com/41906513/139402305-6e0d70a7-a140-4da6-a2e9-e5aa9654af39.png)

## Balances REST api(dummy) :
![image](https://user-images.githubusercontent.com/41906513/139402375-29d6d7d8-3403-4aa4-80cd-220553896ec4.png)

## Transactions REST api(dummy) :
![image](https://user-images.githubusercontent.com/41906513/139402468-2ac75e67-3df7-4dd2-b5e4-5e10e7ce6532.png)

Using GraphQL plugin, we can now query the three APIs in a flexible manner, without having to change the underlying flows:

## Inbuilt console URL for graphQL UI :
http://localhost:8081/graphiql

(Same can be done using any Rest API client.

Sample curl :

curl --location --request GET 'http://localhost:8081/graphql' \
--header 'Content-Type: application/json' \
--data-raw '{"query":"query\r\n{\r\n  account(id:\"12345\"){\r\n      firstName\r\n      lastName\r\n      balances{\r\n          amount\r\n      }\r\n      transactions{\r\n          transactionId\r\n      }\r\n  }\r\n  }","variables":{}}')

![image](https://user-images.githubusercontent.com/41906513/139392754-25b405eb-f136-411c-a6da-6d97140274d1.png)

Ref : https://github.com/Jitendra85/MuleSoft-GraphQL-Demo
