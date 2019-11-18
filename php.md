# Important things // PHP

## Database

### PDO - MySQL Database Connection
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
### Error document handling
Handling error pages - present a file when ab error occurs:  
`ErrorDocument ERROR_ID FILE_PATH_AND_NAME`

**Example:**
```php
ErrorDocument 404 /404.php
```