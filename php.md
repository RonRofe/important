# Important things // PHP

## Database
### PDO - MySQL Database Connection
Enforce the connection with the database to be on UTF-8.  
Put an array with this configuration in the DB connection Object:  
`array(PDO::MYSQL_ATTR_INIT_COMMAND => "SET NAMES utf8")`

**Example:**  
`$dbh = new PDO(
    'mysql:host=HOST;dbname=DATABASE_NAME',
    'USERNAME',
    'PASSWORD',
    array(PDO::MYSQL_ATTR_INIT_COMMAND => "SET NAMES utf8")
)`