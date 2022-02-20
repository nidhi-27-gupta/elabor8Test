To test the endpoints I have created two collections in postman. To run the collection, just import them in the postman tool and run. They can be run using the commandline or integrated in the pipeline using newman.
The reason for choosing postman is just that I am using this tool in the current project for api testing.


About the collections:

API test without using data set.postman_collection.json

Lets talk about this collection first. As the name suggests, this collection does not use the provided dataset csv. It have four test cases which cover the following scenarios:

1. Get all facts
2. Get fact details for a valid existing fact id
3. Get fact details for a valid non existing fact id
4. Get fact details for a invalid fact id

These endpoints don't use any authourization, otherwise we could test unauthorized user test case.


API test using data set.postman_collection.json

This collection uses data driven testing to test the facts/{id} endpoint and asserts that if the fact id is found in the database, it has the correct user id.