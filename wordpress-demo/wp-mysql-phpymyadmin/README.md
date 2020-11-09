## 🎨 WordPress, MySQL and phpMyAdmin in Docker

## Setup
- Create a new directory for your project

- Create a new file called `docker-compose.yml`, and put the [content](docker-compose.yml) there

- Run this command from the directory to start the containers
```bash
docker-compose up 
```

## Access 
- **WordPress** will be available on [http://localhost](http://localhost)
- **phpMyAdmin** will be available on [http://localhost:8183](http://localhost:8183)
> user : wordpress_user, password : wordpress_password

## Work 
You can now start work on the wordpress site.

#### Example : Create a simple plugin

- Create a new PHP file in the plugins folder called `my_sample_plugin.php` and 

- In the `hello_wordpress.php` add this content :
```php
<?php
/*
  Plugin Name: My First Plugin
  Plugin URI: https://wordpress.org/plugins/search/hello-world/
  Description: Hello World! This is my first plugin
  Author: Talha Ibne Imam
  Version: 1.0.0
  Author URI: https://cse031sust02.github.io/
*/
```

-  Go to the [plugins section](http://localhost/wp-admin/plugins.php) of your WordPress Admin Panel, you will see your newly added plugin!
