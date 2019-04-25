# REST

Representational State Transfer (REST) is a software architectural style that defines a set of constraints to be used for creating Web services.

```bash
GET     =>  READ        : Read or Retrieve a Resource
POST    =>  CREATE      : Create a new Resource
PUT     =>  UPDATE      : Update a Resource
DELETE  =>  DELETE      : Delete a Resource
Head    =>  CHECK       : Check if a Resource exists ?
OPTIONS =>  SUPPORT     : Retrieve all the verbs supported by a Resource

```

##### HTTP Response Codes

- `200 - OK` : Successful `GET` request
- `201 - Created` : Successful `POST` request
- `400 - Bad Request` Some missing or invalid parameters in     `POST` or  `PUT` requests
- `401 - Unauthorized` : Not authorized to perform certian action. Create or delete a resource without providing auth details
- `403 - Forbidden` : User doesn't have sufficent rights to perform action. 
- `404 - Not Found` : User was looking for, was not found
- `405 - Method not Allowed` : HTTP verb used not supported. e.g. user trying to update a read-only resource
- `410 - Gone` : Resource has been moved to another location. e.lg. delete and already deleted resource that has been moved to trash
- `500 - Internal Server Error` : Server encounters an unexpected condition and doesn't complete request
- `501 - Not Implemented` : Server doesn't support. e.g. server receives a request method that it doesn't recognize

