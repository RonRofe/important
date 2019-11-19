# Important things // PHP

## Database

### PDO - MySQL Database Connection -> UTF8 Enconding
Enforce the connection with the database to be on UTF-8.  
Put an array with this configuration in the DB connection object:  
`array(PDO::MYSQL_ATTR_INIT_COMMAND => "SET NAMES utf8")`

**Example:**
```php
$dbh = new PDO(
    'mysql:host=HOST;dbname=DATABASE_NAME',
    'USERNAME',
    'PASSWORD',
    array(PDO::MYSQL_ATTR_INIT_COMMAND => "SET NAMES utf8")
)
```

## .htaccess File
### Error Document Handling
Handling error pages - present a file when ab error occurs:  
`ErrorDocument ERROR_ID FILE_PATH_AND_NAME`

**Example:**
```php
ErrorDocument 404 /404.php
```

## General configurations

### Server Timezone
Changing configured timezone so times will operate as desired.  
Should be set in the top of the file: `date_default_timezone_set(TIME_ZONE_NAME)`

**Example:**
```php
date_default_timezone_set('Asia/Jerusalem');
```