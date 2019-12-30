# KinveyPostmanRequests
Postman requests collection for Kinvey REST API

# 1. Import collection and environment variables
- Open Postman -> File -> Import -> Kinvey.postman_collection.json
- Open Postman -> File -> Import -> Kinvey Variables.postman_environment.json

After importing, you would have a "Kinvey" collection (in "Collections" tab) and "Kinvey Variables" (in Environments) added.

# 2. Update environment variables
Go to Postman -> Manage Environments -> Kinvey Variables

Set the values for:
- host
- appKey
- appSecret
- masterKey

The above values are used to construct requests' URLs and Authorization Headers.

# 3. Register/Login a user
Most requests require a user session token as Authorization header. To get it go to Collections -> Kinvey -> Users

Make a request with "Register" or "Login" a user. After the requests succeeds, the user's ID, username and access token will be automatically populated in Kinvey Variables (user_id, username, accessToken variables).

In "Tests" section you may see the code which parses the returned response and populates the variables automatically.
