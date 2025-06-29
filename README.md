// To change WordPress's default logo to my logo, write the above code to the functions.php file.

function my_custom_login_logo() { ?>
    <style type="text/css">
        #login h1 a {
            background-image: url('YOUR-LOGO-URL');
            width: 250px; /* Adjust based on your logo size */
            height: 80px;
            background-size: contain;
        }
    </style>
<?php }
add_action('login_enqueue_scripts', 'my_custom_login_logo');



// When click logo then go action to home page
function my_custom_login_logo_url() {
    return home_url();
}
add_filter('login_headerurl', 'my_custom_login_logo_url');
