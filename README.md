# TD_dbExport
Live (MySQL) database exporter


Add the following code to the bottom of your code on every page
```
if( !isset($_SERVER['HTTP_X_REQUESTED_WITH']) ) {
    require "/path/to/directory/config.inc.php";
    require "/path/to/directory/TD_dbExport.php";
    $export_database = new TD_dbExport($TD_dbExport_DB);
    $export_database->export_to_file("database_file_name");
}
```

$TD_dbExport_DB can also be a connection variable

The function parameter of export_to_file is the name of the file where you want to export to
