# Dog Walker Controllers

Your task is to start building out a Web API for your Dog Walker application.

1. Create a new Web API project in Visual Studio.
1. Create a `Models` folder and copy models from your Dog Walker console application to `Models` directory of your API project.
1. Create a Walker controller. Walker JSON representation should include Neighborhood. It does not need to include any other related entities such as Walks. The controller should support Get All, Get By Id, Create, Update, and Delete

   ```json
   {
     "id": 1,
     "name": "Jane Joe",
     "neighborhoodId": 2,
     "neighborhood": {
       "id": 2,
       "name": "Antioch"
     },
     "walks": null
   }
   ```

1. Create a Dog controller. Dog JSON representation should include Owner. The controller should support Get All, Get By Id, Create, Update, and Delete
   ```json
   {
       "id": 1,
       "name": "Delta",
       "breed": "Golden Retreiver",
       "ownerId": 1,
       "owner": {
           "id": 1,
           "name": "John Smith",
           "neighborhoodId": 3,
           "neighborhood": null
       },
       "notes": "Bring extra bags... She goes... a lot"
   },
   ```
1. Create an Owner controller. When making a GET request for a single owner by Id, the Owner JSON representation should include an array of Dogs they own, and their Neighborhood. When making a GET request for all owners, the JSON representation does not have to included any related entities. The controller should support Get All, Get By Id, Create, and Update (Note: Not Delete)

   **GET all**

   ```json
   [
     {
       "id": 1,
       "name": "John Smith",
       "address": "301 Plus Park Blvd, Nashville TN",
       "neighborhoodId": 3,
       "neighborhood": null,
       "dogs": null
     },
     {
       "id": 2,
       "name": "Jessie Doe",
       "address": "500 Interstate Blvd S, Nashville TN",
       "neighborhoodId": 5,
       "neighborhood": null,
       "dogs": null
     },
     {
       "id": 2,
       "name": "Rick James",
       "address": "505 Deaderick Street, Nashville TN",
       "neighborhoodId": 9,
       "neighborhood": null,
       "dogs": null
     }
   ]
   ```

   **GET by Id**

   ```json
   {
     "id": 1,
     "name": "John Smith",
     "address": "301 Plus Park Blvd, Nashville TN",\
     "neighborhoodId": 3,
     "neighborhood": {
       "id": 3,
       "name": "Germantown"
     },
     "dogs": [
       {
         "id": 1,
         "name": "Delta",
         "breed": "Golden Retreiver",
         "notes": "Bring extra bags... She goes a lot",
         "ownerId": 1,
         "owner": null
       },
       {
         "id": 8,
         "name": "Janet",
         "breed": "Hound",
         "notes": "She'll try to chase cars",
         "ownerId": 1,
         "owner": null
       }
     ]
   }
   ```
