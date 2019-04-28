
### WP HTTP API


##### Request Helper Functions:
- ` wp_remote_get() ` : Retrieves a URL using the GET HTTP method.
- ` wp_remote_post() ` : Retrieves a URL using the POST HTTP method.
- ` wp_remote_head() ` : Retrieves a URL using the HEAD HTTP method.
- ` wp_remote_request() ` : Retrieves a URL using either the default GET or a custom HTTP method (should be caps) that you specify.

##### Response Helper Functions:

- ` wp_remote_retrieve_body() ` : Retrieves just the body from the response.
- ` wp_remote_retrieve_header() ` : Gives you a single HTTP header based on name from the response.
- ` wp_remote_retrieve_headers() ` : Returns all of the HTTP headers in an array for processing.
- ` wp_remote_retrieve_response_code() ` :  Gives you the number for the HTTP response. This should be 200, but could be 4xx or even 3xx on failure.
- ` wp_remote_retrieve_response_message() ` : Returns the response message based on the response code.
