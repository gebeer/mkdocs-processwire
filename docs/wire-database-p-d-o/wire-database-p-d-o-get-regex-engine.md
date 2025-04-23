Get the regular expression engine used by database
--------------------------------------------------

Returns one of 'ICU' (MySQL 8.0.4+) or 'HenrySpencer' (earlier versions and MariaDB)

Available since version **3.0.166**.

### Usage

    $string = $database->getRegexEngine();

### Return value

`string`

