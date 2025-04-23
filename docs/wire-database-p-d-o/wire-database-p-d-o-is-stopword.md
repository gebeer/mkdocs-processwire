Is given word a fulltext stopword for database engine?
------------------------------------------------------

Available since version **3.0.160**.

### Usage

    // basic usage
    $bool = $database->isStopword(string $word);
    
    // usage with all arguments
    $bool = $database->isStopword(string $word, string $engine = '');

### Arguments

Name

Type(s)

Description

`word`

string

`engine` (optional)

string

DB engine ('myisam' or 'innodb') or omit for current engine

### Return value

`bool`

