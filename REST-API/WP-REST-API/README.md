# WP REST API


##### WP REST API Application

- Mobile Apps
- Custom Admin Panels for WordPress
- Single Page Applications ( SPAs e.g. Angular, React, Veu)
- Integration with other server-side platforms ( Like Node.JS, Java, Ruby,.NET and Django etc.)

##### Authentication

- Basic 
- OAuth 
- Cookie 

##### Endpoints

- `GET wp/v2/posts`         : Retrieve all posts
- `GET wp/v2/posts/100`     : Tetrieve single post with ID = 100
- `POST wp/v2/posts`        : Create new post 
- `PUT wp/v2/posts/100`     : Update post with ID = 100
- `DELETE wp/v2/posts/100`  : Delete post with ID = 100

##### Basic Authentication

- Basic Auth : `Authorization: Basic {base64_encode(username:password)}`
- That is converted to : `Authorization: Basic dHV0c3BsdXM6MTIzNDU2`

##### Plugin Required
- Basic Auth Plugin : `sudo git clone https://github.com/WP-API/Basic-Auth.git`

##### Requests via Commandline

- List Post:
```bash
curl --user admin:password https://example.com/wp-json/
```

- Create Post
```bash
curl  --user admin:password -d "title=hello+world&status=publish&content=lorem+ipsem+!" -H "Content-Type: application/x-www-form-urlencoded" -X POST https://example.com/wp-json/wp/v2/posts
```

- Update Post with ID 100
```bash
curl  --user admin:password -d "title=hello+HELL&status=publish&content=Good+ipsem+!" -H "Content-Type: application/x-www-form-urlencoded" -X PUT https://example.com/wp-json/wp/v2/posts/100
```

- Delete Post with ID 100:
```bash
curl --request DELETE -I --user  admin:password https://example.com/wp-json/wp/v2/posts/100
```



#### Refrences:

- Basic Auth Plugin : https://github.com/WP-API/Basic-Auth
- Curl Options : https://gist.github.com/subfuzion/08c5d85437d5d4f00e58