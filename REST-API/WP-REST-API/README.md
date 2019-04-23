# WP REST API


#### WP REST API Application

- Mobile Apps
- Custom Admin Panels for WordPress
- Single Page Applications ( SPAs e.g. Angular, React, Veu)
- Integration with other server-side platforms ( Like Node.JS, Java, Ruby,.NET and Django etc.)

#### Authentication

- Basic 
- OAuth 
- Cookie 

#### Endpoints

- `GET wp/v2/posts`         : Retrieve all posts
- `GET wp/v2/posts/100`     : Tetrieve single post with ID = 100
- `POST wp/v2/posts`        : Create new post 
- `PUT wp/v2/posts/100`     : Update post with ID = 100
- `DELETE wp/v2/posts/100`  : Delete post with ID = 100


#### HTTP Response Codes

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

