# Ajax in WordPress

#### 1. Pass Nonce & Ajax URL via Localize Script

```php
wp_localize_script(
  'jsforwp-backend-js',
  'jsforwp_globals',
  [
    'ajax_url'    => admin_url( 'admin-ajax.php' ),
    'total_likes' => get_option( 'jsforwp_likes' ),
    'nonce'       => $nonce
  ]
);
```

#### 2. Make Ajax call with Nonce and URL in JavaScript

```js
$.ajax({
  type: "post",
  dataType: "json",
  url: jsforwp_globals.ajax_url,
  data: {
    action: "jsforwp_add_like",
    _ajax_nonce: jsforwp_globals.nonce
  },
  success: function(response) {
   alert(' Success ');
  }
});
```

#### 3. Hook PHP Ajax functions into WordPress Ajax Hooks

```php
function jsforwp_add_like( ) {

  // Change the parameter of check_ajax_referer() to 'jsforwp_likes_nonce'
  check_ajax_referer( 'jsforwp_likes_nonce' );

  $likes = intval( get_option( 'jsforwp_likes' ) );
  $new_likes = $likes + 1;
  $success = update_option( 'jsforwp_likes', $new_likes );

  if( true == $success ) {
    $response['total_likes'] = $new_likes;
    $response['type'] = 'success';
  }

  $response = json_encode( $response );
  echo $response;
  die();

}
// Change 'wp_ajax_your_hook' to 'wp_ajax_jsforwp_add_like'
// Or change to 'wp_ajax_nopriv_your_hook' to 'wp_ajax_nopriv_jsforwp_add_like'
// Change 'your_hook' to 'jsforwp_add_like'
add_action( 'wp_ajax_jsforwp_add_like', 'jsforwp_add_like' );
add_action( 'wp_ajax_nopriv_jsforwp_add_like', 'jsforwp_add_like' );
```


#### 4. Use JavaScript to handle Ajax Response

```js
success: function(response) {
    if ("success" == response.type) {
      // Change the html() value to response.total_likes
      $(".jsforwp-count").html(response.total_likes);
    } else {
      alert("Something went wrong, try logging in!");
    }
  }
```

### References :

- [A demo repo for my AJAX in WordPress Mini Course
](https://github.com/zgordon/wordpress-ajax)

- [How to Use Ajax in WordPress – a Real World Example](https://www.sitepoint.com/how-to-use-ajax-in-wordpress-a-real-world-example/)
  
  
