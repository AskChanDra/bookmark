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
##### Requests via WP HTTP API

###### Authorization header

```php
$wp_request_headers = array(
    'Authorization' => 'Basic ' . base64_encode( 'admin:password' )
);
```

###### Get Post with ID 100 or List all Post

```php

// get List of Posts
// $wp_request_url = 'https://example.com/wp-json/wp/v2/posts';

// Get a Single Post
$wp_request_url = 'https://example.com/wp-json/wp/v2/posts/18';
 
$wp_get_post_response = wp_remote_get(
            $wp_request_url,
            array(
            	'headers' => $wp_request_headers,
            )
        );

echo wp_remote_retrieve_response_code( $wp_get_post_response ) . ' ' . wp_remote_retrieve_response_message( $wp_get_post_response );

echo "<br > Body : " . wp_remote_retrieve_body($wp_get_post_response) . "";
```

- Response Code : ` 200 OK `

###### Create Post

```php
$wp_request_url = 'https://example.com/wp-json/wp/v2/posts';
 
$wp_create_post_response = wp_remote_post(
            $wp_request_url,
            array(
            	'headers' => $wp_request_headers,
                'body' => array(
                    'title'   => 'Hello Worlddd',
                    'status'     => 'publish',
                    'content' => 'this is content ... '
                )
            )
        );

echo wp_remote_retrieve_response_code( $wp_create_post_response ) . ' ' . wp_remote_retrieve_response_message( $wp_create_post_response );
```

- Response Code : ` 201 Created `

###### Update Post with ID 100
```php
$wp_request_url = 'https://example.com/wp-json/wp/v2/posts/100';
 
$wp_update_post_response = wp_remote_request(
            $wp_request_url,
            array(
            	'headers' => $wp_request_headers,
            	'method'  => 'PUT',
                'body' => array(
                    'title'   => 'Hello Sydney',
                    'status'     => 'publish',
                    'content' => 'I hope this is updated content you seeing '
                )
            )
        );

echo wp_remote_retrieve_response_code( $wp_update_post_response ) . ' ' . wp_remote_retrieve_response_message( $wp_update_post_response );

```

- Response Code : ` 200 OK `

###### Delete post with ID 100

```php

$wp_request_url = 'https://example.com/wp-json/wp/v2/posts/100';
 
$wp_delete_post_response = wp_remote_request(
    $wp_request_url,
    array(
        'method'    => 'DELETE',
        'headers'   => $wp_request_headers
    )
);
 
echo wp_remote_retrieve_response_code( $wp_delete_post_response ) . ' ' . wp_remote_retrieve_response_message( $wp_delete_post_response );

```

- Response Code : ` 200 Ok `


#### Refrences:

- Basic Auth Plugin : https://github.com/WP-API/Basic-Auth
- Curl Options : https://gist.github.com/subfuzion/08c5d85437d5d4f00e58
- Introduction to REST API : https://code.tutsplus.com/series/introducing-the-wp-rest-api--cms-896